# Celeste Entities

- [`CourtConfig`](#courtconfig)
- [`CourtTerm`](#courtterm)
- [`ERC20`](#erc20)
- [`CourtModule`](#courtmodule)
- [`Dispute`](#dispute)
- [`Disputable`](disputable)
- [`Arbitrable`](#arbitrable)
- [`Evidence`](#evidence)
- [`AdjudicationRound`](#adjudicationround)
- [`Vote`](#vote)
- [`Appeal`](appeal)
- [`Juror`](#juror)
- [`JurorDispute`](#jurordispute)
- [`JurorDraft`](#jurordraft)
- [`ANJMovement`](#anjmovement)
- [`FeeMovement`](#feemovement)
- [`TreasuryBalance`](treasurybalance)
- [`BrightIdRegisterModule`](#brightidregistermodule)
- [`JurorsRegistryModule`](#jurorsregistrymodule)
- [`SubscriptionModule`](#subscriptionmodule)
- [`SubscriptionPeriod`](#subscriptionperiod)
- [`JurorSubscriptionFee`](#jurorsubscriptionfee)

![Markdown Image](https://cdn.discordapp.com/attachments/1014573389400244225/1080166573668585552/schema.png)

## CourtConfig

| Field                         | Type                   | Description                                   |
| ----------------------------- | ---------------------- | --------------------------------------------- |
| id                            | ID!                    | Court config id                               |
| currentTerm                   | BigInt!                | Current term                                  |
| termDuration                  | BigInt!                | Term duration                                 |
| feeToken                      | ERC20!                 | Token used for fees                           |
| anjToken                      | ERC20                  | Anj token                                     |
| jurorFee                      | BigInt!                | Juror fees                                    |
| draftFee                      | BigInt!                | Draft fees                                    |
| settleFee                     | BigInt!                | Settle fees                                   |
| evidenceTerms                 | BigInt!                | Evidence terms                                |
| commitTerms                   | BigInt!                | Commit terms                                  |
| revealTerms                   | BigInt!                | Reveal terms                                  |
| appealTerms                   | BigInt!                | Appeal terms                                  |
| appealConfirmationTerms       | BigInt!                | Appeal configuration terms                    |
| maxRulingOptions              | Int!                   | Maximum ruling options                        |
| penaltyPct                    | Int!                   | Penalty pct                                   |
| finalRoundReduction           | Int!                   | Final round reduction                         |
| firstRoundJurorsNumber        | BigInt!                | First round juror's number                    |
| appealStepFactor              | BigInt!                | Appeal step factor                            |
| maxRegularAppealRounds        | BigInt!                | Maximum number of regular appeal rounds       |
| finalRoundLockTerms           | BigInt!                | Final round lock terms                        |
| appealCollateralFactor        | BigInt!                | Appeal collateral factor                      |
| appealConfirmCollateralFactor | BigInt!                | Appeal confirm collateral factor              |
| minActiveBalance              | BigInt!                | Minimum active balance                        |
| minMaxPctTotalSupply          | BigInt!                | Min-max pct total supply                      |
| maxMaxPctTotalSupply          | BigInt!                | Maximum pct total supply                      |
| fundsGovernor                 | Bytes                  | Funds govenor address                         |
| configGovernor                | Bytes                  | Config govenor address                        |
| feesUpdater                   | Bytes                  | Fees updater                                  |
| modulesGovernor               | Bytes                  | Modules govenor address                       |
| brightIdRegister              | BrightIdRegisterModule | Brightid register in relation to court config |
| jurorsRegistry                | JurorsRegistryModule!  | Juror registry in relation to court config    |
| subscriptions                 | SubscriptionModule     | Court config subscriptions                    |
| modules                       | [CourtModule!]         | Court config modules                          |
| terms                         | [CourtTerm!]           | Court config terms                            |
| moduleAddresses               | [String!]!             | Module addresses                              |

## CourtTerm

| Field        | Type         | Description                  |
| ------------ | ------------ | ---------------------------- |
| id           | ID!          | Court term id                |
| startTime    | BigInt!      | Court start time             |
| randomnessBN | BigInt!      | Randomness batch number      |
| randomness   | Bytes        | Randomness generator address |
| court        | CourtConfig! | Court configurations         |
| createdAt    | BigInt!      | Block court term was created |

## ERC20

| Field    | Type    | Description    |
| -------- | ------- | -------------- |
| id       | ID!     | Token id       |
| name     | String! | Token name     |
| symbol   | String! | Token symbol   |
| decimals | Int!    | Token Decimals |

## CourtModule

| Field   | Type             | Description          |
| ------- | ---------------- | -------------------- |
| id      | ID!              | Court module id      |
| type    | CourtModuleType! | Court module type    |
| address | Bytes!           | Court module address |
| court   | CourtConfig!     | Court configurations |

## Dispute

| Field            | Type                 | Description                            |
| ---------------- | -------------------- | -------------------------------------- |
| id               | ID!                  | Dispute id                             |
| subject          | Arbitrable!          | Dispute subject                        |
| evidences        | [Evidence!]          | Evidence in relation to dispute        |
| createTermId     | BigInt!              | Dispute term id                        |
| possibleRulings  | Int!                 | Possible rulings for dispute           |
| finalRuling      | Int!                 | Final ruling for dispute               |
| lastRoundId      | BigInt!              | Last round id                          |
| state            | DisputeState!        | Current state of dispute               |
| settledPenalties | Boolean!             | Checks wether penalties are settled    |
| metadata         | String!              | Dispute metadata                       |
| rawMetadata      | Bytes!               | Raw metadata                           |
| disputable       | Disputable           | Disputable info in relation to dispute |
| rounds           | [AdjudicationRound!] | Dispute rounds                         |
| jurors           | [JurorDispute!]      | Jurors in relation to dispute          |
| txHash           | String!              | Transaction hash                       |
| createdAt        | BigInt!              | Block dispute was created              |
| ruledAt          | BigInt               | Dispute ruling timestamp               |

## Disputable

| Field               | Type     | Description                  |
| ------------------- | -------- | ---------------------------- |
| id                  | ID!      | Disputable id                |
| dispute             | Dispute! | Dispute                      |
| title               | String!  | Title of dispute             |
| agreement           | String!  | Disputable aggreement        |
| actionId            | BigInt!  | Action id                    |
| challengeId         | BigInt!  | Challenge id                 |
| address             | Bytes!   | Disputable address           |
| disputableActionId  | BigInt!  | Disputable action id         |
| defendant           | Bytes!   | Defendant address            |
| plaintiff           | Bytes!   | Plaintiff address            |
| organization        | Bytes!   | Organization address         |
| actionContext       | String!  | Action content               |
| rawActionContext    | Bytes!   | Raw action content           |
| challengeContext    | String!  | Context of the challenge     |
| rawChallengeContext | Bytes!   | Raw context of the challenge |

## Arbitrable

| Field    | Type       | Description               |
| -------- | ---------- | ------------------------- |
| id       | ID!        | Arbitrable id             |
| disputes | [Dispute!] | Disputes where arbitrable |

## Evidence

| Field      | Type        | Description                     |
| ---------- | ----------- | ------------------------------- |
| id         | ID!         | Evidence id                     |
| arbitrable | Arbitrable! | Arbitrable evidence             |
| dispute    | Dispute!    | Dispute in relation to evidence |
| data       | Bytes!      | Evidence data identifier        |
| submitter  | Bytes!      | Address of the submitter        |
| createdAt  | BigInt!     | Block evidence was created      |

## AdjudicationRound

| Field            | Type               | Description                               |
| ---------------- | ------------------ | ----------------------------------------- |
| id               | ID!                | Adjudication round id                     |
| number           | BigInt!            | Adjudication round number                 |
| dispute          | Dispute!           | Dispute in relation to adjudication round |
| state            | AdjudicationState! | Current state of adjudication             |
| stateInt         | Int!               | State int                                 |
| draftTermId      | BigInt!            | Draft term id                             |
| draftedTermId    | BigInt             | Drafted term id                           |
| jurorsNumber     | BigInt!            | Juror's number                            |
| settledPenalties | Boolean!           | Check wether penalties are settled        |
| jurorFees        | BigInt!            | Juror fees                                |
| jurors           | [JurorDraft!]      | Jurors in relation to adjudication round  |
| delayedTerms     | BigInt!            | Delayed terms of adjudication round       |
| selectedJurors   | BigInt!            | Selected jurors                           |
| coherentJurors   | BigInt!            | Coherent juror                            |
| collectedTokens  | BigInt!            | Tokens collected for adjudication round   |
| appeal           | Appeal             | Adjudication round appeal                 |
| vote             | Vote               | Vote                                      |
| createdAt        | BigInt!            | Block adjudication round started          |

## Vote

| Field          | Type         | Description            |
| -------------- | ------------ | ---------------------- |
| id             | ID!          | Vote id                |
| winningOutcome | OutcomeType! | Outcome of vote        |
| createdAt      | BigInt!      | Block vote was created |

## Appeal

| Field                | Type               | Description                       |
| -------------------- | ------------------ | --------------------------------- |
| id                   | ID!                | Appeal id                         |
| round                | AdjudicationRound! | Adjudication round                |
| maker                | Bytes!             | Maker address                     |
| appealedRuling       | BigInt!            | Appealed ruling count             |
| appealDeposit        | BigInt!            | Appeal deposit                    |
| taker                | Bytes!             | Taker address                     |
| opposedRuling        | BigInt!            | Opposed ruling count              |
| confirmAppealDeposit | BigInt!            | Deposit after appeal confirmation |
| settled              | Boolean!           | Check wether appeal is settled    |
| settledAt            | BigInt             | Settled at timestamp              |
| confirmedAt          | BigInt             | Appeal confirmation timestamp     |
| createdAt            | BigInt!            | Block appeal was created          |

## Juror

| Field                   | Type                    | Description                 |
| ----------------------- | ----------------------- | --------------------------- |
| id                      | ID!                     | Juror id                    |
| treeId                  | BigInt!                 | Tree id                     |
| activeBalance           | BigInt!                 | Active balance of juror     |
| lockedBalance           | BigInt!                 | Locked balance of juror     |
| availableBalance        | BigInt!                 | Available balance           |
| deactivationBalance     | BigInt!                 | Deactivation balance        |
| withdrawalsLockTermId   | BigInt!                 | Lockterm id for withdrawals |
| disputes                | [JurorDispute!]         | Juror disputes              |
| drafts                  | [JurorDraft!]           | Juror drafts                |
| anjMovements            | [ANJMovement!]          | Juror anjmovement           |
| claimedSubscriptionFees | [JurorSubscriptionFee!] | Subscription fees claimed   |
| createdAt               | BigInt!                 | Block juror was created     |
| uniqueUserId            | Bytes                   | Unique juror id             |
| registerTime            | BigInt                  | Time of registration        |
| addressVoided           | Boolean                 | Address void check          |

## JurorDispute

| Field   | Type     | Description                              |
| ------- | -------- | ---------------------------------------- |
| id      | ID!      | Juror dispute id                         |
| juror   | Juror!   | Juror address                            |
| dispute | Dispute! | Dispute details in relation to the juror |

## JurorDraft

| Field          | Type               | Description                   |
| -------------- | ------------------ | ----------------------------- |
| id             | ID!                | Juror draft id                |
| round          | AdjudicationRound! | Adjudication round            |
| juror          | Juror!             | Juror address                 |
| weight         | BigInt!            | Juror draft weight            |
| locked         | BigInt!            | Total locked                  |
| rewarded       | Boolean!           | Reward check                  |
| rewardedAt     | BigInt             | Reward timestamp              |
| commitment     | Bytes              | Commitment transaction hash   |
| commitmentDate | BigInt             | Committment date              |
| revealDate     | BigInt             | Reveal date                   |
| outcome        | Int                | Verdict                       |
| leaker         | Bytes              | Leaker address                |
| createdAt      | BigInt!            | Block juror draft was created |

## ANJMovement

| Field           | Type             | Description                   |
| --------------- | ---------------- | ----------------------------- |
| id              | ID!              | Anjmovement id                |
| juror           | Juror!           | Juror address                 |
| type            | ANJMovementType! | Anjmovement type              |
| amount          | BigInt!          | Amount                        |
| effectiveTermId | BigInt           | Term id                       |
| createdAt       | BigInt!          | Block anjmovement was created |

## FeeMovement

| Field     | Type             | Description                    |
| --------- | ---------------- | ------------------------------ |
| id        | ID!              | Fee movement id                |
| owner     | Bytes!           | Owner address                  |
| type      | FeeMovementType! | Fee movement type              |
| amount    | BigInt!          | Amount                         |
| createdAt | BigInt!          | Block fee movement was created |

## TreasuryBalance

| Field  | Type    | Description             |
| ------ | ------- | ----------------------- |
| id     | ID!     | Treasury balance id     |
| owner  | Bytes!  | Owner address           |
| token  | ERC20!  | Token details           |
| amount | BigInt! | Treasury balance amount |

## BrightIdRegisterModule

| Field                         | Type         | Description                     |
| ----------------------------- | ------------ | ------------------------------- |
| id                            | ID!          | Register module id              |
| court                         | CourtConfig! | Court configurations            |
| verifiers                     | [Bytes!]!    | Address of verifier             |
| registrationPeriod            | BigInt!      | Registration period             |
| verificationTimestampVariance | BigInt!      | Verification timestamp variance |

## JurorsRegistryModule

| Field             | Type         | Description                    |
| ----------------- | ------------ | ------------------------------ |
| id                | ID!          | Juror registry id              |
| court             | CourtConfig! | Court configurations           |
| totalStaked       | BigInt!      | Total staked                   |
| totalActive       | BigInt!      | Total active jurors            |
| totalDeactivation | BigInt!      | Total no of deactivated jurors |

## SubscriptionModule

| Field                 | Type                  | Description                           |
| --------------------- | --------------------- | ------------------------------------- |
| id                    | ID!                   | Subscription module id                |
| court                 | CourtConfig!          | Court configurations                  |
| currentPeriod         | BigInt!               | Current period of subscription module |
| feeToken              | Bytes!                | Token contract address                |
| periodDuration        | BigInt!               | Time duration for subscription        |
| periodPercentageYield | BigInt!               | Period percentage yield               |
| periods               | [SubscriptionPeriod!] | Subscription period                   |

## SubscriptionPeriod

| Field              | Type                    | Description                      |
| ------------------ | ----------------------- | -------------------------------- |
| id                 | ID!                     | Subscription id                  |
| feeToken           | Bytes!                  | Token contract address           |
| donatedFees        | BigInt!                 | Donated fees                     |
| balanceCheckpoint  | BigInt!                 | Balance at checkpoint            |
| totalActiveBalance | BigInt!                 | Total active balance             |
| instance           | SubscriptionModule!     | Subcription period instance      |
| jurorClaims        | [JurorSubscriptionFee!] | Amount claimed by juror          |
| createdAt          | BigInt!                 | Block subcription period started |

## JurorSubscriptionFee

| Field  | Type                | Description                    |
| ------ | ------------------- | ------------------------------ |
| id     | ID!                 | Subscription id                |
| juror  | Juror!              | Juror infomation               |
| period | SubscriptionPeriod! | Time duration for subscription |
| amount | BigInt!             | Subscription amount            |
