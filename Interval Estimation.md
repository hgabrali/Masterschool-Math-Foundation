# Interval Estimation

[Interval Estimation](https://colab.research.google.com/drive/1r33eVIjJfdoKIWe4VWPDYn2at_P6C4Ls#scrollTo=MDRciGBbFy67) 


### Introduction

An **interval estimation** provides a range of values, instead of a single point, within which a population parameter is likely to fall. This range is typically constructed with a confidence level, such as 95% or 99%, which reflects the degree of certainty that the population parameter lies within the interval.

> 🎓 The most common form of interval estimate is the **confidence interval**.

---

### Confidence Interval

A **confidence interval (CI)** is a type of interval estimate that is used to estimate a population parameter (e.g., population mean, population proportion) based on sample data. A confidence interval provides both an estimated range and a level of confidence that the true population parameter lies within that range.

The general formula for a confidence interval for the population mean is:
$$
\text{CI} = \bar{x} \pm Z \frac{\sigma}{\sqrt{n}}
$$
Where:
* $\bar{x}$ is the sample mean.
* $Z$ is a value corresponding to the desired confidence level (e.g., for 95% confidence, $Z \approx 1.96$).
* $\sigma$ is the population standard deviation.
* $n$ is the sample size.

---

### Confidence Level

The **confidence level** represents the probability that the true population parameter lies within the confidence interval. Common confidence levels are:

* **90% confidence level:** There is a 90% chance that the true population parameter lies within the interval.
* **95% confidence level:** There is a 95% chance that the true population parameter lies within the interval.
* **99% confidence level:** There is a 99% chance that the true population parameter lies within the interval.

Higher confidence levels correspond to wider intervals, which means the interval is less precise but has a higher probability of containing the true population parameter.

This confidence level corresponds to the central area of the normal distribution. For a 95% confidence level, 95% of the distribution is contained within the interval, and the remaining 5% is divided equally between the two tails (2.5% in each tail).

> 🎓 To find the critical value (Z-score) corresponding to the confidence level, we use the Percent Point Function (PPF), which gives the Z-score for the desired cumulative probability. The formula for the Z-score is:
> $$
Z = \text{PPF}\left(\alpha + \frac{1-\alpha}{2}\right)
$$
> where $\alpha$ is the confidence level (e.g., 0.90, 0.95, or 0.99).



# Example of Confidence Interval for the Mean

<img width="792" height="600" alt="image" src="https://github.com/user-attachments/assets/b2b05528-d9cc-4509-a521-f49446d66e6a" />

### Problemin Amacı: Tahmini Bir Aralığa Dönüştürmek

**Senaryo basit:** Bir şehirdeki tüm yetişkin kadınların ortalama boyunu bilmek istiyoruz ama herkesi ölçemeyiz. Bunun yerine 100 kadından oluşan bir örneklem alıyoruz ve bu grubun ortalama boyunu **160 cm** buluyoruz.

**Temel Sorun:** Bu 160 cm'lik "nokta tahmini" ne kadar güvenilir? Gerçek ortalama tam olarak 160 cm olmayabilir. İşte **güven aralığı**, bu tekil tahmini, belirsizliği de hesaba katan daha dürüst ve kullanışlı bir aralığa dönüştürür.

> **Metafor:** 160 cm, bizim en iyi tahminimiz, yani bir hedefe attığımız tek bir ok. Güven aralığı ise bu okun etrafına çizdiğimiz ve "hedefin %95 ihtimalle bu çemberin içinde bir yerde olduğunu düşünüyoruz" dediğimiz bir **güven çemberidir**.

---

### Analiz ve Yorumlama Adımları

Görseldeki çözümün arkasındaki mantığı adım adım inceleyelim.

#### Adım 1: Delilleri Toplamak (Verilen Değerler)

Öncelikle elimizdeki bilgileri ve ne anlama geldiklerini netleştirelim:

* **Örneklem Ortalaması ($\bar{x}$) = 160 cm:** Bu bizim en iyi tekil tahminimiz, yani "okumuzun düştüğü yer".
* **Örneklem Boyutu ($n$) = 100:** Kanıtımızın gücü. 100 kişilik bir örneklem, 10 kişilik bir örneklemden çok daha güvenilirdir.
* **Popülasyon Standart Sapması ($\sigma$) = 8 cm:** Tüm şehirdeki kadınların boylarının genel olarak ne kadar değişken olduğunu gösteren bir değer. (Not: Genellikle bu değer bilinmez, ancak bu örnekte bilindiği varsayılmıştır).
* **Güven Seviyesi = %95:** Oluşturacağımız aralığın, popülasyonun gerçek ortalamasını içerme konusunda ne kadar "emin" olmak istediğimizi belirtir. Bu, çizeceğimiz "güven çemberinin" ne kadar büyük olacağını belirler.

#### Adım 2: Planı Oluşturmak (Formülün Anlamı)

Kullanılan formül şudur:
$$
CI = \bar{x} \pm Z \times \frac{\sigma}{\sqrt{n}}
$$
Bu formülü iki ana parçaya ayırabiliriz:

* **$\bar{x}$ (Nokta Tahmini):** Tahminimizin merkezi. (160 cm)
* **$Z \times \frac{\sigma}{\sqrt{n}}$ (Hata Payı - Margin of Error):** Güven çemberimizin yarıçapı.

Şimdi Hata Payı'nı daha detaylı inceleyelim:

* **$Z$ (Kritik Değer):** Bu, güven seviyemize bağlı olan bir "güven çarpanıdır". %95 güven için bu değer her zaman **1.96**'dır. Bu, "normal dağılımın ortasındaki %95'lik alanı yakalamak için merkezden 1.96 standart sapma kadar uzaklaşmalısın" anlamına gelir.
* **$\frac{\sigma}{\sqrt{n}}$ (Standart Hata - Standard Error):** Bu, tahminimizin ortalama "titreme payıdır". Örneklemimizin ne kadar güvenilir olduğunu gösterir.
    * **Hesaplama:** `$\frac{8}{\sqrt{100}} = \frac{8}{10} = 0.8$` cm.

#### Adım 3: Hesabı Yapmak

Artık tüm parçaları birleştirebiliriz:

1.  **Hata Payını Hesapla:**
    * `Hata Payı = 1.96 × 0.8 = 1.568` cm.
    * **Yorum:**
        > "%95 güvenle, 160 cm'lik örneklem ortalamamızın, şehirdeki kadınların gerçek ortalamasından en fazla **±1.568 cm** uzakta olduğunu tahmin ediyoruz."

2.  **Güven Aralığını Oluştur:**
    * **Alt Sınır:** `$160 - 1.568 = 158.432$` cm.
    * **Üst Sınır:** `$160 + 1.568 = 161.568$` cm.

---

### Nihai Sonuç ve Yorumu

**Sonuç:** `[158.432, 161.568]`

Bu aralığı yorumlamanın en doğru ve pratik yolu şudur:
> "Yaptığımız analize göre, örneklemimizden elde ettiğimiz verilere dayanarak, bu şehirdeki **tüm yetişkin kadınların gerçek boy ortalamasının %95 güvenle 158.43 cm ile 161.57 cm arasında** bir yerde olduğunu tahmin ediyoruz."

* **Daha Teknik Anlamı:** Bu, kullandığımız **yöntemin güvenilirliğini** ifade eder. Eğer bu deneyi (100 kişilik örneklem almayı) defalarca tekrarlasaydık, bu şekilde oluşturacağımız güven aralıklarının **yaklaşık %95'i**, popülasyonun bilinmeyen gerçek ortalamasını içinde barındırırdı.

Bu sonuç, tek bir sayı olan 160 cm'den çok daha değerlidir çünkü tahminimizdeki doğal belirsizliği de hesaba katar.

--- 

## Margin of Error

<img width="687" height="270" alt="image" src="https://github.com/user-attachments/assets/1827253a-08cc-41bd-bc67-3eb216425742" />


---

Bu üç kavram, istatistiksel çıkarımın temel taşlarıdır ve genellikle birbirine karıştırılır:
* Güven Seviyesi (Confidence Level) – Balıkçının Ustalık Seviyesi
* Hata Payı (Margin of Error) – Ağın Büyüklü
* Güven Aralığı (Confidence Interval) – Suya Atılmış Ağ

---

### Ana Metafor: Göldeki Gizemli Balık

Uçsuz bucaksız bir gölde ( **popülasyon** ) yaşayan ve tam yerini bilmediğimiz efsanevi, büyük bir balığın ( **popülasyonun gerçek ortalaması, $\mu$** ) peşinde olan bir balıkçı olduğunuzu hayal edin. Bütün gölü taramak imkansız olduğu için, balığın nerede olabileceğini tahmin etmeniz gerekiyor.

Bir anlığına suyun üzerinde bir hareketlenme görüyorsunuz (bu sizin **örneklem ortalamanız, $\bar{x}$** ). Bu sizin en iyi ipucunuz, yani **nokta tahmininiz**. Ama bilirsiniz ki balık tam olarak orada olmayabilir, o hareketin biraz uzağında olabilir.

İşte bu noktada, tek bir noktaya olta atmak yerine, daha mantıklı bir şey yaparsınız: **ağ atmak**.

---

### 1. Güven Seviyesi (Confidence Level) – Balıkçının Ustalık Seviyesi

* **Nedir?** Genellikle yüzde olarak ifade edilen (90%, 95%, 99%) bir **yöntem güvenilirliği** ölçüsüdür.
* **Ne İşe Yarar?** Tahmin yapma sürecimizin (ağ atma tekniğimizin) uzun vadede ne kadar başarılı olacağını belirtir.
* **Bize Ne Anlatır?**
    * **Metafor:** Güven Seviyesi, sizin **balıkçı olarak ustalığınızı** temsil eder. %95'lik bir güven seviyesi seçmek, "Benim kullandığım bu ağ atma tekniği o kadar iyi ki, bu gölde 100 farklı noktaya ağ atsam, bunların 95'inde efsanevi balığı ağın içinde yakalarım" demektir.
* **Nasıl Yorumlanır? (En Önemli Nokta)**
    * **YANLIŞ YORUM:**
        > "Balığın şu an attığım ağın içinde olma olasılığı %95'tir."
    * **DOĞRU YORUM:**
        > "Bu aralığı oluşturmak için kullandığım **yönteme %95 güveniyorum**." Güven, tek bir sonuca değil, **sürecin kendisine** duyulan güvendir.

---

### 2. Hata Payı (Margin of Error) – Ağın Büyüklüğü

* **Nedir?** Nokta tahmininize (örneklem ortalamasına) ekleyip çıkardığınız ve güven aralığınızın sınırlarını belirleyen **sayısal bir değerdir** (örn: ±5 cm).
* **Ne İşe Yarar?** Tahminimizdeki belirsizliğin miktarını belirler. Güven aralığının "yarıçapıdır".
* **Bize Ne Anlatır?**
    * **Metafor:** Hata Payı, kullanacağınız **ağın ne kadar büyük olduğunu** söyler.
        * **Küçük Hata Payı:** Küçük ve hassas bir ağ. Tahmininiz daha keskindir ama balığı kaçırma riskiniz biraz daha fazladır.
        * **Büyük Hata Payı:** Geniş ve büyük bir ağ. Tahmininiz daha az keskindir ama balığı yakalama konusunda kendinize daha çok güvenirsiniz.
* **Nelerden Etkilenir?**
    * **Güven Seviyesi:** Daha usta bir balıkçı (%99 güven) balığı kaçırmamak için daha **büyük bir ağ** (daha büyük hata payı) kullanır.
    * **Örneklem Boyutu:** Elinizde ne kadar çok ipucu varsa (büyük örneklem, `$n$`), o kadar **küçük bir ağa** (daha küçük hata payı) ihtiyaç duyarsınız.
    * **Verinin Değişkenliği:** Göldeki balık çok hareketliyse (yüksek standart sapma), onu yakalamak için daha **büyük bir ağ** gerekir.

---

### 3. Güven Aralığı (Confidence Interval) – Suya Atılmış Ağ

* **Nedir?** Bir alt ve bir üst sınırdan oluşan **değer aralığıdır** (örn: [155 cm, 165 cm]).
* **Ne İşe Yarar?** Popülasyonun bilinmeyen gerçek parametresi için en olası aralığı tahmin eder.
* **Bize Ne Anlatır?**
    * **Metafor:** Güven Aralığı, balığı gördüğünüz yerin (nokta tahmini) etrafına **atmış olduğunuz ağın ta kendisidir**. Ağın merkezi sizin ilk ipucunuzdur (örneklem ortalaması), kenarları ise hata payı tarafından belirlenir.
* **Nasıl Yorumlanır?**
    * **Formül:** `Güven Aralığı = Nokta Tahmini ± Hata Payı`
    * **Pratik Yorum:**
        > "Elimdeki verilere ve %95 güven seviyesine dayanarak, göldeki efsanevi balığın (popülasyon ortalamasının) gerçek boyunun **155 cm ile 165 cm arasında** bir yerde olduğunu tahmin ediyorum."

---

### Özetle Birlikte Nasıl Çalışırlar?

1.  Önce **ustalık seviyenize** karar verirsiniz (**Güven Seviyesi**, örn: %95).
2.  Bu ustalık seviyesi ve elinizdeki ipuçları (veri), ne kadar **büyük bir ağa** ihtiyacınız olduğunu belirler (**Hata Payı**).
3.  Balığı gördüğünüz noktanın (nokta tahmini) etrafına bu ağı atarsınız ve bu sizin **Güven Aralığınız** olur.

* Bu üçlü, bize tek bir "kuru" tahminden çok daha fazlasını sunar: Hem bir tahmin aralığı verir hem de bu aralığı oluşturan yönteme ne kadar güvenebileceğimizi söyleyerek tahminimizdeki **belirsizliği yönetmemizi** sağlar.


#### Güven Aralığı Kavramları Karşılaştırma Tablosu

| Kavram | Nedir? | Metafordaki Karşılığı | Ne İşe Yarar? | Bize Ne Anlatır? |
| :--- | :--- | :--- | :--- | :--- |
| **Güven Seviyesi** | Bir yüzde değeri (örn: %95) | **Balıkçının Ustalık Seviyesi** | Tahmin yapma yönteminin uzun vadedeki başarısını ve güvenilirliğini belirler. | "Bu yönteme ne kadar güvenebilirim?" sorusunu cevaplar. |
| **Hata Payı** | Tek bir sayısal değer (örn: ±5 cm) | **Ağın Büyüklüğü (Yarıçapı)** | Güven aralığının genişliğini belirleyerek tahminin hassasiyetini ölçer. | "Tahminimin 'oynama payı' ne kadar?" sorusunu cevaplar. |
| **Güven Aralığı** | Bir değer aralığı (örn: [155cm, 165cm]) | **Suya Atılmış Ağın Kendisi** | Popülasyon parametresi için olası değerlerin bulunduğu nihai tahmini sunar. | "Gerçek değer muhtemelen nerede?" sorusunu cevaplar. |



---

### Çıktının Detaylı Yorumlanması

Çıktının her bir parçasının ne anlama geldiğini ve nasıl yorumlanması gerektiğini açıklayalım.

> **Senaryoyu Hatırlayalım:** 200 kişilik bir örneklemin aylık ortalama harcamasını 1000$ bulduk. Tüm popülasyonun (örneğin tüm şehrin) gerçek ortalama harcamasını tahmin etmeye çalışıyoruz. Bu çıktı, bu tahminin etrafına ördüğümüz **"güvenlik ağının"** bir özetidir.

---

#### 1. `Z-score for 90% confidence: 1.6449`

* **Teknik Anlamı:** Bu, %90'lık bir güven seviyesine karşılık gelen **kritik Z-değeridir**. Normal dağılım eğrisinin tam ortasındaki %90'lık alanı yakalamak için, merkezden (ortalamadan) her iki yöne doğru **1.645 standart sapma** gitmemiz gerektiğini söyler.
* **Pratik Yorumu:** Bu bizim "**güven çarpanımızdır**". Tahminimizin etrafına ne kadar geniş bir güvenlik ağı öreceğimizi belirleyen standart bir sayıdır. Güven seviyemizi %95'e çıkarsaydık, bu Z-skoru (ve dolayısıyla ağın genişliği) artacaktı.

#### 2. `Margin of Error: 29.08`

* **Teknik Anlamı:** Bu, **hata payıdır**. Örneklem ortalamamızın, gerçek popülasyon ortalamasından ne kadar uzakta olabileceğini tahmin eden değerdir. (`Z-skoru × Standart Hata` formülüyle hesaplanır).
* **Pratik Yorumu:** Bu, tahminimizin "**artı veya eksi (±)**" kısmıdır. Yaptığımız en iyi tahmin 1000$'dır, ancak bu tahminin **±29.08$** kadar "titreme payı" veya "oynama payı" olduğunu kabul ediyoruz. Bu belirsizlik, tüm popülasyon yerine sadece bir örneklemle çalışmaktan kaynaklanır.

#### 3. `The 90% confidence interval is: [970.92, 1029.08]`

Bu, tüm analizin **nihai sonucudur** ve en önemli kısmıdır.

* **Teknik Anlamı:** Bu, örneklem ortalamasının etrafına hata payının eklenmesi ve çıkarılmasıyla (`1000 ± 29.08`) oluşturulan **güven aralığıdır**.
* **Pratik Yorumu (En Önemli):** Bu sonucu yorumlamanın doğru yolu şudur:
    > "Elimizdeki 200 kişilik örnekleme dayanarak, bu popülasyondaki (örneğin şehirdeki) tüm insanların **gerçek ortalama aylık harcamasının %90 güvenle 970.92$ ile 1029.08$ arasında** bir yerde olduğundan oldukça eminiz."
* **Daha derin bir anlamda ise:** Bu, kullandığımız **yöntemin güvenilirliğini** ifade eder. Eğer bu deneyi (200 kişilik örneklem almayı) defalarca tekrarlasaydık, bu şekilde oluşturacağımız güven aralıklarının **yaklaşık %90'ı**, popülasyonun bilinmeyen gerçek ortalamasını içinde barındıracaktı.

---

### Özetle

Tek bir sayı (`1000$`) vermek yerine bir aralık (`[970.92, 1029.08]`) vermek, istatistiksel olarak çok daha dürüst ve bilgilendiricidir. Çünkü bu aralık, örneklemden kaynaklanan doğal belirsizliği de hesaba katar ve karar vericilere tahminimizin ne kadar sağlam olduğu hakkında bir fikir verir.

---

## Confidence Level Grafik Yorumu: 

<img width="1050" height="726" alt="image" src="https://github.com/user-attachments/assets/e5bdbd8a-6766-42cf-9fbd-e940d294b280" />

Bu grafik, istatistikteki en temel ve en kullanışlı kurallardan biri olan **Ampirik Kural (68-95-99.7 Kuralı)**'nı göstermektedir ve **Güven Seviyesi (Confidence Level)** kavramının görsel temelini oluşturur.

Gelin bu grafiği, güven seviyesi bağlamında detaylı bir şekilde, metaforlar kullanarak yorumlayalım.

---

### Ana Metafor: Okçuluk Hedefi

Bu normal dağılım eğrisini bir **okçuluk hedefi** gibi düşünelim:

* **Hedefin Merkezi (Tam İsabet):** Grafiğin ortası, yani ortalama ($\mu$).
* **Halkalar:** Merkezden dışarı doğru her bir çizgi, 1 standart sapma ($\sigma$) uzaklığı temsil eder.
* **Yüzdeler:** Attığınız okun, hedefin belirli bir halkasının içine düşme olasılığını gösterir.

Bu metaforla, grafiğin güven seviyesi açısından ne anlama geldiğini inceleyelim.

---

### Grafiğin Detaylı Yorumu

Bu grafik, bir tahminin etrafına ne kadar geniş bir "güvenlik ağı" (güven aralığı) örersek, o ağın "doğru" olma (yani popülasyonun gerçek değerini içerme) olasılığının ne kadar artacağını gösterir.

#### Seviye 1: 68.26% Güven Seviyesi (±1 Standart Sapma)

* **Grafikteki Anlamı:** Veri noktalarının yaklaşık **%68'i**, ortalamanın ±1 standart sapma aralığında yer alır. Yeşil ile gösterilen merkezdeki en büyük alandır.
* **Güven Seviyesi Olarak Yorumu:** Eğer örneklem ortalamamızın etrafına ±1 standart sapma genişliğinde bir güven aralığı oluşturursak, bu aralığın popülasyonun gerçek ortalamasını içerme konusunda **%68.26 oranında kendimize güvenebiliriz**.
* **Okçuluk Metaforu:**
    > "Attığım okların yaklaşık %68'i, hedef tahtasının tam merkezini çevreleyen ilk halkanın içine düşer." Bu fena bir başlangıç değildir, ancak ~%32'lik bir ıskalama payı profesyonel uygulamalar için genellikle çok yüksektir.

#### Seviye 2: 95.44% Güven Seviyesi (±2 Standart Sapma) - **EN YAYGIN SEVİYE**

* **Grafikteki Anlamı:** Veri noktalarının yaklaşık **%95'i**, ortalamanın ±2 standart sapma aralığında yer alır. (Yeşil + her iki yandaki 13.59%'luk alanlar).
* **Güven Seviyesi Olarak Yorumu:** Güvenlik ağımızı ±2 standart sapma genişliğine çıkardığımızda, bu aralığın popülasyonun gerçek ortalamasını içerme konusundaki güvenimiz **%95.44'e fırlar**. İstatistikte en yaygın kullanılan **%95 güven seviyesi** standardı buradan gelir. (Hesaplamalarda daha hassas olması için genellikle 1.96 standart sapma kullanılır, bu da 2'ye çok yakındır).
* **Okçuluk Metaforu:**
    > "Attığım okların %95'inden fazlası, hedef merkezini çevreleyen ilk iki halkanın içine düşer." Bu, istatistiksel olarak bir sonuca "güvenmek" için kabul edilen altın standarttır.

