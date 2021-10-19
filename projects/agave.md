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

## En quoi cela profite-t-il à la 1Hive ?

Currently, we have Honeyswap, which allows users to trade on xDAI with super low transaction fees. Given the relatively low volume, the total fees generated in HoneySwap (0.3% per trade) are rather low, and as such we have subsidized liquidity providers by allowing them to farm `HNY`. This has had mixed results.

With Agave, we would enable users to earn a yield on regular HoneySwap Liquidity tokens without a `HNY` subsidy. It also adds extra incentives to liquidity providers by giving them an additional stream of income above the fees generated on HoneySwap.

One of the most powerful features of DeFi is its composability. Currently, HoneySwap is not composable with the other DeFi protocols because it is on a separate chain. With Agave, we will now have another protocol on xDAI making it more ‘sticky’.

Although we will be forking Aave, we will use this as a base for a protocol that fits the needs of the 1Hive community.

Token listing on Agave will be more frictionless than Aave. Using Celeste, anyone can add a token to the Agave market by staking the Agave token, if a token does not meet the associated [Aragon Agreement](https://aragon.org/agreements) it can be challenged with Celeste.

These are some ways that Agave will provide `HNY` more utility as well as increase the price of `HNY`.
