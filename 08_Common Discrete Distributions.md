
# ORTAK AYRIK OLASILIK DAĞILIMLARI ÜZERİNE KAPSAMLI VE KARŞILAŞTIRMA
**(COMPREHENSIVE AND COMPARATIVE EXPERT REPORT ON COMMON DISCRETE PROBABILITY DISTRIBUTIONS)**

---

## Kısım I: Giriş ve Teorik Temeller (Introduction and Theoretical Foundations)

### 1.1. Tanım ve Kapsam: Ayrık Olasılık Dağılımları

**Ayrık Olasılık Dağılımları**, sonuçları sayılabilir (*countable*) bir kümeden gelen rastgele değişkenleri (Random Variables) modellemek için kullanılır. Bu sonuçlar genellikle tam sayılardır (örn: bir madeni paranın iki kez atılmasında Tura gelme sayısı X = {0, 1, 2}). Bu yapı, ayrık dağılımları, **sayım verilerinin** (*count data*) analizinde temel araç haline getirir.

Sürekli dağılımların aksine, ayrık dağılımlarda her bir spesifik sonuç için net bir **olasılık atanır**.

### 1.2. Matematiksel Çerçeve: PMF, Beklenen Değer ve Varyans

Ayrık rastgele değişkenlerin tanımlanmasında kullanılan temel fonksiyon, **Olasılık Kütle Fonksiyonu (Probability Mass Function - PMF)** olarak adlandırılır. PMF, $P(X=x)$, rastgele değişken X'in tam olarak belirli bir $x$ değerini alma olasılığını verir.

**Kritik Koşul:** Rastgele değişkenin alabileceği tüm olası değerler kümesi üzerindeki PMF değerlerinin toplamının kesinlikle **1'e eşit** olması gerekir.

* **Beklenen Değer (Expected Value - μ):** Rastgele değişkenin uzun vadede alması beklenen ortalama değerdir. Merkezi eğilimin temel ölçüsüdür.
* **Varyans (Variance - $\sigma^2$):** Rastgele değişkenin beklenen değer etrafında ne kadar yayıldığının (belirsizlik veya risk) bir ölçüsüdür. Karekökü **Standart Sapmayı** verir.

---

## Kısım II: Temel Ayrık Dağılımların Matematiksel Anatomisi (Mathematical Anatomy of Key Discrete Distributions)

### 2.1. Bernoulli Dağılımı (Bernoulli Distribution)

Tek bir denemenin sonucunu (Başarı=1, Başarısızlık=0) modeller.

| Parametre | PMF | Beklenen Değer ($\mu$) | Varyans ($\sigma^2$) |
| :--- | :--- | :--- | :--- |
| $p$ (Başarı olasılığı) | $P(X=x) = p^x(1-p)^{1-x}$, $x \in \{0,1\}$ | $p$ | $p(1-p)$ |

### 2.2. Binom Dağılımı (Binomial Distribution)

Sabit sayıda ($n$) **bağımsız** ve özdeş Bernoulli denemesinin tekrarında elde edilen başarılı sonuç sayısını ($k$) modeller.

| Parametreler | PMF | Beklenen Değer ($\mu$) | Varyans ($\sigma^2$) |
| :--- | :--- | :--- | :--- |
| $n$ (Deneme Sayısı), $p$ (Başarı Olasılığı) | $P(X=k) = \binom{n}{k} p^k (1-p)^{n-k}$ | $np$ | $np(1-p)$ |

### 2.3. Geometrik Dağılım (Geometric Distribution)

Bir Bernoulli sürecinde **ilk başarının** elde edilmesi için gereken toplam deneme sayısını ($k$) modeller.

| Parametre | PMF | Beklenen Değer ($\mu$) | Varyans ($\sigma^2$) |
| :--- | :--- | :--- | :--- |
| $p$ (Başarı Olasılığı) | $P(X=k) = (1-p)^{k-1}p$ | $1/p$ | $(1-p)/p^2$ |

* **Temel Özellik:** Ayrık alandaki tek **"hafızasız"** (*memoryless*) dağılımdır.

