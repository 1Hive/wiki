# Honeyswap on Polygon

{% hint style="warning" %}
Honeyswap on Polygon and the pComb token has not been fully deployed. Information here is subject to change.
{% endhint %}

## Supported Liquidity Pools

Honeyswap on Polygon uses the Swapr contracts \(which are lightly modified from Uniswap v2\) for pooling liquidity. The Swapr contracts support adjusting fees on a per pool basis. By default all pools have a 0.3% swap fee, with the exception of pools containing wETH, which have a 0.15% swap fee. This fee structure is designed to encourage the use of a common base pair in order to optimize liquidity pathways, however, there is not a strict requirement to use wETH pairs.

Swap fees are split between Liquidity Providers involved in the swap and the Platform's Fee Receiver contract. Liquidity Providers receive 5/6 in fees from each swap, while the Platform Fee Receiver contract receives 1/6 of each swap fee. The Fee Receiver contract uses 1/2 of incoming fees to buy back Honey and the other 1/2 to buy back pComb tokens.

## pCOMB Token

**The pComb token is the local incentive token for Honeyswap on Polygon.**

The value of pComb is derived from trading activity that occurs on Honeyswap on Polygon through automated buybacks tied to swap fees. Half of the repurchased pComb tokens are burned, the other half recycled back into the Farming mechanism for future distribrution. The pComb token has a fixed supply, which will become deflationary as a result of half of the pComb buybacks being burned.

### pCOMB Supply and Emissions

The total fixed supply of pComb tokens is `1,000,000`. An initial airdrop of `5%` of the total fixed supply will be airdropped to the Polygon DeFi user community, including liquidity providers on Honeyswap. `10%` of airdropped tokens are immediately liquid, and the other `90%` are released continuously over `6 months` .

Another `5%` of total fixed supply has been reserved for future promotional purposes by the Tulip Swarm.

The remaining `90%` of pComb supply is scheduled to be distributed via farming over the course of `2 years`, the emission rate decays linearly such that by the end of the initial emission period the rate is `25%` of the initial rate.

1% of the pComb emissions can be earned by referring people to the farms, encouraging people to integrate and promote the farms. The remainder of emissions are split between Honeyswap pairs proportionally to their allocation points.

The pComb allocation points are managed by a multisig of Tulip swarm contributors. _This privilege may be revoked or re-assigned via a pComb-weighted decision vote following the deployment of Gardens, 1Hive's on-chain governance platform, to Polygon_.

The Tulip Swarm's goal for managing the allocation points is to promote the growth of both liquidity and volume on the exchange. Therefore we may need to adjust the Allocation Points policy over time.

### Our Current Policy

**Allocation Point Capacity** - We have chosen to limit the total number of allocation points assigned at any one time to **1,000**. There may be less than 1,000 points assigned at any given time, but not more.

#### Current Allocation

At the time of launch the farms will only be using 600 out of a total of 1000 available allocation points. As the remaining 400 allocation points are added the proportioanl rewards will be diluted.

**Keystone Pool** - We have allocated up to **300** points to support the keystone pair **pComb-WEth** in order to ensure there is a strong incentive to provide liquidity to the reward token.

**Discretionary Pool** - We have **300** points reserved for discretionary use. These points have been used to establish the initial incentivized pairs. **After 4 months** of farming rewards these points will be reassessed and may be re-allocated.

#### Projected Allocations

We plan on piloting additional incentive programs over the next few months using the allocation point system and have reserved allocation points accordingly.

**Trader Pool** - We have allocated **300** points for a trading incentive program. The intent of this program is to reward traders for using Honeyswap. Traders will be periodically awarded a token proportional to their trading volume on Honeyswap. Once the trading incentive program launches, users will be able to deposit this token to earn pComb rewards just like an LP token.

**Performance Pool** - We have allocated **75** points to support a KPI-driven reward program, where a set of eligible pools compete for allocation points in an initial 4-month long pilot season.

**Discovery Pool** - We have allocated **25** points to promote new or relatively illiquid tokens in an effort to establish Honeyswap as the primary venue for trading these tokens.

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
| stkWETH-GHST | 25 | Pending GHST Vote |

## Honeyswap Contracts

Honeyswap on Polygon uses the DxSwap contracts, which were forked from the Uniswap v2 contracts. These contracts allow fees to be adjusted on a per pool basis, the default fee per pool is still 0.3%, but pools containing WETH have a 0.15% fee.

### Contracts

**Factory**: [`0x6F937495013C7DC42aF752d3E0BcC090bd34F7AB`](https://explorer-mainnet.maticvigil.com/address/0x6F937495013C7DC42aF752d3E0BcC090bd34F7AB)\`\`

**Router**:[`0x346880305b57c5A8AaF4170D951f13e91c0bE0a7`](https://explorer-mainnet.maticvigil.com/address/0x346880305b57c5A8AaF4170D951f13e91c0bE0a7/transactions)\`\`

### Subgraphs

Pending Deployment

### Fee Receiver Contract

Pending Deployment.

