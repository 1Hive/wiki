# Fermes xDai

## Token xComb <a href="xcomb-token" id="xcomb-token"></a>

**xComb est le token d'incitation local de Honeyswap sur xDai.**

La valeur de xComb est liée à l'activité de trading de Honeyswap sur xDai par le biais de rachats automatisés liés aux frais de swap. La moitié des tokens xComb rachetés sont brûlés, l'autre moitié est recyclée dans le mécanisme de _Farming_ pour une distribution future. Le token xComb a une offre fixe, qui deviendra déflationniste du fait que la moitié des rachats de xComb sera brûlée.

### xComb – Offre et émission  <a href="xcomb-supply-and-emissions" id="xcomb-supply-and-emissions"></a>

L'offre totale fixe de tokens xComb est de`1,000,000`. Un airdrop initial de `5%` a été envoyé aux fournisseurs de liquidité Honeyswap existants, proportionnellement au temps et à la valeur de la liquidité qu'ils ont fourni sur Honeyswap avant l'airdrop. `10%`des jetons largués sont immédiatement liquides, et les `90%` restants sont libérés en continu sur `6 mois`.

Les `95%` restants de l'approvisionnement en xComb sont distribués par l'intermédiaire du farming sur une période de `2 ans`, le taux d'émission décroît linéairement de sorte qu'à la fin de la période initiale d'émission, le taux sera `25%` du taux initial.

1% des émissions de xComb peuvent être gagnées en référant des personnes aux fermes, en encourageant les gens à participer et en faisant la promotion des fermes. Le reste des émissions est réparti entre les paires d'échange de Honeyswap proportionnellement à leurs points d'allocation. Les points d'allocation seront ajustés au fil du temps pour gérer la liquidité disponible afin d'attirer les traders et de maximiser le volume sur l'échange. Le tableau suivant montre la répartition actuelle des points d'allocation entre les paires :

| Paire      | Points |
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

Les paires incluses dans les fermes seront ajustées au fil du temps, un cadre pour l'évaluation et l'ajout de paires supplémentaires est en cours d'élaboration. Restez à l'écoute !

## Gouvernance <a href="governance" id="governance"></a>

Les contrats de l'AMM Honeyswap ne peuvent pas être mis à niveau. La gouvernance se limite à la définition de l'adresse du destinataire des frais.&#x20;

Le token xComb n'a pas de gouvernance, il a un approvisionnement fixe et ne peut pas être upgradé.

Le contrat de farming xComb n'est pas évolutif, mais les jetons xComb détenus par le contrat peuvent être retirés via la gouvernance afin de transférer les récompenses de farming vers un nouveau contrat. La gouvernance des fermes a été divisée en deux rôles distincts à l'aide d'un contrat _wrapper_.&#x20;

**Manager :** Peut ajouter, supprimer et ajuster les points d'allocation des pools.

**Admin **: Peut changer l'adresse du gestionnaire et initialiser une migration en retirant xComb et en débloquant tous les dépôts bloqués dans le temps.&#x20;

Initialement, le [Tulip swarm multisig](https://xdai.gnosis-safe.io/app/#/safes/0xD5a0d695589Fa9dEC023638b8dD24D71f051C63C/balances) servira de Manager, et les [Décisions](https://wiki.1hive.org/v/francais/projects/honey/decisions) 1Hive contrôleront le rôle d'Admin.

## Contrats des fermes <a href="farm-contracts" id="farm-contracts"></a>

**xCombToken**: [`0x38Fb649Ad3d6BA1113Be5F57B927053E97fC5bF7`](https://blockscout.com/poa/xdai/address/0x38Fb649Ad3d6BA1113Be5F57B927053E97fC5bF7/read-contract)​

**xCombFarm**: [`0xB44825cF0d8D4dD552f2434056c41582415AaAa1`](https://blockscout.com/poa/xdai/address/0xB44825cF0d8D4dD552f2434056c41582415AaAa1/read-contract)​

**xCombFarm Governance Wrapper:** [`0xfBA19af3bE412E08AF9c7Cf60756d238D3cEAd25`](https://blockscout.com/poa/xdai/address/0xfBA19af3bE412E08AF9c7Cf60756d238D3cEAd25/read-contract)​

**xCombAirdrop:** [`0xdD36008685108aFafc11F88bBc66C39A851Df843`](https://blockscout.com/poa/xdai/address/0xdD36008685108aFafc11F88bBc66C39A851Df843/read-contract)​

**ReferralRewardManager:** [`0x82374C59709AAc2f7864191a3c492932379536F4`](https://blockscout.com/poa/xdai/address/0x82374C59709AAc2f7864191a3c492932379536F4/read-contract)​

**FeeReciever:** [`0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7`](https://blockscout.com/xdai/mainnet/address/0xbA13a6414C677d9e7BD3c0BDE5BA4055BF2e72f7/transactions)`​`

### Subgraphs <a href="subgraphs" id="subgraphs"></a>

[Subgraph des fermes xDai](https://api.thegraph.com/subgraphs/name/1hive/honeyfarm-xdai/graphql). Le code source peut être trouvé [ici](https://github.com/1Hive/honeyfarm-subgraph).
