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
