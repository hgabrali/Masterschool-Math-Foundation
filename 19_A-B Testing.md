# A-B Testing

<img width="691" height="446" alt="image" src="https://github.com/user-attachments/assets/e9b74dc1-c18a-46b7-a566-1b709c668764" />


<img width="1243" height="664" alt="image" src="https://github.com/user-attachments/assets/818a30ec-25d8-4e63-be44-c435ee83c326" />


<img width="1098" height="587" alt="image" src="https://github.com/user-attachments/assets/57ead862-52da-44d5-95f2-244c10cce46d" />


# Dijital Optimizasyonda Deneysel Çerçeve: A/B Testleri, Çok Değişkenli Test (MVT) ve Çok Kollu Haydut (MAB) Algoritmalarının Stratejik ve Teknik Analizi

---

## Bölüm I: Giriş ve Deneysel Tasarımın Temelleri

### 1.1. Tanım ve Kapsam: A/B Testi (Split Testing) Nedir?

**A/B Testi (Split Testing veya Bölünmüş Sınama)**, iki veya daha fazla dijital deneyimin (varyasyon/Variation) belirlenmiş bir hedef metrik (örn. Dönüşüm Oranı/Conversion Rate, Tıklama Oranı/Click-Through Rate - CTR) üzerindeki etkisini bilimsel olarak karşılaştırmak amacıyla canlı kullanıcı trafiği kullanılarak gerçekleştirilen **randomize kontrollü deney (Randomized Controlled Trial - RCT)** yöntemidir. Bu metodoloji, kuruluşların tasarım, içerik veya metin gibi öğeleri sistematik olarak değiştirerek, hedef kitlelerinde en çok neyin yankı uyandırdığına ve arzu edilen sonuçlara yol açtığına dair değerli bilgiler edinmelerini sağlar.

Bir A/B testinin temel bileşenleri, mevcut sürümün sunulduğu **Kontrol Grubu (Control/A)** ve değiştirilmiş sürümün sunulduğu **Deney Grubu (Treatment/B)** arasındaki rastgele atama (*Random Assignment*) ve performans metriklerinin ölçülmesidir.

### 1.2. Hipotez Kurulumu ve Etik Çerçeve

Her deneysel süreç, ölçülebilir hedefleri, beklenen etkiyi ve metrik değişimlerini tanımlayan net, kanıta dayalı bir hipotezle başlamalıdır; bu genellikle **SMART (Specific, Measurable, Achievable, Relevant, Time-bound)** çerçevesine uygun olarak formüle edilir. Testin ardından elde edilen sonuç, ya başlangıçtaki hipotezi doğrular ya da hipoteze aykırı çıkar. Başarısız olan testler bile, neyin işe yaramadığına dair kritik bilgiler sunar.

Optimizasyon programlarında etik hususlara öncelik vermek hayati önem taşır. Testlerin amacı, kullanıcıları istismar etmek veya yanıltıcı (*Misleading*) yollarla manipüle etmek değil, **kullanıcı deneyimini (UX) sürekli iyileştirmektir**.

---

## Bölüm II: Deneysel Tasarımın Tarihsel Evrimi (Kronoloji)

### 2.1. İstatistiksel Temeller ve Erken Uygulamalar

A/B testlerinin istatistiksel geçerliliğinin temelini, 1920'lerde modern istatistiğin babası **Ronald A. Fisher** attı. Fisher, özellikle tarımsal deneyler bağlamında, **Varyans Analizi (Analysis of Variance - ANOVA)** ve randomize etme prensiplerini geliştirerek, dijital ortamdaki kontrollü deneylerin **nedensellik (Causality)** temelini oluşturdu.

### 2.2. Dijital Testlerin Doğuşu ve Kurumsallaşması

Dijital A/B testlerinin dönüm noktası, **2000 yılında Google’ın** arama sonuçları sayfasında gösterilen optimal sonuç sayısını belirlemek amacıyla gerçekleştirdiği ilk test oldu. Bu, çevrimiçi dönüşüm oranı optimizasyonu (CRO) çağının başlangıcını işaret etti.

