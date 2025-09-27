# Common Continuous Distributions

[Common Continuous Distributions](https://colab.research.google.com/drive/1_Q8utbwmA1a27-LFl3zOYjWzzjZEjo37#scrollTo=xe1TzefXfHYa)

<img width="675" height="127" alt="image" src="https://github.com/user-attachments/assets/5c7f654b-273e-4aaa-9c2b-145f04d2d757" />


<img width="858" height="673" alt="image" src="https://github.com/user-attachments/assets/586ed94c-117e-4198-aa88-0b28244ddaa5" />

<img width="580" height="368" alt="image" src="https://github.com/user-attachments/assets/828ec00d-d78a-442e-8114-1d81e900c0ea" />

<img width="778" height="308" alt="image" src="https://github.com/user-attachments/assets/5298fb09-c902-4f51-a9c0-059da9c8e52d" />

<img width="789" height="517" alt="image" src="https://github.com/user-attachments/assets/d7c6694d-b933-4c94-82cf-4df668e83423" />


<img width="558" height="263" alt="image" src="https://github.com/user-attachments/assets/d34fe46d-0771-40b3-b7fc-70b58c2cc966" />

<img width="501" height="335" alt="image" src="https://github.com/user-attachments/assets/f8d02573-6a0f-45ec-993a-d5b41d407ea4" />

<img width="791" height="248" alt="image" src="https://github.com/user-attachments/assets/e489ca37-c5dc-48d2-8961-b83ef955fccd" />

---


# Düzgün Dağılım (Uniform Distribution) ve Üstel Dağılım (Exponential Distribution)

## Genel Bakış: İki Farklı Rastgelelik Hikayesi

Bu iki dağılımı, rastgele olayları anlatan iki farklı hikaye anlatıcısı gibi düşünebiliriz:

* **Düzgün Dağılım:** Bu anlatıcı, "Belirlenen sınırlar içinde her şey olabilir ve her sonucun şansı tamamen eşittir" der. Tam bir **eşitlik ve belirsizlik** hikayesidir.
* **Üstel Dağılım:** Bu anlatıcı ise, "Bir sonraki olayın *her an* olması muhtemeldir, ancak en çok *hemen şimdi* olması olasıdır" der. Bu, bir **bekleyiş ve aciliyet** hikayesidir.

---

### Bölüm 1: Düzgün Dağılım – "Adil Fırsatlar Dünyası"

Bu dağılım, en basit ve en öngörülemez rastgelelik türüdür.

* **Metafor:** Düzgün dağılımı, mükemmel bir şekilde karıştırılmış bir **tombala torbası** veya **kusursuz bir piyango makinesi** gibi düşünün. Belirli bir aralıktaki (örneğin 1'den 100'e kadar) her bir topun çekilme olasılığı kesinlikle aynıdır. 5 gelmesi ne kadar olasıysa, 95 gelmesi de o kadar olasıdır.

* **Ne Zaman Kullanılır?** Bir olayın belirli sınırlar ($a$ ve $b$) içinde gerçekleşeceğini bildiğiniz, ancak bu sınırlar içinde herhangi bir sonuca öncelik vermek için hiçbir nedeninizin olmadığı durumları modellemek için kullanılır.

* **Görsel Hikayesi (PDF Grafiği):** Grafiği bir **dikdörtgen** veya **düz bir platodur**. Bu platonun yüksekliği ($\frac{1}{b-a}$) tüm aralık boyunca sabittir. Bu, olasılığın aralığın her noktasına "adil" bir şekilde dağıtıldığı anlamına gelir.

* **Örnek Senaryo:** Bir bilgisayarın 0 ile 1 arasında rastgele bir sayı üretmesi. Veya bir otobüsün durağa saat 10:00 ile 10:10 arasında herhangi bir anda gelebileceğini ve bu aralıktaki her saniyenin eşit olasılıklı olduğunu varsaymak.

---

### Bölüm 2: Üstel Dağılım – "Her An Olabilir Dünyası"

Bu dağılım, olaylar arasındaki **bekleme süresini** modellemek için kullanılır ve Düzgün Dağılımın tam tersi bir mantığa sahiptir.

* **Metafor:** Üstel dağılımı, yoğun bir caddede **boş bir taksi beklemek** gibi düşünün. En olası senaryo, bir taksinin *hemen şimdi* veya çok kısa bir süre içinde geçmesidir. 5 dakika bekledikten sonra hala taksi geçmediyse, umudunuzu yitirmeye başlarsınız. 30 dakika sonra bir taksinin geçme olasılığı oldukça düşüktür.

* **Ne Zaman Kullanılır?** Olayların sabit bir ortalama oranda gerçekleştiği bir süreçte, bir sonraki olaya kadar geçecek süreyi modellemek için kullanılır.
    * Bir web sitesine bir sonraki kullanıcının gelmesine kadar geçecek süre.
    * Bir ampulün patlamasına kadar geçecek ömür.
    * Bir müşteri hizmetleri temsilcisinin bir sonraki çağrıyı almasına kadar geçen süre.

* **Görsel Hikayesi (PDF Grafiği):** Grafiği, yüksek bir noktadan başlayıp hızla aşağı inen bir **kaydırak** gibidir. En yüksek noktası sıfırdadır, çünkü bekleme süresinin kısa olma olasılığı en yüksektir. Bekleme süresi uzadıkça, olasılık (eğrinin yüksekliği) hızla sıfıra yaklaşır.

* **Anahtar Karakter: Lambda ($\lambda$):** Bu dağılımın kaderini **oran parametresi** olan Lambda ($\lambda$) belirler. $\lambda$, bir zaman biriminde olayın ne sıklıkla gerçekleştiğini gösterir.
    * **Yüksek $\lambda$:** Olaylar sık olur (örneğin, yoğun bir kafeye dakikada 3 müşteri gelir). Bekleme süresi kısadır, bu yüzden kaydırak **çok diktir**.
    * **Düşük $\lambda$:** Olaylar nadirdir (sakin bir kütüphaneye saatte 2 kişi gelir). Bekleme süresi uzundur, bu yüzden kaydırak **daha yatıktır**.

* **Hafızasızlık Özelliği (Memorylessness):** Bu, Üstel Dağılımın en ilginç ve karşı-sezgisel özelliğidir. "Geçmişin önemi yoktur" der.
    * **Örnek:** Ortalama ömrü 1000 saat olan bir ampul düşünün. Eğer bu ampul 800 saattir yanıyorsa, "yorulduğu" için yakında patlama olasılığının daha yüksek olduğunu düşünebilirsiniz. Ancak Üstel Dağılıma göre bu yanlıştır! Ampulün "hafızası" yoktur. 800 saattir yanıyor olması, önümüzdeki 100 saat daha yanma olasılığını, sıfır kilometre bir ampulün ilk 100 saat yanma olasılığından farklı kılmaz.
 
  #### Karşılaştırmalı Özet Tablosu

| Özellik | Düzgün Dağılım (Uniform) | Üstel Dağılım (Exponential) |
| :--- | :--- | :--- |
| **Metafor** | Adil Fırsatlar / Kusursuz Piyango | Her An Olabilir / Taksi Bekleme Oyunu |
| **Cevapladığı Soru** | "Bu aralıkta herhangi bir sonucun olasılığı nedir?" | "Bir sonraki olaya kadar ne kadar beklemem gerekecek?" |
| **PDF Grafiği** | **Dikdörtgen** (Olasılık sabit) | **Kaydırak** (Olasılık zamanla azalır) |
| **Ana Parametre(ler)**| Başlangıç ($a$) ve Bitiş ($b$) noktaları | Oran Parametresi ($\lambda$) |
| **Örnek Senaryo** | 0-100 arasında rastgele sayı seçimi. | Bir sonraki depreme kadar geçecek süre. |
| **Hafıza?** | Uygulanamaz | **Hafızasızdır** (Geçmiş, geleceği etkilemez) |

---
# TABLO INCELEME:

<img width="557" height="366" alt="image" src="https://github.com/user-attachments/assets/0cecf2e2-f287-4a3e-ba4f-6fcada79dba2" />

### Ana Metafor: Terzi ve Müşteri

Bu grafiğe bakarken kendinizi bir **terzi** olarak düşünün:

* **Histogram (Yeşil Çubuklar):** Bu, ölçülerini aldığınız **müşterinizdir**. Gerçek, canlı ve kendine özgü küçük pürüzleri olan veriyi temsil eder.
* **PDF Çizgisi (Kırmızı Çizgi):** Bu, müşterinize mükemmel uyacağını düşündüğünüz **elbise kalıbınızdır**. İdealize edilmiş, pürüzsüz ve matematiksel bir modeli temsil eder.

**Amacımız:** "Kalıp, müşteriye ne kadar iyi uyuyor?" sorusunu cevaplamaktır. Eğer uyum iyiyse, doğru modeli seçmişiz demektir.

---

### Grafiği Yorumlama Adımları

İşte bu grafiği analiz ederken izlemeniz gereken adımlar:

#### Adım 1: Hikayeyi Anlamak (Eksenleri Oku)

* **X Ekseni (Time Between Calls):** Ne ölçüyoruz? Müşteri hizmetlerine gelen iki arama arasındaki **bekleme süresini** (dakika cinsinden).
* **Y Ekseni (Density):** Bu "olasılık yoğunluğu" demektir. Basitçe, grafiğin bu noktasındaki yükseklik, o bekleme süresinin ne kadar yaygın olduğunu gösterir. Yükseklik ne kadar fazlaysa, o bekleme süresi o kadar sık görülür.

**İlk Gözlem:** Grafiğin en sol tarafı (0-2 dakika arası) en yüksek. Bu bize anında şunu söyler: **Kısa bekleme süreleri çok yaygın, uzun bekleme süreleri ise çok nadir.**

#### Adım 2: Gerçek Dünya ile Tanışmak (Histogram - Yeşil Çubuklar)

Bu yeşil çubuklar, sizin **gözlemlediğiniz gerçek verilerdir**. Belki de bir saat boyunca oturup iki arama arasındaki süreleri kronometreyle ölçtünüz ve bu sonuçları bir grafiğe döktünüz.

* **Nelere Dikkat Etmeli?**
    * Çubukların genel şekline bakın. En uzun çubuk solda mı? Evet.
    * Sağa doğru gittikçe çubukların boyu düzenli bir şekilde kısalıyor mu? Evet.
    * Bu şekil, "bir olayın hemen gerçekleşme olasılığı en yüksek, bekledikçe olasılık azalır" diyen **Üstel Dağılımın tipik parmak izidir.**

#### Adım 3: Teorik Modeli İncelemek (PDF - Kırmızı Çizgi)

Bu kırmızı çizgi, `scipy.stats.expon` gibi bir kütüphane kullanarak çizdiğimiz **idealize edilmiş matematiksel modeldir**. Bu, verilerimizin uyduğunu düşündüğümüz teorik "kaydırak" şeklidir.

* **Nelere Dikkat Etmeli?**
    * Lejantta $\lambda$ (Lambda) = 0.2 yazdığını görüyoruz. Bu, modelimizin "oran parametresidir". Bu bağlamda, **dakikada ortalama 0.2 arama** geldiği anlamına gelir.
    * Çizginin şekli, histogramın genel akışını takip ediyor mu? Evet, o da en yüksekten başlayıp hızla alçalıyor.

#### Adım 4: Büyük Karşılaşma (Model ve Veri Uyumu)

Şimdi en önemli kısma geldik: Terzinin kalıbı müşteriye uyuyor mu?

* Kırmızı çizgiye bakın. Yeşil çubukların tepelerinden yumuşak bir şekilde geçerek onların genel şeklini özetliyor mu? **Kesinlikle evet!**
* Bu, Üstel Dağılım modelinin, müşteri aramaları arasındaki süreyi açıklamak için **çok iyi bir seçim olduğunu** gösterir. Uyum mükemmel değil (çünkü gerçek dünya her zaman biraz "pürüzlüdür"), ama istatistiksel olarak çok güçlü bir uyum var.

#### Adım 5: Dedektiflik Zamanı (Sayısal İpuçları)

Grafiğin altındaki sayılar, bu uyumu doğrulayan son kanıtlardır.

* **Mean: 5.0 (Ortalama):** Gözlemlenen verilerde, iki arama arasındaki ortalama bekleme süresi **5 dakikadır**.
* **Lambda ($\lambda$) ile Bağlantı Kur:** Üstel dağılımın en önemli özelliklerinden biri şudur: $Ortalama = 1 / \lambda$.
    * Bizim modelimizde $\lambda=0.2$'ydi.
    * Hesaplayalım: $1 / 0.2 = 5$.
    * **Bu bir tesadüf değil!** Verilerimizin ortalaması (5.0), modelimizin parametresinden ($\lambda=0.2$) türetilen teorik ortalama ile birebir eşleşiyor. Bu, modelimizin doğruluğuna dair en güçlü kanıttır.
* **Variance: ~25.0 (Varyans):** Üstel dağılımda ikinci bir kural daha vardır: $Varyans = 1 / \lambda^2$.
    * Hesaplayalım: $1 / (0.2 * 0.2) = 1 / 0.04 = 25$.
    * Verilerimizin varyansı da teorik varyans ile eşleşiyor!

---

### Sonuç ve Yorum

> Bu grafiğe baktığımda şunları söylerdim:
> "Müşteri aramaları arasındaki bekleme sürelerini gösteren veri (histogram), teorik bir Üstel Dağılım (PDF çizgisi) ile çok güçlü bir uyum göstermektedir. Verinin ortalaması (5 dakika) ve varyansı (~25), modelin oran parametresi ($\lambda=0.2$) ile teorik olarak birebir tutarlıdır. Bu, müşteri gelişlerinin 'hafızasız' bir süreci takip ettiğini ve kısa bekleme sürelerinin çok daha yaygın olduğunu doğrulamaktadır."

---


<img width="521" height="332" alt="image" src="https://github.com/user-attachments/assets/5389365f-52e0-4dfd-956e-0330418d1906" />

### Ana Metafor: Partideki DJ ve Dans Eden Kalabalık

Bu grafiğe, bir partideki durum olarak bakalım:

* **Histogram (Mavi Çubuklar):** Bu, pistte **dans eden kalabalıktır**. İnsanların enerjisi anlık olarak değişir; bazı anlarda coşku artar (uzun çubuklar), bazı anlarda azalır (kısa çubuklar). Her zaman biraz kaotik ve pürüzlüdür.
* **PDF Çizgisi (Kırmızı Çizgi):** Bu, partide çalan elektronik bir şarkının **kusursuz ve sabit ritmidir (beat)**. Şarkı boyunca ritim hiç değişmez, hep aynı seviyededir.

**Amacımız:** "Dans eden kalabalığın genel enerjisi, şarkının sabit ritmine uyuyor mu?" sorusunu cevaplamaktır.

---

### Grafiği Yorumlama Adımları

İşte bu grafiği analiz ederken izlemeniz gereken adımlar:

#### Adım 1: Sahneyi Anlamak (Eksenleri ve Başlığı Oku)

* **Başlık (Uniform Distribution: Daily Temperature Modeling):** Günlük sıcaklık verilerini Düzgün Dağılım ile modellemeye çalıştığımızı anlıyoruz.
* **X Ekseni (Temperature °C):** Ölçtüğümüz şeyin 15°C ile 35°C arasındaki sıcaklık değerleri olduğunu görüyoruz.
* **Y Ekseni (Density):** Olasılık yoğunluğunu gösterir. Düzgün Dağılım için bu eksendeki en önemli nokta, teorik modelin (kırmızı çizgi) **düz** olmasıdır.

#### Adım 2: Gerçek Veriyi Gözlemlemek (Histogram - Mavi Çubuklar)

Bu mavi çubuklar, belirli bir zaman diliminde **kaydedilmiş gerçek günlük sıcaklık değerleridir**.

* **Nelere Dikkat Etmeli?**
    * **Dalgalanma:** Çubukların boyları birbiriyle aynı değil. Bazı sıcaklık değerleri (örneğin 16°C, 20°C, 30°C civarı) diğerlerinden daha sık gözlemlenmiş. Bu normaldir, çünkü gerçek dünya verileri her zaman "gürültülü" ve değişkendir. Kalabalığın enerjisinin anlık olarak değişmesi gibi.
    * **Genel Eğilim:** En önemli nokta budur. Çubuklarda belirgin bir **eğilim var mı?** Örneğin, sola veya sağa doğru sistematik bir yükselme veya alçalma var mı? Çan eğrisi gibi ortada bir tepe noktası oluşuyor mu? **Hayır**. Mavi çubuklar, tüm sıcaklık aralığına **belirgin bir tercih olmaksızın** yayılmış gibi görünüyor.

#### Adım 3: İdeal Modeli Tanımak (PDF - Kırmızı Çizgi)

Bu kırmızı çizgi, bizim **teorik varsayımımızdır**. Bu varsayım şudur: "15°C ile 35°C arasındaki herhangi bir sıcaklık değerinin gerçekleşme olasılığı birbirine eşittir."

* **Nelere Dikkat Etmeli?**
    * **Parametreler:** Lejantta `$a=15$` ve `$b=35$` yazdığını görüyoruz. Bunlar, modelimizin alt ve üst sınırlarıdır. Kırmızı çizgi tam olarak bu aralıkta düz bir şekilde uzanır.
    * **PDF Yüksekliği:** Düzgün dağılımda PDF'in yüksekliği her zaman `$1 / (b - a)$` formülüyle hesaplanır.
        * ```
          1 / (35 - 15) = 1 / 20 = 0.05
          ```
        * Grafiğe baktığımızda kırmızı çizginin Y ekseninde tam olarak **0.05** seviyesinde olduğunu görürüz. Bu, modelin doğru bir şekilde çizildiğini teyit eder.

#### Adım 4: Büyük Karşılaşma (Model ve Veri Uyumu)

Şimdi kritik soruyu soralım: Kalabalığın dansı (mavi çubuklar), şarkının sabit ritmine (kırmızı çizgi) uyuyor mu?

* **Gözlem:** Mavi çubuklar kırmızı çizginin etrafında dalgalanıyor. Bazen üstüne çıkıyor, bazen altına iniyor.
* **Yorum:** Bu mükemmel bir uyum değil, ancak Düzgün Dağılım için aradığımız şey de bu değil. Aradığımız şey, verinin **sistematik bir desene sahip olmamasıdır**. Kırmızı çizgi, mavi çubukların **ortalama seviyesini** oldukça iyi temsil ediyor. Veriler belirli bir yerde kümelenmiyor veya bir yöne doğru azalmıyor.
* **Sonuç:** Bu nedenle, bu sıcaklık verilerini Düzgün Dağılım ile modellemek **makul bir yaklaşımdır**. Bu model, "Bu aralıkta herhangi bir sıcaklık olabilir ve hiçbiri diğerinden daha olası değildir" şeklindeki ana fikri başarıyla yakalar.

---

### Sonuç ve Yorum

> "Gözlemlenen günlük sıcaklık verileri (histogram), 15°C ile 35°C arasında belirgin bir eğilim veya kümelenme göstermemektedir. Verilerdeki gürültü ve dalgalanmalara rağmen, herhangi bir sıcaklık değerinin diğerinden daha olası olduğuna dair bir kanıt yoktur. Bu nedenle, bu aralıktaki tüm sıcaklıkların eşit olasılıklı olduğunu varsayan Düzgün Dağılım modeli (PDF çizgisi), bu veri setinin genel davranışını açıklamak için **mantıklı ve basit bir model** olarak kabul edilebilir."

