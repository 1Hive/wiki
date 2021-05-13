# Honeyswap on xDai

## Supported Liquidity Pools

Honeyswap on xDai uses the Uniswap v2 contracts for pooling liquidity. All pools have a 0.3% swap fee, of which 5/6 go directly to Liquidity Providers involved in the swap. The remaining 1/6 is split evenly between buybacks of Honey and xComb.

## xComb Token

The xComb token is the local incentive token for Honeyswap on xDai.

The value of xComb is derived from trading activity that occurs on Honeyswap on xDai through automated buybacks tied to swap fees. Half of the repurchased xComb tokens are burned, the other half recycled back into the Farming mechanism for future distribrution. The xComb token has a fixed supply, which will become deflationary as a result of half of the xComb buybacks being burned. 

### xComb Supply and Emissions 

The total fixed supply of xComb tokens is `1,000,000`. An initial airdrop of `5%` of the total fixed supply was airdropped to existing Honeyswap Liquidity providers proportional to the amount time and liquidity value contributed to Honeyswap prior to the airdrop. Airdropped tokens are not immediately liquid, they are subject to a vesting period and get released continuously over `xdays` . 

The remaining xComb supply is scheduled to be distributed via the farming over the course of `2 years`, the emission rate decays linearly such that by the end of the initial emmission period  the rate is `25%` of the initial rate. 

1% of the xComb emissions can be earned by referring people to the farms, encouraging people to integrate and promote the farms.  The remainder of emissions are split between honeyswap pairs proportionally to their allocation points. Allocation points will be adjusted over time to curate the available liquidity in order to attract traders and maximize volume on the exchange. The following table shows the current distribution of allocation points among pairs:

| Pair | Points |
| :--- | :--- |
| HNY-xComb | 20 |
| HNY-AGVE | 4 |
| HNY-WETH | 4 |
| HNY-xDAI | 4 |
| AGVE-WETH | 2 |
| HNY-STAKE | 2 |
| HNY-LINK | 2 |
| WETH-WBTC | 1 |
| HNY-WBTC | 1 |
| USDC-xDAI | 1 |

This initial allocation of points to pairs took historic trading volume on Honeyswap into account, a framework for evaluating and adding additional pairs is being worked on. Stay tuned!

## Deployment Information

Honeyswap on xDai uses the Uniswap v2 contracts. 

### Contracts

**UniswapV2Factory**:[`0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7`](https://blockscout.com/poa/xdai/address/0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7)\*\*\*\*

**UniswapV2Router02**:[`0x1C232F01118CB8B424793ae03F870aa7D0ac7f77`](https://blockscout.com/poa/xdai/address/0x1C232F01118CB8B424793ae03F870aa7D0ac7f77)

**xCombToken**: Pending Deployment

**xCombFarm**: Pending Deployment

**FeeReciever:** Pending Deployment

### Subgraphs

The deployment data is indexed by forks of two subgraphs:

[Uniswap v2 Subgraph](https://thegraph.com/explorer/subgraph/1hive/uniswap-v2): A fork of the official Uniswap v2 subgraph with adjustments to use xDai as the base currency and a modified set of whitelisted tokens. Source code can be found [here](https://github.com/1Hive/uniswap-v2-subgraph).

[Ethereum Blocks](https://thegraph.com/explorer/subgraph/1hive/xdai-blocks): A fork of the Blocklytics Ethereum Blocks subgraph with no modifications, deployed for xDai. Source code can be found [here](https://github.com/1Hive/ethereum-blocks).

### Fee Receiver Contract

Honeymaker is a SushiMaker deployment and accompanying bot that converts LP shares on Honeyswap into Honey for the Honey Common Pool.

SushiMaker is deployed at [`0x076b64f9F966e3bBD0FCdC79D490Ab71cF961bb0`](https://blockscout.com/poa/xdai/address/0x076b64f9F966e3bBD0FCdC79D490Ab71cF961bb0).

The bot periodically calls the `convert` function on the SushiMaker contract for selected pairs on Honeyswap to convert the LP shares to Honey.

The source code for the bot can be found [here](https://github.com/1hive/honeymaker).

