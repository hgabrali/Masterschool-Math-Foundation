
# Yaygın Sürekli Dağılımların Kapsamlı ve Karşılaştırmalı Analizi: Teori, Tarihçe ve Uygulamalar

Amac: Istatistiksel çıkarımın ve risk modellemesinin temelini oluşturan en yaygın **sürekli olasılık dağılımlarını (Common Continuous Probability Distributions)** derinlemesine incelemektedir. Dağılımların matematiksel tanımlarını, tarihsel gelişim kronolojisini, birbirleriyle olan ilişkilerini ve günümüzdeki endüstriyel, finansal ve akademik uygulama alanlarını detaylı olarak karşılaştırmalı bir perspektifle sunmaktadır.

---

## 1. Giriş ve Temel Kavramlar (Introduction and Fundamental Concepts)

### 1.1. Sürekli Dağılımların Tanımı ve Önemi

**Sürekli dağılımlar**, sonsuz sayıda olası değere sahip olan olayların olasılıklarını tanımlar. Sürekli bir rastgele değişkenin (Continuous Random Variable) sonsuz sayıda olası değer alabilmesi nedeniyle, belirli tek bir sonucun gerçekleşme olasılığı **sıfırdır**. Bunun yerine, ilgi duyulan olasılık, rastgele değişkenin belirli bir **aralıkta** yer almasıyla hesaplanır. Bu, sürekli istatistiği, belirli bir sonucun kesin olasılığa sahip olduğu ayrık (Discrete) istatistikten ayırır ve matematiksel analizde **integral kalkülüsünün** kullanımını zorunlu kılar.

### 1.2. Olasılık Yoğunluk Fonksiyonu (PDF, Probability Density Function)

Bir sürekli rastgele değişken X'in olasılık yoğunluk fonksiyonu (**PDF**), $f(x)$ ile gösterilir. Bu fonksiyon, X rastgele değişkeninin $x$ civarında bir değer alma eğilimini, yani olasılık yoğunluğunu (*probability density*) ifade eder.

$f(x)$ bir olasılık değeri sağlamaz; aksine, bir $a$ ile $b$ aralığındaki olasılığı bulmak için $f(x)$'in bu aralıktaki integralinin hesaplanması gerekir.

PDF'nin geçerli bir olasılık fonksiyonu olması için iki temel koşulu sağlaması gerekir:
1. Tüm $x$ değerleri için olasılık yoğunluğu negatif olmamalıdır: $f(x) \ge 0$.
2. Tüm olası değerler kümesi üzerindeki toplam yoğunluk 1'e eşit olmalıdır (tüm alan 1'dir): $\int_{-\infty}^{\infty} f(x) dx = 1$.

Bu fonksiyon, ayrık değişkenler için kullanılan Olasılık Kütle Fonksiyonu'ndan (PMF, Probability Mass Function) niteliksel olarak farklıdır.

### 1.3. Kümülatif Dağılım Fonksiyonu (CDF, Cumulative Distribution Function)

**Kümülatif dağılım fonksiyonu (CDF)**, $F(x)$ ile gösterilir ve rastgele değişken X'in belirli bir $x$ değerinden küçük veya $x$'e eşit olma olasılığını tanımlar: $F(x) = P(X \le x)$. CDF, olasılıkları $x$ değerine kadar kümülatif olarak topladığı için, çıktı değeri daima 0 ile 1 arasında yer alır ve $x$ arttıkça asla azalmayan (*non-decreasing*) bir fonksiyondur.

CDF, istatistiksel çıkarım ve karar verme süreçlerinde son derece pratik bir araçtır. Özellikle, kümülatif olasılıklar doğrudan **yüzdelik dilimlere** (*percentiles*) eşdeğerdir.

### 1.4. PDF ve CDF Arasındaki Matematiksel İlişki

PDF ve CDF, Kalkülüsün Temel Teoremi (*Fundamental Theorem of Calculus*) sayesinde sıkı bir matematiksel ilişki içindedir.

* **CDF'nin Hesaplanması:** CDF, PDF'nin negatif sonsuzluktan $x$'e kadar entegrasyonu (integral alma) yoluyla elde edilir:
    $F(x) = \int_{-\infty}^{x} f(t) dt$.
* **PDF'nin Hesaplanması:** Karşılıklı olarak, PDF, CDF'nin türevi (*differentiation*) alınarak elde edilir:
    $f(x) = \frac{d}{dx} F(x)$.

---

## 2. Sürekli Dağılımların Tarihsel Gelişimi ve Kronolojisi

### 2.1. Erken Keşifler ve Normal Dağılımın Kökeni

**Normal Dağılım (Normal Distribution)** veya diğer adıyla **Gauss-Laplace Dağılımı**, istatistiğin en eski ve merkezi dağılımıdır.
* **1733: Abraham de Moivre:** Normal dağılımın en erken formu, Binom dağılımının limit formu olarak keşfedildi.
* **1809 - 1812: Gauss ve Laplace:** Dağılım, Carl Friedrich Gauss tarafından astronomik ölçümlerdeki hataları modellemek (**"Hata Yasası"**) ve Pierre-Simon Laplace tarafından genel olasılık teorisi bağlamında bağımsız olarak yeniden formüle edildi.
* **19. Yüzyıl Sonları: Karl Pearson:** Dağılıma **"Normal Eğri"** (*Normal Curve*) adını verdi.

### 2.2. Dağılımların Kronolojik Sıralaması ve Türevsel İhtiyaçlar

