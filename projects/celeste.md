---
description: An in development subjective oracle.
---

# Celeste

Visit the [Celeste documentation](https://1hive.gitbook.io/celeste/) for more detailed information.

TLDR: Celeste answers questions by asking them to a random selection of users. The users do not know each other but must answer the same as the majority. Anyone not answering the same as the majority will lose money, anyone answering along with the majority will make money. It is expected this will lead users to answer in accordance with established community values and norms. Within the 1Hive protocol Celeste will not be used to decide a vote’s outcome but will be used to decide whether or not a vote belongs within the organisation.

## What is it

Celeste is a Subjective Oracle, enabling smart contracts to ask questions and receive answers, it can be used to resolve subjective disputes, settle prediction markets, moderate content, and more by enabling developers of decentralized applications to construct and arbitrate challenge-response games.

By invoking Celeste, a developer can align incentives between parties by ensuring that it is common knowledge that defectors from an agreed upon strategy will be punished.

On a technical level, Celeste is a fork of [Aragon Court](https://aragon.org/court), which is used for decentralized dispute resolution. The main difference between Celeste and Aragon Court, besides being on xDai and using Honey as its staking token, is that we have chosen to integrate brightID in order to limit how much stake individuals can add to the system.

## How it works

In order to understand how celeste works, its helpful to first understand the general pattern of an optimistic, or challenge-response game.

Let’s say we want to create an escrow workflow for 1hive’s proposal process. Alice creates a proposal saying they will work on a project that is broken up into milestones, funds are placed into escrow and released upon request as milestones are completed. When Alice completes the first milestone, she can place a deposit as collateral in order to request the associated funds are released along with proof that the milestone was completed as expected. We can then, from a smart contract perspective, _optimistically_ assume that Alice is honest and completed the work as expected even though the smart contract has no way to validate that the work was actually completed, so long as no one is willing to dispute the action by putting up an equal amount of collateral and block the withdrawal.

This same pattern can be used in a wide range of use cases, where there is public knowledge of what is true, but where it is not practical or simply impossible to compute that in a smart contract because the determination or judgement required is subjective in nature.

A naive solution to this problem is to just have people vote when there is a need to provide subjective information to a smart contract. But having everyone participate in a vote every time would be incredibly inefficient, what we want to do instead is to create a system where the first person interacting has a strong incentive to provide the contract with the proper information, and a sufficient disincentive to provide incorrect information.

Coming back to the example of escrow, when Alice makes the request to withdraw funds and attests that she has completed the work, Bob observes the request and determines that the proof that Alice has provided is insufficient, and chooses to challenge the withdrawal by putting up collateral and offering Alice the opportunity to withdraw their request or to add additional collateral in order to escalate and resolve the dispute by invoking Celeste.

In most cases there won’t be any need for disputes, the fact that the disputes can be escalated will be enough in most cases to ensure that participants act honestly, but in the event that there is a dispute, participants who have staked honey in Celeste will be drafted to provide a resolution.

The protocol selects participants \(keepers\) to evaluate a dispute and provide a resolution. They are selected proportionally to amount of honey they have staked. We assume that the majority of drafted participants will provide the correct result, but allow anyone to appeal this decision to a larger group of keepers, until we reach a final appeal round where all actively staked keepers can participate in the resolution. As things are appealed the cost in terms of both time, capital, and attention increases, and as it does we can also expect the precedent set by the decision to have a greater impact and either build or erode significant trust in the mechanism as a whole. Essentially the process is designed to minimize the need to create disputes and to resolve disputes with minimal need for escalation, but as disputes do get escalated the the incentive to provide the most appropriate response is amplified.

By incorporating brightID in Celeste we improve upon purely stake based incentives by ensuring that influence over outcomes are broadly distributed and represent a greater number of unique perspectives in the eventual outcomes, making the mechanism more resilient to attacks and making the subjective resolutions more legitimate.

## Why its important

There are a bunch of new and interesting opportunities that can be built on Celeste, we can use it to settle prediction markets, create escrow type workflows, curate and categorize tokens on honeyswap, and even help validate computation that happens off-chain.

However, the most important initial use case for 1hive is integrating celeste with conviction voting mechanism that we use to distribute honey, so that we can enable the community to dispute and block proposals that may have sufficient support to execute but which do not align with the expections of the community defined in the community covenant.

Additionally, from a purely economic perspective, Celeste is really valuable to 1hive for two reasons.

1. People will need to stake honey to participate as a keeper, and pay fees in honey in order to create and appeal disputes. As demand to use celeste increases, we will see demand to buy and hold honey increase.
2. Because we are limiting the amount of honey individuals can stake in Celeste, we can expect that by promoting adoption of Celeste we will see the gini-coefficient of Honey decrease resulting in a more resilient and decentralized community.

## **Useful Links**

Discussion about Celeste:

{% embed url="https://forum.1hive.org/t/celeste-a-brief-primer/1483" %}

