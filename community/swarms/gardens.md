---
description: Building Gardens
---

# 🌻 Gardens

The 🌻Gardens Swarm manages the development of the Gardens Template and associated Aragon Apps and is doing the initial experiments into how Gardens should best be structured. Updates can be seen on [Token Engineering Commons](https://tecommons.medium.com/) medium page.

Gardens are a social, financial, and technical foundation for online communities to organize. This empowers people to coordinate around causes, social movements, or even memes. Gardens are designed to be operationally decentralized and autonomous from day one.

## Proposal Information

### Background, Overview and Proposal Rationale

We are building the first implementation of the Commons Stack’s Commons Model, a DAO initially funded by a Trusted Seed (Hatch), later powered by an Augmented Bonding Curve (ABC), whose funds are managed with Conviction Voting (CV), and governed with Dandelion Voting (DV). See our previous successful funding request: [Bootstrapping the Gardens Swarm DAO](https://forum.1hive.org/t/bootstrapping-the-1hive-gardens-swarm-dao/1159)

### Proposal description

This proposal is to support the Gardens Swarm team to continue developing improvements and adaptations to 1hive’s marketplace app (hatch and augmented bonding curve), and the conviction voting frontend.

Because of the ~80% drop in the HNY price since the original proposal we need to request more HNY to finish our work in partnership with the TE Commons and the Commons Stack.

### Deliverables so far:

We have delivered a useable prototype for each of the 4 pieces of the DAO:

Hatch: We adapted Aragon Black’s fundraising app (Specifically presale.sol) and upgraded it to use Aragon connect. Here’s the second iteration: [hatch.tecommons.org](https://hatch.tecommons.org/)

ABC: We adapted Aragon Convert to use 1hive Marketplace (which converts tokens without batching). You can exchange TESTTEC Tokens via an Augmented Bonding Curve: [convert.tecommons.org](https://convert.tecommons.org/)

CV: We adapted 1hive Honeypot v1 to be used with two tokens, and adjusted the governance token price oracle to read from the bonding curve instead of honeyswap. You can vote with Conviction Voting Here: [gov.tecommons.org](https://gov.tecommons.org/#/)

DV: We ran a demo of 1hive Dandelion Voting with the TEC community here: TEC Test Dandelion Voting App

And most recently, we are tying all four of these prototypes together in a 2 part launch, the first part of this is the TEC Test HatchDAO launched here: [hatch.tecommons.org](https://hatch.tecommons.org/)

A lot of documentation and sensemaking around the various parameters has been happening in the Forum to reduce the reliance on technocracy to design cryptoeconomies: https://forum.tecommons.org/c/Token-talk-anything-about-the-TEC-token-such-as-issuance-and-hatches/9

Legal strategies have been solidified and can be duplicated for others. We have a 2 part launch where initially there is no bonding curve, the participants technically lose money, making it much easier, especially since we are able to use the Commons Stack’s Swiss Association as a legal shield.

### Upcoming Deliverables:

The 1hive Gardens Swarm is one of several work streams building the first iteration of the future of Public Goods funding. Here is a general overview of the project’s roadmap:

Now: User testing has begun of the initial system

Jan 10th-ish: The ABC and CV aragon apps will be ready to be added into the Test Hatch DAO

Jan 20th-ish: The Hatch Smart Contracts will have full test coverage and be frozen for review

Jan28th-ish: Have the initial Models for the Hatch done so we can start proposing Parameters for the TEC Hatch DAO

Feb 1st-ish: The ABC and CV contracts will finish user testing and be frozen for review.

Feb 7th-ish: Do a second test, this time a full dress rehearsal with parameters chosen by a vote

March 10th-ish: Launch the TEC Hatch, this time a full dress rehearsal with parameters chosen by a vote

March 30th-ish: TEC votes for Commons Upgrade

April 30th-ish: Improvements based on TEC experience are finished being integrated and other communities are invited to use the template.

### Expected duration or delivery date:

There will be 1 more full Dress Rehearsal launch test and the final template will be ready for any community to play with in April, after the successful Hatch and Upgrade of the TE Commons, as the first Commons.

After this launch we expect to request funding for continued work on this template from the TE Commons itself.

## Useful Links 

[Aragon DAO](https://aragon.1hive.org/#/gardensswarm/) holding Gardens funds.

[Excel sheet](https://docs.google.com/spreadsheets/d/1oRDecU-weSTOLv061N5O7VAJcDfU5XGqmu21ntTXOos/edit#gid=1361585578%20) showing hours spent and payments made.

## Roles and Responsibilities

### Gardens Swarm Team

| Member | Role |
| :--- | :--- |
| [Griff](https://github.com/griffgreen) | Researcher |
| [Sem](https://github.com/sembrestels) | Solidity Developer and Researcher |
| [Viviane](https://github.com/vivianedias) | Web Developer |
| [Paulo](https://github.com/pjcolombo) | Web Developer |
| [Rayne](https://github.com/anthonyoliai) | Developer |
| [Fioreb](https://forum.1hive.org/u/fioreb) | Designer |
| [Fabi](https://github.com/famole/) | Web Developer |
| [Marko](https://github.com/markoprljic) | Designer |

### Advisors

| Members | Role |
| :--- | :--- |
| [willjgriff](https://github.com/willjgriff) | Solidity Developer |
| [rperez89](https://github.com/rperez89) | Web Developer |
| [fabriv](https://github.com/fabriziovigevani) | Web Developer |

Each of the above members, swarm team and advisors, have equal voting weight within the Gardens DAO to manage funds.

### Skills and previous experience in related or similar work:

Griff - I have been working full time in the DAO space for 5 years (TheDAO, Giveth, Commons Stack, etc) and was the product owner for the Aragon DAC for 6 months.

Sem - Led the development of Conviction Voting Aragon App

Fiore - 1hive designer

Viviane - Dev. Contributed to Conviction Voting frontend

Paulo - Dev. Developed Committees Aragon App and contributed to Conviction Voting too

Fabi - Dev. Strong background on Frontend and Mobile development, contributed to 1hive taking some issues and started to work with smart contracts some time ago.

Rayne - Dev Fresh graduate, still very new to the space. Currently also a Fauna community moderator at 1hive.

Marko - Prominent designer in the space: Consensys, Giveth, DAppNode, Commons Stack, Panvala, Metagame and many more.

Adrià - White hat hacker legend and Ethereum Core Dev. Part of the WHG team that audited the original AragonOS and MakerDAO deployments, and reviewed code for dozens of other projects.

Rodrigo, Fabri, and Will are 1hive seed members that have worked on Gardens and are advising the project.

## Funding Information
### Amount of HNY requested:
200 HNY

### Ethereum address where funds shall be transferred:
0xc542cc61ed9be9e6e29652ac8a918554ecd2bc98 - Gardens Swarm DAO Agent (https://aragon.1hive.org/#/gardensswarm/)

### How Funds Will Be Used

This HNY will pay devs a rate of 25-50 xDAI an hour. As the project evolves more individual agreements might need to be made (Bounties for tasks, etc) but the hourly rate will stay around 25-50 xDAI/hr (based on experience) for the foreseeable future.

Honey is Money (but it’s not a great unit of account ) All payments will happen in HNY, but based on the exchange rate of the date that the vote to pay out is made.

### Financial Transparency

We have open accounting and you can see exactly how payments are handled and what everyone did to deserve them in this spreadsheet: https://docs.google.com/spreadsheets/d/1oRDecU-weSTOLv061N5O7VAJcDfU5XGqmu21ntTXOos/edit#gid=1361585578

## Funding Proposals

One funding proposal was made which was accepted by the community: [https://forum.1hive.org/t/bootstrapping-the-1hive-gardens-swarm-dao/1159](https://forum.1hive.org/t/bootstrapping-the-1hive-gardens-swarm-dao/1159).
