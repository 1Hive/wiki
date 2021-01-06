# Pollen

Pollen is a contributor rank used to recognize contributions to 1Hive’s [Discord](https://discord.com/invite/P4rRDUKTAU), [Discourse](https://forum.1hive.org/), and [Github](https://github.com/1Hive) communities, and reward these contributions with weekly distributions of Honey.

## How do I participate

As soon as you start interacting on 1hive’s Discord, Discourse, and Github communities you’ll start earning Pollen.

Pollen is computed using **SourceCred** to create and analyze a graph of interactions between community members. While not a perfect representation of the value of contributions, Pollen can help reward the interactions that are important but too granular to warrant creating proposals for or claiming from a swarm.

In order to receive weekly pollen distributions you’ll need to register your accounts on supported platforms and link them to your xDai address. You can do this by posting the below in 1hive Discord’s `#🐛onboarding` channel:

```text
#🏵pollen
github: justabee
discourse: justabee
discord: justabee#1234
xDai: 0x0...000
```

Replacing`justabee`, `justabee#1234` and `0x0...000` with your accounts.

You also have to be [**Verified** ]()in discord in order to receive weekly pollen distributions.

If you have questions, are interested in how pollen is calculated, or auditing the distributions, just hop on the [`#🏵pollen`](https://discord.gg/y8fPNcNdAa) channel.

## Pollen Distribution

Pollen uses SourceCred to maintain a score for individuals dependent on the contributions they have made to Discord, Discourse and GitHub. SourceCred monitors all messages and contributions and applies a multiplier to a base score of 1 cred per action. One of the primary ways of earning cred is when text you write or actions you create are responded too positively by other members through the use of emojis. Writing messages do not earn cred. The weights for Cred distribution are decided by 1Hive community.

Cred earned within 1Hive is only useful within 1Hive, it isn't transferable and scoring is retroactive so if you sign up to pollen after having earned some, you will still receive cred for that period \(although you will only receive a honey reward for the period after registering\).

The [Pollen Explorer](https://1hive.github.io/pollen/#/explorer) has a leaderboard of Pollen users displaying the cred they have earned throughout their engagement with 1Hive.

The weights that determine the Pollen earned for each action can be seen in the [pollen explorer](https://1hive.github.io/pollen/#/explorer%20) by clicking on "SHOW WEIGHT CONFIGURATION".

![](../../.gitbook/assets/image%20%288%29.png)

### Discord Pollen Weights

On Discord, in order to mint cred for other users through emoji responses, users giving the response must be [Verified](). Minting to self is disabled and the system also weights the minting amount to others depending on how much cred the minter has earned.

| Total Cred | Mint Weight |
| :--- | :--- |
| 120+ Cred  | Mint 1x |
| 90+ Cred | Mint 0.75x |
| 60+ Cred | Mint 0.50 |
| 30+ Cred  | Mint 0.25x |
| 0 to 30 Cred  | Mint 0x |

All emojis give 1 cred, apart from the below exceptions.

| Emoji | Mint Weight |
| :--- | :--- |
|  🍯 + `:Honeypot:` \(custom emoji\) | 2x |
| 🐝 + `:Honeybee:` \(custom emoji\) | 2x |
| 💩 | 0x |
| 👎 | 0x |

Channels that give 0x cred include: `#✅check-in` ,`#🐸memes` ,`#🤖bot-commands` `#🕹arcade` ,`#🦩lounge` ,`#🍱kitchen` , Fauna channels and all of the Information channels.

The `#🍄nominations` channel mints 95% of cred for users who have been tagged in messages, users sharing a tagged user get 5% cred for emoji responses. All users tagged will share cred equally amongst all tagged users in that message.

### Forum Pollen Weights

On the Discourse forum the total cred a user can mint is dependent on the trust level of the user.

| Trust level | Mint Weight |
| :--- | :--- |
| 4 | Mint 1.5x |
| 3 | Mint 1.25x |
| 2 | Mint 1x |
| 1 | Mint 0.1x |
| 0 | Mint 0x |

### Additional Weights

\*\*\*\*[**pluginBudgets.json**](https://github.com/1Hive/pollen/blob/master/config/pluginBudgets.json) ****- Payout distribution amount by 'plugin': Discord, Discourse, and GitHub.

[**Grain.json** ](https://github.com/1Hive/pollen/blob/master/config/grain.json)- Payout based on total cred, recent week, and a catch up for any retro active payments that were missed.

\*\*\*\*[**Dependencies.json**](https://github.com/1Hive/pollen/blob/master/config/dependencies.json) - Monthly payout balancer.

## Rules

Due to the infancy of the SourceCred software there are still some ways to exploit it. Various parameter changes have minimized this risk but 1Hive still imposes the following rules, which are known and monitored by many in the community.

1. **One account per user policy** A user is not allowed to own and operate multiple accounts
2. **No reactions/likes trading allowed** Entering agreements with other users to like/react each other’s posts is not allowed. Reactions/Likes trading is defined by a pattern of 2 or more users mutually reacting to most or all of each other’s posts, **regardless of the quality of the content.**
3. **Bug use / Exploits / Manipulation** If you find a bug or exploit in the system, please report it immediately. Those using a bug or exploit to their advantage may risk account deactivation.

## Useful Links

Previous and ongoing [updates to Pollen parameters](https://forum.1hive.org/t/updates-to-sourcecred/726).

[General rules](https://forum.1hive.org/t/pollen-rules-and-a-reporting-system/1155) for engaging in Pollen.

[SourceCred documentation](https://sourcecred.io/docs/) for further information.

[The Pollen Swarm](../../community/swarms/pollen.md)