**2007-2012:** Amazon, Microsoft (Bing) ve diğer büyük teknoloji şirketleri, binlerce A/B testi yapmayı yaygınlaştırdı ve otomatik deney altyapıları (*Automated Experimentation Infrastructures*) geliştirdi.

### 2.3. Kronolojik Gelişim ve Gelişmiş Optimizasyon Yaklaşımları (2013-Günümüz)

**2013-2017:** Netflix, LinkedIn ve Booking.com gibi şirketler, yüksek deney hızı (*Experiment Velocity*) ve karmaşık metrik çerçevelerine odaklanarak test süreçlerini ölçeklendirdi.

**2018 ve Sonrası:** Odak noktası, deneylerin verimliliğini artırmak ve istatistiksel önyargıyı (*Bias Mitigation*) azaltmak oldu. Bu dönemde:
* **CUPED (Controlled-experiment Using Pre-Experiment Data):** Deney öncesi verileri kullanarak varyansı azaltma ve test süresini kısaltma teknikleri benimsendi.
* **MAB (Multi-Armed Bandit):** Kümülatif ödülü maksimize etmeye odaklanan algoritmik yaklaşımlar popülerleşti.

Tarihsel ilerleme, teknoloji şirketlerinin test süresi boyunca kaybedilen potansiyel kazanç maliyetini (**Opportunity Cost/Regret**) minimize etmeye odaklandığını göstermektedir. Geleneksel A/B testleri, keşif aşamasında zayıf varyasyonlara eşit trafik tahsis ederek kaynak israfına yol açar. Çok Kollu Haydut (MAB) algoritmalarının yaygınlaşması, bu pişmanlık maliyetini azaltma arayışının doğrudan bir sonucudur.

---

## Bölüm III: İstatistiksel Temeller ve Metodolojik Zorluklar

### 3.1. İstatistiksel Anlamlılık ve Örneklem Büyüklüğü

A/B testinin temel amacı, gözlemlenen sonucun rastgele şans (*Random Chance*) eseri değil, test edilen değişikliğin bir sonucu olduğunu istatistiksel olarak kanıtlamaktır. Bu süreçte iki ana risk yönetilir:
* **Tip I Hata ($\alpha$):** Yanlış pozitif (bir fark yokken varmış gibi kabul etmek). Endüstri standardı genellikle %5.
* **Tip II Hata ($\beta$):** Yanlış negatif (gerçek bir farkı tespit edememek). Güç (*Power*) metriği (%80 hedeflenir) ile kontrol edilir.

Gerekli **Örneklem Büyüklüğünün (Sample Size)** hesaplanması kritiktir. En belirleyici faktör, **Tespit Edilebilir Minimum Etki (Minimum Detectable Effect - MDE)** olarak adlandırılan, analistin tespit etmeyi arzuladığı en küçük yüzdesel değişimdir. İstatistik teorisine göre, gerekli örneklem büyüklüğü ($N$), MDE’nin karesiyle ters orantılıdır ($N \propto 1/MDE^2$).

### 3.2. Kritik Metodolojik Hatalar

A/B test sonuçlarının güvenilirliğini tehdit eden yaygın hatalar:
* **Testi Erken Durdurma (Early Stopping):** İstatistiksel anlamlılık eşiğine erken ulaşılması durumunda testin hemen durdurulması, Tip I Hata riskini önemli ölçüde artırır.
* **Yetersiz Örneklem Büyüklüğü:** Tip II Hata riskini yükseltir.
* **Segmentasyon İhmali:** Farklı kullanıcı segmentlerinin (*User Segments*) varyasyonlara nasıl tepki verdiğine dair içgörüleri gözden kaçırmaya neden olur.

Optimizely’nin Sekansiyel Olasılık Oranı Testi (*Sequential Likelihood Ratio Test*) gibi modern metodolojiler, gerekli güvenilirlik seviyesini korurken test süresini esnekleştirerek ticari baskı ile bilimsel gereklilik arasındaki dengeyi sağlamayı amaçlar.

---

## Bölüm IV: Çoklu Değişkenli Deney Yaklaşımları: A/B/N ve MVT

### 4.1. A/B/N Testi