### 2.4. Hipergeometrik Dağılım (Hypergeometric Distribution)

Binom'un aksine, örnekleme işlemi **yedeklemesiz** (*without replacement*) yapılır, bu nedenle denemeler **bağımlıdır**.

| Parametreler | PMF | Beklenen Değer ($\mu$) | Varyans ($\sigma^2$) |
| :--- | :--- | :--- | :--- |
| $N$ (Pop. Büyüklüğü), $m$ (İlgi Öğesi), $n$ (Örneklem) | $P(X=k) = \frac{\binom{m}{k}\binom{N-m}{n-k}}{\binom{N}{n}}$ | $n \frac{m}{N}$ | $n \frac{m}{N} \frac{N-m}{N} \frac{N-n}{N-1}$ |

* **Özellik:** Varyans formülündeki $\frac{N-n}{N-1}$ terimi, **Sonlu Popülasyon Düzeltme Faktörü** olarak bilinir.

### 2.5. Poisson Dağılımı (Poisson Distribution)

Belirli bir zaman aralığında veya mekanda meydana gelen **nadir olayların** sayısını ($k$) modellemek için kullanılır.

| Parametre | PMF | Beklenen Değer ($\mu$) | Varyans ($\sigma^2$) |
| :--- | :--- | :--- | :--- |
| $\lambda$ (Ortalama Olay Oranı) | $P(X=k) = \frac{e^{-\lambda} \lambda^k}{k!}$ | $\lambda$ | $\lambda$ |

* **Ayırt Edici Özellik:** Beklenen Değer ($\mu$) ve Varyans ($\sigma^2$) birbirine **eşittir** ($\mu = \sigma^2 = \lambda$).
* **Aşırı Yayılım (Overdispersion):** Gerçek veride $\sigma^2 > \mu$ ise, Poisson varsayımlarının (bağımsızlık, sabit oran) ihlal edildiği ve Negatif Binom gibi modellere geçilmesi gerektiği anlaşılır.

---

## Kısım III: Tarihsel Gelişim ve Kronolojik Sıralama

| Dağılım (Distribution) | Kurucu (Founder) | Ana Eser (Key Publication) | Yayım Yılı (Publication Year) | Kronolojik Sıra (Order) |
| :--- | :--- | :--- | :--- | :--- |
| **Bernoulli / Binom** | **Jacob Bernoulli** | *Ars Conjectandi* | **1713** | **1.** (Temel) |
| **Poisson** | **Siméon Denis Poisson** | *Recherches sur la probabilité des jugements...* | **1837** | **2.** |
| **Hipergeometrik** | (Teorik Gelişim) | (Örnekleme Teorisi Kaynakları) | **19. Yüzyıl Başları** | **3.** |

---

## Kısım IV: Karşılaştırmalı Analiz ve Dağılımlar Arasındaki İlişkiler

### 4.1. Bağımlılık ve Örnekleme Metodu: Binom vs. Hipergeometrik

| Kriter | Binom Dağılımı | Hipergeometrik Dağılım |
| :--- | :--- | :--- |
| **Örnekleme** | Yedeklemeli (With Replacement) | **Yedeklemesiz (Without Replacement)** |
| **Bağımlılık** | Bağımsız Denemeler | **Bağımlı Denemeler** |
| **Kullanım Zorunluluğu** | $n/N$ oranı küçükse | **$n/N > 0.05$ ise (Sonlu Popülasyon)** |
| **Varyans Etkisi** | Daha yüksek risk/belirsizlik tahmini | **FPC Faktörü nedeniyle daha düşük varyans ve gerçekçi tahmin** |

### 4.2. Yoğunluk ve Nadir Olaylar: Binom vs. Poisson

* **İlişki:** Poisson, Binom dağılımının bir **limit durumudur**.
* **Yakınsama Koşulları:** Deneme sayısı $n \rightarrow \infty$, başarı olasılığı $p \rightarrow 0$ iken, ortalama olay oranı $\lambda = np$ **sabit** kalır.
* **Üstünlük:** Sonsuz potansiyel denemenin olduğu (nadir olaylar) ve olay oranının ($\lambda$) sabit olduğu durumlarda Poisson daha basit ve uygundur.

