# User Process

The below is an attempt to begin documenting the process that the 1Hive DAO and Celeste will use in order to decide the outcome of challenged actions. After doing research to understand the process myself I felt it would be useful to share some of what I’ve learnt. I think it’s especially useful for those interested in becoming a keeper (previously “juror”), and those interested in using Celeste to get answers to questions.

The term **action** is used to define the question that needs to be decided by Celeste. Within the 1Hive DAO, actions could be conviction voting proposals or standard votes (referred to on the 1Hive UI as decisions). In the 1Hive context Celeste will not decide on the outcome of a conviction voting proposal or standard vote, but whether that vote belongs within the 1Hive DAO. For example, if someone creates a proposal to take a large amount of money from the common pool without any obvious benefit to the community and they currently own a large amount of HNY, there is no way for other HNY holders to prevent them from staking their HNY to that proposal and stealing the money. With Celeste this proposal could be challenged and should Celeste deem it not inline with the [Community Covenant](../../community-covenant.md), it will be cancelled.

## Steps in the Process

There are many steps involved in the process from creating disputable actions to an outcome regarding them being decided. This diagram briefly displays the steps involved. The description below it goes into more details, including cost requirements for each party. In some cases time and amounts have been specified. However, these aren’t final and are likely to change. Some terminology is also likely to change between now and release.

![Celeste user flow](https://forum.1hive.org/uploads/default/optimized/1X/f5ac9f29b90317689b95d93e6a4242e046852468\_2\_207x500.png)

### Creating an action

To create an action (proposal or vote) a user must first deposit the action collateral amount of 0.3 HNY. When the action is finalised/executed/cancelled the action creator can claim the collateral back. However, if the action is successfully challenged the action collateral is awarded to the challenger.

### Challenging an action

Actions can be challenged anytime they are available for being voted on. In the case of conviction voting proposals they can be challenged even after voting has finished and they are executable, but not after they have been executed. The challenger will specify a settlement amount which would be accepted if the original action creator did not want to raise the action to Celeste. The settlement amount must be less than or equal to actions original collateral requirement. The challenger will pay a challenge amount of 0.3 HNY (which is returned to them if they win the challenge or send to the original actions creator should they lose) plus Celeste fees (returned to them should they win the challenge).

### Settling an action

Within 3 days of the challenge being created, the original action creator has the chance to settle the action. This will cancel the action, award the challenger with the settlement amount and return all funds the challenger previously payed to the challenger.

### Disputing an action

Should the action creator disagree with the challenge, they can choose to dispute it, raising it to Celeste to decide an outcome. The action creator, who has already paid the action collateral, will now pay Celeste fees (returned to them should they win the dispute).

### Evidence period

Now a dispute has been raised to Celeste to decide, there is an evidence period of 7 days, within which both action creator and challenger can submit evidence to the court. If both parties finalise the submission of their evidence before the 7 days passes then the following draft stage is available from that point.

### Registering as a keeper - prior to the above operations and before drafting

Anyone can register as a keeper in Celeste by staking HNY. The more HNY a keeper stakes, the more likely they will be picked to decide a dispute. However, using BrightId there will be a max stake per keeper which will reduce as more HNY is staked to Celeste. keepers are rewarded $10 in HNY for each dispute they make a decision on plus a passive reward once every 30 days for remaining staked. This reward will be determined by conviction voting proposals.

### Drafting keepers

Once evidence has been submitted, draft() needs to be called on Celeste by anyone in order to prepare it to allow keepers to decide an outcome. Part of the Celeste fees, paid earlier, include a draft() call fee which will be sent to whoever calls draft() for a particular dispute. The first draft will employ 3 keepers.

### Adjudicating

Drafted keepers must now vote on the outcome of the dispute using a commit - reveal process. They have 2 days to commit a decision, then 2 days to reveal their decision. If a keeper leaks their decision before revealing it, this can be submitted to Celeste and that keeper will be slashed. If they don’t vote they will be slashed. If they vote opposite to the majority they will be slashed. The slashed funds will be awarded to the keepers who vote for the majority outcome.

### Appealing

Once a decision has been made by the keepers there is a 2 day period to allow anyone who opposes the outcome to appeal it. To appeal a ruling requires a deposit of 3x the Celeste fees for employing a new round of keepers. This deposit minus Celeste fees is forfeit to the appeal confirmer (as described below) if the appeal is unsuccessful. If the appeal is not confirmed, the outcome they appealed for becomes the winning outcome for this dispute.

### Confirming appeal

If someone disagrees with the appeal they can confirm it, raising it to a second round of disputes (going from the [drafting keepers](user-process.md#drafting-keepers) stage above) which will employ 9 keepers, raised by a factor of 3 for each new round of a dispute up to a total of 4 rounds. To confirm an appeal requires a deposit of 2x the Celeste fees for this round. This deposit minus Celeste fees is forfeit to the appeal creator if the appeal is successful.

### Final appeal round

There can only be a max of 4 appeal rounds, 5 rounds total including the initial round. The 5th round will be the final appeal round, at which point every keeper is employed too adjudicate a dispute. Their vote weight is determined by the amount they have staked at that point, unlike previous rounds where each keepers vote weight was the same. The amount they can be slashed increases proportional to their vote weight.

### Ruling

Once 2 days have passed after an adjudication period and no appeal has been made, or the final appeal round has ended, the majority ruling becomes the outcome and a function can be executed which will either cancel or unpause the action associated with it. At this stage, as we know the outcome, we can settle all the owed amounts for the action creator and challenger, keepers and slashed keepers, appealers and appeal confirmers. There is a function settlePenalties() which similar to draft() has a reward for being called, paid by the Celeste fees, which prepares Celeste for keepers and appealers to claim the funds owed to them.

For more in depth details on operating as keeper see the links referenced here: [https://help.aragon.org/category/47-aragoncourt](https://help.aragon.org/category/47-aragoncourt) The 1Hive UI will be very similar.
