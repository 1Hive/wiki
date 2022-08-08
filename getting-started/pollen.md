---
description: Earn Honey for contributions
---

# Pollen

Pollen is a contributor rank used to recognize contributions to 1Hive’s [Discord](https://discord.com/invite/P4rRDUKTAU), [Forum](https://forum.1hive.org/), and [Github](https://github.com/1Hive) communities, and reward these contributions with weekly distributions of Honey.

## How do I participate

As soon as you start interacting on 1Hive’s Discord, Forum, and Github communities you’ll start earning Pollen, which gets added to your registered wallet as sweet sweet Honey.

In order to receive weekly pollen distributions you’ll need to create accounts on supported platforms and link them to your xDai address. You can do this by sending the following commands in 1Hive Discord’s 🤖**bot-commands** channel:

* **Save wallet address and Discord information - required**: Send `!pollen save-wallet <wallet-address>` to add your wallet address, Discord ID and Discord username to the Pollen DB.
* **Save Discourse (Forum) account - optional**: Send `!pollen verify-discourse <discourse-username>` and follow the process to verify and add your Discourse username to the Pollen DB.
* **Save GitHub account - optional**: Send `!pollen verify-github <github-username>` and follow the process to verify and add your GitHub username (in case you have one) to the Pollen DB.

Make sure to replace `<wallet-address>`, `<discourse-username>` and `<github-username>` with your information.

You also have a `!pollen userinfo` command to check the info you saved in the DB.

If you have questions, are interested in how pollen is calculated, or auditing the distributions, just hop on the [🏵**pollen**](https://discord.com/invite/y8fPNcNdAa) channel.

## Rules

{% hint style="warning" %}
In case of not complying with the rules, the [Pollen DAO](../community/swarms/pollen.md) reserves the right to remove any user from Pollen or request ban from the server, forum and github.
{% endhint %}

Due to the infancy of the SourceCred software there are still some ways to exploit it. Various parameter changes have minimized this risk but 1Hive still imposes the following rules, which are known and monitored by many in the community.

1. **One account per user policy:** A user is not allowed to own and operate multiple accounts.
2. **No reactions/likes trading allowed:** Entering agreements with other users to like/react to each other’s posts is not allowed. Reactions/Likes trading is defined by a pattern of 2 or more users mutually reacting to most or all of each other’s posts, regardless of the quality of the content.
3. **Bug use / Exploits / Manipulation:** If you find a bug or exploit in the system, please report it immediately. Those using a bug or exploit to their advantage may risk account deactivation.

## Pollen Distribution

Pollen is computed using **SourceCred** to create and analyze a graph of interactions between community members. While not a perfect representation of the value of contributions, Pollen can help reward the interactions that are important but too granular to warrant creating proposals for or claiming from a Swarm.

SourceCred monitors all messages and contributions to Discord, the Forum and GitHub and applies a multiplier to a base score of 1 cred per action. One of the primary ways of earning cred is when text you write or actions you create are responded to positively by other members through the use of emojis. Writing messages alone do not earn cred. The weights for Cred distribution are decided by the 1Hive community.

Cred earned within 1Hive is only useful within 1Hive. It isn't transferable and scoring is retroactive so if you sign up to pollen after having earned some, you will still receive cred for that period (although you will only receive a honey reward for your cred for the period after registering).

The [Pollen Explorer](https://1hive.github.io/pollen/#/explorer) has a leaderboard of Pollen users displaying the cred they have earned throughout their engagement with 1Hive.

The weights that determine the Pollen earned for each action can be seen in the [pollen explorer](https://1hive.github.io/pollen/#/explorer) by clicking on "SHOW WEIGHT CONFIGURATION".

![](<../.gitbook/assets/image (4).png>)

### Total Distribution

The weekly Honey distribution is capped at 25 Honey. 5% of the weekly distribution goes directly to the SourceCred team.

### Distribution Rate

Weekly payout is determined by a contributor's recent contribution's as well as their total contribution.

* **Weekly contribution** is the amount distributed for Pollen earned by users in the last week.
* **Total contribution** is the amount distributed for all Pollen earned by users up to the distribution date.
* **Decay Rate** is the rate at which the total contribution calculation decays for each previous week. Eg for a decay rate of 40%, the previous week is weighted at 100%, the second previous week is weighted at 60%, the third previous week is weighted at 36%, etc.

| Distribution Parameter | Allocation & Rate |
| ---------------------- | ----------------- |
| Weekly Contribution    | 25 HNY            |
| Total Contribution     | 8 HNY             |
| Decay Rate             | 40%               |

### Platform Distribution

A breakdown of each platforms relative distribution of Pollen each week.

| Platform | Percent of Distribution |
| -------- | ----------------------- |
| GitHub   | 30%                     |
| Discord  | 40%                     |
| Forum    | 30%                     |

### Discord Pollen Weights

On Discord, in order to mint cred for other users through emoji responses, users must have received some cred in the past. Minting to self is disabled and the system also weights the minting amount to others depending on how much cred the minter has earned.

| Total Cred   | Mint Weight |
| ------------ | ----------- |
| 160+ Cred    | 1x          |
| 120+ Cred    | 0.75x       |
| 80+ Cred     | 0.5x        |
| 40+ Cred     | 0.25x       |
| 0 to 40 Cred | 0x          |

All emojis give 1 cred, apart from the below exceptions.

| Emoji                            | Mint Weight |
| -------------------------------- | ----------- |
| 🍯 + `:Honeypot:` (custom emoji) | 2x          |
| 🐝 + `:Honeybee:` (custom emoji) | 2x          |
| 💩                               | 0x          |
| 👎                               | 0x          |

Channels that give 0 cred include: 🐸**memes**, 🤖**bot-commands**, 🕹**arcade**, 🦩**lounge**, 🍱**kitchen**, :coffee:**cafe** 🐱**Fauna** channels and all of the **Information** channels.

The 🐝**social-curation** channel gives 0.5x the standard cred weight.

The 🌈**design** channel gives 0.75x the standard cred weight.

The 🍄**nominations** channel mints 95% of cred for users who have been tagged in messages. Users sharing a tagged user get 5% cred for responses. All users tagged will share cred equally amongst all tagged users in that message.

All support channels such as :thunder\_cloud\_rain:**help**, **help-es**, and **help-fr** give 2.5x the standard cred weight.

### Forum Pollen Weights

On the Forum the total cred a user can mint is dependent on the trust level of the user.

| Trust level | Mint Weight |
| ----------- | ----------- |
| 4           | 1.5x        |
| 3           | 1.25x       |
| 2           | 1x          |
| 1           | 0.1x        |
| 0           | 0x          |

## Useful Links

Previous and ongoing [updates to Pollen parameters](https://forum.1hive.org/t/updates-to-sourcecred/726).

[General rules](https://forum.1hive.org/t/pollen-rules-and-a-reporting-system/1155) for engaging in Pollen.

[SourceCred documentation](https://sourcecred.io/docs/) for further information.
