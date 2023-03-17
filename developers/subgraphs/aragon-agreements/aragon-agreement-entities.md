# Aragon Agreement Entities

* ``[`Agreement`](aragon-agreement-entities.md#agreement)``
* ``[`Signer`](aragon-agreement-entities.md#signer)``
* ``[`Signature`](aragon-agreement-entities.md#signature)``
* ``[`Action`](aragon-agreement-entities.md#action)``
* ``[`Challenge`](aragon-agreement-entities.md#challenge)``
* ``[`Dispute`](aragon-agreement-entities.md#dispute)``
* ``[`Evidence`](aragon-agreement-entities.md#evidence)``
* ``[`Version`](aragon-agreement-entities.md#version)``
* ``[`Disputable`](aragon-agreement-entities.md#disputable)``
* ``[`CollateralRequirement`](aragon-agreement-entities.md#collateralrequirement)``
* ``[`Staking`](aragon-agreement-entities.md#staking)``
* ``[`StakingMovement`](aragon-agreement-entities.md#stakingmovement)``
* ``[`ERC20`](aragon-agreement-entities.md#erc20)``
* ``[`ArbitratorFee`](aragon-agreement-entities.md#arbitratorfee)``
* ``[`AragonInfo`](aragon-agreement-entities.md#aragoninfo)``

### Agreement <a href="#agreement" id="agreement"></a>

| Field          | Type           | Description                     |
| -------------- | -------------- | ------------------------------- |
| id             | ID!            | Agreement id                    |
| dao            | Bytes!         | Dao address                     |
| stakingFactory | Bytes          | Staking factory address         |
| currentVersion | Version        | Current version of the agrement |
| actions        | \[Action!]     | Agreement actions               |
| signers        | \[Signer!]     | Agreement signers               |
| versions       | \[Version!]    | Agreement versions              |
| disputables    | \[Disputable!] | Agreement disputables           |

### Signer <a href="#signer" id="signer"></a>

| Field      | Type          | Description                      |
| ---------- | ------------- | -------------------------------- |
| id         | ID!           | Signer id                        |
| agreement  | Agreement!    | Agreements signed by the signer  |
| address    | Bytes!        | Signer address                   |
| actions    | \[Action!]    | Actions in relation to signer    |
| signatures | \[Signature!] | Signatures in relation to signer |

### Signature <a href="#signature" id="signature"></a>

| Field     | Type     | Description                     |
| --------- | -------- | ------------------------------- |
| id        | ID!      | Signature id                    |
| signer    | Signer!  | Signer in relation to signature |
| version   | Version! | Signature version               |
| createdAt | BigInt!  | Block signiture was created     |

### Action <a href="#action" id="action"></a>

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
| challenges            | \[Challenge!]          | Action challenges                      |
| createdAt             | BigInt!                | Block action was created               |

### Challenge <a href="#challenge" id="challenge"></a>

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

### Dispute <a href="#dispute" id="dispute"></a>

| Field                      | Type         | Description                               |
| -------------------------- | ------------ | ----------------------------------------- |
| id                         | ID!          | Dispute id                                |
| disputeId                  | BigInt!      | Unique dispute identifier                 |
| ruling                     | BigInt!      | Dispute ruling                            |
| challenge                  | Challenge!   | Dispute challenge                         |
| submitterFinishedEvidence  | Boolean!     | Check wether submitter finished evidence  |
| challengerFinishedEvidence | Boolean!     | Check wether challenger finished evidence |
| evidences                  | \[Evidence!] | Evidence in relation to Dispute           |
| createdAt                  | BigInt!      | Block dispute was created                 |

### Evidence <a href="#evidence" id="evidence"></a>

| Field     | Type     | Description                     |
| --------- | -------- | ------------------------------- |
| id        | ID!      | Evidence id                     |
| dispute   | Dispute! | Dispute in relation to evidence |
| data      | Bytes!   | Evidence data                   |
| submitter | Bytes!   | Submitter address               |
| createdAt | BigInt!  | Block evidence was created      |

### Version <a href="#version" id="version"></a>

| Field          | Type          | Description                       |
| -------------- | ------------- | --------------------------------- |
| id             | ID!           | Version id                        |
| agreement      | Agreement!    | Version agreement                 |
| versionId      | BigInt!       | Unique version identifier         |
| content        | Bytes!        | Version content                   |
| title          | String!       | Version title                     |
| arbitrator     | Bytes!        | Arbitrator address                |
| appFeesCashier | Bytes!        | App fees cashier address          |
| effectiveFrom  | BigInt!       | Block app version is effective    |
| signatures     | \[Signature!] | Signitures in relation to Version |

### Disputable <a href="#disputable" id="disputable"></a>

| Field                        | Type                      | Description                      |
| ---------------------------- | ------------------------- | -------------------------------- |
| id                           | ID!                       | Disputable id                    |
| address                      | Bytes!                    | Disputable address               |
| agreement                    | Agreement!                | Agreement in relation to dispute |
| activated                    | Boolean!                  | Check wether dispute is active   |
| currentCollateralRequirement | CollateralRequirement!    | Current collateral requirement   |
| collateralRequirements       | \[CollateralRequirement!] | Collateral requirements          |
| actions                      | \[Action!]                | Actions in relation to dispute   |

### CollateralRequirement <a href="#collateralrequirement" id="collateralrequirement"></a>

| Field             | Type        | Description               |
| ----------------- | ----------- | ------------------------- |
| id                | ID!         | Collateral requirement id |
| disputable        | Disputable! | Disputable collateral     |
| token             | ERC20!      | Token address             |
| challengeDuration | BigInt!     | Duration of the challenge |
| actionAmount      | BigInt!     | Action amount             |
| challengeAmount   | BigInt!     | Challenge Amount          |

### Staking <a href="#staking" id="staking"></a>

| Field      | Type                | Description                     |
| ---------- | ------------------- | ------------------------------- |
| id         | ID!                 | Staking id                      |
| user       | Bytes!              | User address                    |
| token      | ERC20!              | Token used for stake            |
| available  | BigInt!             | Staking amount avilable         |
| locked     | BigInt!             | Amount locked                   |
| challenged | BigInt!             | Staking amount challenged       |
| total      | BigInt!             | Total amount staked             |
| movements  | \[StakingMovement!] | Movement in relation to staking |

### StakingMovement <a href="#stakingmovement" id="stakingmovement"></a>

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

### ERC20 <a href="#erc20" id="erc20"></a>

| Field    | Type    | Description          |
| -------- | ------- | -------------------- |
| id       | ID!     | Token address        |
| name     | String! | Name of token        |
| symbol   | String! | Token symbol         |
| decimals | Int!    | Decimals value of 18 |

### ArbitratorFee <a href="#arbitratorfee" id="arbitratorfee"></a>

| Field  | Type    | Description                   |
| ------ | ------- | ----------------------------- |
| id     | ID!     | Arbitrator fee id             |
| token  | ERC20!  | Token used for arbitrator fee |
| amount | BigInt! | Arbitrator fee amount         |

### AragonInfo <a href="#aragoninfo" id="aragoninfo"></a>

| Field  | Type       | Description            |
| ------ | ---------- | ---------------------- |
| id     | ID!        | Aragon info id         |
| orgs   | \[Bytes!]! | Organization addresses |
| apps   | \[Bytes!]! | Apps addresses         |
| tokens | \[Bytes!]! | Token address          |
