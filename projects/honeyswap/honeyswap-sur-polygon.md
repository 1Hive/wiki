# Honeyswap sur Polygon

{% hint style="info" %}
Honeyswap sur Polygon et le token pComb n'ont pas été entièrement déployés. Les informations présentées ici sont susceptibles d'être modifiées.
{% endhint %}

## Pools de liquidité supportés <a id="supported-liquidity-pools"></a>

Honeyswap sur Polygon utilise les contrats Swapr \(qui sont légèrement modifiés à partir d'Uniswap v2\) pour le pool de liquidité. Les contrats Swapr permettent d'ajuster les frais sur une base par pool. Par défaut, tous les pools ont des frais de swap de 0,3%, à l'exception des pools contenant wETH, qui ont des frais de swap de 0,15%. Cette structure de frais est conçue pour encourager l'utilisation d'une paire de base commune afin d'optimiser les voies de liquidité, cependant, il n'y a pas d'obligation stricte d'utiliser les paires wETH.

Les frais de swap sont répartis entre les fournisseurs de liquidité impliqués dans le swap et le contrat Fee Receiver de la plate-forme. Les fournisseurs de liquidité reçoivent 5/6 des frais de chaque swap, tandis que le contrat Fee Receiver de la plateforme reçoit 1/6 des frais de swap. Le contrat Fee Receiver utilise la moitié des frais entrants pour racheter du Honey et l'autre moitié pour racheter des tokens pComb.

## Token pComb  <a id="pcomb-token"></a>

**pComb est le token d'incitation local de Honeyswap sur Polygon.**

La valeur de pComb est liée à l'activité de trading de Honeyswap sur Polygon par le biais de rachats automatisés liés aux frais de swap. La moitié des tokens pComb rachetés sont brûlés, l'autre moitié est recyclée dans le mécanisme de _Farming_ pour une distribution future. Le token pComb a une offre fixe, qui deviendra déflationniste du fait que la moitié des rachats de pComb sera brûlée.

### pComb – Offre et émission  <a id="pcomb-supply-and-emissions"></a>

The total fixed supply of pComb tokens is `1,000,000`. An initial airdrop of `5%` of the total fixed supply will be airdropped to the Polygon DeFi user community, including liquidity providers on Honeyswap. `10%` of airdropped tokens are immediately liquid, and the other `90%` are released continuously over `6 months` .

Another `5%` of total fixed supply has been reserved for future promotional purposes by the Tulip Swarm.

The remaining `90%` of pComb supply is scheduled to be distributed via farming over the course of `2 years`, the emission rate decays linearly such that by the end of the initial emission period the rate is `25%` of the initial rate.

1% of the pComb emissions can be earned by referring people to the farms, encouraging people to integrate and promote the farms. The remainder of emissions are split between Honeyswap pairs proportionally to their allocation points.

The pComb allocation points are managed by a multisig of Tulip swarm contributors. _This privilege may be revoked or re-assigned via a pComb-weighted decision vote following the deployment of Gardens, 1Hive's on-chain governance platform, to Polygon_.

L'objectif du Tulip Swarm en matière de gestion des points d'allocation est de promouvoir la croissance de la liquidité et du volume sur l'échange. Par conséquent, il se peut que nous devions ajuster la politique des points d'allocation au fil du temps.

### Notre politique actuelle <a id="our-current-policy"></a>

**Nombre de points d'allocation** - Nous avons choisi de limiter à 1000 le nombre total de points d'allocation attribués à un moment donné. Il peut y avoir moins de 1000 points d'allocation à un moment donné, mais pas plus.

#### Allocation actuelle <a id="current-allocation"></a>

Au moment du lancement, les fermes n'utiliseront que 600 points d'allocation sur un total de 1000 disponibles. Au fur et à mesure que les 400 points d'allocation restants seront ajoutés, les récompenses proportionnelles seront diluées.

**Keystone Pool** - Nous avons alloué jusqu'à **300** points pour soutenir la paire clé **pComb-wETH** afin de garantir une forte incitation à fournir des liquidités au token de récompense.

**Réserve à discrétion** - Nous avons **300** points réservés pour une utilisation à discrétion. Ces points ont été utilisés pour établir les premières paires incitatives. Après **4 mois** de farming, ces points seront réévalués et pourront être réaffectés.

#### Allocations prévues <a id="projected-allocations"></a>

We plan on piloting additional incentive programs over the next few months using the allocation point system and have reserved allocation points accordingly.

**Trader Pool** - We have allocated **300** points for a trading incentive program. The intent of this program is to reward traders for using Honeyswap. Traders will be periodically awarded pComb proportional to their trading volume on Honeyswap. Details on the trading rewards program will be announced as they become available.

**Performance Pool** - We have allocated **75** points to support a metrics-driven reward program, where a set of eligible pools compete for allocation points in an initial 4-month long pilot season.

**Discovery Pool** - We have allocated **25** points to promote new or relatively illiquid tokens in an effort to establish Honeyswap as the primary venue for trading these tokens.

### Tableau des points d'allocation actuels de pComb <a id="current-pcomb-allocation-points-table"></a>

| Paire | Points | Catégorie |
| :--- | :--- | :--- |
| wETH-pCOMB | 300 | Keystone |
| wETH-HNY | 50 | à discrétion |
| wETH-wMATIC | 50 | à discrétion |
| wETH-wBTC | 50 | à discrétion |
| wETH-USDC | 50 | à discrétion |
| wETH-USDT | 25 | à discrétion |
| wETH-DAI | 25 | à discrétion |
| wETH-AAVE | 25 | à discrétion |

## Contrats Honeyswap  <a id="honeyswap-contracts"></a>

Honeyswap sur Polygon utilise les contrats DxSwap, qui sont un fork des contrats Uniswap v2. Ces contrats permettent d'ajuster les frais de chaque pool, les frais par défaut par pool sont toujours de 0,3%, mais les pools contenant du WETH ont des frais de 0,15%.

### Contrats <a id="contracts"></a>

**Factory**: [`0x6F937495013C7DC42aF752d3E0BcC090bd34F7AB`](https://explorer-mainnet.maticvigil.com/address/0x6F937495013C7DC42aF752d3E0BcC090bd34F7AB)​

**Router**:[`0x346880305b57c5A8AaF4170D951f13e91c0bE0a7`](https://explorer-mainnet.maticvigil.com/address/0x346880305b57c5A8AaF4170D951f13e91c0bE0a7/transactions)​

### Subgraphs <a id="subgraphs"></a>

Déploiement en attente

### Fee Receiver Contract <a id="fee-receiver-contract"></a>

Déploiement en attente

