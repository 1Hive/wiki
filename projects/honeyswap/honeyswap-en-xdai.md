# Honeyswap en xDai

## Contratos de Honeyswap e información de implementación

### Contratos AMM&#x20;

Honeyswap en xDai utiliza los contratos AMM de Uniswap v2.

**UniswapV2Factory**:[`0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7`](https://blockscout.com/poa/xdai/address/0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7)

**UniswapV2Router02**:[`0x1C232F01118CB8B424793ae03F870aa7D0ac7f77`](https://blockscout.com/poa/xdai/address/0x1C232F01118CB8B424793ae03F870aa7D0ac7f77)

**ReferralRewardManager:** [`0x82374C59709AAc2f7864191a3c492932379536F4`](https://blockscout.com/poa/xdai/address/0x82374C59709AAc2f7864191a3c492932379536F4/read-contract)

**FeeReciever:** [`0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7`](https://blockscout.com/xdai/mainnet/address/0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7/transactions)``

### Subgraphs

[Honeyswap Subgraph on xDai](https://api.thegraph.com/subgraphs/name/1hive/honeyswap-xdai). Se puede encontrar el código fuente [aquí](https://github.com/1Hive/honeyswap-subgraph).

[Ethereum Blocks](https://thegraph.com/explorer/subgraph/1hive/xdai-blocks). Se puede encontrar el código fuente [aquí](https://github.com/1Hive/ethereum-blocks).

### Honeymaker

[Honeymaker](https://github.com/1hive/honeymaker) es un bot acompañante que llama periódicamente a la función `takeProtocolFee()` en el contrato FeeReceiver para pares seleccionados en Honeyswap para convertir las tarifas de LP ganadas a Honey y xComb.&#x20;
