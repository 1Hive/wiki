---
description: Şu anda geliştirilen subjektif oracle.
---

# Celeste \(Yakında\)

Celeste hakkında ve Celeste'in 1Hive için ne kadar önemli olduğu hakkında konuşuyorduk; ancak Celeste'in ne olduğuna, nasıl işlediğine ve niçin önemli olduğuna dair üst düzey bir bilgi kaynağı yoktu.

## Celeste Nedir?

Celeste, akıllı sözleşmelerin sorular sorup yanıtlar almasına olanak sağlayan Subjektif bir Oracle'dır; subjektif ihtilafların çözümlenmesinde, tahmin piyasalarının karara bağlanmasında, içeriklerin moderasyonunda ve daha bir sürü konuda merkeziyetsiz uygulama geliştiricilere kimlik sorma-yanıt verme oyunlarıyla geliştirme ve arbitraj yapma olanağı sunmaktadır.

Geliştiriciler, Celeste'e başvurarak üzerinde anlaşmaya varılan bir stratejiden dönenlerin cezalandırılacağının herkes tarafından bilinen bir şey olduğunu güvence altına alarak farklı taraflar arasındaki teşvikleri işbirliği haline dönüştürebilir.

Teknik düzeyde, Celeste merkeziyetsiz ihtilaf çözümü için kullanıl [Aragon Court](https://aragon.org/court)'un bir fork'udur. Celeste ile Aragon Court arasındaki temel fark, xDai üzerinde olmak ve staking token olarak Honey kullanmanın yanı sıra kişilerin sistemdeki oy haklarını sınırlandırmak için BrightID'yi entegre etmeyi tercih etmiş olmasıdır.

## İşleyiş Nasıldır?

Celeste'in nasıl işlediğini anlayabilmekaçısından öncelikle optimist ve kimlik sor-yanıt ver oyununun genel örüntüsü hakkında bilgi sahibi olmak faydalı olacaktır.

Diyelim ki 1Hive'ın teklif süreci için bloke hesaplı bir iş akışı oluşturmak istedik. Alice de kilometre taşları olarak bölünmüş şekilde bir proje üzerinde çalışmak istediğini söyleyerek bir teklif oluşturdu; fonlar bloke hesaba yerleştirildi ve kilometre taşları tamamlandıkça talep üzerine Alice'e iletildi. Alice ilk kilometre taşını tamamladığında, söz konusu kilometre taşının beklendiği şekilde tamamlandığını gösteren bir kanıtla birlikte ilgili fonları talep etmek üzere bir teminat yatırabilir. Ardından biz de, akıllı sözleşme perspektifinden, optimistik bir şekilde Alice'in dürüst olduğunu ve her ne kadar akıllı sözleşme işin gerçekten tamamlanıp tamamlanmadığını doğrulayamasa dahi herhangi birisi eşik miktarda teminat yatırıp Alice'in para çekmesini bloke etmek üzere ihtilafa girişmeye niyetlenmediği sürece işin gerçekten tamamlandığını varsayabiliriz.

Bu örüntüyü neyin doğru olduğuna dair herkes tarafından bilinen bir konu söz konusu olduğunda ama verilmesigereken kararın doğası gereği subjektif oluşundan dolayı akıllı bir sözleşmede hesaplanması pratik olmayan ya da imkansız olan geniş çapta bir sürü duruma uyarlamak mümkündür. 

Bu probleme getirilebilecek çözümlerden biri, bir akıllı sözleşmeye subjektif bir bilgi sağlama ihtiyacı duyulduğunda insanlara oy verdirmek olabilir. Ancak her seferinde herkesin oy verme işlemine katılması gerçekten çok verimsizdir; onun yerine biz, etkileşimde bulunan ilk kişinin sözleşmeye uygun bilgi sağlaması için güçlü bir istek duyacağı ve yanlış bilgi vermemek için de yeterli bir caydırıcı faktör bulunacak bir sistem kurmak istiyoruz.

Yukarıdaki bloke hesaplı örneğe geri dönecek olursak, Alice fon çekmek için talepte bulunup işi tamamladığını iddia ettiğinde, Bob bu talebi fark edip Alice'in sunduğu kanıtın yetersiz olduğuna karar vermiş olsun ve Alice'in para çekme talebine karşı çıkmak için teminat yatırıp Alice'e hem talep ettiği tutarı hem de Celeste'e başvurarak ihtilafı oluşturup çözmek üzere ekstra teminat yatırmasını istesin.

Çoğu durumda, ihtilafa gerek olmayacaktır; ihtilafların ortaya çıkabilme ihtimali dahi çoğu durumda katılımcıların dürüst davranmaları için yeterli olacaktır. Bununla birlikte, ihtilaf oluşması halinde, Celeste'e honey stake eden katılımcılardan bir çözüm sağlamaları istenecektir.

Protokol, ihtilafı değerlendirmek ve biz çözüm sunmak üzere katılımcılar seçecektir \(koruyucular\). Bu kişiler, stake ettikleri honey miktarı oranında seçileceklerdir. Görevlendirilen katılımcıların çoğunluğunun doğru sonucu sunacaklarını varsayıyoruz; ancak herkesin daha büyük bir koruyucu grubu ile bu kararı da aktif olarak honey stake eden bütün koruyucuların çözüm için katılım gösterebileceği son bir temyiz turuna ulaşana kadar temyiz etme hakkı olacak. Temyiz sayısı arttıkça; zaman, sermaye ve dikkat açısından maliyet artacak ve maliyet arttığından dolayı verilecek kararın oluşturacağı emsalin daha büyük etki yaratacağını ve mekanizmaya dair önemli bir güven oluşturabileceğini veya erozyona uğratabileceğini bekleyebiliriz. Temel olarak, süreç ihtilaf oluşturma ihtiyacını minimuma indirmek ve ihtilafların da çok büyümeden çözüme kavuşturulması için tasarlandı. Ancak ihtilaflar ortaya çıktığında en uygun yanıtın verilmesi için kullanılan teşvik de artırılmış olacak.

BrightID'yi Celeste'e entegre ederek, sonuçlar üzerindeki etkinin daha geniş bir dağılıma sahip olduğu ve nihai sonuç üzerinde daha fazla sayıda özgün bakış açısının temsil edildiğini sağlama alarak tamamen stake bazlı teşviklerden daha iyi, saldırılara karşı daha sağlam ve subjektif kararları daha meşru hale getiren bir sistem oluşturmuş oluyoruz.

## Niçin Önemli?

Celeste üzerinde geliştirilebilecek bir sürü yeni ve ilginç fırsat bulunmakta. Celeste'i tahmin piyasalarının karara bağlanmasında, bloke hesap tarzı iş akışlarının oluşturulmasında, honeyswap üzerinde token oluşturma ve kategorize etmede ve hatta chain dışında gerçekleşen hesaplamaların doğrulanmasına yardımcıolmada dahi kullanabiliriz.

Bununla birlikte, 1Hive için en önemli ilk kullanım alanı, honey dağıtımında kullandığımız kanaat oyu mekanizmalarına entegre etmektir. Böylece, uygulamaya geçirilmek için yeterli desteğe sahip olmasına rağmen topluluk sözleşmesinde tanımlanan topluluk beklentileriyle bağdaşmayan tekliflere topluluğun karşı çıkması ve bunları bloke etmesi amacıyla kullanıma sunabiliriz.

Ayrıca, tamamen ekonomik perspektiften bakacak olursak, Celeste 1Hive için iki temel nedenden dolayı gerçekten değerlidir.

1. Koruyucu olarak katılım göstermek için insanlar honey stake etmek ve ihtilaflar oluşturup bu ihtilafları temyize götürmek için honey cinsinden ücret ödemek zorunda olacaklardır. Celeste kullanımına ilişkin talep arttıkça, honey satın alma ve elde tutma talebinin de arttığını göreceğiz.
2. Celeste üzerinde her bir kişinin stake edebileceği honey miktarını sınırlandırdığımızdan dolayı, Celeste'in benimsenmesini teşvik ederek Honey'nin gini katsayısının düştüğünü göreceğiz ve bu da sonuçta daha sağlam ve daha merkeziyetsiz bir ekonomiye yol açacak.

## Ne Zaman Hazır Olacak?

Celeste bir süredir aktif olarak geliştirilmekte. Hâlâ yapılacak bir sürü iş var; ancak Celeste'i yıl bitmeden hizmete sunacağımızı ve 1Hive DAO'yu da kanaat teklifleri ve kararlarının tatrışmaya açılabileceği şekilde güncellemeyi umut ediyoruz. Sürece dahil olmak veya süreci takip etmek isterseniz gözünüz Discord'daki Celeste Swarm'ında olsun. Önümüzdeki haftalarda ekstra güncellemeler, ilerlemeler ve açılış planlarını paylaşabiliriz.![:sun\_with\_face:](https://forum.1hive.org/images/emoji/apple/sun_with_face.png?v=9)![:sun\_with\_face:](https://forum.1hive.org/images/emoji/apple/sun_with_face.png?v=9)![:sun\_with\_face:](https://forum.1hive.org/images/emoji/apple/sun_with_face.png?v=9)

## Faydalı Bağlantılar

Celeste hakkında tartışmalar:

{% embed url="https://forum.1hive.org/t/celeste-a-brief-primer/1483" %}