İkiden fazla varyasyonun (A, B, C, N...) aynı anda karşılaştırılmasıdır. Genellikle tek bir öğenin (örneğin, beş farklı Eylem Çağrısı/Call to Action - CTA metni) en iyi seviyesini bulmak için kullanılır. Varyasyon sayısının artması, her varyasyon için istatistiksel anlamlılığa ulaşma süresini uzatır.

### 4.2. Çok Değişkenli Test (Multivariate Testing - MVT)

Bir web sayfasındaki birden fazla bağımsız öğenin (**Faktörler/Factors** veya Konumlar/Locations) farklı içerik seçeneklerinin (**Seviyeler/Levels** veya İçerik Varyasyonları) **tüm olası kombinasyonlarını** (*Combinations*) aynı anda test etme yöntemidir.

* **Faktöriyel Yapı:** Örneğin, 3 farklı başlık, 2 farklı gövde metni ve 2 farklı bilgi formu test edilirse, toplam $3 \times 2 \times 2 = 12$ farklı varyasyon oluşturulur.
* **Üstünlüğü:** Öğeler arasındaki **etkileşimi (Element Interaction)** ölçebilme yeteneği.
* **Kısıtlaması:** Gerektirdiği yüksek trafik hacmi. Varyasyon sayısının çarpımsal olarak artması, A/B testine göre çok daha fazla kullanıcı trafiği gerektirir. Bu nedenle düşük trafikli siteler için pratik değildir.

### 4.3. MVT ve A/B Testinin Stratejik Kullanımı

MVT ve A/B testleri birbirini tamamlayan yöntemlerdir. Stratejik kullanım genellikle iki aşamadan oluşur:
1.  **Geniş Keşif (MVT):** Bir sayfadaki hangi öğelerin hedeflere ulaşmak için en önemli olduğunu belirler.
2.  **Rafinasyon (A/B):** MVT ile en etkili olduğu tespit edilen öğe üzerinde daha sonra odaklanmış A/B testleri yürütülür.

---

## Bölüm V: Dinamik Optimizasyon: Çok Kollu Haydut (Multi-Armed Bandit - MAB) Algoritmaları

### 5.1. MAB Algoritması ve Keşif-Sömürü İkilemi

**Çok Kollu Haydut (Multi-Armed Bandit - MAB) algoritması**, pekiştirmeli öğrenme (*Reinforcement Learning*) tabanlı bir optimizasyon tekniğidir. Geleneksel A/B testinin amacı istatistiksel kesinlik yoluyla öğrenmek iken, MAB’ın temel amacı, test süresi boyunca **kümülatif ödülü (Cumulative Reward) maksimize etmektir.**

Algoritmanın kalbinde, yeni seçenekleri deneme (**Keşif/Exploration**) ve performansı kanıtlanmış seçenekleri çoğunlukla sunmaya (**Sömürü/Exploitation**) devam etme ikilemi yatar.

### 5.2. Dinamik Trafik Tahsisi Mekanizması

MAB, makine öğrenimi kullanarak test sırasında toplanan verilerden öğrenir ve **daha iyi performans gösteren varyasyonlar lehine ziyaretçi tahsisini dinamik olarak artırır.** Zayıf performans gösteren varyasyonlara trafik tahsisi zamanla giderek azalır. Bu dinamik yaklaşım, zayıf seçeneklere kaynak harcama maliyetini (*regret*) minimize ederek testin genel verimliliğini artırır.

### 5.3. MAB vs. Geleneksel A/B Testi: Kritik Karşılaştırma

| Özellik (Feature) | A/B Testi | Çok Kollu Haydut (MAB) |
| :--- | :--- | :--- |
| **Temel Amaç** | İstatistiksel olarak en iyi varyantı tespit etmek (Öğrenme) | Kümülatif ödülü gerçek zamanlı maksimize etmek (Kazanma) |
| **Keşif Stratejisi** | Sabit, eşit dağıtım (Saf Keşif, ardından Saf Sömürü) | Sürekli ve Dinamik Dengeleme (Keşif/Sömürü) |
| **Yakınsama Hızı** | Daha yavaş, kesin sonuca ulaşmak için sabit süre gerekir | Daha hızlı adaptasyon ve yakınsama |
| **Kullanım Kolaylığı** | Uygulaması kolay | Algoritmik ve istatistiksel olarak daha karmaşık |
| **İstatistiksel Kesinlik** | Yüksek istatistiksel kesinlik (Tüm varyasyonların oranları hakkında) | İstatistiksel kesinlik ikinci planda kalır (Odak performans maksimizasyonu) |

