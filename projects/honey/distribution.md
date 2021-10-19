---
description: >-
  Conviction voting is used to regulate the distribution of Honey from the
  common pool.
---

# Distribution

## Conviction Voting

Conviction Voting allows proposals to be created and considered continuously and simultaneously. Participants can signal their preferences for the proposals they support, but they are not able to “double count” their influence across multiple proposals.&#x20;

When they start supporting a proposal, the support (called conviction) does not immediately apply, but instead must charge up over time according to an exponential decay function or half-life.

Currently there are two types of proposals that impact Honey distribution, signaling proposals which **do not** request honey, and funding proposals which **do** request honey.

For funding proposals, there is an execution threshold that is determined based on the proportion of funds requested relative to the funds available in the common pool. The greater the proportion, the greater the threshold required.

For a deeper dive on the conviction voting, check out this [cadCAD model](https://github.com/BlockScience/Aragon\_Conviction\_Voting) exploring the mechanism.

The conviction voting implementation 1Hive uses has been developed in collaboration with [Aragon](https://aragon.org), [Commons Stack](https://commonsstack.org), and [Block Science](https://block.science).
