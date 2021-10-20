---
description: Protocole de prêt
---

# Agave

{% hint style="warning" %}
Cette page reflète la [proposition initiale d'Agave](https://forum.1hive.org/t/announcing-agaave-aave-on-xdai/1792). Agave est toujours en cours de développement et cette page peut encore être incomplète ou inexacte.
{% endhint %}

## Aperçu

Agave est un protocole décentralisé de marché monétaire non-custodial où les utilisateurs peuvent participer en tant que déposants ou emprunteurs. Il s'agit d'un fork de [Aave](https://aave.com) déployé sur xDAI.&#x20;

Les déposants fournissent des liquidités au marché pour gagner un revenu passif, tandis que les emprunteurs peuvent emprunter de manière surcollatéralisée (perpétuellement) ou sous-collatéralisée (liquidité d'un bloc) (c'est-à-dire des prêts flash).

### Comment ça fonctionne ?

Les utilisateurs déposent des tokens dans le protocole, ils reçoivent en retour un aToken. Ce aToken produit ensuite des intérêts. En outre, lorsqu'ils déposent, les utilisateurs peuvent choisir d'utiliser leur dépôt comme garantie et l'utiliser pour emprunter d'autres actifs. Ceci est fonctionnellement équivalent à l'offre d'un effet de levier. Par exemple, si un utilisateur dépose des `HNY`, il peut ensuite les utiliser comme garantie pour emprunter des `DAI` et acheter d'autres `HNY`.

## Possibilités

### Prêts

Les utilisateurs peuvent prêter des tokens au protocole. L'intérêt est déterminé dynamiquement par le taux d'utilisation du token dans le protocole. Ainsi, lorsque l'offre du token diminue, le taux d'intérêt augmente.

### Emprunts

Une fois qu'un utilisateur a prêté au protocole, il dispose d'une ligne de crédit qu'il peut utiliser pour emprunter.

### Emprunts par délégation

Les prêteurs peuvent étendre leur ligne de crédit à d'autres adresses. Cela donne effectivement la possibilité aux utilisateurs qui n'ont rien déposé dans Agave de prêter à partir du protocole sans capital.

### Prêts Flash

Les prêts flash Agave sont plus puissants que la plupart des prêts proposés sur mainnet. Les utilisateurs peuvent emprunter plusieurs tokens dans la même transaction. De plus, les prêts flash d'Agave n'ont pas besoin d'être totalement remboursés dans la même transaction : Une partie du prêt peut être ajoutée comme dette si l'utilisateur a suffisamment de garanties dans le protocole.

## Token

Agave dispose d'un token principalement utilisé pour la gouvernance du protocole.

* Ajouter/supprimer des tokens du marché
* Activer/désactiver la possibilité d'utiliser des tokens spécifiques comme garantie
* Définir les taux de garantie
* LTV Maximum _(loan to value rate)_
* Seuil de liquidation
* Pénalité de liquidation
* Utilisé comme garantie
* Emprunt stable

Le jeton est également _stakeable_, ce qui permet aux détenteurs d'AGAVE de percevoir un rendement sur le token `AGAVE` lui-même. Le pool de tokens mis en jeu est utilisé comme assurance en cas de déficit.

## En quoi cela profite-t-il à 1Hive ?

Actuellement, nous avons Honeyswap, qui permet aux utilisateurs de négocier sur xDAI avec des frais de transaction très bas. Étant donné le volume relativement faible, les frais totaux générés par HoneySwap (0,3 % par transaction) sont plutôt bas, et nous avons donc subventionné les fournisseurs de liquidités en leur permettant de farmer HNY. Les résultats sont mitigés.

Avec Agave, nous permettons aux utilisateurs d'obtenir un rendement sur les tokens de liquidité standards de HoneySwap sans subvention en `HNY`. Cela ajoute des incitations supplémentaires aux fournisseurs de liquidité en leur donnant un flux de revenu supplémentaire en plus des frais générés sur HoneySwap.

Une des caractéristiques les plus importantes de la DeFi est sa composabilité. Actuellement, HoneySwap n'est pas composable avec les autres protocoles DeFi car il est sur une chaîne séparée. Avec Agave, nous aurons maintenant un autre protocole sur xDAI, ce qui le rendra plus "collant".

Même si nous allons forker Aave, nous l'utiliserons comme base pour un protocole qui correspond aux besoins de la communauté 1Hive.

Le listing de tokens sur Agave sera plus simple que sur Aave. En utilisant Celeste, n'importe qui peut ajouter un token au marché Agave en stakant le token Agave. Si un token ne respecte pas l'[accord Aragon](https://aragon.org) associé, il peut être contesté avec Celeste.

Ce sont là quelques exemples de la manière dont Agave fournira plus d'utilité à `HNY`, tout en augmentant le prix de `HNY`.