#### Seviye 3: 99.72% Güven Seviyesi (±3 Standart Sapma)

* **Grafikteki Anlamı:** Veri noktalarının neredeyse tamamı, yani **%99.7'si**, ortalamanın ±3 standart sapma aralığında yer alır.
* **Güven Seviyesi Olarak Yorumu:** Neredeyse mutlak bir kesinlik istediğimizde, aralığımızı ±3 standart sapma genişliğinde oluştururuz. Bu durumda, aralığımızın gerçek ortalamayı içerme konusunda **%99.72 oranında kendimize güvenebiliriz**.
* **Okçuluk Metaforu:**
    > "Attığım okların neredeyse hiçbiri hedef tahtasının üçüncü halkasından daha uzağa düşmez." Bu, imalat (Six Sigma) veya parçacık fiziği gibi hataların maliyetinin çok yüksek olduğu alanlarda aranan bir güven düzeyidir.

---

### Özet ve Ana Fikir: Güven ve Hassasiyet Dengesi

Bu grafik bize istatistikteki en temel ödünleşmeyi (trade-off) gösterir: **Güven vs. Hassasiyet**.

| Güven Seviyesi | Aralık Genişliği | Yorum (Okçuluk Metaforu) |
| :--- | :--- | :--- |
| **~68%** | Dar (±1σ) | Hedefe yakın ama ıskalama riski var. (**Hassas ama daha az güvenilir**). |
| **~95%** | Orta (±2σ) | Hedefi yakalama olasılığı yüksek, iyi bir denge. (**Dengeli**). |
| **~99.7%** | Geniş (±3σ) | Hedefi neredeyse kesin yakalar ama çok geniş bir alanı tarar. (**Çok güvenilir ama daha az hassas**). |