| Dağılım Adı (İngilizce) | Keşif/Geliştirme Yılı (Yaklaşık) | Öncü/Kurucu Figürler | Bağlam ve Temel Fonksiyon |
| :--- | :--- | :--- | :--- |
| **Normal Distribution (Gaussian)** | 1733 / 1809-1812 | A. de Moivre, C. F. Gauss, P. S. Laplace | Merkezî Limit Teoremi, Ölçüm Hataları (Hata Yasası). |
| **Chi-square Distribution ($\chi^2$)** | 1876 / 1900 | F. Helmert, K. Pearson | Normal verinin varyansının örnekleme dağılımı; Uyum iyiliği testi. |
| **Student's t-Distribution** | 1908 | W. Gosset ("Student") | Küçük örneklemler ve bilinmeyen popülasyon standart sapması ile ortalama tahmini. |
| **F-Distribution (Fisher–Snedecor)** | 1924 | R. A. Fisher, G. Snedecor | İki varyans oranının karşılaştırılması; Varyans Analizi (ANOVA). |

* **1876: Ki-Kare Dağılımı ($\chi^2$, Chi-Square Distribution):** Karl Pearson, 1900 yılında bu fonksiyona Ki-Kare adını vererek, **uyum iyiliği** (*goodness-of-fit*) testlerinde kullanılmasını sağladı.
* **1908: Student's t-Dağılımı (Student's t-Distribution):** William Gosset ("Student"), **küçük örneklem hacimlerinde** Normal dağılımın varsayımlarının geçerli olmadığı durumlara çözüm bulmak amacıyla t-dağılımını geliştirdi.
* **1924: F-Dağılımı (F-Distribution):** Sir Ronald A. Fisher tarafından **varyans oranlarını karşılaştırmak** için (özellikle Varyans Analizi - ANOVA bağlamında) tanıtıldı.

### 2.3. Türetilmiş Dağılımların İstatistiksel Çıkarım İçin Doğuşu

Normal dağılım, "ideal" popülasyonu temsil ederken; $t$, $\chi^2$ ve $F$ dağılımları, "gerçek dünya"nın sınırlamaları ve belirsizlikleri (örnekleme hatası, serbestlik derecesi) altında güvenilir sonuçlar elde etmek için doğrudan Normal dağılımdan matematiksel olarak **türetilmiştir**. Bu dağılımlar, **hipotez testlerinin** ve **güven aralıklarının** oluşturulması için hayati bir araç seti sağlamaktadır.

---

## 3. Temel Sürekli Dağılımların Detaylı Analizi

### 3.1. Normal Dağılım (Normal/Gaussian Distribution, $N(\mu, \sigma^2)$)

<img width="774" height="285" alt="image" src="https://github.com/user-attachments/assets/0ecebad6-a624-4caa-8bfe-e01b328f2bd1" />


* **Parametreler:** Ortalama ($\mu$, Mean) ve Varyans ($\sigma^2$) veya Standart Sapma ($\sigma$, Standard Deviation).
* **PDF:** Çan şeklindedir: $f(x|\mu, \sigma^2) = \frac{1}{\sigma\sqrt{2\pi}} e^{-(x-\mu)^2/(2\sigma^2)}$, $-\infty < x < \infty$.
* **Özellikler:** $\mu$'ya göre simetriktir. Standart Normal Dağılım, $\mu=0$ ve $\sigma=1$ parametrelerine sahip özel bir durumdur.

### 3.2. Üstel Dağılım (Exponential Distribution, $Exp(\lambda)$)

<img width="625" height="522" alt="image" src="https://github.com/user-attachments/assets/20a11a38-b5f4-4f0d-ab25-cc7b11ceaf21" />


Poisson süreci bağlamında, **olaylar arasındaki zaman aralıklarını** modellemek için kullanılır.

* **Parametreler:** Hız parametresi ($\lambda$, rate) veya ortalama olay zamanı ($\beta=1/\lambda$, scale parameter).
* **PDF:** Yalnızca pozitif değerler için tanımlıdır ($x \ge 0$): $f(x|\lambda) = \lambda e^{-\lambda x}$, $x \ge 0$.
* **Hafızasızlık Özelliği (Memoryless Property):** Bir sistemin belirli bir süre çalışmış olması, gelecekteki arızalanma olasılığını etkilemez: $P(X > s+t | X > s) = P(X > t)$.

### 3.3. Tekdüze Dağılım (Uniform Distribution, Rectangular Distributions, $U(a,b)$)

<img width="352" height="557" alt="image" src="https://github.com/user-attachments/assets/87978a3e-1a89-4f51-8a44-7c05236bbfe4" />


Belirli bir $a$ ve $b$ aralığındaki tüm sonuçların **eşit olasılık yoğunluğuna** sahip olduğu en basit sürekli dağılımdır.

* **Parametreler:** Alt sınır ($a$) ve üst sınır ($b$).
* **PDF:** $f(x|a,b) = \frac{1}{b-a}$, $a \le x \le b$.
* **Özellikler:** Ortalaması $(a+b)/2$, varyansı $(b-a)^2/12$'dir. Simülasyonlarda rastgele sayı üretmek için kullanılır.

### 3.4. Gama Dağılımları Ailesi (The Gamma Family of Distributions)

<img width="537" height="282" alt="image" src="https://github.com/user-attachments/assets/48262cb1-9024-4cb9-a892-9cd17a9e417f" />