---

## Bölüm VI: Uygulama Alanları ve Başarı Örnekleri (Vaka Çalışmaları)

### 6.1. Pazarlama ve Dönüşüm İyileştirmeleri

* **CTA Optimizasyonu:** Going adlı seyahat platformu, CTA düğmesi metnini değiştirerek premium deneme başlangıçlarını aylık bazda %104 artırdı.
* **Kullanıcı Akışı Optimizasyonu:** E-ticarette ödeme akışlarının iyileştirilmesi veya bağış akışlarının optimize edilmesi.

### 6.2. Ürün ve Kullanıcı Deneyimi (UX/UI) Optimizasyonu

* **Stratejik Yerleşim:** Clear Within örneğinde, "Sepete Ekle" (*Add-to-Cart*) gibi kritik CTA öğelerinin sayfanın üst kısmında görünür olacak şekilde yerleştirilmesi, sepete ekleme oranını %80 artırdı.
* **Güven ve Şeffaflık:** T.M. Lewin, ürün sayfalarına net iade mesajları ve boyutlandırma önerileri ekleyerek satışları %7 artırdı.
* **Sayfa Sadeliği:** Swiss Gear, ürün sayfasını basitleştirerek %52 dönüşüm artışı sağladı.

Bu vaka çalışmaları, testlerin daima kullanıcı yolculuğundaki en yüksek sürtünme noktalarına (*High-friction points*) odaklanması gerektiğini göstermektedir.

---

## Bölüm VII: Sonuç ve Stratejik Öneriler

A/B testleri, modern dijital işletmelerin operasyonel ve stratejik kararlarını bilimsel bir çerçevede yönlendirmesini sağlayan temel deneysel yöntemlerdir. Ronald A. Fisher’ın prensiplerinden yola çıkarak, teknoloji şirketlerinin ihtiyaçları doğrultusunda Çok Değişkenli Test (MVT) ve Çok Kollu Haydut (MAB) gibi gelişmiş metodolojilere evrilmiştir.

### 7.1. Karar Matrisi: Hangi Test Türü Ne Zaman Kullanılmalı?

| Amaç (Objective) | Tavsiye Edilen Yöntem | Anahtar Kısıtlama/Gereksinim |
| :--- | :--- | :--- |
| Tek bir değişken üzerinde net sonuç ve uzun vadeli öğrenme | A/B Testi (Split Testing) | İstatistiksel anlamlılığa ulaşmak için yeterli süre ve trafik |
| Birden fazla öğenin etkileşimini anlama ve en iyi kombinasyonu bulma | Çok Değişkenli Test (MVT) | Çok yüksek trafik hacmi (Faktöriyel yapıdan dolayı) |
| Kısa ömürlü kampanyalarda anlık kümülatif ödülü maksimize etme (Performans) | Çok Kollu Haydut (MAB) | Algoritmik karmaşıklık ve istatistiksel kesinlikten taviz |
| Sayfa öğelerinin önemini belirleme ve A/B testi için hipotez oluşturma | MVT, A/B testi ile sinerjik kullanılmalı | En az üç bağımsız öğe olmalıdır |

### 7.2. Stratejik Öneriler

1.  **Veriye Dayalı Kültürün Benimsenmesi:** Kişisel görüşler yerine verilere değer veren ve sürekli deneyi teşvik eden bir deney kültürü (*Culture of Experimentation*) oluşturulmalıdır.
2.  **İstatistiksel Protokollere Uyum:** Tip I ve Tip II hatalarını önlemek için yetersiz örneklem büyüklüğü kullanılması veya testlerin zamanından önce durdurulması gibi yaygın hatalardan kaçınılmalıdır. MDE'nin karesel etkisi dikkate alınarak, test edilecek değişikliklerin yüksek potansiyelli (*yüksek MDE hedefli*) olmasına özen gösterilmelidir.
3.  **Teknolojik Hazırlık:** Yüksek hacimli ve hızlı optimizasyon gerektiren dinamik ortamlarda (örneğin reklam gösterimleri veya kişiselleştirilmiş öneriler), kümülatif ödülü maksimize eden MAB algoritmalarının ve yapay zeka destekli optimizasyon araçlarının teknik altyapıya entegrasyonu planlanmalıdır.