* Sonuç olarak bu grafik, bir tahmin yaparken seçtiğimiz güven seviyesinin, sonucumuzu ifade edeceğimiz aralığın genişliğini nasıl doğrudan etkilediğini gösteren görsel bir haritadır.
* Ne kadar çok güvenmek isterseniz, o kadar geniş bir aralık vermek zorunda kalırsınız.

--- 
## Percent Point Function - PPF ( Z- Skorleri) Yorumu:

<img width="675" height="352" alt="image" src="https://github.com/user-attachments/assets/6a893451-0544-4cb0-877a-3495b4add876" />

Bu grafik ve formül, bir önceki "Ampirik Kural" grafiğindeki genel yaklaşımdan (%95 için kabaca ±2 standart sapma gibi) çok daha hassas bir adıma geçmemizi sağlıyor. Bu, herhangi bir güven seviyesi için gereken **kritik Z-skorunu** tam olarak nasıl bulacağımızın tarifidir.

---

### Ana Fikir: Güven Aralığının Sınırlarını Belirlemek

> **Metafor:** Bir önceki "okçuluk hedefi" metaforumuzu hatırlayalım. Ampirik Kural bize kabaca "ilk halkanın", "ikinci halkanın" nerede olduğunu söylüyordu. Bu grafik ve formül ise bize, örneğin "%90'lık isabet bölgesi"nin bittiği o **keskin çizgiyi** tam olarak nasıl çizeceğimizi gösteren bir harita ve pergel görevi görür.

