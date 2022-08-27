# KKU Zombi İstilası

#### Kırıkkale Üniversitesi 3. sınıf 2. dönem Proje 2 dersi dönem projesi 

### İçerik

- Projenin Amacı
- Projenin Adımları
- Projenin Sonuçları
- Geliştirmek İçin Kullandığınız Araçlar, Teknolojiler, Platform ve Diller
- Ekran Görüntüleri




#####  ** Not :Akademik proje olduğu için kod dosyaları gizlenmiştir**

#

### Projenin Amacı

- Projemin amacı insanların oyun oynarken hem eğlenip hem de stres atarak boş vakitlerini
kaliteli bir şekilde geçirmelerini sağlamaktır. Oyuncu yerden mermi, can ve bomba
toplayarak şehrin ışıklandırma sistemine saldıran zombileri durdurmaya çalışır. Işıklar söner
ise zombiler daha fazla güçlenir ve oyun kaybedilir. Zombiler kampüs içerisinde doğar ve
Yenişehir trafoya saldırmaya çalışır kullanıcı sadece Yenişehir’de loot toplaya bilir
kullanıcının amacı cephanesini akıllıca kullanarak kampüsteki ve şehirdeki zombileri
öldürmektir.

#

### Projenin Adımları

- Kurulum ve Hazırlık; İlk olarak projemi geliştirebilmek için gerekli olan Unity
kurulumu yaptım. Daha sonra Unity üzerinde bir 3D oyun projesi oluşturdum. Projeme
başlamadan önce kullanacağım ev, yol, silah ve düşman modellerine uygun model
paketlerini buldum ve indirdim.

- Haritanın oluşturulması; Oyunum harita olarak bir mahalleden ve bir üniversite
kampüsünden oluşuyor. İlk olarak mahallemi tasarlamaya başladım. Mahallemi
oluşturabilmek için bir 3D Plane nesnesi oluşturdum. Mahallem bu nesne üzerine
yükselecek. Plane nesnem üzerine ilk olarak ev modellerimi ekledim. İndirmiş olduğum
ev modellerine Box Collider eklenmemişti, indirmiş olduğum 4 farklı ev modeli için
Box Collider oluşturdum. Bu sayede evlerin oyun içerisinde fiziki bir kabuğunun
olmasını sağladım. Evlere box çölledir eklemesiydim oyunu oynar iken ev modellerinin
duvarlarından içeri girebilirdik. Evlerimi oluşturduktan sonra evler arasında yol
modellerim ile caddeler oluşturdum. Mahallemin güzel ve gerçekçi gözükebilmesi için
yol boyamaları, trafik ışıkları, barikatlar, direkler, trafolar ve ağaçlar kullandım.
Mahallemi oluşturduktan sonra kampüsümü tasarlamaya başladım. Kampüs tasarımımı
bir 3D nesne olan terrain üzerine yapacağım. Burada terrain kullanmamın amacı
kampüs içerinde yer alan dağlar tepeler ve buna benzer arazi şartlarını oluştura biliyor
olmamızdır. İlk olarak tasarımı dağardan başladım kampüsümün etrafını yüksek
dağlarla çevreledim. Daha sonra kampüs içerindeki yolları oluşturdum. Yol tasarımı
bittikten sonra kampüste yer alan fakülteleri terrainime ev modellerini kullanarak
ekledim. Burada eklemiş olduğum evlere de Box Collider ekleyerek gerçekçi bir yapı
olmasını sağlam. Harita tasarımımda en son olarak ağaçlandırma işlemleri yaptım.

- Karakterin oluşturulması; Oyunum fps türde olduğu için kamera açısını insan göz
hizasına göre ayarladım. Daha sonra kamerada karakterin kollarının ve silahların doğru
acıda gözükmesini sağladım. Karakterin eline silah modelimi yerleştirdikten sonra bir
canvas objesi sayesinde silahımın crosshairini ekranın orta noktasına sabitledim. Silah
modelimi ateşliye bilmek için bir c# script dosyası oluşturdum. Bu dosya içerisinde
kameramın baktığı orta noktanın yani crosshairimin gösterdiği noktadaki obje ile
etkileşime girilmesini ve silah sağ mause clik tuşu ile ateşlendiğinde gerekli animasyon
ve seslerin oynatılmasını sağladım. Silahın vurduğu objenin hangi sınıfa ait olduğuna
anlamak için Sahnemde kullandığım her objeye bir tag ile işaretledim. Vurduğum nesne düşman tagı ile işaretlenmiş ise kan efektini oynattım ve vurulan nesnenin can özelliğini vuran silahın darbe gücüne göre azalttım. Vurulan nesne herhangi bir çevre elemanı ise
vurulan noktada mermi izi çıkmasını ve bir süre sonra kaybolmasını sağladım. Vurmuş
olduğum obje haraket edebilme özelliğine sahipse yani bir çöp kovası yada benzer bir
objeyse merminin hasar gücüne göre hareket etmesini sağladım.

