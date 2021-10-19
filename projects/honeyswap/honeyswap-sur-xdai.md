# Honeyswap sur xDai

## Contrats et informations sur le déploiement

### Contrats AMM  <a href="amm-contracts" id="amm-contracts"></a>

Honeyswap sur xDai utilise les contrats AMM Uniswap v2.

**UniswapV2Factory**:[`0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7`](https://blockscout.com/poa/xdai/address/0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7)​

**UniswapV2Router02**:[`0x1C232F01118CB8B424793ae03F870aa7D0ac7f77`](https://blockscout.com/poa/xdai/address/0x1C232F01118CB8B424793ae03F870aa7D0ac7f77)​

**ReferralRewardManager:** [`0x82374C59709AAc2f7864191a3c492932379536F4`](https://blockscout.com/poa/xdai/address/0x82374C59709AAc2f7864191a3c492932379536F4/read-contract)​

**FeeReciever:** [`0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7`](https://blockscout.com/xdai/mainnet/address/0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7/transactions)`​`

### Subgraphs <a href="subgraphs" id="subgraphs"></a>

[Subgraph des fermes xDai](https://api.thegraph.com/subgraphs/name/1hive/honeyfarm-xdai/graphql). Le code source peut être trouvé [ici](https://github.com/1Hive/honeyfarm-subgraph).

[Ethereum Blocks](https://thegraph.com/explorer/subgraph/1hive/xdai-blocks). Le code source peut être trouvé [ici](https://github.com/1Hive/ethereum-blocks).

### Honeymaker <a href="honeymaker" id="honeymaker"></a>

[Honeymaker](https://github.com/1hive/honeymaker)  est un bot d'accompagnement qui fait appel périodiquement à la fonction  `takeProtocolFee()`du contrat FeeReceiver pour les paires sélectionnées sur Honeyswap afin de convertir les commissions LP gagnées en Honey et xComb.

## Pools de liquidité supportés <a href="supported-liquidity-pools" id="supported-liquidity-pools"></a>

Honeyswap sur xDai utilise les contrats d'Uniswap v2 pour le pool de liquidité. Tous les pools ont des frais de swap de 0,3%, dont 5/6 vont directement aux fournisseurs de liquidité impliqués dans le swap. Le 1/6 restant est réparti équitablement entre les rachats de HNY et de xComb.