---

### Grafiğin Detaylı Yorumu

Bu normal dağılım grafiği, bir güven aralığının anatomisini gösterir:

* **`$1 - \alpha$` (Kırmızı Alan - Güven Bölgesi):** Bu, bizim **Güven Seviyemizdir**. Eğer %95 güvenle çalışıyorsak, bu kırmızı alan tüm dağılımın %95'ini temsil eder. Bu, tahminimizin içine düşmesini umduğumuz "başarı" bölgesidir.
* **`$\alpha$` (Beyaz Alanlar Toplamı - Risk Bölgesi):** Eğer ortadaki alan `$1 - \alpha$` ise, geriye kalan toplam alan `$\alpha$`'dır. Bu `$\alpha$` değerine **anlamlılık düzeyi (significance level)** denir ve bizim göze aldığımız toplam **hata riskini** temsil eder. %95 güvende, riskimiz `$\alpha = 1 - 0.95 = 0.05$`'tir (%5).
* **`$\alpha / 2$` (Kuyruklar - Hata Payları):** Normal dağılım simetrik olduğu için, toplam %5'lik riski iki uca eşit olarak paylaştırırız. Bu, sağdaki ve soldaki beyaz "kuyruk" alanlarının her birinin **%2.5 (`$\alpha/2$`)** olduğu anlamına gelir. Bu kuyruklar, aralığımızın dışında kalan "ıskalama" bölgeleridir.

