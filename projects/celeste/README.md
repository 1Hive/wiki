---
description: Un oracle subjectif en développement.
---

# Celeste \(Coming soon\)

Nous avons parlé de Celeste et de son importance pour 1hive, mais il n'y a pas eu une source d'informations de haut niveau sur ce que c'est, comment cela fonctionne et pourquoi c'est important en un seul endroit.

TLDR : Celeste répond aux questions en les posant à une sélection aléatoire d'utilisateurs. Les utilisateurs ne se connaissent pas mais doivent répondre de la même manière que la majorité. Quiconque ne répond pas de la même manière que la majorité perdra de l'argent, quiconque répondra avec la majorité gagnera de l'argent. On s'attend à ce que cela amène les utilisateurs à répondre conformément aux valeurs et normes communautaires établies. Dans le cadre du protocole 1Hive, Celeste ne sera pas utilisé pour décider du résultat d’un vote, mais sera utilisé pour décider si un vote appartient ou non à l’organisation.

## Qu'est-ce que c'est

Celeste is a Subjective Oracle, enabling smart contracts to ask questions and receive answers, it can be used to resolve subjective disputes, settle prediction markets, moderate content, and more by enabling developers of decentralized applications to construct and arbitrate challenge-response games.

By invoking Celeste, a developer can align incentives between parties by ensuring that it is common knowledge that defectors from an agreed upon strategy will be punished.

On a technical level, Celeste is a fork of [Aragon Court](https://aragon.org/court), which is used for decentralized dispute resolution. The main difference between Celeste and Aragon Court, besides being on xDai and using Honey as its staking token, is that we have chosen to integrate brightID in order to limit how much stake individuals can add to the system.

## Comment ça marche

In order to understand how celeste works, its helpful to first understand the general pattern of an optimistic, or challenge-response game.

Let’s say we want to create an escrow workflow for 1hive’s proposal process. Alice creates a proposal saying they will work on a project that is broken up into milestones, funds are placed into escrow and released upon request as milestones are completed. When Alice completes the first milestone, she can place a deposit as collateral in order to request the associated funds are released along with proof that the milestone was completed as expected. We can then, from a smart contract perspective, _optimistically_ assume that Alice is honest and completed the work as expected even though the smart contract has no way to validate that the work was actually completed, so long as no one is willing to dispute the action by putting up an equal amount of collateral and block the withdrawal.

This same pattern can be used in a wide range of use cases, where there is public knowledge of what is true, but where it is not practical or simply impossible to compute that in a smart contract because the determination or judgement required is subjective in nature.

A naive solution to this problem is to just have people vote when there is a need to provide subjective information to a smart contract. But having everyone participate in a vote every time would be incredibly inefficient, what we want to do instead is to create a system where the first person interacting has a strong incentive to provide the contract with the proper information, and a sufficient disincentive to provide incorrect information.

Coming back to the example of escrow, when Alice makes the request to withdraw funds and attests that she has completed the work, Bob observes the request and determines that the proof that Alice has provided is insufficient, and chooses to challenge the withdrawal by putting up collateral and offering Alice the opportunity to withdraw their request or to add additional collateral in order to escalate and resolve the dispute by invoking Celeste.

In most cases there won’t be any need for disputes, the fact that the disputes can be escalated will be enough in most cases to ensure that participants act honestly, but in the event that there is a dispute, participants who have staked honey in Celeste will be drafted to provide a resolution.

The protocol selects participants \(keepers\) to evaluate a dispute and provide a resolution. They are selected proportionally to amount of honey they have staked. We assume that the majority of drafted participants will provide the correct result, but allow anyone to appeal this decision to a larger group of keepers, until we reach a final appeal round where all actively staked keepers can participate in the resolution. As things are appealed the cost in terms of both time, capital, and attention increases, and as it does we can also expect the precedent set by the decision to have a greater impact and either build or erode significant trust in the mechanism as a whole. Essentially the process is designed to minimize the need to create disputes and to resolve disputes with minimal need for escalation, but as disputes do get escalated the the incentive to provide the most appropriate response is amplified.

By incorporating brightID in Celeste we improve upon purely stake based incentives by ensuring that influence over outcomes are broadly distributed and represent a greater number of unique perspectives in the eventual outcomes, making the mechanism more resilient to attacks and making the subjective resolutions more legitimate.

## Pourquoi c'est important

There are a bunch of new and interesting opportunities that can be built on Celeste, we can use it to settle prediction markets, create escrow type workflows, curate and categorize tokens on honeyswap, and even help validate computation that happens off-chain.

However, the most important initial use case for 1hive is integrating celeste with conviction voting mechanism that we use to distribute honey, so that we can enable the community to dispute and block proposals that may have sufficient support to execute but which do not align with the expections of the community defined in the community covenant.

Additionally, from a purely economic perspective, Celeste is really valuable to 1hive for two reasons.

1. People will need to stake honey to participate as a keeper, and pay fees in honey in order to create and appeal disputes. As demand to use celeste increases, we will see demand to buy and hold honey increase.
2. Because we are limiting the amount of honey individuals can stake in Celeste, we can expect that by promoting adoption of Celeste we will see the gini-coefficient of Honey decrease resulting in a more resilient and decentralized community.

## Quand sera-t-il prêt

Celeste has been under active development for some time. There is still lots to do, but we expect to be able to launch Celeste and upgrade the 1hive DAO so that conviction proposals and decisions can be disputed before the end of the year. Keep an eye on the Celeste swarm in discord if you’d like to get involved or follow progress, we should have additional progress, updates, and roll out plans to share over the coming weeks.![:sun\_with\_face:](https://forum.1hive.org/images/emoji/apple/sun_with_face.png?v=9)![:sun\_with\_face:](https://forum.1hive.org/images/emoji/apple/sun_with_face.png?v=9)![:sun\_with\_face:](https://forum.1hive.org/images/emoji/apple/sun_with_face.png?v=9)

## **Liens utiles**

Discussion sur Celeste :

{% embed url="https://forum.1hive.org/t/celeste-a-brief-primer/1483" %}

