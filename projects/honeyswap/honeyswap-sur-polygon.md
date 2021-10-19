# Honeyswap sur Polygon

## Contrats et informations sur le déploiement

### Contrats AMM

**Honeyswap Factory**: [`0x03DAa61d8007443a6584e3d8f85105096543C19c`](https://polygonscan.com/address/0x03DAa61d8007443a6584e3d8f85105096543C19c/contracts#code)****

**Honeyswap Router**: [`0xaD340d0CD0B117B0140671E7cB39770e7675C848`](https://polygonscan.com/address/0xaD340d0CD0B117B0140671E7cB39770e7675C848/contracts#code)

**ReferralRewardReceiver**: [`0xf72e8827aa4c03e2c49aa95a6550dd4c8a65a969`](https://polygonscan.com/address/0xf72e8827aa4c03e2c49aa95a6550dd4c8a65a969#code)``

**FeeReceiver**: [`0xA25958B0C9bbEE1821dB5CE3d85bc56848Fddf78`](https://polygonscan.com/address/0xA25958B0C9bbEE1821dB5CE3d85bc56848Fddf78#code)

### Subgraphs

[Honeyswap Subgraph sur Polygon](honeyswap-sur-polygon.md#contrats-et-informations-sur-le-deploiement). Le code source peut être trouvé [ici](https://github.com/1Hive/honeyswap-subgraph).

### Honeymaker

[Honeymaker](https://github.com/1hive/honeymaker)  est un bot d'accompagnement qui fait appel périodiquement à la fonction  `takeProtocolFee()`du contrat FeeReceiver pour les paires sélectionnées sur Honeyswap afin de convertir les commissions LP gagnées en Honey et pComb.

## Pools de liquidité supportés <a href="supported-liquidity-pools" id="supported-liquidity-pools"></a>

Honeyswap sur Polygon utilise les contrats Swapr (qui sont légèrement modifiés à partir d'Uniswap v2) pour le pool de liquidité. Les contrats Swapr permettent d'ajuster les frais sur une base par pool. Par défaut, tous les pools ont des frais de swap de 0,3%, à l'exception des pools contenant wETH, qui ont des frais de swap de 0,15%. Cette structure de frais est conçue pour encourager l'utilisation d'une paire de base commune afin d'optimiser les voies de liquidité, cependant, il n'y a pas d'obligation stricte d'utiliser les paires wETH.

Les frais de swap sont répartis entre les fournisseurs de liquidité impliqués dans le swap et le contrat Fee Receiver de la plate-forme. Les fournisseurs de liquidité reçoivent 5/6 des frais de chaque swap, tandis que le contrat Fee Receiver de la plateforme reçoit 1/6 des frais de swap. Le contrat Fee Receiver utilise la moitié des frais entrants pour racheter du Honey et l'autre moitié pour racheter des tokens pComb.