> **Özetle grafik bize der ki:** "%95'lik bir güven aralığı oluşturmak için, dağılımın en soldaki %2.5'lik ve en sağdaki %2.5'lik kısımlarını dışarıda bırakıp, ortadaki %95'lik dilimi almalısın."

---

### Formülün Yorumu: PPF ile Sınırları Çizmek

Grafikteki o sınır çizgilerini (kritik Z-skorlarını) bulmak için **Yüzde Noktası Fonksiyonu (Percent Point Function - PPF)** kullanılır.

* **PPF Nedir?** PPF, bir "ters harita" gibidir. Ona bir alan (olasılık) verirsiniz, o size o alanın bittiği yerdeki Z-skorunu söyler. Python'da bu `scipy.stats.norm.ppf()` fonksiyonudur.
* **Formül:**
    $$
    Z = \text{PPF}\left(1 - \frac{1-\alpha}{2}\right)
    $$
Bu formül ilk bakışta karmaşık görünebilir ama aslında grafiği okumaktan başka bir şey değildir. Gelin %95 güven seviyesi (`$\alpha = 0.95$`) için adım adım uygulayalım:

1.  **`$(1 - \alpha)$`:** Toplam hata payını bul. `$1 - 0.95 = 0.05$` (%5).
2.  **`(1 - \alpha) / 2`:** Tek bir kuyruktaki hata payını bul. `$0.05 / 2 = 0.025$` (%2.5). Bu, sağ kuyruğun alanıdır.
3.  **`1 - (...)`:** PPF fonksiyonu soldan sağa doğru alanları okur. Biz sağdaki sınır çizgisini aradığımıza göre, o çizginin *solunda kalan toplam alanı* bulmamız gerekir. Bu da `Tüm Alan (1) - Sağ Kuyruk Alanı (0.025)` demektir. `$1 - 0.025 = 0.975$` (%97.5).
4.  **`PPF(0.975)`:** Fonksiyona soruyoruz: "Dağılımın en solundan başlayıp alanın %97.5'ini taradığımda hangi Z-skoruna ulaşırım?"
    * **Cevap: 1.96.**

İşte meşhur **%95 güven için Z=1.96** değerinin nereden geldiğinin matematiksel açıklaması budur.

---

### Özetle

Bu görsel, bize herhangi bir güven seviyesi için Hata Payı'nı hesaplarken kullanmamız gereken **kritik Z-değerini bulmanın evrensel yöntemini** öğretir. Bu yöntem sayesinde, sadece %68, %95 gibi genel kurallara bağlı kalmak yerine, %88 veya %97 gibi herhangi bir özel güven seviyesi için de hassas istatistiksel analizler yapabiliriz.