Üstel dağılımın bir genellemesi olup, özellikle bir dizi bağımsız üstel olayın (Poisson sürecindeki olaylar) tamamlanması için gereken **kümülatif bekleme sürelerini** modellemek için kullanılır.

* **Parametreler:** Şekil parametresi ($\alpha$, shape parameter) ve Ölçek parametresi ($\beta$, scale parameter).
* **İlişkisel Durumlar:**
    * **Üstel Dağılım:** $\alpha=1$ olduğunda, Gama dağılımı $Exp(1/\beta)$ Üstel dağılıma dönüşür.
    * **Ki-Kare Dağılımı ($\chi^2$):** $\alpha=\nu/2$ ve $\beta=2$ olduğunda, $\nu$ serbestlik dereceli Ki-Kare dağılımını verir.

### 3.5. Diğer Önemli Sürekli Dağılımlar

<img width="875" height="352" alt="image" src="https://github.com/user-attachments/assets/57c87adf-f302-45c8-b196-4089f7f88923" />

* **Lognormal Dağılım:** Bir rastgele değişkenin doğal logaritması Normal dağılıma uyuyorsa, değişkenin kendisi Lognormal dağılıma uyar. Yalnızca pozitif değerler alır ve **sağa çarpık** değişkenleri modellemek için kullanılır (örn: gelir dağılımı, finansal varlık fiyatları).

<img width="446" height="665" alt="image" src="https://github.com/user-attachments/assets/f60b63bf-76ad-40f7-9d23-7d13086bd5c1" />

* **Weibull Dağılımı:** **Güvenilirlik analizi** ve **yaşam süresi modellemesi** (*failure time modeling*) için çok esnek bir araçtır. Şekil parametresi sayesinde arıza oranının zamanla değişmesini (azalması, sabit kalması, artması) modellemeye olanak tanır.

<img width="1295" height="566" alt="image" src="https://github.com/user-attachments/assets/8fe096d5-9b14-4f1a-a8a1-152ff44bf408" />

  
* **Beta Dağılımı:** Sabit $[0, 1]$ aralığında tanımlanmış rastgele değişkenleri modellemek için idealdir. Genellikle **olasılıkları, oranları veya yüzdeleri** modellemek için kullanılır.

---

## 4. İstatistiksel Çıkarım Dağılımları

<img width="751" height="413" alt="image" src="https://github.com/user-attachments/assets/d906ac40-6e1c-41f6-b532-294fff15830d" />


Normal dağılımdan türetilmiş bu dağılımlar, küçük örneklem belirsizliğini ve varyans karşılaştırmalarını hesaba katarak modern **hipotez testlerinin** ve çıkarımın temelini oluşturur.

### 4.1. Student's t-Dağılımı (Student's t-Distribution, $t_\nu$)

<img width="600" height="306" alt="image" src="https://github.com/user-attachments/assets/33a842ed-0918-4793-8034-211f26ec7787" />


Popülasyon standart sapması ($\sigma$) bilinmediğinde ve özellikle **örneklem büyüklüğü ($n$) küçük olduğunda** popülasyon ortalamasını tahmin etmek için geliştirilmiştir.

* **Yapı ve Serbestlik Derecesi ($\nu$):** Genellikle $\nu = n-1$. T-istatistiği, $t_\nu = \frac{Z}{\sqrt{\chi^2_\nu / \nu}}$ şeklinde elde edilir.
* **Normal Dağılım ile İlişkisi:** Normal dağılıma benzer şekilde çan şeklindedir ancak **kuyrukları daha ağırdır** (*heavier tails*). Örneklem büyüklüğü arttıkça ($\nu \rightarrow \infty$), t-dağılımı asymptotically Normal dağılıma yaklaşır.
* **Uygulama:** Ortalamaları test eden Student's t-testi ve güven aralıklarının oluşturulmasında kullanılır.

### 4.2. Ki-Kare Dağılımı ($\chi^2$, Chi-Square Distribution, $\chi^2_\nu$)

<img width="865" height="470" alt="image" src="https://github.com/user-attachments/assets/4582c936-5697-4b3d-9864-093ef4caca26" />


$\nu$ serbestlik derecesiyle, $\nu$ adet bağımsız standart normal rastgele değişkenin **karelerinin toplamının** dağılımıdır.

* **Yapı ve Parametre:** Tek parametresi serbestlik derecesidir ($\nu$). Dağılım, daima pozitif değerler alır ve **sağa çarpıktır**.
* **Uygulamalar:**
    * Varyansın Örnekleme Dağılımı.
    * **Uyum İyiliği Testleri** (*Goodness-of-Fit Tests*).
    * **Bağımsızlık Testleri** (*Tests of Independence*).

### 4.3. F-Dağılımı (F-Distribution, $F_{\nu_1, \nu_2}$)

<img width="547" height="696" alt="image" src="https://github.com/user-attachments/assets/1c8f2343-015a-4049-892c-243c0d5f9daf" />


**İki varyansın oranını** karşılaştırmak için tasarlanmıştır.

* **Yapı ve Parametreler:** İki bağımsız Ki-Kare değişkeninin, kendi serbestlik derecelerine bölünmüş oranının dağılımıdır: $F_{\nu_1, \nu_2} \equiv \frac{\chi^2_{\nu_1}/\nu_1}{\chi^2_{\nu_2}/\nu_2}$. İki serbestlik derecesi parametresi vardır: Pay serbestlik derecesi ($\nu_1$) ve payda serbestlik derecesi ($\nu_2$).
* **Uygulama:** Temel olarak **Varyans Analizinde (ANOVA)** kullanılır. Üç veya daha fazla popülasyon ortalamasının eşit olup olmadığını test etmek için idealdir.

