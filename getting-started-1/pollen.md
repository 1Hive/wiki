---
description: Katkıda bulunarak Honey kazanabilirsiniz
---

# Pollen

Pollen; 1Hive'ın [Discord](https://discord.com/invite/P4rRDUKTAU), [Forum](https://forum.1hive.org/) ve [Github](https://github.com/1Hive) topluluklarında yapılan katkıları belirlemek ve bu katkıları haftalık Honey dağıtımı ile ödüllendirmek için kullanılan bir sıralama sistemidir.

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

Bu örnekteki`justabee`, `justabee#1234` ve`0x0...000` ile kendi hesaplarınızı değiştirmeniz yeterlidir. Not: `Discourse` ile[ Forum](https://forum.1hive.org/) kastedilmektedir.

Aklınıza takılan bir soru olursa, pollenin nasıl hesaplandığını ya da dağıtımların nasıl denetlendiğini merak ediyorsanız, [`#🏵pollen`](https://discord.gg/y8fPNcNdAa) kanalına gelip sorabilirsiniz.

## Pollen Dağıtımı

Pollen, topluluk üyeleri arasındaki etkileşimlerin bir grafiği oluşturulup bu grafiğin analizinin yapılması için **SourceCred** kullanılarak hesaplanır. Yapılan katkıların değerini en iyi şekilde temsil etmemesine rağmen, Pollen bir teklif oluşturmak için veya Swarm'dan talep etmek için nispeten küçük olmasına rağmen aynı zamanda da önemli olan etkileşimlerin ödüllendirilmesine yardımcı olmaktadır.

Sourcecred; Discord, Discourse ve Github'daki bütün mesajları ve yapılan katkıları izler ve eylem 1 baz puana bir çarpan uygular. Cred kazanmanın temel yöntemlerinden biri, yazdığınız bir metnin veya oluşturduğunuz eylemlerin diğer kullanıcıların emoji kullanımı yoluyla pozitif olarak karşılanmasıdır. Mesaj yazmak, cred kazandırmaz. Cred dağıtımının ağırlıklarına 1Hive topluluğu karar verir.

1Hive'da kazanılan Cred, yalnızca 1Hive içerisinde işe yarar. Başka bir yere devredilebilir değildir ve puanlamalar geriye dönüktür. Dolayısıyla, bir miktar cred kazandıktan sonra pollen'e kaydolmanız halinde geçmişte kazandığınız cred'ler de hesabınıza eklenmiş olur \(ancak honey ödemelerini yalnızca kayıt olduktan sonraki dönem için alırsınız\).

[Pollen Explorer](https://1hive.github.io/pollen/#/explorer), 1Hive ile etkileşimde bulundukları süre boyunca Pollen'e kayıtlı kullanıcıların cred puanlarını gösteren bir skor tahtasıdır.

Her bir eylem için kazanılan Pollen'i belirleyen ağırlıklara [pollen explorer](https://1hive.github.io/pollen/#/explorer%20) üzerinde "SHOW WEIGHT CONFIGURATION" kısmına tıklayarak bakabilirsiniz.

![](../.gitbook/assets/image%20%288%29.png)

### Toplam Dağıtım

Haftalık Honey dağıtımı, 33 Honey'nin 15000$'dan düşük olması halinde 33 HNY veya 15000$ olacak şekilde belirlenmiştir. Haftalık dağıtımın %5'i doğrudan SourceCred ekibine gitmektedir.

![&#x15E;ekil1. Dolar de&#x11F;erine g&#xF6;re haftal&#x131;k Honey da&#x11F;&#x131;t&#x131;m&#x131;](../.gitbook/assets/image%20%2814%29.png)

### Dağıtım Oranı

Haftalık ödeme, katkıda bulunanın yakın zamanda gösterdiği katkılarla birlikte toplam katkısına göre belirlenmektedir. 

* **Haftalık katkı**, kullanıcıların son hafta içerisinde kazandıkları Pollen için dağıtılan miktardır.
* **Toplam katkı**, kullanıcıların dağıtım tarihine kadar kazandıkları bütün Pollen için dağıtılan miktardır.
* **Azalma hızı,** toplam katkı hesaplamasının bir önceki hafta için azalma hızıdır. Örneğin, %40'lık azalma hızı kullanıldığında, bir önceki haftanın ağırlığı %100 iken iki hafta öncesi %60, üç hafta öncesi ise %36 ağırlığa sahiptir.

| Dağıtım Parametresi | Dağıtım & Oran |
| :--- | :--- |
| Haftalık Katkı | 25 HNY |
| Toplam Katkı | 8 HNY |
| Azalma Hızı | 40% |

### Platform Dağıtımı

Her hafta yapılan Pollen dağıtımına ilişkin platformların oranları:

| Platform | Dağıtım Yüzdesi |
| :--- | :--- |
| GitHub | 30% |
| Discord | 40% |
| Forum | 30% |

### Discord Pollen Ağırlıkları

Discord üzerinde, diğer kullanıcılar için emoji etkileşimleriyle cred mint etmek için kullanıcıların geçmişte bir miktar cred kazanmış olmaları gerekmektedir. Kendine cred mint etmek mümkün değildir ve sistem ayrıca başkalarına cred min etme ağırlığını da etkileşimi veren kişinin kazandığı cred miktarına göre belirlemektedir.

| Toplam Cred | Mint Ağırlığı |
| :--- | :--- |
| 120+ Cred | 1x |
| 90+ Cred | 0.75x |
| 60+ Cred | 0.5x |
| 30+ Cred | 0.25x |
| 0 to 30 Cred | 0x |

Aşağıdaki istisnalar haricinde bütün emojiler 1 cred verir.

| Emoji | Mint Ağırlığı |
| :--- | :--- |
| 🍯 + `:Honeypot:` \(özel emoji\) | 2x |
| 🐝 + `:Honeybee:` \(özel emoji\) | 2x |
| 💩 | 0x |
| 👎 | 0x |

0 cred veren kanallar şunlardır: ✅check-in, \*\*🐸memes, 🤖bot-commands, 🕹arcade, 🦩lounge, 🍱kitchen, Fauna ve Bilgi kanallarının hepsi.

🐝**social-curation** kanalı, standard cred ağırlığının 0.25x'ini vermektedir.

🍄**nominations** kanalı, yazılan mesajlarda etiketlenen kullanıcılara cred'in %95'ini mint etmektedir. Birini etiketleyen kullanıcılar, etkileşimler için %5 cred kazanırlar. Bir mesaj içerisinde etiketlenen kullanıcıların tamamı, söz konusu mesajdaki cred'i eşit derecede paylaşırlar.

### Forum Pollen Ağırlıkları

Forumda, bir kullanıcının mint edebileceği toplam cred, kullanıcının güvenilirlik düzeyine bağlıdır.

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>Trust level</p>
        <p>(G&#xFC;venilirlik D&#xFC;zeyi)</p>
      </th>
      <th style="text-align:left">Mint A&#x11F;&#x131;rl&#x131;&#x11F;&#x131;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">1.5x</td>
    </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">1.25x</td>
    </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">1x</td>
    </tr>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">0.1x</td>
    </tr>
    <tr>
      <td style="text-align:left">0</td>
      <td style="text-align:left">0x</td>
    </tr>
  </tbody>
</table>

## Kurallar

SourceCred yazılımının çok yeni olmasından dolayı, kötüye kullanma yöntemleri de bulunmaktadır. Çeşitli parametre değişiklikleri bu riski minimuma indirmiştir; ancak 1Hive hâla topluluğun çoğu tarafından bilinen ve izlenen şu kuralları da uygulamaktadır.

1. **Kullanıcı başına bir hesap politikası.** Bir kullanıcının birden fazla hesaba sahip olmasına izin verilmez.
2. **Etkileşim/beğeni ticaretine izin verilmez.** Başka kullanıcılarla birbirinin paylaşımlarına beğeni verme/etkileşim verme konusunda anlaşma yapmaya izin verilmez. Etkileşim/Beğeni ticareti, 2 veya daha fazla kullanıcının ortak olarak birbirlerinin bütün paylaşımlarına veya çoğuna içerik kalitesine bakmaksızın etkileşim vermesidir.
3. **Bug'lardan Faydalanma / Kötüye Kullanma / Manipülasyon.** Sistemde bir bug veya açık bulmanız halinde lütfen bunu derhal raporlayın. Bir bug'dan veya açıktan kendi yararına faydalananların hesapları devre dışı bırakılacaktır.

## Faydalı Bağlantılar

Pollen parametrelerindeki [eski ve devam eden güncellemeler](https://forum.1hive.org/t/updates-to-sourcecred/726).

Pollen'e ilişkin [genel kurallar](https://forum.1hive.org/t/pollen-rules-and-a-reporting-system/1155).

Ayrıntılı bilgi için [SourceCred dokümantasyonu](https://sourcecred.io/docs/).

