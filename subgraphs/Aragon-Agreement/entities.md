# Aragon Agreement Entities

- [`Agreement`](#agreement)
- [`Signer`](#signer)
- [`Signature`](#signature)
- [`Action`](#action)
- [`Challenge`](#Challenge)
- [`Dispute`](dispute)
- [`Evidence`](#evidence)
- [`Version`](#version)
- [`Disputable`](#disputable)
- [`CollateralRequirement`](#collateralrequirement)
- [`Staking`](staking)
- [`StakingMovement`](#stakingmovement)
- [`ERC20`](#erc20)
- [`ArbitratorFee`](#arbitratorfee)
- [`AragonInfo`](#aragoninfo)

## Agreement

| Field          | Type          | Description                     |
| -------------- | ------------- | ------------------------------- |
| id             | ID!           | Agreement id                    |
| dao            | Bytes!        | Dao address                     |
| stakingFactory | Bytes         | Staking factory address         |
| currentVersion | Version       | Current version of the agrement |
| actions        | [Action!]     | Agreement actions               |
| signers        | [Signer!]     | Agreement signers               |
| versions       | [Version!]    | Agreement versions              |
| disputables    | [Disputable!] | Agreement disputables           |

## Signer

| Field      | Type         | Description                      |
| ---------- | ------------ | -------------------------------- |
| id         | ID!          | Signer id                        |
| agreement  | Agreement!   | Agreements signed by the signer  |
| address    | Bytes!       | Signer address                   |
| actions    | [Action!]    | Actions in relation to signer    |
| signatures | [Signature!] | Signatures in relation to signer |

## Signature

| Field     | Type     | Description                     |
| --------- | -------- | ------------------------------- |
| id        | ID!      | Signature id                    |
| signer    | Signer!  | Signer in relation to signature |
| version   | Version! | Signature version               |
| createdAt | BigInt!  | Block signiture was created     |

## Action

| Field                 | Type                   | Description                            |
| --------------------- | ---------------------- | -------------------------------------- |
| id                    | ID!                    | Action id                              |
| agreement             | Agreement!             | Agreement in relation to action        |
| disputable            | Disputable!            | Disputable in relation to action       |
| actionId              | BigInt!                | Unique identifier                      |
| disputableActionId    | BigInt!                | Disputable action id                   |
| context               | Bytes!                 | Context of the action                  |
| closed                | Boolean!               | Checks wether action is open or closed |
| submitter             | Signer!                | Signer that submitted the action       |
| version               | Version!               | Agreement version                      |
| collateralRequirement | CollateralRequirement! | Collateral requirement for action      |
| lastChallenge         | Challenge              | Last challenge                         |
| challenges            | [Challenge!]           | Action challenges                      |
| createdAt             | BigInt!                | Block action was created               |

## Challenge

| Field                   | Type            | Description                        |
| ----------------------- | --------------- | ---------------------------------- |
| id                      | ID!             | Challenge id                       |
| action                  | Action!         | Challenge action                   |
| challengeId             | BigInt!         | Unique challenge identifier        |
| context                 | Bytes!          | Context of the challenge           |
| endDate                 | BigInt!         | Challenge end date                 |
| challenger              | Bytes!          | Challenger                         |
| settlementOffer         | BigInt!         | Settlement offer for the challenge |
| state                   | ChallengeState! | Current state of the challenge     |
| submitterArbitratorFee  | ArbitratorFee   | Submitter arbitrator fee           |
| challengerArbitratorFee | ArbitratorFee!  | Challenger arbitrator fee          |
| dispute                 | Dispute         | Challenge dispute                  |
| createdAt               | BigInt!         | Block challenge was created        |

## Dispute

| Field                      | Type        | Description                               |
| -------------------------- | ----------- | ----------------------------------------- |
| id                         | ID!         | Dispute id                                |
| disputeId                  | BigInt!     | Unique dispute identifier                 |
| ruling                     | BigInt!     | Dispute ruling                            |
| challenge                  | Challenge!  | Dispute challenge                         |
| submitterFinishedEvidence  | Boolean!    | Check wether submitter finished evidence  |
| challengerFinishedEvidence | Boolean!    | Check wether challenger finished evidence |
| evidences                  | [Evidence!] | Evidence in relation to Dispute           |
| createdAt                  | BigInt!     | Block dispute was created                 |

## Evidence

| Field     | Type     | Description                     |
| --------- | -------- | ------------------------------- |
| id        | ID!      | Evidence id                     |
| dispute   | Dispute! | Dispute in relation to evidence |
| data      | Bytes!   | Evidence data                   |
| submitter | Bytes!   | Submitter address               |
| createdAt | BigInt!  | Block evidence was created      |

## Version

| Field          | Type         | Description                       |
| -------------- | ------------ | --------------------------------- |
| id             | ID!          | Version id                        |
| agreement      | Agreement!   | Version agreement                 |
| versionId      | BigInt!      | Unique version identifier         |
| content        | Bytes!       | Version content                   |
| title          | String!      | Version title                     |
| arbitrator     | Bytes!       | Arbitrator address                |
| appFeesCashier | Bytes!       | App fees cashier address          |
| effectiveFrom  | BigInt!      | Block app version is effective    |
| signatures     | [Signature!] | Signitures in relation to Version |

## Disputable

| Field                        | Type                     | Description                      |
| ---------------------------- | ------------------------ | -------------------------------- |
| id                           | ID!                      | Disputable id                    |
| address                      | Bytes!                   | Disputable address               |
| agreement                    | Agreement!               | Agreement in relation to dispute |
| activated                    | Boolean!                 | Check wether dispute is active   |
| currentCollateralRequirement | CollateralRequirement!   | Current collateral requirement   |
| collateralRequirements       | [CollateralRequirement!] | Collateral requirements          |
| actions                      | [Action!]                | Actions in relation to dispute   |

## CollateralRequirement

| Field             | Type        | Description               |
| ----------------- | ----------- | ------------------------- |
| id                | ID!         | Collateral requirement id |
| disputable        | Disputable! | Disputable collateral     |
| token             | ERC20!      | Token address             |
| challengeDuration | BigInt!     | Duration of the challenge |
| actionAmount      | BigInt!     | Action amount             |
| challengeAmount   | BigInt!     | Challenge Amount          |

## Staking

| Field      | Type               | Description                     |
| ---------- | ------------------ | ------------------------------- |
| id         | ID!                | Staking id                      |
| user       | Bytes!             | User address                    |
| token      | ERC20!             | Token used for stake            |
| available  | BigInt!            | Staking amount avilable         |
| locked     | BigInt!            | Amount locked                   |
| challenged | BigInt!            | Staking amount challenged       |
| total      | BigInt!            | Total amount staked             |
| movements  | [StakingMovement!] | Movement in relation to staking |

## StakingMovement

| Field           | Type                    | Description                     |
| --------------- | ----------------------- | ------------------------------- |
| id              | ID!                     | Staking movement id             |
| staking         | Staking!                | Staking info                    |
| amount          | BigInt!                 | Movement amount                 |
| agreement       | Agreement!              | Staking agreement               |
| action          | Action!                 | Action in realtion to stake     |
| actionState     | StakingActionState!     | Current state of staking action |
| collateralState | StakingCollateralState! | Current state of collateral     |
| createdAt       | BigInt!                 | Block movement was created      |

## ERC20

| Field    | Type    | Description          |
| -------- | ------- | -------------------- |
| id       | ID!     | Token address        |
| name     | String! | Name of token        |
| symbol   | String! | Token symbol         |
| decimals | Int!    | Decimals value of 18 |

## ArbitratorFee

| Field  | Type    | Description                   |
| ------ | ------- | ----------------------------- |
| id     | ID!     | Arbitrator fee id             |
| token  | ERC20!  | Token used for arbitrator fee |
| amount | BigInt! | Arbitrator fee amount         |

## AragonInfo

| Field  | Type      | Description            |
| ------ | --------- | ---------------------- |
| id     | ID!       | Aragon info id         |
| orgs   | [Bytes!]! | Organization addresses |
| apps   | [Bytes!]! | Apps addresses         |
| tokens | [Bytes!]! | Token address          |
