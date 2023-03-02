---
description: 'Token Contract Address:  0x4291F029B9e7acb02D49428458cf6fceAC545f81'
---

# Water

The Water token provides sustainable liquidity between 1Hive and other communities with aligned interests on Gnosis Chain. 100% of the circulating supply of Water is added to liquidity pools for these community tokens, letting Water serve as a proxy for shared liquidity between many tokens at once.

Thanks to the price correlation effect of tokens paired in liquidity pools on decentralized exchanges, Water itself functions like an index token of all the participating tokens.

### How it Works

Participating communities each provided $100k in their own token to join, which were paired with Water on [Honeyswap](https://app.honeyswap.org/) at an arbitrary value of $1 per Water, and are held in a Gnosis Safe owned by representatives from each community.

These liquidity pools (LPs) facilitate swaps, making it less expensive for people to buy and sell these tokens due to price slippage. Each token can route through Water, then through all the LPs of paired tokens, accessing the liquidity of all participating tokens.&#x20;

Because 100% of circulating Water is added to liquidity pools, the price of Water is a function of the price of the tokens it is paired with. [Profits from arbitrage](https://forum.1hive.org/t/water-shared-liquidity-proposal/5019/25) incentivize the trades that make price correlation reliable.

Once circulating, Water can be bought on the open market by anyone. When an investor buys Water, the value of Water and all its paired tokens increases due to price correlation, and since 100% of that initial circulating supply of Water is in LPs, there is no corresponding downside to this since there are no privately owned tokens to be sold.

As more investors choose to buy and hold Water, its price becomes more a function of speculation than price correlation alone. However, communities in Water can choose to add more liquidity to the LPs to regain the share of token supply in LPs vs. speculative tokens. In this way the communities can realize the gains provided by private investors.

### Governance

Water's governance is designed for security and simplicity.  A board of 12 representatives - 2 from each of the 6 projects included, serve as signers on 2 Gnosis Safes that execute transactions for Water:

1.  [Minting Safe](https://gnosis-safe.io/app/gno:0xb07d552A26940aB91a94aCff650e124820674124) (8 of 12 signers)

    Token Contract owner. This safe mints Water tokens, sends to the LP Safe to pair with project tokens, and holds leftover Water tokens after the liquidity pools are funded.
2.  [LP Safe](https://gnosis-safe.io/app/gno:0xb5F50e42aD28fB4BFc25b6B4c5a34AaD30649FC0) (5 of 12 signers)

    This safe holds community tokens to be paired with Water, funds liquidity pools, holds the LP tokens, and sends leftover Water tokens to the Minting Safe.

Participating communities agreed to the following terms, which are the board's responsibility to execute:

* **RageQuit -** Participating communities can choose to leave Water at anytime and get their tokens back at a 15% penalty (either getting back 85% of the total tokens it provided, or 85% of its tokens still in the LP, whichever is lower).&#x20;
* **ExCommunicate -** The governance board for Water can terminate a community from Water at no penalty, giving the community 100% of the tokens from their Water LP.&#x20;
* **ReUp -** The participating communities can collectively choose to add more liquidity to Water using the same governance process of the initial funding, so long as no new tokens are joining.

### Participating Communities

Their are 6 communities whose tokens are paired to Water:

* $HNY - [1Hive](https://1hive.eth.limo/) **-** A community of web3 builders
* $FOX - [Shapeshift](https://shapeshift.com/) - Non-custodial crypto asset management
* $BRIGHT - [BrightID](https://www.brightid.org/)  - Decentralized proof of unique humanity
* $GIV - [Giveth](https://giveth.io/) - Regenerative economic systems funding public goods
* $WORK - [Opolis](https://opolis.co/) - Simplifying self employment for workers in web3
* $TEC - [Token Engineering Commons](https://tecommons.org/) - Advancing the field of Token Engineering

### Water Resource Links:

* [Dune Analytics Dashboard](https://dune.com/paul2/water-token-dashboard)
* [Honeyswap Analytics](https://info.honeyswap.org/#/token/0x4291f029b9e7acb02d49428458cf6fceac545f81)
* [Blockscout](https://blockscout.com/xdai/mainnet/address/0x4291F029B9e7acb02D49428458cf6fceAC545f81)
* [Coingecko](https://www.coingecko.com/en/coins/1hive-water)