### 4.4. Dağılımların Hiyerarjisi

$\chi^2$, $t$ ve $F$ dağılımları arasındaki matematiksel bağımlılık, istatistiksel testlerin birbiriyle entegre bir yapıda olduğunu gösterir. T-dağılımı ve F-dağılımı, Normal dağılımdan türetilen $\chi^2$ dağılımını temel alır. Örneğin, $F_{1,\nu} = t^2_\nu$.

---

## 5. Karşılaştırmalı Özellikler ve Matematiksel Özet

### Table 2: Yaygın Sürekli Dağılımların Karşılaştırmalı Matematiksel Özellikleri

| Dağılım (Distribution) | Parametreler | PDF Alanı (Domain) | Ortalama (Mean, E[X]) | Varyans (Variance, Var[X]) | Temel Özellik |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Normal ($N(\mu, \sigma^2)$)** | Ortalama ($\mu$), Std. Sapma ($\sigma$) | $(-\infty, \infty)$ | $\mu$ | $\sigma^2$ | Simetri, Merkezî Limit Teoremi. |
| **Uniform ($U(a,b)$)** | Alt Sınır ($a$), Üst Sınır ($b$) | $[a,b]$ | $(a+b)/2$ | $(b-a)^2/12$ | Tüm değerler eşit olasılığa sahiptir. |
| **Exponential ($Exp(\lambda)$)** | Hız Oranı ($\lambda$) | $[0,\infty)$ | $1/\lambda$ | $1/\lambda^2$ | Hafızasızlık (Memoryless). |
| **Gamma ($Gamma(\alpha,\beta)$)** | Şekil ($\alpha$), Ölçek ($\beta$) | $[0,\infty)$ | $\alpha\beta$ | $\alpha\beta^2$ | Üstel ve $\chi^2$ dağılımlarının genellemesi. |
| **Lognormal ($LN(\mu, \sigma^2)$)** | Log Ortalama ($\mu$), Log Varyans ($\sigma^2$) | $(0,\infty)$ | $e^{\mu+\sigma^2/2}$ | $e^{2\mu+\sigma^2}(e^{\sigma^2}-1)$ | Pozitif çarpıklık, Finansta kullanılır. |
| **Chi-square ($\chi^2_\nu$)** | Serbestlik Derecesi ($\nu$) | $[0,\infty)$ | $\nu$ | $2\nu$ | Normal değişkenlerin karelerinin toplamı. |
| **Student's t ($t_\nu$)** | Serbestlik Derecesi ($\nu$) | $(-\infty, \infty)$ | $0$ ($\nu>1$) | $\nu/(\nu-2)$ ($\nu>2$) | Ağır kuyruklar, küçük örneklem belirsizliği. |

---

## 6. Güncel Uygulama Alanları ve Vaka Örnekleri

### 6.1. Finans ve Ekonometri

* **Stok Fiyatları Modellemesi ve Risk Yönetimi:** Lognormal Dağılım (stok fiyatları) ve Normal Dağılım (günlük getiriler).
* **Hipotez Testleri:** Student's t-Dağılımı (küçük örneklemlerde finansal iddiaların testi, ağır kuyruk olaylarını yakalama).

### 6.2. Kalite Kontrol ve Mühendislik

* **Üretim Toleransları ve Kalite Kontrol:** Normal Dağılım (ölçümlerin kalitesi).
* **Güvenilirlik Mühendisliği ve Yaşam Süresi Modelleri:** Weibull ve Üstel Dağılım (parça ömrü, arıza oranları).
* **Kuyruk Teorisi (Queuing Theory):** Üstel Dağılım (müşteri varışları arasındaki süre).

### 6.3. Akademik Araştırma ve Çıkarım Testleri

* **Varyans Analizi (ANOVA):** F-Dağılımı (üç veya daha fazla grubun ortalamalarının karşılaştırılması).
* **Uyum İyiliği ve Bağımsızlık Testleri:** Ki-Kare Dağılımı (kategorik değişkenlerin bağımsızlığı, veri uyumu).

### 6.4. Dağılım Seçimi ve Model Karmaşıklığı

Dağılım seçimi, modellenen sistemin davranışına dair temel varsayımların bir ifadesidir. Karmaşık süreçler için (finansal verilerin ağır kuyrukları, sistemlerin eskimesi), **Student's t**, **Lognormal** veya **Weibull** gibi daha esnek dağılımların kullanılması gereklidir. Bu seçim, modelin gerçek dünya karmaşıklığına ne kadar yakın olduğunu ve dolayısıyla tahminlerin ne kadar sağlam olduğunu doğrudan belirler.

---

## 7. Sonuç ve Öneriler

### 7.1. Özet: Sürekli Dağılımların Entegre Rolü

Sürekli dağılımlar, modern nicel bilimin temel direkleridir. Normal dağılımın matematiksel temeli, 18. ve 19. yüzyıllarda hata ve doğal fenomenleri modellemek için atılmışken; Student’s t, Ki-Kare ve F gibi türev dağılımlar, 20. yüzyılın başlarında, küçük örneklem belirsizliği ve varyans karşılaştırmaları gibi pratik istatistiksel çıkarım ihtiyaçlarına cevap vermek üzere geliştirilmiştir. Bu hiyerarşik yapı, dağılımların birbirinden bağımsız değil, entegre bir istatistiksel araç seti oluşturduğunu gösterir.

