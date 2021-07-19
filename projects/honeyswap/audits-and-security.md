# Audits & Security

## Certik Audit

The Honeyswap contracts have been audited by CertiK security assessors. You can read their audit report below.

{% file src="../../.gitbook/assets/rep-1hive\_honeyswap\_contracts-22\_04\_2021.pdf" %}

Some changes have been made to the contracts post-audit. However, the core mechanisms remain unchanged. As a result, the audit still provides a valid assessment of the current state of the security of the main contracts.   
  
The airdrop contracts have not been audited. However, the airdrop contract only holds the airdrop funds and do not interact or influence the farming contracts in any way.

## Internal Audit

[Original text of the internal audit](https://hackmd.io/BFrhyOTUQ3O9REs5PuZahQ?view)

#### General function <a id="General-function"></a>

* The farming contract allows users to deposit ERC20 tokens into set pools and earn rewards in another token proportional to their share in the pool
* The contract tracks multiple pools
* Depositors can set a referrer upon depositing which will get rewarded proportionally to the rewards earned by the depositor
* The rewards are xComb tokens referred to as `hsfToken` in the code
* Depositors may lock their deposit for a fixed period of time to own a larger share of the pool and thus the rewards

#### Relevant contracts <a id="Relevant-contracts"></a>

* **ReferralRewarder.sol**: stores rewards for referrers
* **HSFToken.sol**: ERC20 reward token
* **HoneyFarm.sol**: Keeps track of pools and deposits

#### Critical functions <a id="Critical-functions"></a>

As the contract deals with deposit tokens and the reward token one must ensure that the relevant transfers are only called when appropriate and with the correct parameters. Furthermore any state that may lead to their invocation has to be checked to make sure that it’s correctly updated.

#### HSFToken.sol <a id="HSFTokensol"></a>

**General**

* Uses the standard ERC20 implementation from the OpenZeppelin smart contract library
* The `_mint()` method is only called once during construction with the total supply credited to the deployer
* The reward token has no additional embedded functionality

**Potential detected failure points**

none

#### ReferralRewarder.sol <a id="ReferralRewardersol"></a>

**General**

* has an immutable `exchangeRate` property that determines how referrers are compensated
* Tokens are only transferred within the `distributeReward` method
* Uses the standard `Ownable` implementation from the OpenZepplin library for method access restriction \(not fully compatible with ERC173, missing `supportsInterface` method\)

**distributeReward\(\)**

* Is access restricted so that only the owner address may call it
* Scales the given `reward` parameter by the `exchangeRate`
* compares reward to balance to ensure that the method doesn’t revert due to insufficient funds
* fires a `MissingReward` event incase the method failed to provide the necessary reward

**Potential detected failure points**

* **May run out of rewards**: deployer can ensure the contract cannot run out by depositing enough rewards such that `rewarder_reserves = exchange_rate * total_farm_reward_dist`
* **Owner can drain contract**: draining is prevented by setting the owner to the farming contract after deployment
* **distributeReward may revert due to integer overflow**: aslong as the `exchangeRate` paramater is set to less than `type(uint256).max / rewardToken.totalSupply() + 1` it cannot overflow when performing the multiplication

#### HoneyFarm.sol <a id="HoneyFarmsol"></a>

**General - Definitions & Maths:**

* **Total reward distribution**:  All rewards in the farming contract are paid out in the form of the reward  token. The amount being distributed at any time t can be denoted by the  function d\(t\)=m⋅t+ds where m is the slope of the line and ds is the starting distribution rate. If te is the time at which distribution ends, the distribution rate at the end de is d\(te\).  Since we want the distribution rate to decrease over time we’ll denote  de as a percentage r of ds, so de=r⋅ds . The total HSF to be distributed s is the area under the graph between 0 and te

![](../../.gitbook/assets/image%20%282%29.png)

  
 Since the graph is just a sloped line, the area underneath it can be  
 broken down into a triangle and rectangle. The sum of their areas should  
 be equal to the total reward distribution:

![](../../.gitbook/assets/image%20%2815%29.png)

Now that the starting distribution rate is calculated one can easily  
 calculate the slope since it’s simply the change in the distribution rate  
 divided by the time:

![](../../.gitbook/assets/image%20%2816%29.png)

Since the slope will be negative and it’s simpler to deal with positive,  
 unsigned numbers the contract simply stores the flipped sign value and  
 negates it via subtraction instead of addition in the calculations where  
 it’s used:  


![](../../.gitbook/assets/image%20%2818%29.png)

The above calculations are used in the constructor to calculate the slope  
 and the starting distribution rate. Note that since solidity doesn’t  
 support fractional numbers the scaling constant `SCALE` is used to scale  
 fractional numbers up and down.

The final piece of math that is needed is how to calculate the amount to be  
 distributed between two arbitrary time points d\(t1,t2\), this can be  
 done by integrating our d\(t\) function over that period. All that means  
 is calculating the area under the graph during that period. To do that one  
 again can simply splits the area into geometric shapes to calculate its  
 area and simplifies the resulting equation:

![](../../.gitbook/assets/image%20%2817%29.png)

Which brings us to the final equation which is used in the  
 `getDistribution` method. The result is scaled by the `SCALE` constant:  
 d\(t1,t2\)=\(t2−t1\)⋅\(2⋅ds−\(−m\)⋅\(t2+t1\)\)/2

Since the amount of outputed rewards will be steadily decreasing m will  
 be a negative value. Since it’s simpler to only have to deal with positive  
 numbers in the code we use the formula above where m is negated, −m is  
 thus positive and is the value that is actually stored in the `distributionSlope` property.

* **Pools**:  The farming contract distributes rewards in the reward token to all its  pools, proportional to their allocation. Each pool tracks a single ERC20  token. So if a pool is allocated 20% of their rewards and a user’s deposit  has 50% of the total shares in the pool, that user will receive 10% of the  total distributed rewards so long as these parameters do not change.
* **Keeping track of rewards**:  The rewards a given deposit accrues is dependant on its shares relative to  the total shares contained in the pool. Shares are calculated by taking  the token deposit amount times a multiplier. For non-timelocked deposits  the multiplier is 1. For timelocked deposits the multiplier increases  linearly with lock length.

**General - Publicly accessible properties:**

* `SCALE`: constant, by what value calculations are scaled to maintain precision. If `SCALE` is say 10^18 then the value 0.1 would be stored as 0.1 \* `SCALE` so 10^17. This is done to maintain precision in different calculations throughout the contract
* `hsf`: immutable, address of the reward token
* `referralRewarder`: address of the referral rewarder, while not explicitly immutable it can only be set once in the lifetime of the contract in the `setReferralRewarder` method
* `poolInfo`: returns information for a certain pool when given the pool token’s address. Pool information includes:
  * `allocation`: what share of the distributed rewards are allocated to the pool, always relative to the total allocation poitns
  * `lastRewardTimestamp`: the timestamp at which the pool’s information was last updated. A pool is updated every time a pool’s properties are changed, a new pool is created, a new deposit is created, closed or its rewards withdrawn
  * `accHsfPerShare`: represents the rewards one share unit would’ve accrued if staked since the beginning of the pool
  * `totalShares`: total shares current in the pool
* `totalAllocationPoints`: total points allocated to different pools
* `totalDeposits`: how many deposits have already been created, also used as the deposit ID of the next deposit
* `depositInfo`: returns information for a certain deposit when given the deposit ID. Deposit information includes:
  * `amount`: deposited token amount
  * `rewardDebt`: used to account for reward accumulator pre-deposit
  * `unlockTime`: time at which the owner may withdraw his deposited tokens and close his deposit. 0 if the deposit isn’t locked
  * `rewardShare`: how many shares the deposit contains.
  * `setRewards`: earned rewards not accounted for via the reward accumulator. Typically only set if a deposit has been downgraded externally.
  * `pool`: pool that the deposit belongs to
  * `referrer`: the address set to receive referral rewards upon receiving rewards
* `distributionSlope`: immutable, slope of the distribution function \(−m
* \)
* `startDistribution`: immutable, distribution per unit of time when distribution starts
* `minTimelock`: imutable, shortest permitted time-locked deposit. Even when this value is above 0 it still allows non-locked deposits
* `maxTimeLock`: immutable, longest permitted time-locked deposit
* `startTime`: immutable, time at which reward distribution begins
* `endTime`: immutable, time at which reward distribution ends
* `timeLockMultplier`: immutable, multplying factor used when determining the share multiplier for time-locked deposits. Scaled by `SCALE`
* `timeLockConstant`: immutable, constant factor used when determining the share multplier for time-locked deposits. Scaled by `SCALE`
* `downgradeFee`: immutable, fee taken from the deposit’s underlying deposit amount \(not rewards\) when a deposit is downgraded. Scaled by `SCALE`
* `contractDisabledAt`: timestamp at which the contract was disabled. Set to 0 if the contract hasn’t been disabled yet. Can only be set once
* `owner`: returns the address of the current contract owner. The owner can  add and adjust pools, set the baseURI used to determine the token URI and  disable the contract. \(what disabling entails is described below\)

**General - publicly accessible methods**

This section does not include properties that behave like mentioned, these  
 are mentioned in the section above.

Not explicitly listed here but also available are all the methods required  
 to be compatible with the ERC721 standard. This includes the metadata and  
 enumerable extension of the ERC721 standard as proposed in EIP721.

* `constructor(IERC20 _hsf, [uint256 _startTime, uint256 _endTime, uint256 _totalHsfToDistribute, uint256 _endDistributionFraction, uint256 _minTimeLock, uint256 _maxTimeLock, uint256 _timeLockMultiplier, uint256 _timeLockConstant, uint256 _downgradeFee])`:  Partially initializes the farming contract. Calculates and stores the  `distributionSlope` and `startDistribution` properties. Transfers the  total required reward tokens to itself from the deployer address. Stores  the different parameters into the relveant properties except for  `_totalHsfToDistribute` and `_endDistributionFraction` which are just  used for the one-time calculation. Also checks whether the given  `_endTime` is after the `_startTime` and if the maximum lock time is  larger than the minimum lock time.
* `poolLength()`: view, returns the amount of pools that the farm currently  tracks.
* `getPoolByIndex(uint256 _index)`: view, returns a tuple of pool information when given a  pool index. The pool information tuple contains the address of the  ERC20 token that needs to be deposited in order to earn rewards  \(`poolToken`\) for that pool, as well as all the information returned  by the poolInfo property in the same order.
* `setBaseURI`: allows the owner to set the baseURI of the contract. The  baseURI is used to determine the tokenURI as part of the ERC721 standard  metadata extension.
* `disableContract`: allows the owner to disable the contract. This  
   withdraws any remaining rewards and allows all depositors to withdraw  
   their tokens and accrued rewards regardless of the set unlock time. This  
   is implemented as a more trustless alternative to the classical migrator  
   method typically found in a lot of farming contracts.

  Emits a `Disabled()` event.

* `add`: adds a new pool if a pool for the specified ERC20 token does  
   already exist.

  Emits a `PoolAdded(IERC20 indexed poolToken, uint256 allocation)` event  
   with the token address and allocation points for the new pool.

* `set`: adjusts the allocation points of a given pool.

  Emits a `PoolUpdated(IERC20 indexed poolToken, uint256 allocation)`  
   event with the token address and the new allocation points.

* `getDistribution(uint256 _from, uint256 _to)`: view, returns the total  rewards that the contract will or has distributed between two  timestamps. Result scaled by `SCALE`.
* `getTimeMultiple(uint256 _unlockTime)`: view, returns the multiple a  deposit with an unlock time of `_unlockTime` if created with the current  `block.timestamp`. Result scaled by `SCALE`
* `pendingHsf(uint256 _depositId)`: view, returns the pending rewards for the deposit with a deposit ID of `_depositId`. Returns `0` if the deposit  does not exist. To verify whether a deposit exists simply use the  `ownerOf(uint256 _depositId)` method. If it reverts a deposit with the  given ID does not exist.
* `createDeposit(IERC20 _poolToken, uint256 _amount, uint256 _unlockTime, address _referrer)`: creates a new deposit in the specified pool. Create  
   a non-locked deposit if the `_unlockTime` parameter is set to `0`.  
   Requires the creator to have approved the contract to spend at least  
   `_amount` tokens and actually have the required balance. To indicate no  
   referrer simply call the `createDeposit` method with the zero address  
   as the referrer. Contracts which create deposits must make sure that  
   they’re able to appropriately handle incoming ERC721 token as specified  
   in EIP721.

  Emits a `Transfer(address indexed from, address indexed to, uint256 indexed tokenId)` event with the `from` address being the zero address.

  Emits a `Referred(address indexed referrer, uint256 depositId)` event if the set referrer is not the zero address.

* `closeDeposit(uint256 _depositId)`: closes the deposit if the sender is the  owner of the deposit. Also to be able to close the deposit the deposit  
   must either be a non-locked deposit or the `unlockTime` must have passed. Locked deposits may be unlocked early if the owner address decides to  disable the contract. Returns the deposited tokens as well as the accrued  rewards to the one closing their deposit. As well as rewarding the referral address \(if present\).

  Emits a `Transfer(address indexed from, address indexed to, uint256 indexed tokenId)` event with the `to` address being the zero address.

  Emits a `MissingReward(address indexed referrer, uint256 owedReward)`  
   event from the referral rewarder address if it has run out of rewards.

* `setReferralRewarder`: sets the address for the referral rewarder. Can only  be called once by the owner address and completes the initialization of  the farm.
* `withdrawRewards(uint256 _depositId)`: must be called by the owner of the deposit. Withdraws the rewards and resets the accumulator. Also  
   downgrades the deposit if the unlock time has passed. Also sends the  
   referrer rewards \(if one was set\). Partially withdraws the original  
   deposit as part of downgrade reward \(if the deposit was downgraded in  
   as part of the call\)

  Emits a `DepositDowngraded(address indexed downgrader, uint256 indexed depositId, uint256 downgradeReward)` event if the deposit has been downgraded.

  Emits a `RewardsWithdraw(uint256 indexed depositId, uint256 rewardAmount)` event with the outgoing xComb rewards as the `rewardAmount`

  Emits a `MissingReward(address indexed referrer, uint256 owedReward)`  
   event from the referral rewarder address if it has run out of rewards  
   \(never fired if no referrer set\).

* `downgradeExpired(uint256 _depositId)`: allows anyone to downgrade a  
   deposit who’s unlock time has passed and which hasn’t been downgraded  
   yet. Gives the caller a part of the original deposit as part of a  
   downgrade reward. The part that is given as a reward is determined by the  
   percentage stored in the `downgradeFee` property.

  Emits a `DepositDowngraded(address indexed downgrader, uint256 indexed depositId, uint256 downgradeReward)` event if the deposit has been downgraded with the caller as the `downgrader`.

* `updatePool(IERC20 _poolToken)`: updates the accumulator of the pool with  the given `_poolToken`. **Does not** emit a `PoolUpdated` event.
* `massUpdatePools()`: calls `updatePool` on all pools

