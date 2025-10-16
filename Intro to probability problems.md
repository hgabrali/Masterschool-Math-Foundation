# Permütasyon ve Kombinasyon Problemleri

Aşağıda, kombinatorik alanında sıkça karşılaşılan permütasyon ve kombinasyon problemlerine dair çözümler bulunmaktadır.

---

### 1. 7 koşucunun bir yarışta ilk 3 sıraya kaç farklı şekilde yerleşebileceği?

Bu, bir **permütasyon (sıralama)** problemidir, çünkü ilk 3 pozisyondaki sıralama önemlidir. (Örneğin, 1. Ayşe, 2. Bora farklı bir sonuçtur; 1. Bora, 2. Ayşe farklı bir sonuçtur.)

Permütasyon formülü $P(n, k) = \frac{n!}{(n-k)!}$ şeklindedir.
Burada $n=7$ (toplam koşucu sayısı) ve $k=3$ (ilk 3 pozisyon) olarak verilmiştir.

**Hesaplama:**
$$P(7, 3) = \frac{7!}{(7-3)!} = \frac{7!}{4!} = 7 \times 6 \times 5 = 210$$

Yani, 7 koşucu bir yarışta ilk 3 sıraya **210** farklı şekilde yerleşebilir.

---

### 2. A, B, C, D, E harfleri kullanılarak, tekrar etmeden kaç farklı 5 harfli şifre oluşturulabilir?

Bu da bir **permütasyon (sıralama)** problemidir, çünkü bir şifrede harflerin sırası önemlidir ve tekrar yoktur.

Toplam 5 harf (A, B, C, D, E) var ve 5 harfli bir şifre oluşturulacak. Tekrar olmadığı için her harf sadece bir kez kullanılabilir.

Bunu hesaplamanın iki yolu vardır:

**Yol 1: Çarpım Kuralı**
* İlk konum için 5 seçeneğiniz var.
* İkinci konum için kalan 4 seçeneğiniz var.
* Üçüncü konum için kalan 3 seçeneğiniz var.
* Dördüncü konum için kalan 2 seçeneğiniz var.
* Beşinci konum için kalan 1 seçeneğiniz var.

Toplam yol sayısı:
$$5 \times 4 \times 3 \times 2 \times 1 = 120$$

**Yol 2: Permütasyon Formülü**
Bu, $n$ farklı öğenin tümünün sıralandığı özel bir permütasyon durumudur, yani $P(n, n) = n!$.
Burada $n=5$ olduğundan:
$$P(5, 5) = 5! = 120$$

Yani, 5 harf kullanılarak, tekrar etmeden **120** farklı 5 harfli şifre oluşturulabilir.

---

### 3. 10 kişilik bir gruptan 4 kişilik bir takım kaç farklı şekilde oluşturulabilir?

Bu bir **kombinasyon** problemidir, çünkü bir takım oluşturulurken kişilerin seçilme sırası önemli değildir; önemli olan takımın kendisidir. Yani, "Ayşe, Bora, Cem, Derya" takımını seçmek ile "Bora, Ayşe, Derya, Cem" takımını seçmek aynı takımdır.

Kombinasyon formülü $C(n, k) = \binom{n}{k} = \frac{n!}{k!(n-k)!}$ şeklindedir.
Burada $n=10$ (toplam kişi sayısı) ve $k=4$ (takıma seçilecek kişi sayısı) olarak verilmiştir.

**Hesaplama:**
$$C(10, 4) = \frac{10!}{4!(10-4)!} = \frac{10!}{4!6!}$$

Faktöriyelleri açalım ve sadeleştirelim:
$$C(10, 4) = \frac{10 \times 9 \times 8 \times 7 \times 6!}{4! \times 6!} = \frac{10 \times 9 \times 8 \times 7}{4 \times 3 \times 2 \times 1}$$
$$C(10, 4) = \frac{5040}{24}$$

Sadeleştirmeleri yapalım:
$$C(10, 4) = 10 \times 3 \times 7 = 210$$

Yani, 10 kişilik bir gruptan **210** farklı 4 kişilik takım oluşturulabilir.

---