---
# 🧪 HYPOTHESIS TESTING: The Engine Behind ML's A/B Testing

## 🚀 Key Application in Machine Learning: A/B Testing

This section explores how statistical hypothesis testing serves as the foundation for crucial decision-making processes in Machine Learning, particularly within A/B testing frameworks.

## 🔬 Machine Learning Uygulamalarında Hipotez Testi: A/B Testleri

Bağımsız ve eşli hipotez testleri, Makine Öğrenimi ve Veri Biliminde sadece kullanıcı deneyimini değil, aynı zamanda modelin iç bileşenlerini ve performansını karşılaştırmak için de temel araçlardır.

| Kullanım Alanı | Amaç ve Açıklama | Örnek Senaryo | İstatistiksel Bağlantı |
| :--- | :--- | :--- | :--- |
| **Model/Algoritma Seçimi** 🤖 | İki veya daha fazla farklı ML modelinin (Örn: Lineer Regresyon vs. Rastgele Orman) aynı görevde anlamlı olarak farklı performans gösterip göstermediğini test etmek. | Model A'nın ortalama **RMSE** (Kök Ortalama Kare Hatası) değeri, Model B'nin ortalama RMSE değerinden istatistiksel olarak daha düşük mü? | **Eşli $t$-Testi** (Paired $t$-Test) |
| **Özellik Mühendisliği (Feature Engineering)** 🛠️ | Yeni eklenen veya dönüştürülen bir özelliğin, modelin nihai performansını anlamlı bir şekilde artırıp artırmadığını değerlendirmek. | Özellik X'i kullanan modelin ortalama hassasiyeti (Precision), kullanmayan modelinkinden istatistiksel olarak farklı mı? | **Bağımsız $t$-Testi** veya $t$-Testi Varyantları |
| **Optimizasyon/Hiperparametre Ayarı** ⚙️ | Bir hiperparametrenin (Örn: Öğrenme oranı) iki farklı değeriyle eğitilen model setlerinin performans sonuçlarını karşılaştırmak. | Learning Rate = 0.01 ile elde edilen doğruluk (Accuracy) ortalaması, Learning Rate = 0.001 ile elde edilenden daha iyi mi? | **Bağımsız $t$-Testi** (Independent Two-Sample $t$-Test) |
| **Kullanıcı Deneyimi (UX) - A/B Testi** 🧑‍💻 | ML tarafından sunulan iki farklı çıktının veya önerinin (Örn: Kişiselleştirilmiş Başlık A vs. Başlık B) kullanıcı davranışı (tıklama, dönüşüm) üzerindeki etkisini ölçmek. | Reklam B'nin tıklama oranı (**CTR**), Reklam A'nın CTR'sinden istatistiksel olarak daha yüksek mi? | **İki Örneklem Oran Testi** (Two Sample Test for Proportions) |
| **Tıbbi/Bilimsel Deneyler** 🧪 | ML destekli bir tanı aracının (Model A) performansı ile geleneksel bir yöntemin (Model B) performansını karşılaştırmak. | Model A'nın hastalığı doğru teşhis etme oranı, Model B'ninkinden anlamlı derecede farklı mı? | **İki Örneklem Oran Testi** veya **Eşli $t$-Testi** |


<img width="1216" height="592" alt="image" src="https://github.com/user-attachments/assets/b7849c95-dacb-48f9-9c49-39c022e4dfbc" />


# 🛒 A/B Testi: Satın Alma Miktarı Analizi (Sol Kuyruk t-Testi)

Bu analiz, iki farklı ürün tasarımının (A ve B) kullanıcı başına ortalama satın alma miktarı üzerinde anlamlı bir fark yaratıp yaratmadığını Welch's $t$-Testi (Varyanslar eşit değil varsayımı) ile test etmektedir.

