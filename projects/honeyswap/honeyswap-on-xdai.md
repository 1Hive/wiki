# Honeyswap on xDai

## Honeyswap Contracts and Deployment Info

### AMM Contracts

Honeyswap on xDai uses the Uniswap v2 AMM contracts.

**UniswapV2Factory**:[`0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7`](https://blockscout.com/poa/xdai/address/0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7)

**UniswapV2Router02**:[`0x1C232F01118CB8B424793ae03F870aa7D0ac7f77`](https://blockscout.com/poa/xdai/address/0x1C232F01118CB8B424793ae03F870aa7D0ac7f77)

**ReferralRewardManager:** [`0x82374C59709AAc2f7864191a3c492932379536F4`](https://blockscout.com/poa/xdai/address/0x82374C59709AAc2f7864191a3c492932379536F4/read-contract)

**FeeReciever:** [`0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7`](https://blockscout.com/xdai/mainnet/address/0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7/transactions)\`\`

### Subgraphs

[Honeyswap Subgraph on xDai](https://api.thegraph.com/subgraphs/name/1hive/honeyswap-xdai). Source code can be found [here](https://github.com/1Hive/honeyswap-subgraph).

[Ethereum Blocks](https://thegraph.com/explorer/subgraph/1hive/xdai-blocks). Source code can be found [here](https://github.com/1Hive/ethereum-blocks).

### Honeymaker

[Honeymaker](https://github.com/1hive/honeymaker) is an accompanying bot that periodically calls the `takeProtocolFee()` function on the FeeReceiver contract for selected pairs on Honeyswap to convert the LP fees earned to Honey and xComb.

