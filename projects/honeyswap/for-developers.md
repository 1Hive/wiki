# Geliştiriciler İçin

## HoneySwap

Honeyswap, Uniswap'ın xDai üzerinde modifiye edilmiş halidir.

### Sözleşmeler

**UniswapV2Factory**:[`0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7`](https://blockscout.com/poa/xdai/address/0xA818b4F111Ccac7AA31D0BCc0806d64F2E0737D7)\*\*\*\*

**UniswapV2Router02**:[`0x1C232F01118CB8B424793ae03F870aa7D0ac7f77`](https://blockscout.com/poa/xdai/address/0x1C232F01118CB8B424793ae03F870aa7D0ac7f77)

### Önyüz

Önyüz, [honeyswap.org](https://honeyswap.org/) adresine konuşlandırılmıştır ve kaynak koda ise [şuradan ](https://github.com/1Hive/uniswap-interface)erişilebilir. Yapılan önemli modifikasyonlar, yeniden markalama ve düzenlenmiş bir token listesidir.

### Info.honeyswap.org

Honeyswap için uniswap.info fork'u. [info.honeyswap.org](https://info.honeyswap.org) adresinden erişilebilir.

### Subgraph'lar

Honeyswap forku, aşağıdaki iki subgraph fork'u ile güçlendirilmiştir:

[Uniswap v2 Subgraph](https://thegraph.com/explorer/subgraph/1hive/uniswap-v2): Temel para birimi olarak xDai'yi ve bir token beyaz listesini kullanacak şekilde ayarlanmış resmi Uniswap v2 subgraph'ının bir forku. Kaynak koduna [şuradan ](https://github.com/1Hive/uniswap-v2-subgraph)ulaşabilirsiniz.

[Ethereum Blocks](https://thegraph.com/explorer/subgraph/1hive/xdai-blocks): xDai'de, üzerinde herhangi bri değişiklik yapılmadan kullandığımız Blocklytics Ethereum Blocks fork'u. Kaynak koduna şuradan ulaşabilirsiniz.

### Önyüz

Önyüz, Etherscan yerine Blockscout'ı kullanacak şekilde uygun token listeleri ve çıkış adresleri ile küçük değişikliklerle uniswap.info'nun kaynak kodunun bir fork'udur.

Önyüzün kaynak koduna [şuradan ](https://github.com/1Hive/uniswap-info/)erişebilirsiniz.

### Honeymaker

Honeymaker, Sushimaker dağıtımıdır ve LP paylarını Honeywap üzerinden Honey Ortak Havuzuna Honey göndermek için dönüştüren ek bottur.

SushiMaker şu adrese konuşlandırılmıştır: [`0x076b64f9F966e3bBD0FCdC79D490Ab71cF961bb0`](https://blockscout.com/poa/xdai/address/0x076b64f9F966e3bBD0FCdC79D490Ab71cF961bb0).

Bot, periyodik olarak Sushimaker sözleşmesinde Honeyswap üzerindeki seçilmiş çiftler için `convert`foksiyonunu çağırıp LP paylarını Honey'e dönüştürür.

Botun kaynak kodu [şu adreste](https://github.com/1hive/honeymaker) bulunabilir.

### Faydalı Bağlantılar

[Ortak Havuz Subgraph](https://thegraph.com/explorer/subgraph/onbjerg/honey)'ı.