---

## 1. Hipotezler ve Seviyeler

| Parametre | Değer/İfade | Açıklama |
| :--- | :--- | :--- |
| **Sıfır Hipotezi** ($H_0$) | $\mu_A - \mu_B = 0$ | Ortalamalar arasında fark yoktur. |
| **Alternatif Hipotez** ($H_1$) | $\mu_A - \mu_B < 0$ | Tasarım B'nin ortalaması, A'dan anlamlı olarak daha yüksektir (Sol Kuyruk Testi). |
| **Anlamlılık Seviyesi** ($\alpha$) | $0.05$ | Reddetme bölgesi için belirlenen %5 risk. |

---

## 2. Örneklem Verileri ve t-İstatistiği

| Grup | $n$ (Büyüklük) | $\bar{x}$ (Ortalama) | $s$ (Std. Sapma) |
| :--- | :--- | :--- | :--- |
| **A (Tasarım A)** | $n_A = 80$ | $\bar{x} = 50$ | $s_A = 10$ |
| **B (Tasarım B)** | $n_B = 20$ | $\bar{y} = 55$ | $s_B = 15$ |

### 🚀 t-İstatistiği Hesabı (Welch's $t$-Testi)

$$t = \frac{(\bar{X} - \bar{Y}) - 0}{\sqrt{\frac{s_A^2}{n_A} + \frac{s_B^2}{n_B}}}$$

$$t = \frac{50 - 55 - 0}{\sqrt{\frac{10^2}{80} + \frac{15^2}{20}}} = \frac{-5}{\sqrt{1.25 + 11.25}} \approx \mathbf{-1.414}$$

*Test, yaklaşık $df \approx 23.38$ serbestlik dereceli $t$-dağılımını takip eder.*

---

## 3. P-Değeri ve Karar 🛑

### P-Değeri:

$$\text{p-value} = P(T < -1.414 \mid H_0 \text{ doğru}) = \mathbf{0.085}$$

### Karar (Conclusion):

$$\mathbf{p\text{-value} (0.085) > \alpha (0.05)}$$

### Neden $H_0$ Reddedilmedi? ❌

$H_0$'ın reddedilmemesinin temel nedeni, hesaplanan p-değerinin ($\mathbf{0.085}$), anlamlılık seviyesi ($\alpha=0.05$) eşiğinin **üzerinde** kalmasıdır.

* $H_0$ doğru iken bu kadar ekstrem bir farkın görülme olasılığı **%8.5**'tir.
* Bu olasılık, belirlediğimiz kabul edilebilir hata riskinden **(\%5)** daha yüksektir.
* Bu nedenle, Tasarım B'nin daha iyi olduğuna dair kanıt, istatistiksel olarak **yeterli derecede güçlü değildir**. Sonuç, tesadüfi olabilir.

