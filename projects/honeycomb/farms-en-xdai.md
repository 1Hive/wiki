# Farms en xDai

## xComb Token

**El token xComb es el token de incentivo local para Honeyswap en xDai.**

El valor de xComb se deriva de la actividad comercial que se produce en Honeyswap en xDai a través de recompras automatizadas vinculadas a tarifas de intercambio. La mitad de los tokens xComb recomprados se queman, la otra mitad se recicla nuevamente en el mecanismo de farming para su futura distribución. El token xComb tiene un suministro fijo, que se volverá deflacionario como resultado de la quema de la mitad de las recompras de xComb.

### Suministro y Emisiones de xComb&#x20;

El suministro fijo total de tokens xComb es de `1,000,000`. Un airdrop inicial del 5% del suministro fijo total se envió a los proveedores de liquidez existentes de Honeyswap  proporcionalmente a la cantidad de tiempo y valor de liquidez aportados a Honeyswap antes del airdrop. El `10%` de los tokens del airdrop son inmediatamente líquidas y el otro `90%` se libera continuamente durante `6 Meses`.

El `95%` del suministro restante de xComb está programado para distribuirse a través del farming en el transcurso de `2 years`, la tasa de emisión decae linealmente de tal manera que al final del período de emisión inicial la tasa es el `25%` de la tasa inicial.

El 1% de las emisiones de xComb puede obtenerse invitando personas a las farms, alentando a las personas a integrarse y promocionar las farms. El resto de las emisiones se dividen entre pares de intercambio de honeyswap proporcionalmente a sus puntos de asignación. Los puntos de asignación se ajustarán con el tiempo para seleccionar la liquidez disponible con el fin de atraer a los operadores y maximizar el volumen en el intercambio. La siguiente tabla muestra la distribución actual de puntos de asignación entre pares:

| Par        | Puntos |
| ---------- | ------ |
| xDAI-xComb | 20     |
| xDAI-HNY   | 5      |
| xDAI-AGVE  | 5      |
| HNY-AGVE   | 3      |
| HNY-WETH   | 3      |
| xDAI-STAKE | 2      |
| xDAI-LINK  | 2      |
| WETH-WBTC  | 2      |
| xDAI-WETH  | 2      |
| USDC-xDAI  | 1      |

Los pares incluidos en las farms se irán ajustando con el tiempo, se está trabajando en un marco para evaluar y agregar pares adicionales.

## Gobernanza

Los contratos AMM de Honeyswap no se pueden actualizar. La gobernanza se limita a establecer la dirección del receptor de la tarifa.&#x20;

El token xComb no tiene ninguna gobernanza, tiene un suministro fijo y no se puede actualizar.

El contrato de farming de xComb no se puede actualizar, pero los tokens de xComb en poder del contrato se pueden retirar a través de la gobernanza para hacer la transición de las recompensas de farm a un nuevo contrato. La gobernanza de las farms se ha dividido en dos funciones distintas mediante un contrato wrapper.

**Manager:** Puede agregar, eliminar y ajustar puntos de asignación de pools.

**Admin**: Puede cambiar la dirección del administrador e inicializar una migración retirando xComb y desbloqueando todos los depósitos bloqueados por tiempo.

Inicialmente, el multisig [Tulip swarm ](https://xdai.gnosis-safe.io/app/#/safes/0xD5a0d695589Fa9dEC023638b8dD24D71f051C63C/balances)actuará como administrador, y las [decisiones](../honey/decisiones.md) de controlarán el rol de administrador.

## Contratos de las Farms

**xCombToken**: [`0x38Fb649Ad3d6BA1113Be5F57B927053E97fC5bF7`](https://blockscout.com/poa/xdai/address/0x38Fb649Ad3d6BA1113Be5F57B927053E97fC5bF7/read-contract)

**xCombFarm**: [`0xB44825cF0d8D4dD552f2434056c41582415AaAa1`](https://blockscout.com/poa/xdai/address/0xB44825cF0d8D4dD552f2434056c41582415AaAa1/read-contract)

**xCombFarm Governance Wrapper:** [`0xfBA19af3bE412E08AF9c7Cf60756d238D3cEAd25`](https://blockscout.com/poa/xdai/address/0xfBA19af3bE412E08AF9c7Cf60756d238D3cEAd25/read-contract)

**xCombAirdrop:** [`0xdD36008685108aFafc11F88bBc66C39A851Df843`](https://blockscout.com/poa/xdai/address/0xdD36008685108aFafc11F88bBc66C39A851Df843/read-contract)

**FeeReceiver:** [`0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7`](https://blockscout.com/xdai/mainnet/address/0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7/transactions)``

### Subgraphs

[Farms Subgraph on xDai](https://api.thegraph.com/subgraphs/name/1hive/honeyfarm-xdai). El código fuente se puede encontrar [aquí](https://github.com/1Hive/honeyfarm-subgraph).
