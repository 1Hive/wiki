# Fermes Polygon

## Token pComb  <a href="pcomb-token" id="pcomb-token"></a>

**pComb est le token d'incitation local de Honeyswap sur Polygon.**

La valeur de pComb est liée à l'activité de trading de Honeyswap sur Polygon par le biais de rachats automatisés liés aux frais de swap. La moitié des tokens pComb rachetés sont brûlés, l'autre moitié est recyclée dans le mécanisme de _Farming_ pour une distribution future. Le token pComb a une offre fixe, qui deviendra déflationniste du fait que la moitié des rachats de pComb sera brûlée.

### pComb – Offre et émission  <a href="pcomb-supply-and-emissions" id="pcomb-supply-and-emissions"></a>

L'offre totale fixe de tokens pComb est de `1'000'000`. Un premier airdrop de `5%` de l'offre totale sera effectué auprès de la communauté DeFi sur Polygon, y compris les fournisseurs de liquidités sur Honeyswap. `10%` des jetons largués sont immédiatement liquides, et les `90%` restants sont distribués en continu sur `6 mois`.

`5%` de l'offre totale fixe a été réservée à des fins promotionnelles futures par le Tulip Swarm.

Les `90%` restants de l'approvisionnement en pComb seront distribués par le biais du farming sur une période de `2 ans`, le taux d'émission décroît linéairement de telle sorte qu'à la fin de la période d'émission initiale, le taux sera `25%` du taux initial.

1% des émissions de pComb peuvent être gagnées en référant des personnes aux fermes, en encourageant les gens à participer et en faisant la promotion des fermes. Le reste des émissions est réparti entre les paires d'échange de Honeyswap proportionnellement à leurs points d'allocation.

Les points d'allocation pComb sont gérés par un multisig de contributeurs du Tulip Swarm. Ce privilège peut être révoqué ou réattribué par le biais d'un vote de décision pondéré par pComb, après le déploiement de Gardens, la plateforme de gouvernance on-chain de 1Hive.

L'objectif du Tulip Swarm en matière de gestion des points d'allocation est de promouvoir la croissance de la liquidité et du volume sur l'échange. Par conséquent, il se peut que nous devions ajuster la politique des points d'allocation au fil du temps.

## Notre politique actuelle <a href="our-current-policy" id="our-current-policy"></a>

**Nombre de points d'allocation** - Nous avons choisi de limiter à 1000 le nombre total de points d'allocation attribués à un moment donné. Il peut y avoir moins de 1000 points d'allocation à un moment donné, mais pas plus.

### Allocation actuelle <a href="current-allocation" id="current-allocation"></a>

Au moment du lancement, les fermes n'utiliseront que 600 points d'allocation sur un total de 1000 disponibles. Au fur et à mesure que les 400 points d'allocation restants seront ajoutés, les récompenses proportionnelles seront diluées.

**Keystone Pool** - Nous avons alloué jusqu'à **300** points pour soutenir la paire clé **pComb-wETH** afin de garantir une forte incitation à fournir des liquidités au token de récompense.

**Réserve à discrétion** - Nous avons **300** points réservés pour une utilisation à discrétion. Ces points ont été utilisés pour établir les premières paires incitatives. Après **4 mois** de farming, ces points seront réévalués et pourront être réaffectés.

### Allocations prévues <a href="projected-allocations" id="projected-allocations"></a>

Nous prévoyons de déployer d'autres programmes d'incitation au cours des prochains mois et avons réservé des points d'allocation en conséquence.

**Trader Pool** - Nous avons alloué 300 points pour un programme d'incitation au trading. Le but de ce programme est de récompenser les traders qui utilisent Honeyswap. Les traders recevront périodiquement des pComb proportionnellement à leur volume d'échange sur Honeyswap. Les détails sur le programme de récompenses de trading seront annoncés dès qu'ils seront disponibles.

**Performance Pool** - Nous avons alloué 75 points pour soutenir un programme de récompense basé sur des données chiffrées, dans lequel un ensemble de pools éligibles sont en concurrence pour obtenir des points d'allocation au cours d'une saison pilote initiale de 4 mois.

**Discovery Pool** - Nous avons alloué 25 points pour promouvoir des nouveaux tokens, ou relativement illiquides, dans le but d'établir Honeyswap comme principal lieu d'échange pour ces tokens.

### Tableau des points d'allocation actuels de pComb <a href="current-pcomb-allocation-points-table" id="current-pcomb-allocation-points-table"></a>

| Paire       | Points | Catégorie    |
| ----------- | ------ | ------------ |
| wETH-pCOMB  | 300    | Keystone     |
| wETH-HNY    | 50     | à discrétion |
| wETH-wMATIC | 50     | à discrétion |
| wETH-wBTC   | 50     | à discrétion |
| wETH-USDC   | 50     | à discrétion |
| wETH-USDT   | 25     | à discrétion |
| wETH-DAI    | 25     | à discrétion |
| wETH-AAVE   | 25     | à discrétion |

## Gouvernance <a href="governance" id="governance"></a>

Le token pComb n'a pas de gouvernance, il a un approvisionnement fixe et ne peut pas être upgradé.

Le contrat de farming pComb n'est pas évolutif, mais les jetons xComb détenus par le contrat peuvent être retirés via la gouvernance afin de transférer les récompenses de farming vers un nouveau contrat. La gouvernance des fermes a été divisée en deux rôles distincts à l'aide d'un contrat _wrapper_.&#x20;

**Manager :** Peut ajouter, supprimer et ajuster les points d'allocation des pools.

**Admin **: Peut changer l'adresse du gestionnaire et initialiser une migration en retirant xComb et en débloquant tous les dépôts bloqués dans le temps.&#x20;

Initialement, le [Tulip swarm multisig](https://xdai.gnosis-safe.io/app/#/safes/0xD5a0d695589Fa9dEC023638b8dD24D71f051C63C/balances) servira de Manager, et les [Décisions](https://wiki.1hive.org/v/francais/projects/honey/decisions) 1Hive contrôleront le rôle d'Admin.

## Contrats des Fermes  <a href="honeyswap-contracts" id="honeyswap-contracts"></a>

Honeyswap sur Polygon utilise les contrats DxSwap, qui sont un fork des contrats Uniswap v2. Ces contrats permettent d'ajuster les frais de chaque pool, les frais par défaut par pool sont toujours de 0,3%, mais les pools contenant du WETH ont des frais de 0,15%.

**pComb Token **: [`0x37d1ebc3af809b8fadb45dce7077efc629b2b5bb`](https://polygonscan.com/token/0x37d1ebc3af809b8fadb45dce7077efc629b2b5bb)

**pComb Farm **:** **[`0x62d7E2484FCFc6752B9473260efE1B86caBAc34e`](https://polygonscan.com/address/0x62d7E2484FCFc6752B9473260efE1B86caBAc34e#code)

**pCombAirdrop :** [`0x3Fe30742aD8491402c8aee251ff57e3E9b18Ff87`](https://polygonscan.com/address/0x3fe30742ad8491402c8aee251ff57e3e9b18ff87#code)``

### Subgraph

[Honeyswap Subgraph sur Polygon](fermes-polygon.md#contrats-et-informations-sur-le-deploiement). Le code source peut être trouvé [ici](https://github.com/1Hive/honeyswap-subgraph).