### 4. Bir torbada 6 farklı renk top bulunmaktadır. Bu 6 topun hepsini çekip bir sıraya kaç farklı şekilde dizebilirsiniz?

Bu bir **permütasyon (sıralama)** problemidir, çünkü topları hem çekiyor hem de **bir sıra halinde düzenliyorsunuz**, bu da sıranın önemli olduğu anlamına gelir. Ayrıca, 6 farklı top olduğu ve tüm 6 topu düzenlediğiniz belirtiliyor.

Toplam $n=6$ farklı top var ve bu 6 topun hepsini sıralamak istiyoruz ($k=6$).

Bu, $n$ farklı öğenin tümünün sıralanması durumudur ve $n!$ (n faktöriyel) ile hesaplanır.

**Hesaplama:**
$$6! = 6 \times 5 \times 4 \times 3 \times 2 \times 1 = 720$$

Yani, 6 farklı topu çekip bir sıraya **720** farklı şekilde dizebilirsiniz.

---

### 5. 52 kartlık bir desteden, bir iskambil oyununda eliniz için 5 kartı kaç farklı şekilde seçebilirsiniz?

Bu bir **kombinasyon** problemidir, çünkü bir kart oyununda elinize gelen 5 kartın sırası önemli değildir; önemli olan hangi 5 kartın elinizde olduğudur.

Kombinasyon formülü $C(n, k) = \binom{n}{k} = \frac{n!}{k!(n-k)!}$ şeklindedir.
Burada $n=52$ (toplam kart sayısı) ve $k=5$ (seçilecek kart sayısı) olarak verilmiştir.

**Hesaplama:**
$$C(52, 5) = \frac{52!}{5!(52-5)!} = \frac{52!}{5!47!}$$

Faktöriyelleri açıp sadeleştirelim:
$$C(52, 5) = \frac{52 \times 51 \times 50 \times 49 \times 48 \times 47!}{5 \times 4 \times 3 \times 2 \times 1 \times 47!}$$
$$C(52, 5) = \frac{52 \times 51 \times 50 \times 49 \times 48}{5 \times 4 \times 3 \times 2 \times 1}$$

Paydadaki değer: $5 \times 4 \times 3 \times 2 \times 1 = 120$.

