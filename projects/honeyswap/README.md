---
description: >-
  Honeyswap est un réseau d'échanges décentralisés qui est géré et entretenu par
  la communauté 1Hive.
---

# Honeyswap

## Aperçu

Honeyswap est un dispositif composé de contrats de pool de liquidité déployés sur plusieurs chaînes compatibles EVM qui partagent des interfaces communes gérées par la communauté 1Hive. Pour le moment, Honeyswap fonctionne sur xDai et Polygon, mais prévoit d'étendre le support à d'autres chaînes EVM et rollups dans le futur.

Honeyswap utilise un **modèle multi-token** pour gérer l'équilibre entre les incitations **globales** et **locales**. Le développement, le support et le travail de maintenance qui ont des avantages **globaux** sont financés en utilisant le Honey du pool commun de 1Hive. Les récompenses des fermes, où les avantages sont localisés sur une chaîne spécifique, utilisent **un token Comb** qui peut être considéré comme un dérivé du volume sur cette chaîne spécifique.

Les frais d'échange sur Honeyswap sont répartis comme suit : \
1/12 → Honey\
1/12 → Token Comb local de la chaîne \
5/6 → Directement vers le pool de fournisseurs de liquidités ayant facilité l'échange

{% hint style="info" %}
**Les transactions des paires ETH sur Polygon ont des frais réduits (0,15%)**
{% endhint %}

## Interface Honeyswap

L'[interface Honeyswap](https://app.honeyswap.org/#/swap) offre une expérience open source pour le trading et le pooling de liquidité. Elle prend également en charge le routage des transactions vers des pools de liquidité tiers, de sorte que les utilisateurs soient sûrs d'obtenir la meilleure exécution pour leurs transactions.

Vous pouvez vous connecter à Honeyswap à partir de n'importe quel réseau pris en charge, et vous serez en mesure d'interagir avec le pool sur ce réseau.

## Honeyswap Analytics&#x20;

[Honeyswap Analytics](https://info.honeyswap.org) offre une interface open source pour analyser la liquidité, le volume et l'historique des transactions.

## Gestionnaire d'actifs Honeycomb

Honeycomb offre une interface open source pour la gestion des positions DeFi, y compris le dépôt et le retrait sur les fermes Comb.

## Contrats Honeyswap et informations sur le déploiement&#x20;

Les contrats et le déploiement associé sont similaires mais pas identiques. Veuillez consulter les sous-sections correspondantes pour obtenir des informations détaillées sur les déploiements sur les différents réseaux pris en charge.
