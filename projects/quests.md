# Quests

{% hint style="warning" %}
Quests is still under development, if you wish to contribute join the [🌟Quests Swarm](../community/swarms/quests.md).
{% endhint %}

Quests is a Celeste enabled incentivised bounty platform allowing users or organisations to publish bounties for work which anyone can claim by providing evidence of completion. Quests are open ended and are defined purely by a text description, quest players submit a text description as evidence for completing a quest which can be verified by other users and disputed with Celeste should the evidence not meet the original quests criteria.

## Overview

Each quest is a single contract and consists of:

* A title and [description](quests.md#quest-descriptions) of the work required.
* The reward ERC20 token which any user or organisation can send to the quests contract address to fund.&#x20;
* An expiry time and refund address.

Quest players submit claim requests for a quest, including evidence, for some or all of the quests available bounty, along with a deposit. The claim request is fulfillable after a 7 day delay period.&#x20;

During the delay period other users can [verify](quests.md#verifying-a-quest) that the evidence submitted demonstrates completion of the quest. If they believe that the quest has not been completed to the standard specified in the quest description then it can be challenged, also requiring a deposit, and raising it to Celeste which will decide whether the work has been completed as expected or not.&#x20;

The Celeste outcome will determine whether or not the claim request should be fulfilled and who is rewarded with the participants deposits. Whoever out of the player and challenger loses will lose their deposit to the winner.

## Quest descriptions

Quest descriptions are open ended but must include details of the work required, payment criteria and amounts, and evidence required to verify completion. Upon completion of the quest, players specify the reward amount in the claim request, which may be the full amount held by the quest or a portion, depending on how the quest defined the payment criteria.

A quest that is intended to be completed only once would define in the payment criteria that it would reward all of its bounty to the first player to successfully submit a claim request. However, a quest intended to be completed multiple times, for example “writing a blog post with your vision for 1Hive” could define the payment criteria such that each completion receives 1 HNY or perhaps a diminishing reward. Eg the first submission receives 2 HNY the second receives 1.5 HNY and each subsequent completion receives 0.5 less HNY than the last.

The evidence required for completing a quest will depend on the work expected. For a quest on writing a blog post, the evidence required will likely include a link to the blog post. It may also specify the minimum length of the blog post and that it hasn't been copied from somewhere else. For a quest on adding a feature to a web UI, the evidence required will likely include a link to the code written, some screenshots of the deployed feature and some reference to the code standard expected.

## Verifying a quest

Quests can be verified by anyone. Although in many cases the quest verifier will be the original creator of the quest, in some cases the quest is funded by more than one user or an organisation so there is a financial incentive to verify them.

Quest players must make a deposit with their claim request which is paid to a verifier should they successfully challenge the claim request. Quest verifiers also have to make a deposit, which is lost if their challenge is unsuccessful. However, this is less than the deposit for creating a claim request but large enough to prevent spamming of challenging of claim requests.&#x20;

The first thing to look for when verifying a quest is whether the claimed amount is in line with the quests payment criteria. If it isn't it can immediately be challenged and Celeste will verify the challenge.&#x20;

Besides verifying the claim amount the verification of evidence submitted in a claim request is dependant on the evaluation criteria specified in the quest. For example if a quests evaluation criteria require links to completed code and screenshots then these should be included in the evidence submitted by the quest player and should be verified as being accurate.
