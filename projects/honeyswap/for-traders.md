# Borsacılar İçin

## Toplam İşlem Maliyetini Düşünün

Borsalar arasında fiyat ve likidite değişkenlik göstermektedir. En iyi fiyatı aldığınızdan emin olmak için, _**toplam işlem maliyetinin**_ göz önünde bulundurulması önemlidir. Bunun içerisinde spot fiyatla birlikte genel işlem masrafları \(gas ücretleri gibi\), genel alım satım masrafları \(broker, likidite ve platform işlem ücretleri\) ve yaptığınız işlemin boyutuna ve borsada bulunan likiditeye bağlı olarak işlemdeki kayma oranı bulunmaktadır. 

$$
Toplam Maliyet = Spot Fiyat + Gas Fee + Platform Ücreti + Kayma
$$

Honeyswap, xDai üzerinde çalışmaktadır; dolayısıyla genel işlem ücretleri yok denecek kadar azdır. Genel işlem ücretleri ağdaki yoğunluğuna bağlı olarak işlem başına genellikle 5 ila 20 dolar arasında değişen genel alım işlem masrafları bulunan Uniswap ve diğer Ethereum bazlı merkeziyetsiz borsalarla karşılaştırılacak olursa, Honeyswap üzerinde alım satım yapmak genel işlem masraflarınızı önemli ölçüde düşürecektir.

Honeyswap'taki genel alım satım masrafları Uniswap'taki ile aynıdır: Her bir işlemden %0.3 alım satım ücreti alınır. Referans olması açısından, şu anda Coinbase'deki piyasa yapıcı \(maker\) ve piyasa alıcı \(taker\) ücretleri %0.5'tir.

Honeyswap, hâlâ oldukça küçük bir borsa olduğundan dolayı tokenlerin çoğunda likidite diğer borsalara göre epey düşüktür. Dolayısıyla işlem yapanlar, yine toplam işlem maliyetine eklenmesi gereken fiyat kaymasıyla karşılaşabilirler. Bu etki, işleminizin boyutuna göre artmaktadır.

Sonuç olarak, **bir sürü küçük alım satım işlemi yapmak gibi bir niyetiniz varsa Honeyswap diğer alternatiflere göre çok daha düşük bir toplam işlem maliyeti sunmaktadır.**

### Spot fiyatı

Honeyswap, otomatik piyasa yapıcı \(Automated Market Maker\) bir borsadır. Bu da, fiyatın alım ve satım borsaları aracılığıyla belirlendiği anlamına gelmektedir.

### Gas Fees

xDai üzerinde, gas ücretlerinin 1 GWEI'den yüksek olmasına gerek yoktur. Şu linkten, daha önce Ethereum Mainnet üzerinde yaptığınız işlemler için ne kadar gas harcadığınızı görebilirsiniz.  

| Networks | Ortalama İşlem Ücreti |
| :--- | :--- |
| Eth Mainnet | $3 |
| xDai | $0.0004 |
| Matic | $0.000001 |

### Broker, Likidite, Platform Ücretleri

Honeyswap platformunda işlem ücretleri, %0.3'tür. Bu, borsaların çoğuyla rekabetçi bir orandır. Bunun %0.25'i likidite sağlayıcılara giderken %0.5'i ise 1Hive ortak havuzuna gelir olarak geri döner.

| Borsalar | Taker | Maker |
| :--- | :--- | :--- |
| Binance | 0.10% | 0.1% |
| OKEX | 0.15% | 0.10% |
| Bitfinex | 0.20% | 0.10% |
| Kraken | 0.26% | 0.16% |
| Uniswap | 0.30% | 0.30% |
| **Honeyswap** | **0.30%** | 0.30% |
| Coinbase Pro | 0.50% | 0.50% |

### Fiyat Kayması

Kayma, spot fiyata göre ödenen fiyatta meydana gelen değişiklitir. Kayma, ticaret hacminin, ticaret boyutunun ve likiditenin belirleyici olduğu bir fonksiyondur. Fiyat kaymasının en düşük şekilde gerçekleşmesi için ticaret hacmi ile ticaret boyutunun düşük, likiditenin ise yüksek olması istenir.

## Araçlar

[Honeyswap](https://honeyswap.org/#/swap) - xDai üzerinde alım satım yapmak için kullanılır.

[Honeyswap Analytics](https://info.honeyswap.org) - Platforma ilişkin tablolar, ticaret hacmi, havuz likiditesi ve diğer analitik veriler için.

[Coingecko](https://www.coingecko.com/en) - Honeyswap verileri, Coingecko'nun token piyasa veri setine entegre edilmiştir.