**Nihai Sonuç:** Yeterli kanıt olmadığından, **Sıfır Hipotezi reddedilmez** (**Don't reject $H_0$**).

---

<img width="1166" height="544" alt="image" src="https://github.com/user-attachments/assets/1c674480-b262-4d04-b3d4-a581e5edae0e" />

# 🧪 A/B Testi ve t-Testleri İş Akışı (A/B Testing and t-Tests Workflow)

A/B Testi, iki varyasyonu (A/B) karşılaştırmak için kullanılan bir metodolojidir. Bu süreç, genellikle bir hipotez testi olan $t$-Testi ile sonuçlandırılır.

---

## 🗺️ Süreç Adımları (Workflow Steps)

Bu tablo, A/B test sürecini baştan sona adımlarıyla ve her adımdaki temel aksiyonlarla açıklamaktadır.

| # | Adım (Step) | Açıklama (Description) | Bağlantılı İstatistiksel Kavram |
| :---: | :--- | :--- | :--- |
| **1** 💡 | **Varyasyonları Önerme (Propose Variations)** | Karşılaştırılacak iki farklı versiyon (A ve B) belirlenir. Bu, bir web sayfasının iki farklı başlığı, bir modelin iki farklı çıktısı vb. olabilir. | **Sıfır Hipotezi ($H_0$)** ve **Alternatif Hipotezin ($H_1$)** Kurulması. |
| **2** 🎲 | **Örneklemi Rastgele Bölme (Randomly Split Sample)** | Test edilecek kullanıcı veya veri grubu, iki eşit ve bağımsız gruba (A ve B) rastgele ayrılır. Rastgelelik, önyargıyı (bias) azaltmak için kritik öneme sahiptir. | **Bağımsız Örneklemler** (Independent Samples) Varsayımı. |
| **3** 🎯 | **Her Grup İçin Sonuçları Ölçme (Measure Outcomes)** | Her iki varyasyona maruz kalan grupların çıktıları ölçülür ve karşılaştırılabilir bir metrik (Örn: Ortalama satın alma miktarı, tıklama oranı) belirlenir. | **Örneklem İstatistiklerinin** ($\bar{x}, s, n$) Hesaplanması. |
| **4** 📈 | **Karar Vermek İçin İstatistiksel Analiz (Statistical Analysis to Make a Decision)** | Elde edilen metrikler, aradaki farkın rastlantısal mı yoksa istatistiksel olarak anlamlı mı olduğunu belirlemek için analiz edilir. **$t$-Testi** bu aşamanın temel aracıdır. | **$t$-Testinin** Uygulanması, **P-Değeri**nin hesaplanması ve **Anlamlılık Seviyesi ($\alpha$)** ile karşılaştırılması. |

### 🔑 $t$-Testi Bağlantısı

$t$-Testi, analiz aşamasında (Adım 4) kullanılır ve iki grup arasındaki farkın basit şanstan mı kaynaklandığını yoksa varyasyonlardan birinin gerçekten diğerinden daha iyi olup olmadığını belirlememizi sağlar.

---


# 📉 A/B Testi: Dönüşüm Oranları (Two-Proportion Z-Test)

* Neden Binomial kullanildi?
* Hangi istatistik kullanilacak bu durumda?
* Law of large numbers´in buradaki kullanim amaci nedir?
* Bu örnekte Gaussein nerede devreye girer?
* Distribution´i neden standardize ederiz?, Neyi cözmemizi saglar?
* Sample proportion neden all samples´lari consider eder?
* Neden Left-tailed test secildi?
* Sample icin p-Value nedir? Nasil bulunur? Hangi parameterlara bakmak gerekir?
  

  
<img width="1192" height="566" alt="image" src="https://github.com/user-attachments/assets/ebf23c20-9d41-486c-a596-b260b4582db9" />


<img width="1120" height="538" alt="image" src="https://github.com/user-attachments/assets/2defc1ad-8bf4-4d47-93bb-3cc5e66f3693" />

<img width="1209" height="555" alt="image" src="https://github.com/user-attachments/assets/cd515dbe-0dac-47e1-a647-4b79299521ed" />

<img width="1087" height="535" alt="image" src="https://github.com/user-attachments/assets/9c812e64-d70f-498c-b56b-d9b9380cc41f" />

<img width="1215" height="580" alt="image" src="https://github.com/user-attachments/assets/6bdae407-4986-4a05-9f5e-2d124f64c64f" />

<img width="1214" height="577" alt="image" src="https://github.com/user-attachments/assets/c4fdcc71-7729-4fc7-bd5e-3733f010b491" />

<img width="1236" height="611" alt="image" src="https://github.com/user-attachments/assets/4099cac1-790c-4917-a2a7-a10dc4dc1a57" />




Bu bölüm, A/B testinde dönüşüm oranlarını karşılaştırmak için kullanılan İki Oran Z-Testi'nin matematiksel altyapısını ve uygulama örneğini detaylandırır.

---

## A. Temel Yapı ve Varsayımlar

### 1. Neden Binom (Binomial) Dağılımı Kullanıldı?

* **Açıklama:** A/B testinde her bir kullanıcının çıktısı (dönüşüm var/yok) iki sonuçlu bir denemedir (Bernoulli). $X$ ve $Y$, $n$ sayıda bağımsız Bernoulli denemesindeki toplam başarı sayısını (dönüşüm sayısını) temsil ettiğinden, **Binom Dağılımını** takip ederler.
* **Görsel İfade:** $X \sim \text{Binomial}(n_A, p_A) \quad \text{ve} \quad Y \sim \text{Binomial}(n_B, p_B)$

### 2. Hangi İstatistik Kullanılacak Bu Durumda?

* **İstatistik:** **Z-İstatistiği** (İki Oran Z-Testi).
* **Neden:** Örneklem büyüklükleri yeterince büyük olduğunda, Binom dağılımını Normal Dağılım ile yakınlaştırmak (approximate) mümkündür, bu da Z-testi kullanmamızı sağlar.

### 3. Büyük Sayılar Yasasının ve Gaussian Yaklaşımının Rolü 🎯

* **Law of Large Numbers (LLN) Amacı:** Örneklem oranlarının ($\hat{p}_A, \hat{p}_B$) gerçek popülasyon oranlarına ($p_A, p_B$) yaklaşmasını sağlar, güvenilir tahminciler elde ederiz.
* **Gaussian (Normal) Yaklaşımı:** Merkezi Limit Teoremi (CLT) sayesinde, $n$ büyükse, örneklem oranlarının farkının dağılımı **Normal Dağılıma** yaklaşır. Bu, test istatistiği olarak $Z$ kullanmamızın temelini oluşturur.

---

## B. Test İstatistiği ve Standardizasyon

### 4. Dağılımı Neden Standartlaştırırız? 📏

* **Amaç:** Dağılımı standart bir ölçeğe ($Z \sim N(0, 1)$) dönüştürmek.
* **Çözüm:** Hesaplanan $z$-değerini, Standart Normal Dağılım tabloları veya yazılımları kullanarak p-değerini bulmak için evrensel olarak karşılaştırmamızı sağlar.

### 5. Örneklem Oranı Neden Tüm Örneklemleri ($X+Y$) Dikkate Alır? (Pooled Estimate) 🧩

* **Neden:** Sıfır Hipotezi ($H_0: p_A = p_B = p$) altında, her iki popülasyonun da **aynı ortak $p$ oranına** sahip olduğu varsayılır. Bu bilinmeyen $p$'yi tahmin etmek için en iyi yol, iki örneklemden toplanan tüm veriyi birleştirmektir.
* **Formül (Birleştirilmiş Oran Tahmini):**
    $$\hat{p} = \frac{X + Y}{n_A + n_B}$$

### Test İstatistiği (Test Statistic) Formülü:

$$Z = \frac{\hat{p}_A - \hat{p}_B - 0}{\sqrt{\hat{p}(1-\hat{p})\left(\frac{1}{n_A} + \frac{1}{n_B}\right)}} \approx N(0, 1)$$

---

## C. Örnek Uygulama ve Karar

### 6. Neden Sol Kuyruk Testi Seçildi? ⬅️

* **Hipotez:** $H_1: p_A - p_B < 0$ (Yani, $p_B > p_A$).
* **Seçim Nedeni:** Test, Tasarım B'nin dönüşüm oranının A'dan **daha yüksek olduğunu** kanıtlamayı amaçlar. Eğer bu doğruysa, fark $p_A - p_B$ **negatif** çıkacaktır. Negatif değerler, $Z$-dağılımının sol kuyruğunda yer aldığı için Sol Kuyruk Testi seçilmiştir.

### 7. Örnek Sonuçları ve Yorum

| İstatistik | Değer |
| :--- | :--- |
| **Gözlemlenen $Z$** ($z$) | $\mathbf{-1.336}$ |
| **P-Değeri** | $\mathbf{0.091}$ |
| **Anlamlılık Seviyesi** ($\alpha$) | $\mathbf{0.05}$ |

**Karar ve Yorum:**

1.  **Karşılaştırma:** $\text{p-value} (0.091) > \alpha (0.05)$
2.  **Sonuç:** $H_0$ **Reddedilmez** (**Do not reject $H_0$**).
3.  **Yorum:** %5 anlamlılık seviyesinde, Tasarım B'nin dönüşüm oranının Tasarım A'dan anlamlı derecede daha yüksek olduğuna dair **yeterli istatistiksel kanıt yoktur**. Gözlemlenen fark şanstan kaynaklanmış olabilir.