### 7.2. İstatistiksel Modellemede Dağılım Seçiminin Kritik Önemi

Bir istatistiksel modelin veya hipotez testinin güvenilirliği, seçilen dağılımın temel özelliklerinin (simetri, pozitiflik, hafızasızlık, kuyruk kalınlığı) gözlemlenen veriye uygun olup olmamasına bağlıdır. Özellikle risk modellemesinde, Lognormal yerine Normal dağılımın kullanılması, büyük, aşırı olayların olasılığını hafife almaya (*ince kuyruk varsayımı*) yol açar ve hatalı risk hesaplamalarına neden olabilir.

### 7.3. Gelecek Perspektifi

Modern veri bilimi ve makine öğrenimi, yüksek boyutlu ve karmaşık verilerle çalışmaktadır. Bu bağlamda, klasik dağılımların genellemeleri (örneğin, çok değişkenli Student’s t-dağılımı süreçleri) giderek önem kazanmaktadır. Sürekli dağılımların derinlemesine anlaşılması, parametrik yöntemlerin gücünü ve parametrik olmayan yöntemlerle entegrasyonunu sağlamak için temel bir yetkinlik olarak kalacaktır.












---

# Introduction to Continuous Distributions
<img width="730" height="417" alt="image" src="https://github.com/user-attachments/assets/7fd55c10-9097-4ec4-8143-2f65c634c7d8" />
<img width="811" height="711" alt="image" src="https://github.com/user-attachments/assets/2e6c86d1-aa90-46cf-b10d-58d999bf4ef1" />
<img width="812" height="455" alt="image" src="https://github.com/user-attachments/assets/e39c1617-8ebf-4dcc-adb8-28db52b0f9ac" />
<img width="763" height="622" alt="image" src="https://github.com/user-attachments/assets/62d63364-b096-45cc-a4b0-3630727d41aa" />
<img width="767" height="652" alt="image" src="https://github.com/user-attachments/assets/d8c106eb-92e7-45b5-bc75-ded24e9fbcb5" />
<img width="743" height="452" alt="image" src="https://github.com/user-attachments/assets/2b6f9f8e-6a66-4d55-bc90-4e9799808f1d" />
<img width="777" height="537" alt="image" src="https://github.com/user-attachments/assets/cd6639b4-311c-4e6f-8d5d-80a6df19d879" />
<img width="747" height="404" alt="image" src="https://github.com/user-attachments/assets/1c6cda6b-bd58-4e3f-b2c0-e3debb17c337" />

---

## Genel Bakış: Olasılığın İki Farklı Dünyası

Olasılık dünyasını iki ana krallığa ayırabiliriz: **Kesikli (Discrete)** ve **Sürekli (Continuous)**. Aralarındaki temel fark, ölçtüğümüz şeyin "sayılabilir" mi yoksa "ölçülebilir" mi olduğudur.

---

## Karşılaştırma ve Metaforlar

### 1. Kesikli Dağılım vs. Sürekli Dağılım

Görsellerde bu ikili arasındaki fark net bir şekilde gösteriliyor.

* **Kesikli Dağılım (Bilye Torbası Metaforu):**
    * **Ne Olduğu:** Elinizde bir torba olduğunu ve içinde 3 kırmızı, 5 mavi bilye olduğunu hayal edin. Torbadan bir bilye çektiğinizde gelebilecek sonuçlar **sayılabilir** ve **sınırlıdır**: ya kırmızıdır ya da mavidir. "Yarı kırmızı, yarı mavi" bir bilye çekemezsiniz.
    * **Örnekler:** Zar atışı (1, 2, 3, 4, 5, 6 gelebilir), yazı-tura (yazı veya tura), bir saatte gelen müşteri sayısı (10, 11, 12... ama 10.5 müşteri gelemez).
    * **Grafiği (PMF - Olasılık Kütle Fonksiyonu):** Her bir olayın (örneğin 3 gelmesi) olasılığını gösteren ayrı **çubuklardan** oluşur. Her çubuğun yüksekliği, tam olarak o değerin gerçekleşme olasılığını verir. Örneğin, `$P(X = 3)$` yani "zarın tam 3 gelme olasılığı" anlamlıdır ve bir değeri vardır (1/6).
 
* **Sürekli Dağılım (Su Bardağı Metaforu):**
    * **Ne Olduğu:** Şimdi de elinizde bir su bardağı olduğunu düşünün. Bardağı ne kadar doldurdunuz? 150 ml olabilir, 150.1 ml olabilir, 150.112345... ml olabilir. İki değer arasında **sonsuz sayıda** olası değer vardır. Değerler "sayılamaz", ancak bir aralıkta **"ölçülebilir"**.
    * **Örnekler:** Bir insanın boyu, bir arabanın hızı, bir odanın sıcaklığı.
    * **Grafiği (PDF - Olasılık Yoğunluk Fonksiyonu):** Ayrı çubuklar yerine **kesintisiz bir eğri** şeklindedir. Burada kritik bir fark var: Eğrinin bir noktadaki yüksekliği doğrudan olasılığı vermez! Tek bir noktanın olasılığı sıfırdır. Neden mi? Çünkü *tam olarak* 175.00000... cm boyunda biri olma ihtimali, sonsuz olasılık içinde matematiksel olarak sıfırdır.
    * **Anlamlı Olan Nedir?** "Boyunun 175 cm ile 176 cm *arasında* olma olasılığı" gibi bir aralığın olasılığı anlamlıdır. Bu olasılık, eğrinin altında kalan **alandır**.
 
  ### 2. Sürekli Dağılımların Araçları: PDF ve CDF

