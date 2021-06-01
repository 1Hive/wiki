# Honeyswap on Polygon

{% hint style="warning" %}
Honeyswap on Polygon and the pComb token has not been fully deployed. Information here is subject to change. 
{% endhint %}

## Supported Liquidity Pools

Honeyswap on Polygon uses the Swapr contracts \(which are lightly modified from Uniswap v2\) for pooling liquidity. The Swapr contracts support adjusting fees on a per pool basis. By default all pools have a 0.3% swap fee, with the exception of pools containing WETH, which have a 0.15% swap fee. This fee structure is designed to encourage the use of a common base pair in order to optimize liquidity pathways, however, there is not a strict requirement to use WETH pairs. 

Swap fees are split between Liquidity Providers involved in the swap \(5/6\) and the Platforms Fee Reciever contract \(1/6\). The Fee Receiver contract uses 1/2 of incoming fees to buyback Honey and the other half to buyback pComb tokens. 

## pCOMB Token

**The pComb token is the local incentive token for Honeyswap on Polygon.**

The value of pComb is derived from trading activity that occurs on Honeyswap on Polygon through automated buybacks tied to swap fees. Half of the repurchased pComb tokens are burned, the other half recycled back into the Farming mechanism for future distribrution. The pComb token has a fixed supply, which will become deflationary as a result of half of the pComb buybacks being burned. 

### pCOMB Supply and Emissions 

The total fixed supply of pComb tokens is `1,000,000`. An initial airdrop of `5%` of the total fixed supply will be airdropped to Honeyswap on Polygon user community. `10%` of airdropped tokens are immediately liquid, and the other `90%` are released continuously over `6 Months` .  

The remaining `95%` of pComb supply is scheduled to be distributed via the farming over the course of `2 years`, the emission rate decays linearly such that by the end of the initial emmission period  the rate is `25%` of the initial rate. 

1% of the pComb emissions can be earned by referring people to the farms, encouraging people to integrate and promote the farms.  The remainder of emissions are split between honeyswap pairs proportionally to their allocation points. Allocation points will be adjusted over time to curate the available liquidity in order to attract traders and maximize volume on the exchange. The following table shows the current distribution of allocation points among pairs:

| Pair | Points |
| :--- | :--- |
| wETH-pCOMB | 18 |
| wETH-USDC | 3 |
| wETH-HNY | 3 |
| wETH-wMATIC | 3 |
| wETH-wBTC | 3 |
| wETH-USDT | 2 |
| wETH-DAI | 2 |
| wETH-AAVE | 2 |
| wETH-MUST | 1 |
| wETH-QUICK | 1 |
| wETH-GHST | 1 |
| wETH-LINK | 1 |

This initial allocation of points to pairs took historic trading volume on Polygon based exchanges into account, a framework for evaluating and adding additional pairs is being worked on. Stay tuned!

## Honeyswap Contracts

Honeyswap on Polygon uses the DxSwap contracts, which were forked from the Uniswap v2 contracts. These contracts allow fees to be adjusted on a per pool basis, the default fee per pool is still 0.3%, but pools containing WETH are 0.15%. 

### Contracts

**Factory**: [`0x6F937495013C7DC42aF752d3E0BcC090bd34F7AB`](https://explorer-mainnet.maticvigil.com/address/0x6F937495013C7DC42aF752d3E0BcC090bd34F7AB)\`\`

**Router**:[`0x346880305b57c5A8AaF4170D951f13e91c0bE0a7`](https://explorer-mainnet.maticvigil.com/address/0x346880305b57c5A8AaF4170D951f13e91c0bE0a7/transactions)\`\`

### Subgraphs

Pending Deployment

### Fee Receiver Contract

Pending Deployment.

