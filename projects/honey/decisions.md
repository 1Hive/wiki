---
description: >-
  Changes to protocol parameters or smart contract updates requires making
  discrete, binary choice decisions via voting.
---

# Décisions

## Decision Surface

From a design perspective, 1Hive aims to minimize the need to make discrete decisions, favoring bottom up decision making and local autonomy of participants. Therefore, we do **not** use decisions for day to day operations or determining strategic direction. However, we have a process for making these types of decisions so that we have some ability to make changes to the protocol and parameters over time.  

The 1Hive DAO is made up of smart contracts that regulate how Honey is issued and distributed. As a young project we expect there will be a need to upgrade or change parameters that influence how these contracts work. We expect that the need for such changes will become increasing rare, and perhaps eventually become so rare they are deemed unnecessary, but for now it is seems prudent to retain the ability to upgrade contracts via decision votes. If and when the community deems appropriate a decision vote can be used to remove the capability of making any future decisions. 

## Decision Process

The decision process is made purposely difficult and biased towards the status quo. Making changes to the protocol and parameters is by design a fairly arduous process that should not be undertaken lightly. 

Since decisions are used infrequently and only to make technical changes to the protocol or parameters **there is no user interface for the creation of a decision**. A technical user must prepare a transaction which creates a decision vote, its best practice for such transactions to be reviewed by many people publicly before they are submitted. The account that submits a decision is required to send **5 Honey to the common pool** as part of the vote creation process, they can make a proposal to request reimbursement but there is no guarantee that such a proposal will be supported especially if the creation of decision vote was not expected or broadly supported by the community. 

Once a vote is created it will show up in the frontend as a _decision._ Voting on each decision is open for 2 weeks. In order to pass there must be an **approval quorum** of atleast 10 percent of the total supply voting in favor, and over 50% of voters in support. If a vote is approved, there is a 48 hour delay before the vote can be enacted, allowing people to react to the outcome and make decisions before the effects of the vote are realized. 

Additionally, the entire balance of Honey for accounts which vote in support of a decision are locked as soon as they vote yes, preventing all transfers from their address until after the vote has concluded. This restriction helps to ensure that people that vote in favor of a decision have a strong belief that approving the decision is both necessary and beneficial to the community because they will be locked in and exposed  to any changes in value associated with a controversial decision being forced through, while people who vote against are free to exit by selling their Honey.

