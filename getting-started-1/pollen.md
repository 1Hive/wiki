---
description: Katkıda bulunarak Honey kazanabilirsiniz
---

# Pollen

Pollen; 1Hive'ın [Discord](https://discord.com/invite/P4rRDUKTAU), [Discourse](https://forum.1hive.org/) ve [Github](https://github.com/1Hive) topluluklarında yapılan katkıları belirlemek ve bu katkıları haftalık Honey dağıtımı ile ödüllendirmek için kullanılan bir sıralama sistemidir.

## Nasıl Katılırım?

Haftalık Pollen dağıtımlarından pay almak için, 1Hive Discord'unda [Verified ](discord/#bot-komutlari)olmalısınız. Ardından, 1Hive'ın Discord, Discourse ve Github topluluklarıyla etkileşimde bulunmaya başlar başlamaz kayıt olurken verdiğiniz cüzdan adresinizde Honey'e dönüşecek şekilde Pollen kazanmaya da başlamış olursunuz.

Haftalık pollen dağıtımlarından pay almak için, desteklenen platfomlardaki hesaplarınızı kaydettirerek bunları xDai adresinize bağlamanız gerekmektedir. Bunu da, 1Hive Discord'un `#🐛onboarding` kanalına aşağıdaki formatta bilgilerinizi girerek yapabilirsiniz:

```text
#🏵pollen
github: justabee
discourse: justabee
discord: justabee#1234
xDai: 0x0...000
```

Bu örnekteki`justabee`, `justabee#1234` ve`0x0...000` ile kendi hesaplarınızı değiştirmeniz yeterlidir.

Aklınıza takılan bir soru olursa, pollenin nasıl hesaplandığını ya da dağıtımların nasıl denetlendiğini merak ediyorsanız, [`#🏵pollen`](https://discord.gg/y8fPNcNdAa) kanalına gelip sorabilirsiniz.

## Pollen Dağıtımı

Pollen, topluluk üyeleri arasındaki etkileşimlerin bir grafiği oluşturulup bu grafiğin analizinin yapılması için **SourceCred** kullanılarak hesaplanır. Yapılan katkıların değerini en iyi şekilde temsil etmemesine rağmen, Pollen bir teklif oluşturmak için veya Swarm'dan talep etmek için nispeten küçük olmasına rağmen aynı zamanda da önemli olan etkileşimlerin ödüllendirilmesine yardımcı olmaktadır.

Sourcecred; Discord, Discourse ve Github'daki bütün mesajları ve yapılan katkıları izler ve eylem 1 baz puana bir çarpan uygular. Cred kazanmanın temel yöntemlerinden biri, yazdığınız bir metnin veya oluşturduğunuz eylemlerin diğer kullanıcıların emoji kullanımı yoluyla pozitif olarak karşılanmasıdır. Mesaj yazmak, cred kazandırmaz. Cred dağıtımının ağırlıklarına 1Hive topluluğu karar verir.

1Hive'da kazanılan Cred, yalnızca 1Hive içerisinde işe yarar. Başka bir yere devredilebilir değildir ve puanlamalar geriye dönüktür. Dolayısıyla, bir miktar cred kazandıktan sonra pollen'e kaydolmanız halinde geçmişte kazandığınız cred'ler de hesabınıza eklenmiş olur \(ancak honey ödemelerini yalnızca kayıt olduktan sonraki dönem için alırsınız\).

[Pollen Explorer](https://1hive.github.io/pollen/#/explorer), 1Hive ile etkileşimde bulundukları süre boyunca Pollen'e kayıtlı kullanıcıların cred puanlarını gösteren bir skor tahtasıdır.

Her bir eylem için kazanılan Pollen'i belirleyen ağırlıklara pollen explorer üzerinde "SHOW WEIGHT CONFIGURATION" kısmına tıklayarak bakabilirsiniz.

The weights that determine the Pollen earned for each action can be seen in the [pollen explorer](https://1hive.github.io/pollen/#/explorer%20) by clicking on "SHOW WEIGHT CONFIGURATION".

![](../.gitbook/assets/image%20%288%29.png)

### Toplam Dağıtım

The weekly Honey distribution is capped at $15,000 or 33 Honey if 33 Honey is worth less than $15,000. 5% of the weekly distribution goes directly to the SourceCred team.

![Figure 1. Weekly distribution in Honey based on USD value](../.gitbook/assets/image%20%2814%29.png)

### Distribution Rate

Weekly payout is determined by a contributor's recent contribution's as well as their total contribution. 

* **Weekly contribution** is the amount distributed for Pollen earned by users in the last week.
* **Total contribution** is the amount distributed for all Pollen earned by users up to the distribution date.
* **Decay Rate** is the rate at which the total contribution calculation decays for each previous week. Eg for a decay rate of 40%, the previous week is weighted at 100%, the second previous week is weighted at 60%, the third previous week is weighted at 36%, etc.

| Distribution Parameter | Allocation & Rate |
| :--- | :--- |
| Weekly Contribution | 25 HNY |
| Total Contribution | 8 HNY |
| Decay Rate | 40% |

### Platform Distribution

A breakdown of each platforms relative distribution of Pollen each week.

| Platform | Percent of Distribution |
| :--- | :--- |
| GitHub | 30% |
| Discord | 40% |
| Discourse | 30% |

### Discord Pollen Weights

On Discord, in order to mint cred for other users through emoji responses, users giving the response must be [Verified](discord/#tips). Minting to self is disabled and the system also weights the minting amount to others depending on how much cred the minter has earned.

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

## Rules

Due to the infancy of the SourceCred software there are still some ways to exploit it. Various parameter changes have minimized this risk but 1Hive still imposes the following rules, which are known and monitored by many in the community.

1. **One account per user policy** A user is not allowed to own and operate multiple accounts.
2. **No reactions/likes trading allowed** Entering agreements with other users to like/react each other’s posts is not allowed. Reactions/Likes trading is defined by a pattern of 2 or more users mutually reacting to most or all of each other’s posts, **regardless of the quality of the content.**
3. **Bug use / Exploits / Manipulation** If you find a bug or exploit in the system, please report it immediately. Those using a bug or exploit to their advantage may risk account deactivation.

## Useful Links

Previous and ongoing [updates to Pollen parameters](https://forum.1hive.org/t/updates-to-sourcecred/726).

[General rules](https://forum.1hive.org/t/pollen-rules-and-a-reporting-system/1155) for engaging in Pollen.

[SourceCred documentation](https://sourcecred.io/docs/) for further information.

