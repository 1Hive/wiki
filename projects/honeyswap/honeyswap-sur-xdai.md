# Honeyswap sur xDai

## Pools de liquidité supportés <a id="supported-liquidity-pools"></a>

Honeyswap sur xDai utilise les contrats d'Uniswap v2 pour le pool de liquidité. Tous les pools ont des frais de swap de 0,3%, dont 5/6 vont directement aux fournisseurs de liquidité impliqués dans le swap. Le 1/6 restant est réparti équitablement entre les rachats de HNY et de xComb.

## Token xComb <a id="xcomb-token"></a>

xComb est le token d'incitation local de Honeyswap sur xDai.

La valeur de xComb est liée à l'activité de trading de Honeyswap sur xDai par le biais de rachats automatisés liés aux frais de swap. La moitié des tokens xComb rachetés sont brûlés, l'autre moitié est recyclée dans le mécanisme de _Farming_ pour une distribution future. Le token xComb a une offre fixe, qui deviendra déflationniste du fait que la moitié des rachats de xComb sera brûlée.

### xComb Supply and Emissions <a id="xcomb-supply-and-emissions"></a>

The total fixed supply of xComb tokens is `1,000,000`. An initial airdrop of `5%` of the total fixed supply was airdropped to existing Honeyswap Liquidity providers proportional to the amount time and liquidity value contributed to Honeyswap prior to the airdrop. `10%` of airdropped tokens are immediately liquid, and the other `90%` are released continuously over `6 Months` .

The remaining `95%` of the xComb supply is scheduled to be distributed via farming over the course of `2 years`, the emission rate decays linearly such that by the end of the initial emmission period the rate is `25%` of the initial rate.

1% of the xComb emissions can be earned by referring people to the farms, encouraging people to integrate and promote the farms. The remainder of emissions are split between honeyswap pairs proportionally to their allocation points. Allocation points will be adjusted over time to curate the available liquidity in order to attract traders and maximize volume on the exchange. The following table shows the current distribution of allocation points among pairs:

The pairs included in the farms will be adjusted over time, a framework for evaluating and adding additional pairs is being worked on. Stay tuned!

## Gouvernance <a id="governance"></a>

The Honeyswap AMM contracts are not upgradeable. Governance is limited to setting the fee reciever address.

The xComb token does not have any governance, it has a fixed supply and cannot be upgraded.

xComb farming contract is not upgradeable, but the xComb tokens held by the contract can be withdrawn to via governance in order to transition the farming rewards to a new contract. Governance of the farms has been split into two distinct roles using a wrapper contract.

**Manager:** Can add, remove, and adjust allocation points of pools.

**Admin**: Can change the manager address and initialize a migration by withdrawing xComb and unlocking all time-locked deposits.

Initially the [Tulip swarm multisig](https://xdai.gnosis-safe.io/app/#/safes/0xD5a0d695589Fa9dEC023638b8dD24D71f051C63C/balances) will serve as the Manager, and 1Hive [Decisions](https://wiki.1hive.org/projects/honey/decisions) will control the Admin role.

## Deployment Information <a id="deployment-information"></a>

### AMM Contracts <a id="amm-contracts"></a>

Honeyswap on xDai uses the Uniswap v2 AMM contracts.

**UniswapV2Factory**:[`0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7`](https://blockscout.com/poa/xdai/address/0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7)​

**UniswapV2Router02**:[`0x1C232F01118CB8B424793ae03F870aa7D0ac7f77`](https://blockscout.com/poa/xdai/address/0x1C232F01118CB8B424793ae03F870aa7D0ac7f77)​

### Farm Contracts <a id="farm-contracts"></a>

**xCombToken**: [`0x38Fb649Ad3d6BA1113Be5F57B927053E97fC5bF7`](https://blockscout.com/poa/xdai/address/0x38Fb649Ad3d6BA1113Be5F57B927053E97fC5bF7/read-contract)​

**xCombFarm**: [`0xB44825cF0d8D4dD552f2434056c41582415AaAa1`](https://blockscout.com/poa/xdai/address/0xB44825cF0d8D4dD552f2434056c41582415AaAa1/read-contract)​

**xCombFarm Governance Wrapper:** [`0xfBA19af3bE412E08AF9c7Cf60756d238D3cEAd25`](https://blockscout.com/poa/xdai/address/0xfBA19af3bE412E08AF9c7Cf60756d238D3cEAd25/read-contract)​

**xCombAirdrop:** [`0xdD36008685108aFafc11F88bBc66C39A851Df843`](https://blockscout.com/poa/xdai/address/0xdD36008685108aFafc11F88bBc66C39A851Df843/read-contract)​

**ReferralRewardManager:** [`0x82374C59709AAc2f7864191a3c492932379536F4`](https://blockscout.com/poa/xdai/address/0x82374C59709AAc2f7864191a3c492932379536F4/read-contract)​

**FeeReciever:** [`0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7`](https://blockscout.com/xdai/mainnet/address/0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7/transactions)`​`

### Subgraphs <a id="subgraphs"></a>

The deployment data is indexed by forks of two subgraphs:

​[Uniswap v2 Subgraph](https://thegraph.com/explorer/subgraph/1hive/uniswap-v2): A fork of the official Uniswap v2 subgraph with adjustments to use xDai as the base currency and a modified set of whitelisted tokens. Source code can be found [here](https://github.com/1Hive/uniswap-v2-subgraph).

​[Ethereum Blocks](https://thegraph.com/explorer/subgraph/1hive/xdai-blocks): A fork of the Blocklytics Ethereum Blocks subgraph with no modifications, deployed for xDai. Source code can be found [here](https://github.com/1Hive/ethereum-blocks).

### Honeymaker <a id="honeymaker"></a>

​[Honeymaker](https://github.com/1hive/honeymaker) is an accompanying bot that periodically calls the `takeProtocolFee()` function on the FeeReceiver contract for selected pairs on Honeyswap to convert the LP fees earned to Honey and xComb.

