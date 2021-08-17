# Farms on Polygon

## pCOMB Token

**The pComb token is the local incentive token for Honeyswap on Polygon.**

The value of pComb is derived from trading activity that occurs on Honeyswap on Polygon through automated buybacks tied to swap fees. Half of the repurchased pComb tokens are burned, the other half recycled back into the Farming mechanism for future distribution. The pComb token has a fixed supply, which will become deflationary as a result of half of the pComb buybacks being burned.

### pCOMB Supply and Emissions

The total fixed supply of pComb tokens is `1,000,000`. An initial airdrop of `5%` of the total fixed supply will be airdropped to the Polygon DeFi user community, including liquidity providers on Honeyswap. `10%` of airdropped tokens are immediately liquid, and the other `90%` are released continuously over `6 months` .

Another `5%` of total fixed supply has been reserved for future promotional purposes by the Tulip Swarm.

The remaining `90%` of pComb supply is scheduled to be distributed via farming over the course of `2 years`, the emission rate decays linearly such that by the end of the initial emission period the rate is `25%` of the initial rate.

1% of the pComb emissions can be earned by referring people to the farms, encouraging people to integrate and promote the farms. The remainder of emissions are split between Honeyswap pairs proportionally to their allocation points.

The pComb allocation points are managed by a multisig of Tulip swarm contributors. _This privilege may be revoked or re-assigned via a pComb-weighted decision vote following the deployment of Gardens, 1Hive's on-chain governance platform, to Polygon_.

The Tulip Swarm's goal for managing the allocation points is to promote the growth of both liquidity and volume on the exchange. Therefore we may need to adjust the Allocation Points policy over time.

## Our Current Policy

**Allocation Point Capacity** - We have chosen to limit the total number of allocation points assigned at any one time to **1,000**. There may be less than 1,000 points assigned at any given time, but not more.

### Current Allocation

At the time of launch the farms will only be using 575 out of a total of 1000 available allocation points. As the remaining 425 allocation points are added the proportional rewards will be diluted.

**Keystone Pool** - We have allocated up to **300** points to support the keystone pair **pComb-wETH** in order to ensure there is a strong incentive to provide liquidity to the reward token.

**Discretionary Pool** - We have **300** points reserved for discretionary use. These points have been used to establish the initial incentivized pairs. **After 4 months** of farming rewards these points will be reassessed and may be re-allocated.

### Projected Allocations

We plan on piloting additional incentive programs over the next few months using the allocation point system and have reserved allocation points accordingly.

**Trader Pool** - We have allocated **300** points for a trading incentive program. The intent of this program is to reward traders for using Honeyswap. Traders will be periodically awarded pComb proportional to their trading volume on Honeyswap. Details on the trading rewards program will be announced as they become available.

**Performance Pool** - We have allocated **75** points to support a metrics-driven reward program, where a set of eligible pools compete for allocation points in an initial 4-month long pilot season.

**Discovery Pool** - We have allocated **50** points to promote new or relatively illiquid tokens in an effort to establish Honeyswap as the primary venue for trading these tokens.

### Current pComb Allocation Points Table

| Pair | Points | Category |
| :--- | :--- | :--- |
| wETH-pCOMB | 300 | Keystone |
| wETH-HNY | 50 | Discretionary |
| wETH-wMATIC | 50 | Discretionary |
| wETH-wBTC | 50 | Discretionary |
| wETH-USDC | 50 | Discretionary |
| wETH-USDT | 25 | Discretionary |
| wETH-DAI | 25 | Discretionary |
| wETH-AAVE | 25 | Discretionary |
| SURF-WAVE | 13 | Discovery |

## Governance

The pComb token does not have any governance, it has a fixed supply and cannot be upgraded.

xComb farming contract is not upgradeable, but the xComb tokens held by the contract can be withdrawn to via governance in order to transition the farming rewards to a new contract. Governance of the farms has been split into two distinct roles using a wrapper contract.

**Manager:** Can add, remove, and adjust allocation points of pools.

**Admin**: Can change the manager address and initialize a migration by withdrawing xComb and unlocking all time-locked deposits.

Initially the [Tulip swarm multisig ](https://polygon.gnosis-safe.io/app/#/safes/0xD5a0d695589Fa9dEC023638b8dD24D71f051C63C/balances)will serve as the Manager, and 1Hive [Decisions](../honey/decisions.md) will control the Admin role.

## Farm Contracts

**pComb Token**: [`0x37d1ebc3af809b8fadb45dce7077efc629b2b5bb`](https://polygonscan.com/token/0x37d1ebc3af809b8fadb45dce7077efc629b2b5bb)

**pComb Farm**: ****[`0x62d7E2484FCFc6752B9473260efE1B86caBAc34e`](https://polygonscan.com/address/0x62d7E2484FCFc6752B9473260efE1B86caBAc34e#code)

**pCombAirdrop:** [`0x3Fe30742aD8491402c8aee251ff57e3E9b18Ff87`](https://polygonscan.com/address/0x3fe30742ad8491402c8aee251ff57e3e9b18ff87#code)\`\`

### Subgraphs

[Farms Subgraph on xDai](https://api.thegraph.com/subgraphs/name/1hive/honeyfarm-xdai). Source code can be found [here](https://github.com/1Hive/honeyfarm-subgraph).