- Silahlar; Projemde bir adet otomatik uzun namlulu silah, bir adet pompalı saldırı silahı,
bir adet uzun mesafe keskin nişancı silahı ve bir adet 6 patlar tabanca olmak üzere
toplamda 4 adet silah modeli kullandım. Bu sillah modellerini internetten indirdim.
İndirmiş olduğum modellerin her birini karakterimin eline yerleştirdim ve gerçekçi bir
tutuş pozisyonunda ayarladım. Daha sonra tüm silahlarıma ateş animasyonu, şarjör
yenileme animasyon yapmak için Unity içinde bulunan animatörü kullandım . Silah
modellerimin her biri için bir C# script dosyası oluşturdum. Bu doysa üzerinden her
silah için farklı ateş sesi, sarjor değiştirme sesi, mermi bitiş sesi olmak üzere 4 adet
ses dosyasının ilgili zamanlarda yönetilmesini sağladım. Bunlarla beraber ateş, mermi
izi ve kan izi efektlerimi scriptime her silah için ekledim. Ayrıca oluşturmuş olduğum
dosya içerisinde dışarıdan almış olduğum efekt ve seslerin doğru zamanda çalıştırıla
bilmesi için her özelliği bir tuşa atadım. Mause sağ click tuşu ateş et fonksiyonumu
çalıştırıyor, Mause sol click tuşu zoom fonksiyonumu çağırıyor, keskin nişancı
tüfeğimde sağ click crosshairimi değiştirerek dürbün özelliğini aktif ediyor, R tuşu
karakterin elindeki silaha uygun cephane varsa şarjör dolduruyor. Silah modellerimin
genel işlemleri bittikten sonra bu modellerin de yönetimini GameKontrolcu isimli C#
script dosyamın içerisinde yaptım. Burada silahlarım arasında geçişi yönettim.
Klavyeden 1 numaraya basıldığında Ak-47 isimli silahın karakterimin eline
yerleşmesini ve bu silaha uygun ses ve animasyonların aktif edilmesini sağladım.
Klavyeden 2 numaraya basıldığında Pompali isimli silahın karakterimin eline
yerleşmesini ve bu silaha uygun ses ve animasyonların aktif edilmesini sağladım.
Klavyeden 3 numaraya basıldığında Sniper isimli silahın karakterimin eline
yerleşmesini ve bu silaha uygun ses ve animasyonların aktif edilmesini sağladım.
Klavyeden 4 numaraya basıldığında Magnum isimli silahın karakterimin eline
yerleşmesini ve bu silaha uygun ses ve animasyonların aktif edilmesini sağladım.
Klavyeden Q numaraya basıldığında silahlar arasında gezinilmesini sağladım. Silah
modellerime ek olarak düşmanlara toplu hasar verebilmek için bir el bombası modelli
kullandım. Bombanın atılabilmesi işlemini G harfine atadım. G tuşuna basıldığında
kamera pozisyonunda cross ile işaretlenen acıya bombanın fırlatılmasını ve ulaştığında
bir yarı çapta patlamasını sağladım. Bomba atıldığında gerçekçi bir görünüm olması
için ses ve animasyon oynattım .

- Yerden Loot Toplaması; Oyunum içerisinde yerden bomba, can ve silah modellerime
özel mermi alınabiliyor. Bu işlemlerin her biri için haritada çıkacak notları belirledim
daha sonra GameKontrol nesneme Mermi_Kutusu_Olustur, Bomba_Kutusu_Olustur ve
Healt_Kutusu_Olustur isimli C# script dosyalarımı ekledim. Bu dosyalarda lootların
kaç saniye aralıkla oluşacağını ve oluştuğunda sahnede gösterilecek olan modelleri
ekledim. Oyuncunun loot topluya bilmesi icin gerekli olan işlemleri silah modellerimin
scriptlerinin icersinde yer alan OnTriggerEnter fonksiyonu ile yaptım. Kullanıcının
hangi loota çarptığını anlamak için loodlarımı taglar ile işaretledim ve alınan loodu
toplam envartere ekledim.