### 4.3. Tekrarlama Yapısı: Binom, Geometrik ve Negatif Binom

* **Binom:** Sabit $n$ denemesi içindeki başarı sayısını sayar.
* **Geometrik:** **İlk başarıya** ulaşana kadar gereken toplam deneme sayısını sayar. (Negatif Binom'un $r=1$ özel hali)
* **Negatif Binom:** $r$ sayıda başarı elde edilene kadar geçen toplam deneme sayısını sayar.

#### Ortak Ayrık Dağılımların Karşılaştırmalı Matematiksel Özellikleri

| Dağılım | Parametreler | PMF | Beklenen Değer ($\mu$) | Varyans ($\sigma^2$) | Temel Varsayım |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Bernoulli** | $p$ | $p^x(1-p)^{1-x}$ | $p$ | $p(1-p)$ | Tek Bağımsız Deneme |
| **Binom** | $n, p$ | $\binom{n}{k} p^k (1-p)^{n-k}$ | $np$ | $np(1-p)$ | Sabit $n$ Deneme, Bağımsızlık |
| **Geometrik** | $p$ | $(1-p)^{k-1}p$ | $1/p$ | $(1-p)/p^2$ | İlk Başarıya Kadar Geçen Deneme, Bağımsızlık |
| **Poisson** | $\lambda$ | $\frac{e^{-\lambda} \lambda^k}{k!}$ | $\lambda$ | $\lambda$ | Bağımsız Olaylar, Sabit Oran $\lambda$ |
| **Hipergeo.** | $N, m, n$ | $\frac{\binom{m}{k}\binom{N-m}{n-k}}{\binom{N}{n}}$ | $n \frac{m}{N}$ | $n \frac{m}{N} \frac{N-m}{N} \frac{N-n}{N-1}$ | Yedeklemesiz Örnekleme, Bağımlılık |

---

## Kısım VI: Sonuç ve Uzman Önerileri

### 6.1. Model Seçiminde Kritik Faktörler ve Uzmanlık Önerileri

1.  **Bağımlılık ve Örnekleme Mekanizması Kontrolü:**
    * Eğer $N$ sonluysa ve **$n/N > 0.05$** ise, **Hipergeometrik** dağılım kullanmak zorunludur. Yanlış model seçimi (Binom) risk tahminlerinin hatalı olmasına yol açar.
2.  **Varyansın Ortalama İle Karşılaştırılması (Aşırı Yayılım Analizi):**
    * Poisson varsayımı $\mu = \sigma^2$'dır. Eğer verilerde **$\sigma^2 > \mu$ (Aşırı Yayılım)** gözlemlenirse, Poisson varsayımları ihlal edilmiştir; **Negatif Binom** gibi daha esnek dağılımlara geçiş yapılmalıdır.
3.  **Yaklaşım Koşullarının Doğrulanması (Konverjans):**
    * Binom'dan Poisson'a geçiş yapmadan önce $n$ yeterince büyük ve $p$ yeterince küçük (nadir olay) koşullarının sağlandığından emin olun.








---
# Common Discrete Distributions

<img width="779" height="183" alt="image" src="https://github.com/user-attachments/assets/e06ad81a-021e-4d1b-9415-0fac19c28e4f" />

<img width="750" height="497" alt="image" src="https://github.com/user-attachments/assets/18268b86-a0c1-46aa-bc68-602ae6590a3b" />


<img width="832" height="649" alt="image" src="https://github.com/user-attachments/assets/3234ca36-2b1a-478f-a939-a429407fe833" />

<img width="774" height="676" alt="image" src="https://github.com/user-attachments/assets/c4e6c7b0-ad1e-4929-905e-b2dc3052b9a2" />

* The Python code snippets illustrate how to compute and visualise these distributions using scipy.stats.

* **Colab Notebook:** [Common Discrete Distributions (Google Colab)](https://colab.research.google.com/drive/184bGblS6BrftHLSQ4diAIBh4v4ol4Y63)

---

