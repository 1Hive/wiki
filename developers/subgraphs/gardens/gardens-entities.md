# Gardens Entities

* ``[`Organization`](gardens-entities.md#organization)``
* ``[`Config`](gardens-entities.md#config)``
* ``[`ConvictionConfig`](gardens-entities.md#convictionconfig)``
* ``[`VotingConfig`](gardens-entities.md#votingconfig)``
* ``[`Proposal`](gardens-entities.md#proposal)``
* ``[`Cast`](gardens-entities.md#cast)``
* ``[`Stake`](gardens-entities.md#stake)``
* ``[`StakeHistory`](gardens-entities.md#stakehistory)``
* ``[`User`](gardens-entities.md#user)``
* ``[`Supporter`](gardens-entities.md#supporter)``
* ``[`Token`](gardens-entities.md#token)``
* ``[`CollateralRequirement`](gardens-entities.md#collateralrequirement)``
* ``[`ArbitratorFee`](gardens-entities.md#arbitratorfee)``

![Markdown Image](https://raw.githubusercontent.com/1Hive/gardens/master/packages/subgraph/schema.png)

### Organization <a href="#organization" id="organization"></a>

| Field                   | Type         | Description                                       |
| ----------------------- | ------------ | ------------------------------------------------- |
| id                      | ID!          | Organization ID                                   |
| createdAt               | BigInt!      | Block organization was created                    |
| config                  | Config!      | Two types to choose (Veneto or Boboli)            |
| token                   | Token        | Organization’s token                              |
| wrappableToken          | Token        | Organization wrapped tokens                       |
| proposalCount           | Int!         | Count of proposals in organization                |
| proposals               | \[Proposal!] | Proposals related to organization                 |
| supporterCount          | Int!         | Count of supporters for a proposal                |
| honeyLiquidity          | BigInt       | Initial liquidity amount for new token            |
| incentivisedPriceOracle | Bytes        | 2% of the contract’s balance of the Gardens token |
| unipool                 | Bytes        | Unipool farming contract address                  |
| fluidProposals          | Bytes        | Swarm funding proposal address                    |
| active                  | Boolean!     | Check whether organization is active              |

### Config <a href="#config" id="config"></a>

| Field      | Type             | Description                                     |
| ---------- | ---------------- | ----------------------------------------------- |
| id         | ID!              | Config ID                                       |
| conviction | ConvictionConfig | parameters are set in the Aragon Agreement app  |
| voting     | VotingConfig     | parameters are set in the Conviction Voting app |

### ConvictionConfig <a href="#convictionconfig" id="convictionconfig"></a>

| Field                       | Type    | Description                          |
| --------------------------- | ------- | ------------------------------------ |
| id                          | ID!     | Conviction config id                 |
| decay                       | BigInt! | Conviction decay amount              |
| weight                      | BigInt! | Number of support votes              |
| maxRatio                    | BigInt! | Max threshold amount for proposal    |
| pctBase                     | BigInt! | Pct base number                      |
| stakeToken                  | Token   | Staked token                         |
| totalStaked                 | BigInt! | Total amount staked                  |
| maxStakedProposals          | Int!    | Maximun number of staked prposals    |
| minThresholdStakePercentage | BigInt! | Minimum threshold stake amount       |
| fundsManager                | Bytes   | Funds manager address                |
| requestToken                | Token   | Request token contract address       |
| stableToken                 | Token   | Stable token contract address        |
| stableTokenOracle           | Bytes   | Stable token oracle contract address |
| contractPaused              | Boolean | Check whether contract is paused     |

### VotingConfig <a href="#votingconfig" id="votingconfig"></a>

| Field                      | Type    | Description                                                            |
| -------------------------- | ------- | ---------------------------------------------------------------------- |
| id                         | ID!     | Voting Config ID                                                       |
| token                      | Token   | Token adress                                                           |
| settingId                  | BigInt! | Setting id                                                             |
| voteTime                   | BigInt! | Amount of time allotted to vote                                        |
| supportRequiredPct         | BigInt! | Min % of voting amount required for a decision vote to pass            |
| minimumAcceptanceQuorumPct | BigInt! | Min % of the total token supply in support for a decision vote to pass |
| delegatedVotingPeriod      | BigInt! | Voting period delegates can vote on behalf of delegators               |
| quietEndingPeriod          | BigInt! | Duration before the end of a vote to detect non-quiet endings          |
| quietEndingExtension       | BigInt! | Duration to extend a vote in the case of a non-quiet ending            |
| executionDelay             | BigInt! | The duration for delay before vote can be executed                     |
| createdAt                  | BigInt! | Block vote was created                                                 |

### Proposal <a href="#proposal" id="proposal"></a>

| Field                        | Type                      | Description                                  |
| ---------------------------- | ------------------------- | -------------------------------------------- |
| id                           | ID!                       | Proposal ID                                  |
| organization                 | Organization!             | Organization related to proposal             |
| number                       | BigInt!                   | Proposal number                              |
| creator                      | Bytes!                    | Proposal creator address                     |
| status                       | ProposalStatus!           | Status of the proposal                       |
| statusInt                    | Int!                      | Proposal status count                        |
| type                         | ProposalType!             | Proposal type                                |
| typeInt                      | Int!                      | Proposal type number                         |
| createdAt                    | BigInt!                   | Block proposal created                       |
| weight                       | BigInt!                   | Weight of last proposal                      |
| metadata                     | String                    | Proposal metadata                            |
| executedAt                   | BigInt                    | Block number proposal was executed at        |
| txHash                       | String!                   | Proposal transaction hash                    |
| link                         | String                    | Link to proposal                             |
| stakes                       | \[Stake!]                 | Stake in relation to proposal                |
| stakesHistory                | \[StakeHistory!]          | Stake history of proposal                    |
| beneficiary                  | Bytes                     | Beneficiary address                          |
| convictionLast               | BigInt                    | Amount for last convition                    |
| requestedAmount              | BigInt                    | Requested amount for proposal                |
| totalTokensStaked            | BigInt                    | Total amount of tokens staked                |
| stable                       | Boolean                   | Check wether proposal is stable              |
| setting                      | VotingConfig              | Setting config for proposal                  |
| startDate                    | BigInt                    | Start date of proposal                       |
| totalPower                   | BigInt                    | Total number of votes                        |
| snapshotBlock                | BigInt!                   | Block number of snapshot                     |
| yeas                         | BigInt                    | Number of yes votes                          |
| nays                         | BigInt                    | Number of no votes                           |
| quietEndingExtensionDuration | BigInt                    | Duration required before voting starts       |
| quietEndingSnapshotSupport   | VoterState                | Snapshot after voting ends                   |
| script                       | Bytes                     | Script address of the proposal               |
| isAccepted                   | Boolean                   | Check whether proposal is accepted           |
| castVotes                    | \[Cast!]                  | Cast votes                                   |
| actionId                     | BigInt!                   | Dispute action id                            |
| disputeId                    | BigInt                    | Dispute id                                   |
| challengeId                  | BigInt!                   | Challenge id                                 |
| challenger                   | Bytes!                    | Challenger to proposal                       |
| challengeEndDate             | BigInt!                   | Date challenge will be accepted or escalated |
| settledAt                    | BigInt!                   | Time challenge was settled                   |
| settlementOffer              | BigInt                    | Token amount received for settlement         |
| disputedAt                   | BigInt!                   | Timestamp dispute was paused                 |
| pausedAt                     | BigInt!                   | Block dispute was paused                     |
| pauseDuration                | BigInt!                   | Duration dispute is paused                   |
| submitterArbitratorFee       | ArbitratorFee             | Submitter arbitration fee                    |
| challengerArbitratorFee      | ArbitratorFee             | Challenger arbitrator fee                    |
| collateralRequirement        | \[CollateralRequirement!] | Collateral requirement for proposal          |

### Cast <a href="#cast" id="cast"></a>

| Field     | Type       | Description                     |
| --------- | ---------- | ------------------------------- |
| id        | ID!        | Cast id                         |
| supporter | Supporter! | Supporter related to cast       |
| caster    | Bytes!     | Caster address                  |
| proposal  | Proposal!  | Proposal related to cast        |
| supports  | Boolean!   | Checke wether support is active |
| stake     | BigInt!    | Stake amount                    |
| createdAt | BigInt!    | Block cast is created at        |

### Stake <a href="#stake" id="stake"></a>

| Field     | Type       | Description                |
| --------- | ---------- | -------------------------- |
| id        | ID!        | Stake id                   |
| type      | StakeType! | Type of stake              |
| supporter | Supporter! | Supporter related to stake |
| proposal  | Proposal!  | Propsal related to stake   |
| amount    | BigInt!    | Amount staked              |
| createdAt | BigInt!    | Block stake was created    |

### StakeHistory <a href="#stakehistory" id="stakehistory"></a>

| Field             | Type       | Description                    |
| ----------------- | ---------- | ------------------------------ |
| id                | ID!        | Stake history id               |
| type              | StakeType! | Type of stake                  |
| supporter         | Supporter! | Supporter                      |
| proposal          | Proposal!  | Type of proposal               |
| tokensStaked      | BigInt!    | Tokens staked                  |
| totalTokensStaked | BigInt!    | Total tokens staked            |
| conviction        | BigInt!    | Number of conviction votes     |
| time              | BigInt!    | Block at which was created     |
| createdAt         | BigInt!    | Timestamp at which was created |

### User <a href="#user" id="user"></a>

| Field             | Type          | Description                    |
| ----------------- | ------------- | ------------------------------ |
| id                | ID!           | User ID                        |
| address           | Bytes!        | Address of user                |
| gardensSigned     | \[String!]    | Number of gardens signed       |
| supports          | \[Supporter!] | Proposals user has supported   |
| representativeFor | \[Supporter!] | Proposals user has represented |

### Supporter <a href="#supporter" id="supporter"></a>

| Field          | Type             | Description                |
| -------------- | ---------------- | -------------------------- |
| id             | ID!              | Supporter ID               |
| user           | User!            | User                       |
| organization   | Organization!    | Supporter’s organization   |
| representative | User             | Supporter’s representative |
| casts          | \[Cast!]         | Supporter’s votes cast     |
| stakes         | \[Stake!]        | Supporter’s stakes         |
| stakesHistory  | \[StakeHistory!] | Supporter stake history    |

### Token <a href="#token" id="token"></a>

| Field        | Type         | Description                        |
| ------------ | ------------ | ---------------------------------- |
| id           | ID!          | Address of token                   |
| name         | String!      | Name of token                      |
| symbol       | String!      | Symbol of token                    |
| decimals     | Int!         | Decimals of token                  |
| organization | Organization | Needed for setting honey liquidity |

### CollateralRequirement <a href="#collateralrequirement" id="collateralrequirement"></a>

| Field             | Type     | Description                             |
| ----------------- | -------- | --------------------------------------- |
| id                | ID!      | Proposal ID                             |
| proposal          | Proposal | Proposal that was challenged            |
| token             | Token    | Token address                           |
| actionAmount      | BigInt   | Amount to settle challenge              |
| challengeAmount   | BigInt   | Amount of deposit required to challenge |
| challengeDuration | BigInt   | Time set for challenge                  |

### ArbitratorFee <a href="#arbitratorfee" id="arbitratorfee"></a>

| Field    | Type      | Description                  |
| -------- | --------- | ---------------------------- |
| id       | ID!       | Arbitrator ID                |
| proposal | Proposal! | Proposal that was challenged |
| token    | Token!    | Token address                |
| amount   | BigInt!   | Amount of fee                |