- Düşmanların oluşturulması; Projemde asker, kadın, kadın2 ve polis olmak üzere 5 adet
zombi modeli yer almaktadır. İlk olarak modellerimin yönetilebilmesini sağlamak için gerekli olan modelleri ekledim. Bunlar; Yapay zeka yönetimi için Nav Mesh Agent,
Fiziksel işlemler için Rigidbody, zombi animasyonu için Animator, Karakterin
konturolu için Character Controller, İlgili sesleri oynata ilmek için Audio Source ve
bütün özellikleri yönetebilmek icin düşman isminde bir C# Script dosyası oluşturdum.
Bu işlemleri bütün zombi modellerime ekledim ve bu modelleri prefab haline getirdim.
Oyunumda zombilerin çıkabilmesi için 2 adet nokta belirledim ve bu noktalardan
GameKontrolcu isimli script düsyam üzerinden belirli zaman aralıklarıyla düşmanların
çıkmasını sağladım. Oluşan zombile mahalle sahnem içerisinde yer alan 2 tane trafodan
birine random olarak saldırmak için görevlendirdim. Oluşan zombilerin hedefe
saldırabilmesi için bir yapay zekaya ihtiyacı var bunu Unity içerisinde yer alan
navigasyon özelliği ile yönettim. Bu özellik nesnelerin yürüyebilecekleri alanları
çiziyor ve nesneyi hedefe en kısa yoldan gönderiyor. Zombilerin adım yüksekliğini ve
çıkabilecekleri yokuş eğimini burada ayarladım. Gercekci değerler vererek oyuncunun
gerçekçi bir deneyim yaşamasını sağladım.

- Ara yüz ve canvas; ilk olarak Ana menüyü oluşturdum. Ana menüde iki adet buton,
oyun adı ve oyun içinden bir kare gösterilir, Butonlardan birincisine yani savaş
butonuna tıklanır ise önce bir yüklenme ekranı gösterilir daha sonra ise oyun başlar,
ikinci buton oyuncan çıkma işlemini gerçekleştirir. Daha sonra kullanıcının oyunu takip
edebilmesi için bir canvas oluşturdum. Canvas üzerinde kalan can, mermi kapasitesi,
sahip olunan can kutusu, sahip olunan bomba ve sahnede bulunan toplam zombi sayısı
bilgileri yer almaktadır. Bu bilgiler anlık olarak güncellenmekledir. Kullanıcı oyunu
durduğunda pause isimli ekran canvas üzerinde açılır bu ekranda oyunun o anki durumu
ve 2 adet buton yer alır, butonlardan ilki devam etmeyi ikincisi ana menüye gitmeyi
sağlar. Oyuncu başarısız olursa Game Over ekranı açılır bu ekranda kaybettiniz yazısı,
sevinen bir zombi iconu ve 2 adet buton yer alır bunlardan birincisi oyunu tekrar
başlatır, ikincisi ise ana menüye gider. Kullanıcı Oyunu kazanırsa kazandınız isimli
ekran yansıtılır bu ekranda bir adet üzülen zombi, kazandınız yazısı ve iki adet buton
yer alır butonların görevi de diğer sayfalarla aynıdır.

#

### Projenin Sonuçları

- Geliştirmiş olduğum oyun insanların kaliteli zaman geçirmesine olanak sağladı. Bununla
beraber kullanıcı oyun içerisinde tek başına ve düşman sayısı çok fazla yani kullanıcıya birde
çok zorlukla elindekileri en iyi kullanarak kurtulması gerektiği ana fikri öğretilmiştir. Oyuncu
mermilerini gereksiz kullanırsa kaybeder burada tasarrufu, yavaş oynarsa kaybeder burada
elindeki fırsatlalar kullanmayı ve canı az iken savaşmak yerine can toplamaz ise yine kaybeder
burada da doğru tercih yapmayı öğrenmesini sağladım.

#

### Geliştirmek İçin Kullandığınız Araçlar, Teknolojiler, Platform ve Diller

- Projemi Unity ve Visual Studio platformları üzerine geliştirdim. Unity oyun ici tasarımlarda
kullandım, Visual Studio yardımı ile oyun içerisinde kullandığım script dosyalarımı C# yazılım
dili kullanarak kodladım.

#