Şimdi sadeleştirmeleri yapalım:
* $\frac{50}{5 \times 2} = \frac{50}{10} = 5$
* $\frac{48}{4 \times 3} = \frac{48}{12} = 4$
* $\frac{51}{1} \rightarrow \text{Bu adımda sadeleştirme için 3'ü kullanabiliriz, 51/3 = 17.}$

Yani çarpım:
$$C(52, 5) = 52 \times \frac{51}{3} \times \frac{50}{5 \times 2} \times 49 \times \frac{48}{4}$$
$$C(52, 5) = 52 \times 17 \times 5 \times 49 \times 4$$

Bu çarpımın sonucu:
$$C(52, 5) = 2,598,960$$

Yani, 52 kartlık bir desteden, bir iskambil oyununda eliniz için **2,598,960** farklı şekilde 5 kart seçebilirsiniz.


---

### Asagidaki görseller, Makine Öğrenimi ve Veri Biliminde A/B testlerinin temeli olan İki Örneklem Oran Testi (Two Sample Test for Proportions) konusunu tüm detaylarıyla, varsayımlarıyla ve bir örnek üzerinden açıklamaktadır.

<img width="757" height="719" alt="image" src="https://github.com/user-attachments/assets/21a89272-62b2-41e4-856a-af30c0efa995" />

<img width="795" height="611" alt="image" src="https://github.com/user-attachments/assets/1f5a7b2b-3233-4145-aeba-6b6f948c3915" />


<img width="788" height="459" alt="image" src="https://github.com/user-attachments/assets/5de08dc9-db3a-4047-bb58-48658a807ce3" />

<img width="811" height="572" alt="image" src="https://github.com/user-attachments/assets/e752f39c-90f4-494c-a136-412e3df43b42" />


<img width="801" height="718" alt="image" src="https://github.com/user-attachments/assets/dd7fc0fc-aecf-4042-a613-e39ae78b1ad7" />

<img width="711" height="592" alt="image" src="https://github.com/user-attachments/assets/47dfc382-55ad-4fb7-9965-c0c78eba1a20" />


# 📊 İki Örneklem Oran Testi (Two Sample Test for Proportions)

Bu test, birbirinden bağımsız iki popülasyonun belirli bir özelliğe sahip olma **oranları** ($p_1$ ve $p_2$) arasında istatistiksel olarak anlamlı bir fark olup olmadığını belirlemek için kullanılır.

---

## 1. Genel Durum ve Tanımlar (General Case) 📝

İki popülasyonu karşılaştırmak istediğimizde kullanılan temel parametreler şunlardır:

* **$p_1 - p_2$:** İki grup arasındaki **popülasyon oranı farkıdır**. (Örn: Chicago ve New York'ta arabası olan hane oranları arasındaki fark).
* **$x$:** Birinci grupta (popülasyon 1) belirtilen kategoriye sahip **gözlemlenen birey sayısıdır** (Örn: Chicago'da arabası olan hane sayısı).
* **$y$:** İkinci grupta (popülasyon 2) belirtilen kategoriye sahip **gözlemlenen birey sayısıdır** (Örn: New York'ta arabası olan hane sayısı).
* **$n_1$:** Birinci grubun **örneklem büyüklüğü** (Örn: Chicago örneklem büyüklüğü).
* **$n_2$:** İkinci grubun **örneklem büyüklüğü** (Örn: New York örneklem büyüklüğü).

---

## 2. Test İstatistiğinin Hesaplanması ve Standartlaştırma 🧮

Oran farklarını test ederken, Normal Dağılım yaklaşımını kullanırız. Ancak $p_1$ ve $p_2$ bilinmediği için özel bir standartlaştırma (pooled estimate) gerekir.

### A. Popülasyon Oranlarının Tahmini ($\hat{p}$)

Popülasyon oranları ($p_1$ ve $p_2$) bilinmediği için, örneklemlerden tahmin edilir:

$$\hat{p}_1 = \frac{X}{n_1} \quad \text{ve} \quad \hat{p}_2 = \frac{Y}{n_2}$$

Alternatif hipotez testi için en iyi yaklaşım, $\Delta = p_1 - p_2$ farkının dağılımını bulmaktır:

$$\hat{\Delta} = \hat{p}_1 - \hat{p}_2$$

### B. Sıfır Hipotezi ($H_0$) Altında Standartlaştırma (Z İstatistiği) 🔬

Eğer **Sıfır Hipotezi ($H_0: p_1 = p_2$ veya $p_1 - p_2 = 0$) doğruysa**, iki popülasyon oranının da aynı $p$ değerine sahip olduğu varsayılır. Bu durumda, $p$'nin en iyi tahminini elde etmek için iki örneği **birleştiririz (pooled estimate)**.

#### Birleştirilmiş Oran Tahmini ($\hat{p}$):

$$\hat{p} = \frac{\text{Toplam Başarı Sayısı}}{\text{Toplam Örneklem Büyüklüğü}} = \frac{X + Y}{n_1 + n_2}$$

#### Z-İstatistiği (Genel Form):

$\hat{p}$ kullanılarak standartlaştırılmış Z istatistiği elde edilir ve bu, Standart Normal Dağılımı ($N(0, 1)$) takip eder:

$$Z = \frac{\hat{p}_1 - \hat{p}_2 - 0}{\sqrt{\hat{p}(1-\hat{p})\left(\frac{1}{n_1} + \frac{1}{n_2}\right)}} \sim N(0, 1)$$

# 📉 3. Hipotez Tipleri ve P-Değeri (p-value) Hesaplama

Hipotez türüne bağlı olarak p-değeri ifadesi ve reddetme bölgesi değişir:

| Test Türü | Hipotezler | P-Değeri İfadesi | Grafiksel Bölge |
| :--- | :--- | :--- | :--- |
| **Sağ Kuyruk** ➡️ | $H_0: p_1 - p_2 = 0$ vs. $H_1: p_1 - p_2 > 0$ | $p\text{-value} = \mathbf{P(Z > z)}$ | Hesaplanan $z$'nin sağında kalan alan. |
| **Sol Kuyruk** ⬅️ | $H_0: p_1 - p_2 = 0$ vs. $H_1: p_1 - p_2 < 0$ | $p\text{-value} = \mathbf{P(Z < z)}$ | Hesaplanan $z$'nin solunda kalan alan. |
| **Çift Kuyruk** ↔️ | $H_0: p_1 - p_2 = 0$ vs. $H_1: p_1 - p_2 \neq 0$ | $p\text{-value} = \mathbf{P(|Z| > |z|)}$ | Hesaplanan $z$'nin mutlak değerinin ($\pm |z|$) her iki kuyruğunda kalan alanların toplamı. |

# 🏙️ 4. Örnek Uygulama ve Karar Verme

**Örnek Senaryo:** Chicago ($p_1$) ve New York'ta ($p_2$) arabası olan hane oranları farklı mı?

| Parametre | Değer/İfade | Açıklama |
| :--- | :--- | :--- |
| **Hipotezler** | $H_0: p_1 = p_2$ vs. $H_1: p_1 \neq p_2$ | **Çift Kuyruk Testi** |
| **Anlamlılık Seviyesi** | $\alpha = 0.05$ | |
| **Veriler (Grup 1)** | $n_1=100$, $x=62$ (Chicago) | |
| **Veriler (Grup 2)** | $n_2=120$, $y=58$ (New York) | |

---

## A. Birleştirilmiş Oran ($\hat{p}$) ve Z-İstatistiği Hesabı 🧮

### Birleştirilmiş Oran ($\hat{p}$):

$$\hat{p} = \frac{x + y}{n_1 + n_2} = \frac{62 + 58}{100 + 120} = \frac{120}{220} \approx \mathbf{0.5455}$$

### Gözlemlenen Z-İstatistiği ($z$):

$$z = \frac{\frac{62}{100} - \frac{58}{120} - 0}{\sqrt{\frac{120}{220}\left(1 - \frac{120}{220}\right)\left(\frac{1}{100} + \frac{1}{120}\right)}} \approx \mathbf{2.0271}$$

---

## B. P-Değeri Hesaplama ve Sonuç 📉

Bu bir çift kuyruk testi olduğu için, p-değeri $z=2.0271$ ve $z=-2.0271$ değerlerinin dışındaki toplam alanı verir:

$$\text{p-value} = \mathbf{P(|Z| > 2.0271)} = \mathbf{0.04265}$$

---

## C. Karar (Conclusion) ✅

p-değeri anlamlılık seviyesi ($\alpha$) ile karşılaştırılır:

$$\text{p-value} (0.04265) < \alpha (0.05)$$

**Sonuç:** p-değeri, anlamlılık seviyesinden **küçüktür**. Bu, Sıfır Hipotezini ($H_0$) **redd etmek** için yeterli kanıt olduğu sonucuna varıldığı anlamına gelir.

**Yorum:** %5 anlamlılık seviyesinde, Chicago ve New York'taki arabası olan hane oranlarının **farklı olduğu kabul edilir**.

# 5. Testin Geçerlilik Koşulları (Assumptions) ✅

Bu sonuçların geçerli olması için aşağıdaki koşulların sağlanması gerekir (Çoğunlukla **Normal Dağılım Yaklaşımının** doğru olması için):

1.  **Bağımsız Basit Rastgele Örneklemler:** İki popülasyondan bağımsız basit rastgele örneklem alınmalıdır ve bu örneklemler de birbirinden bağımsız olmalıdır.
2.  **Büyük Popülasyon Varsayımı:** Her popülasyon büyüklüğü, örneklem büyüklüğünün en az **20 katı** olmalıdır (bağımsızlığı sağlamak için).
3.  **İki Kategori:** Her örneklemdeki bireyler, belirtilen kategoriye ait olup olmamalarına göre iki kategoriye ayrılabilmelidir (**ikili/binom dağılım yapısı**).
4.  **Başarı ve Başarısızlık Sayısı:** Her bir örneklemde, belirtilen kategorideki **başarı sayısı** ($x$) ve **başarısızlık sayısı** ($n - x$) **en az 10** olmalıdır. Bu koşul, $H_0$ doğru olduğunda Gauss (Normal) yaklaşımının geçerli olması için kritik öneme sahiptir.