Sürekli verilerle çalışmak için özel araçlara ihtiyacımız var.

* **PDF (Probability Density Function - Olasılık Yoğunluk Fonksiyonu):**

<img width="440" height="543" alt="image" src="https://github.com/user-attachments/assets/4b0923ac-5e10-4715-86b2-8c7ff46c9d95" />


<img width="440" height="543" alt="image" src="https://github.com/user-attachments/assets/e9aee059-308f-4f99-b702-49f43a38e829" />

* Geometric visualisation of the mode, median and mean of an arbitrary unimodal probability density function.

<img width="1023" height="738" alt="image" src="https://github.com/user-attachments/assets/459157ad-a5c0-45e0-b377-7d3f2d6c33f5" />

* Examples of four continuous probability density functions.

    * **Metafor (Manzara Tepeleri):** PDF eğrisini bir dağ veya tepe manzarası gibi düşünün.
    * **Tepenin Yüksekliği ($f(x)$):** Manzaranın herhangi bir noktasındaki yükseklik, o bölgede bir değerin ortaya çıkmasının ne kadar "yoğun" veya "olası" olduğunu gösterir. Zirveler, en olası değerlerin kümelendiği yerlerdir. Ancak bu yükseklik, tek başına bir olasılık değildir.
    * **Alan (Olasılık):** Belirli bir aralıktaki olasılığı bulmak için o aralıktaki tepenin altında kalan alanı hesaplamamız gerekir ($P(a < X < b)$). Tüm manzaranın (tüm tepelerin) altındaki toplam alan her zaman 1'dir (%100).
 
