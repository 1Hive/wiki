# Teknik Tanıtım

Gardens, tokenize edilmiş topluluklar oluşturmak ve bunları bir araya getirmek için oluşturulmuş bir platformdur. Kullanıcılar bir konuya dikkat çekmek, teklifleri önceliklendirmek ve kolektif olarak paylaşılan kaynakları tahsis etmek için token'lerini stake edebilmektedirler.

### Sorun

Tokenize Topluluklar, güçlü oluşumlardır; ancak bir toplulukta çoğunluk mutabakatının sağlanması zorlu ve sorun çıkarabilecek bir süreçtir. Oy vermek en azından Ethereum Mainnet üzerinde pahalı bir işlemdir ve genellikle oylarının karar vermede yüksek etki yaratacağına güvenen balinaların ilgisini çekmektedir. Bu durum da katılım üzerinde olumsuz bir etki yaratmakta, geniş bir topluluk aidiyetini besleyen sesini duyurma ve etki yaratma gibi olguları zayıflatmaktadır.

### Çözüm

Gardens, tokenize toplulukların, yeni bir mutabakat sağlama süreci olan, aktif topluluk üyelerinin çıkarlarını oransal olarak temsil eden ve kullanıcıların önem verdikleri topluluklara çeşitli şekillerde kolayca katılım göstermesini sağlayan kanaat oylamasını daha iyi şekilde uygulamasına olanak sağlamaktadır. 

* Açık kaynak projeler gibi henüz tokenize olmamış geleneksel çevrimiçi topluluklar bu platformu kullanara tokenize hale gelebilirler, katkı gösterenleri tokenler ile ödüllendirebilir ve projeyi desteklemek isteyen kişilerin token satın alıp tekliflere bu tokenleri stake ederek öncelikler hakkında sinyal verebilirler.
* Mevcut tokenize projeler ise bu platformu kullanarak zincir üzerindeki nakit akışlarının bir kısmını topluluk tarafından yönetilen bir havuza aktararak veya token sahiplerinin proje destekleyici olarak hareket etmelerine olanak sağlayarak topluluklarının dahiliyetini iyileştrebilir, önemli özellikler ve kilometre taşları oluşturup bunları önceliklendirebilirler. 

### Planlanan İşlevsellik

* Kullanıcılar, toplulukları için mevcut bir ERC20 tokenini getirebilecek veya yeni bir token oluşturabilecekler.
  * Mevcut bir ERC20 token kullanılması halinde, ortak havuz tokenlerin stake veya unstake edlimesiyle ilişkili yapılandırabilir bir işlem ücreti yoluyla ya da bağışlar yoluyla fonlanabilir \(örneğin, zincir üzerindeki nakit akışını ortak havuza yönlendirerek\).
  * Yeni bir token oluşturulması halinde ise ortak havuz, tıpkı Honey'de olduğu gibi bir dinamik arz politikası ile fonlanabilir.
* Kullanıcılar, tekliflerin moderayonu için kullanılacak yazılı topluluk ilkeleri oluşturup kullanıma geçirebilecekler.
  * Kullanıcılar teklif oluştururken tokenlerini stake edecekler ve bu tekliflerin topluluk ilkelerini ihlal etmesi halinde bu tekliflere karşı çıkabileceklerdir. Böyle bir ihtilaf durumunda, çözüme kavuşturulması için [Celeste](../celeste/)'e başvurulabilecektir.
* Kullanıcılar, [1hive.org](https://1hive.org/) üzerinde sunulacak arayüz üzerinden toplulukları araştırabilecek, keşfedebilecek ve katılabileceklerdir \(tokenleri Honeyswap üzerinden satın alarak\)
  * Bu listedeki toplulukların sıralaması, Honeyswap üzerinde kendilerine karşılık gelen likidite havuzunda tuttulan Honey miktarı ile belirlenecektir.
* Tekil topluluk sayfalarına 1hive.org/\#/&lt;topluluk adı&gt; şeklinde erişilebilir olacak.
* Teklif metaverisi, kullanıcı profilleri ve yorumların hepsi IPFS üzerinde depolanacak, izinsiz ve merkeziyetsiz bir şekilde alternatif arayüzlerin oluşturulmasına olanak sağlanacaktır.
  * 1hive.org üzerinde erişilebilir hale getirilecek arayüzde görünür kalabilmek için kullanıcılar ve toplulukların 1Hive Topluluk Sözleşmesi'ne bağlı kalması gerekecektir.