[Probability Density Function - Wikipedia](https://en.wikipedia.org/wiki/Probability_density_function)

* **CDF (Cumulative Distribution Function - Kümülatif Dağılım Fonksiyonu):**

<img width="381" height="344" alt="image" src="https://github.com/user-attachments/assets/3900d3ec-a1de-4a4a-999c-31765523da76" />

<img width="378" height="305" alt="image" src="https://github.com/user-attachments/assets/79018f58-facb-4e20-a53a-baa0b173a700" />

<img width="322" height="372" alt="image" src="https://github.com/user-attachments/assets/4723ef95-cb4b-4ca4-b9aa-73ff08898a45" />

   * **Metafor (Tırmanış Rotası):** CDF, bu manzarada en soldan başlayıp sağa doğru ilerlerken, o ana kadar arkanızda bıraktığınız toplam alanı (yani toplam olasılığı) gösteren bir fonksiyondur.
  * Yolculuğun en başında (en solda) arkanızda hiç alan yoktur, yani CDF = 0.
  * Yolculuğun sonunda (en sağda) tüm manzarayı geçtiğiniz için toplam alan 1 olur, yani CDF = 1.
  * Bu araç çok kullanışlıdır. Çünkü iki nokta arasındaki alanı (olasılığı) bulmak için integral ile uğraşmak yerine, sadece o noktalardaki kümülatif değerleri birbirinden çıkarırız: `$P(a < X < b) = CDF(b) - CDF(a)$`.
 

[Cumulative Distribution Function - Wikipedia](https://en.wikipedia.org/wiki/Cumulative_distribution_function) 
 
### 3. Dağılımın Karakterini Anlamak: Ortalama ve Varyans

Her manzara (dağılım) farklıdır. Onları tanımlamak için iki temel ölçütümüz var:

* **Ortalama (Mean / Expected Value, $\mu$):**
    * **Metafor (Denge Noktası):** Manzara şeklini bir kartondan kestiğinizi hayal edin. Ortalama ($\mu$), bu kartonu parmağınızın ucunda **dengeleyebileceğiniz** noktadır. Dağılımın "ağırlık merkezidir".

* **Varyans ve Standart Sapma ($\sigma^2$ ve $\sigma$):**
    * **Metafor (Manzaranın Yayılımı):** Bu değerler, manzaranın ne kadar **yayvan** veya ne kadar **sivri** olduğunu anlatır.
    * **Düşük Standart Sapma:** Değerler ortalamaya çok yakındır. Manzaramız sivri ve dar bir tepe gibidir (örneğin Fuji Dağı). Herkesin boyu birbirine çok yakınsa standart sapma düşük olur.
    * **Yüksek Standart Sapma:** Değerler ortalamadan çok uzağa yayılmıştır. Manzaramız geniş ve basık bir tepe veya yayla gibidir. Sınıfta çok uzun ve çok kısa boylu öğrenciler varsa standart sapma yüksek olur.
 

### 4. Tanışılması Gereken İki Önemli Aile Üyesi

Görsellerde iki popüler dağılım türü tanıtılıyor:

* **1. Düzgün Dağılım (Uniform Distribution):**
---

<img width="353" height="552" alt="image" src="https://github.com/user-attachments/assets/40ae3eea-a0d7-4f2b-8b10-438635bd8c4e" />


   * **Metafor (Mükemmel Düz Bir Plato):** Bu dağılım, belirli bir aralıktaki her sonucun **eşit derecede olası** olduğu durumları tanımlar. PDF grafiği, bir **dikdörtgen** şeklindedir.
   * **Örnek:** Bir bilgisayarın 0 ile 1 arasında rastgele bir sayı üretmesi. 0.2 gelme olasılığı ile 0.8 gelme olasılığı tamamen aynıdır. Hiçbir bölgenin diğerine üstünlüğü yoktur.
      
 **Uniform distribution** may refer to:

* Continuous uniform distribution
* Discrete uniform distribution
* Uniform distribution (ecology)
* Equidistributed sequence

### Sürekli Düzgün Dağılım (Continuous Uniform Distribution)

Bu, istatistikte en yaygın bilinen türdür. Belirli bir aralıktaki (örneğin 0 ile 10 arası) her bir sonucun gerçekleşme olasılığının **tamamen aynı** olduğu durumları ifade eder.

* **Metafor:** Bir otobüsün her saat başı 0 ila 30. dakikalar arasında herhangi bir anda gelebildiğini ve her anın eşit olasılıklı olduğunu düşünün. Durağa rastgele bir zamanda gittiğinizde otobüsün 5. ile 10. dakikalar arasında gelme olasılığı, 20. ile 25. dakikalar arasında gelme olasılığı ile aynıdır.

---

### Kesikli Düzgün Dağılım (Discrete Uniform Distribution)

Bu, **sayılabilir** sayıda ve sonlu olan her bir sonucun gerçekleşme olasılığının eşit olduğu durumları tanımlar.

* **Metafor:** Hilesiz bir zarı attığınızda 1, 2, 3, 4, 5 veya 6 gelme olasılıklarının hepsi birbirine eşittir (1/6). Sonuçlar belirli ve ayrı değerlerdir.

---

### Düzgün Dağılım (Ekoloji)

Bu terim, istatistiksel bir kavram değil, **ekolojik** bir gözlemdir. Bir popülasyondaki bireylerin bir yaşam alanı üzerinde nasıl yayıldığını ifade eder.

* **Açıklama:** Düzgün dağılım, bireylerin birbirinden **eşit uzaklıklarda** bulunduğu bir yerleşim düzenidir. Bu durum genellikle bireyler arası rekabetin (örneğin kaynaklar veya alan için) yüksek olduğu durumlarda görülür.
* **Örnek:** Kendi bölgelerini savunan penguenlerin yuvaları veya su için rekabet eden çöl bitkileri genellikle düzgün bir dağılım sergiler. 🐧

---

### Dengeli Dağılımlı Dizi (Equidistributed Sequence)

Bu, daha çok matematik ve sayı teorisiyle ilgili bir kavramdır. Bir aralıktaki sayıların oluşturduğu bir dizinin, o aralığı ne kadar **"adil" veya "eşit"** bir şekilde doldurduğunu ifade eder.

* **Açıklama:** Basitçe, bir dizideki elemanlar ilerledikçe, herhangi bir alt aralığa düşen eleman sayısının, o aralığın uzunluğuyla orantılı hale gelmesidir. Yani dizi, zamanla aralığın her yerine **eşit bir şekilde yayılır**.

### Düzgün Dağılım Kavramları Karşılaştırma Tablosu

| Kavram | Alan | Temel Fikir | Veri Tipi / Yapı | Örnek / Metafor |
| :--- | :--- | :--- | :--- | :--- |
| **Sürekli Düzgün Dağılım** | İstatistik | Belirli bir aralıktaki her sonucun olasılığı eşittir. | Sürekli (ölçülebilir) aralık | Bir otobüsün 0-30 dk. arasında herhangi bir anda gelmesi. |
| **Kesikli Düzgün Dağılım** | İstatistik | Sonlu sayıdaki her bir ayrık sonucun olasılığı eşittir. | Kesikli (sayılabilir) değerler | Hilesiz bir zar atışı (1, 2, 3, 4, 5, 6). |
| **Düzgün Dağılım (Ekoloji)** | Ekoloji | Bireylerin bir alanda birbirinden eşit uzaklıkta yayılması. | Coğrafi / Fiziksel alan | Rekabet nedeniyle eşit aralıklı penguen yuvaları. 🐧 |
| **Dengeli Dağılımlı Dizi** | Matematik | Bir dizinin elemanlarının bir aralığı adil ve orantılı olarak doldurması. | Sayı dizisi (sequence) | Dizinin zamanla aralığın her yerine eşit yayılması. |

* **2. Normal Dağılım (Gaussian Distribution):**
  
  ---

<img width="512" height="772" alt="image" src="https://github.com/user-attachments/assets/427de5d9-f0c5-48be-9482-e46be14968c6" />


    * **Metafor (Çan Eğrisi Tepesi):** Doğada ve sosyal bilimlerde en sık karşılaşılan dağılımdır. Simetrik bir **çan** şeklindedir.
    * **Özellikleri:** Değerlerin çoğu ortalama ($\mu$) etrafında toplanır. Ortalamadan uzaklaştıkça bu değerlerin görülme sıklığı hızla azalır.
    * **Örnek:** İnsanların boyları, zeka seviyeleri (IQ), ölçüm hataları. Çoğu insan ortalama boydadır; çok uzun veya çok kısa insanlar çok daha azdır.

**Gaussian distribution**, also known as the **Normal distribution**, is defined as a continuous random variable characterized by its mean ($\mu$) and standard deviation ($\sigma$). It is often used to describe phenomena such as:

* Student marks
* Height
* Weight



[Normal distribution- Wikipedia](https://en.wikipedia.org/wiki/Normal_distribution)

### Düzgün Dağılım (Uniform Distribution) ve Normal Dağılım (Gaussian Distribution) Tablosu


| Özellik | Düzgün Dağılım (Uniform Distribution) | Normal Dağılım (Gaussian Distribution) |
| :--- | :--- | :--- |
| **PDF Grafiği (Şekli)** | **Dikdörtgen**. Belirli bir aralıkta olasılık sabittir. | **Çan Eğrisi**. Ortada bir tepe noktası vardır ve kenarlara doğru simetrik olarak azalır. |
| **Olasılıkların Dağılımı** | Tanımlanan aralıktaki **tüm sonuçlar eşit olasılıklıdır**. | Sonuçlar **ortalama etrafında kümelenir**. Ortalamadan uzaklaştıkça olasılık azalır. |
| **Tanımlayıcı Parametreler** | Başlangıç noktası ($a$) ve Bitiş noktası ($b$). | Ortalama ($\mu$) ve Standart Sapma ($\sigma$). |
| **En Olası Değer (Mod)** | Tek bir en olası değer yoktur; aralıktaki tüm değerler eşittir. | En olası değer, dağılımın merkezi olan ortalamadır ($\mu$). |
| **Yayılım Ölçütü** | Aralığın genişliğidir ($b-a$). | Standart sapmadır ($\sigma$). |
| **Karşılaştırmalı Örnek** | **Örnek:** Bir kafeye saat 14:00 ile 15:00 arasında herhangi bir anda gelen bir arkadaşınızı bekliyorsunuz. Arkadaşınızın bu 60 dakikalık zaman dilimindeki herhangi bir anda gelme olasılığı tamamen aynıdır. 14:10'da gelmesi ile 14:50'de gelmesi arasında olasılık farkı yoktur. | **Örnek:** Bir sınıftaki öğrencilerin bir sınavdan aldığı notları düşünelim. Notların çoğu sınıf ortalaması (örneğin 75 puan) etrafında toplanacaktır. 95-100 gibi çok yüksek veya 40-45 gibi çok düşük not alan öğrenci sayısı çok daha az olacaktır. |

 | Özellik | Kesikli Dağılım (Bilye Torbası) | Sürekli Dağılım (Su Bardağı) |
| :--- | :--- | :--- |
| **Veri Türü** | Sayılabilir (1, 2, 3...) | Ölçülebilir (1.5, 2.71, ...) |
| **Olasılık Fonk.** | PMF (Olasılık Kütle Fonksiyonu) | PDF (Olasılık Yoğunluk Fonksiyonu) |
| **Grafik** | Çubuk Grafik | Sürekli Eğri |
| **Tek Nokta Olasılığı**| `$P(X = c) > 0$` (Anlamlıdır) | `$P(X = c) = 0$` (Anlamsızdır) |
| **Aralık Olasılığı**| `$P(a \le X \le b)$` (Noktalar toplanır) | `$P(a \le X \le b)$` (Eğri altındaki alan) |
| **Örnekler** | Zar atışı, müşteri sayısı | Boy, kilo, sıcaklık, zaman |

 ---

 ## Olasılığın İki Farklı Dünyası: Kesikli ve Sürekli ( MINI-ÖZET)

Olasılık dünyası, ölçülen verinin doğasına göre iki ana krallığa ayrılır. Temel ayrım, değerlerin **sayılabilir** mi yoksa **ölçülebilir** mi olduğudur.

---

### 1. Kesikli (Discrete) Dünya

* **Metafor:** Bilye Torbası
* **Temel Fikir:** Değerler arasında geçiş yoktur. Sonuçlar yalnızca belirli, ayrı ve sayılabilir değerler alabilir.
    * *Örnek: Bir torbada sadece kırmızı ve mavi bilyeler vardır; "yarı kırmızı" bir bilye yoktur.*
* **Veri Tipi:** Genellikle tam sayılarla ifade edilir.
    * *Örnekler: Atılan bir zarın sonucu (1, 2, 3, 4, 5, 6), bir saatte gelen müşteri sayısı (10, 11, 12).*
* **Olasılık Sorusu:** "Bir olayın **tam olarak** gerçekleşme olasılığı nedir?" sorusu anlamlıdır.
    * *Örnek: `$P(\text{Zar} = 3)$` (Zarın tam 3 gelme olasılığı)*

### 2. Sürekli (Continuous) Dünya

* **Metafor:** Su Bardağı
* **Temel Fikir:** İki değer arasında sonsuz sayıda başka değer bulunabilir. Değerler bir aralık boyunca kesintisiz bir şekilde akar.
    * *Örnek: Bardaktaki su miktarı 150ml ile 151ml arasında herhangi bir değer olabilir (150.1, 150.11, 150.112...).*
* **Veri Tipi:** Genellikle bir aralıktaki reel sayılarla ifade edilir.
    * *Örnekler: Bir kişinin boyu, bir odanın sıcaklığı, bir işin tamamlanma süresi.*
* **Olasılık Sorusu:** "Bir sonucun **belirli bir aralıkta** olma olasılığı nedir?" sorusu anlamlıdır.
    * *Örnek: `$P(175 \le \text{Boy} \le 176)$` (Boyun 175cm ile 176cm arasında olma olasılığı).*

> **Önemli Not:** Tek bir noktanın olasılığı sıfır kabul edilir, çünkü sonsuz olasılık içinde tek bir noktayı tam isabet ettirmek imkansızdır.
