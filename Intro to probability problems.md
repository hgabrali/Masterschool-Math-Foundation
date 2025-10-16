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

---

<img width="774" height="370" alt="image" src="https://github.com/user-attachments/assets/fa728671-f5ed-450d-89aa-b001a651088d" />

# 📈 Güven Aralıkları ve Hata Payı İlişkisi (Confidence Intervals and Margin of Error)

Verilen soru, **güven aralıkları (confidence intervals)** ve **hata payı (margin of error)** arasındaki temel ilişkileri anlamaya yöneliktir. İpucu olarak verilen hata payı formülü, bu ilişkileri anlamak için anahtardır:

$$\text{margin of error} = Z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}$$

### Formül Bileşenleri:

* **Hata Payı (Margin of Error - ME):** Güven aralığının yarısıdır.
* $Z_{\alpha/2}$: Güven seviyesinden (confidence level) gelen kritik değerdir. **Güven seviyesi arttıkça, $Z_{\alpha/2}$ değeri de artar.**
* $\sigma$: Popülasyon standart sapmasıdır (sabit kabul edilir).
* $n$: Örneklem büyüklüğüdür (sample size).

---

## 🧐 Şık İncelemesi

### Şık 1:

> **Assuming a fixed margin of error, larger samples result in a larger confidence level.**
> (Sabit bir hata payı varsayarsak, daha büyük örneklemler daha büyük bir güven seviyesi sağlar.)

* **Matematiksel Kontrol:** Formülü düzenlersek: $Z_{\alpha/2} = \text{ME} \cdot \frac{\sqrt{n}}{\sigma}$.
* ME ve $\sigma$ sabitse, $Z_{\alpha/2}$ değeri $\sqrt{n}$ ile doğru orantılıdır. $n$ büyüdükçe, $Z_{\alpha/2}$ büyür. $Z_{\alpha/2}$ büyüdükçe, güven seviyesi de **artar**.
* **Bu ifade doğrudur.** ✅

### Şık 2:

> **Assuming a fixed sample size, higher confidence results in a smaller margin of error.**
> (Sabit bir örneklem büyüklüğü varsayarsak, daha yüksek güven daha küçük bir hata payı sağlar.)

* **Matematiksel Kontrol:** Güven seviyesi arttıkça, $Z_{\alpha/2}$ değeri **artar**. Formülde ($ME = Z_{\alpha/2} \cdot \frac{\sigma}{\sqrt{n}}$), $Z_{\alpha/2}$ arttığı için Hata Payı (ME) **büyür**.
* **Bu ifade yanlıştır.** ❌

### Şık 3:

> **Assuming a fixed confidence level, halving the margin of error requires a sample twice as large.**
> (Sabit bir güven seviyesi varsayarsak, hata payını yarıya indirmek için iki kat daha büyük bir örneklem gerekir.)

* **Matematiksel Kontrol:** Hata payını 2'ye bölmek için ($\text{ME}/\mathbf{2}$), $\sqrt{n}$'i $\mathbf{2}$ ile çarpmamız gerekir.
    $$\sqrt{n_{\text{yeni}}} = 2 \cdot \sqrt{n_{\text{eski}}} \implies n_{\text{yeni}} = 4 \cdot n_{\text{eski}}$$
* Yani hata payını yarıya indirmek için örneklemin **dört kat** büyümesi gerekir.
* **Bu ifade yanlıştır.** ❌

### Şık 4:

> **Assuming a fixed confidence level, larger samples result in a smaller margin of error.**
> (Sabit bir güven seviyesi varsayarsak, daha büyük örneklemler daha küçük bir hata payı sağlar.)

* **Matematiksel Kontrol:** Güven seviyesi sabitse, $Z_{\alpha/2}$ sabittir. Formülde $n$ paydada yer alır ve $\sqrt{n}$ olarak ters orantılıdır. $n$ büyüdükçe, $\frac{1}{\sqrt{n}}$ küçülür ve Hata Payı (ME) **küçülür**.
* **Bu ifade doğrudur.** ✅

---

## 💡 Cevap Seçimi (En Temel İlişki)

Soruda birden fazla doğru ifade bulunmaktadır (Şık 1 ve Şık 4). Ancak bu tarz çoktan seçmeli sorularda genellikle en bariz ve temel ilişkiyi anlatan cevap istenir.

* Şık 4, hipotez testlerinin temel ilkesi olan **örneklem büyüklüğü $\leftrightarrow$ hata payı** ilişkisini en basit haliyle ve doğru olarak ifade eder.
* Şık 4, diğer şıkların aksine, formülün en temel ve doğrulanmış sonucudur.

**Doğru Cevap:** **Assuming a fixed confidence level, larger samples result in a smaller margin of error.** (Sabit bir güven seviyesi varsayarsak, daha büyük örneklemler daha küçük bir hata payı sağlar.)

*(Not: Şık 1 de matematiksel olarak doğrudur, ancak Şık 4 en temel istatistiksel ilişkiyi anlatır.)*

<img width="754" height="258" alt="image" src="https://github.com/user-attachments/assets/9671134c-4a41-4687-bb99-6ec24f2be915" />

# 📉 Güven Aralığı Hata Payı Hesabı (t-Dağılımı)

Bu soru, popülasyon standart sapması bilinmediğinde ortalama için %95 güven aralığının hata payını (Margin of Error) ifade eden doğru matematiksel ifadeyi bulmayı amaçlamaktadır.

---

## 🔍 Problemin Analizi

| Parametre | Değer | Yorum |
| :--- | :--- | :--- |
| **Örneklem Büyüklüğü ($n$)** | $20$ | Küçük ($n<30$). |
| **Popülasyon Std. Sapması ($\sigma$)** | Bilinmiyor | **$t$-Dağılımı** kullanılmalıdır. |
| **Örneklem Std. Sapması ($s$)** | $10$ | $\sigma$ yerine $s$ kullanılacaktır. |
| **Güven Seviyesi** | $95\%$ | $\alpha = 0.05 \implies \alpha/2 = \mathbf{0.025}$ |

### Hata Payı (Margin of Error - ME) Formülü:

Popülasyon $\sigma$ bilinmediği için, $t$-Dağılımı kullanılır:

$$\text{ME} = t_{\alpha/2, df} \cdot \frac{s}{\sqrt{n}}$$

### 🛠️ Doğru İfadenin Kurulumu

1.  **Kritik Değer:** $\alpha/2 = 0.025$ olduğu için $t_{0.025}$ kullanılır.
2.  **Standart Hata (SE):** $\frac{s}{\sqrt{n}} = \frac{10}{\sqrt{20}}$

$$\text{ME} = t_{0.025} \cdot \frac{10}{\sqrt{20}}$$

---

## ✅ Doğru Cevap

Seçenekler arasında doğru ifade şudur:

$$\mathbf{t_{0.025} \cdot \frac{10}{\sqrt{20}}}$$


<img width="754" height="388" alt="image" src="https://github.com/user-attachments/assets/a1a4f6b8-b4ee-4a6a-913f-04461a9488ae" />

# 🦠 Anakütle Oranı için Hata Payı Hesabı (Confidence Interval for Proportion)

Bu soru, araştırmacıların elde ettiği verileri kullanarak, hayvanların hastalığı taşıma yüzdesi için \%90 güven seviyesindeki hata payını (Margin of Error) hesaplamayı amaçlamaktadır.

---

## 🔍 Problemin Analizi ve Çözümü

### 1. Verilen Parametreler

| Parametre | İfade/Değer | Açıklama |
| :--- | :--- | :--- |
| **Örneklem Büyüklüğü ($n$)** | $200$ | Toplam test edilen hayvan sayısı. |
| **Başarı Sayısı ($x$)** | $40$ | Hastalığı pozitif çıkan hayvan sayısı. |
| **Güven Seviyesi** | $90\%$ | |
| **Kritik Değer ($Z_{\alpha/2}$)** | $1.645$ | \%90 güven seviyesine karşılık gelen Z değeri. |

### 2. Örneklem Oranının ($\hat{p}$) Hesaplanması

$$\hat{p} = \frac{x}{n} = \frac{40}{200} = \mathbf{0.20}$$

### 3. Hata Payı (Margin of Error - ME) Formülü

Oranlar için hata payı formülü Z-dağılımı kullanır:

$$\text{ME} = Z_{\alpha/2} \cdot \sqrt{\frac{\hat{p}(1 - \hat{p})}{n}}$$

### 4. Hata Payının Hesaplanması 🧮

Değerler formüle yerleştirilir:

$$\text{ME} = 1.645 \cdot \sqrt{\frac{0.20(1 - 0.20)}{200}}$$

$$\text{ME} = 1.645 \cdot \sqrt{\frac{0.16}{200}}$$

$$\text{ME} = 1.645 \cdot \sqrt{0.0008}$$

$$\text{ME} \approx 1.645 \cdot 0.028284$$

$$\text{ME} \approx \mathbf{0.0465}$$

---

## ✅ Doğru Cevap

Hesaplanan hata payı **$0.0465$**'tir.

$$\mathbf{0.0465}$$

<img width="760" height="288" alt="image" src="https://github.com/user-attachments/assets/4a32999c-1d14-45f7-98e8-e19f2ecb8e0a" />

# 🚨 4. İstatistiksel Hata Tipleri Tanımı (Type I and Type II Errors)

Bu soru, istatistiksel hipotez testlerinde yer alan Birinci Tip Hata (Type I Error) ve İkinci Tip Hata (Type II Error) tanımlarının doğru ifadesini bulmayı amaçlamaktadır.

---

## ✅ Doğru Tanımlar

Hipotez testinde hataların matrisi şöyledir:

| Gerçek Durum | $H_0$ Reddedilir | $H_0$ Reddedilmez (Kabul Edilir) |
| :--- | :--- | :--- |
| **$H_0$ Doğru** | **Type I Error ($\alpha$)** | Doğru Karar |
| **$H_0$ Yanlış** | Doğru Karar | **Type II Error ($\beta$)** |

### Şık 1 İncelemesi:

* **Type I Error:** occurs when we **reject a null hypothesis that is true**. (Doğru olan $H_0$'ı reddetme.) $\implies$ **DOĞRU**
* **Type II Error:** occurs when we **accept a null hypothesis that is false**. (Yanlış olan $H_0$'ı kabul etme/reddedememe.) $\implies$ **DOĞRU**

### 🎯 Doğru Cevap

**Type I error occurs when we reject a null hypothesis that is true, while Type II error occurs when we accept a null hypothesis that is false.**

<img width="784" height="341" alt="image" src="https://github.com/user-attachments/assets/293c6ba3-8130-4138-828e-115735f8fcbe" />

# 🗺️ 5. Hipotez Testi Karar Verme Adımları (Hypothesis Testing Decision Steps)

Bu soru, Sıfır Hipotezini ($H_0$) reddedip reddetmeme kararını vermek için izlenmesi gereken genel adımların doğru sırasını sormaktadır. İstatistiksel geçerlilik için **anlamlılık seviyesi ($\alpha$) her zaman veriler analiz edilmeden önce belirlenmelidir.**

---

## ✅ Doğru Sıralama

Doğru sıralama, istatistiksel hipotez testinin mantıksal akışını takip eden ilk şıktır:

1.  **Set the significance level ($\alpha$)** 📉
2.  **Calculate the test statistic based on sample data** 🧮
3.  **Calculate the p-value** 📊
4.  **Compare the p-value with the significance level** ⚖️
5.  **Make a decision to reject or fail to reject ($H_0$)** 🛑

### Şıkların Karşılaştırması:

| Şık | Sıralama | Hata |
| :--- | :--- | :--- |
| **1 (Doğru)** | **$\alpha$ belirle** $\rightarrow$ $t$ hesapla $\rightarrow$ p-değeri hesapla $\rightarrow$ Karşılaştır $\rightarrow$ Karar ver. | Yok. |
| 2 | $t$ hesapla $\rightarrow$ **$\alpha$ belirle** $\rightarrow$ p-değeri hesapla... | $\alpha$ veriden önce belirlenmelidir. |
| 3 | p-değeri hesapla $\rightarrow$ **$\alpha$ belirle** $\rightarrow$ Karşılaştır... | $\alpha$ veriden önce belirlenmelidir. |

**Doğru Cevap:**

> **Set the significance level ($\alpha$), calculate the test statistic based on sample data, calculate the p-value, compare the p-value with the significance level, and make a decision to reject or fail to reject ($H_0$).**

<img width="761" height="280" alt="image" src="https://github.com/user-attachments/assets/55e8a97e-4586-4c33-b4e9-5acce6c33d65" />


# 🚀 6. Hipotez Testi Karar Verme (Kritik Değer Yaklaşımı)

Bu soru, yeni bir öğretim yönteminin öğrenci başarısını artırıp artırmadığını test eden bir hipotez testinde, kritik değer yaklaşımına göre karar vermeyi göstermektedir.

---

## 🔍 Problemin Analizi

| Parametre | İfade/Değer | Açıklama |
| :--- | :--- | :--- |
| **Hipotezler** | $H_1$: Yeni yöntem $\mathbf{>}$ performans sağlar. | **Sağ Kuyruk Testi** |
| **Hesaplanan Test İstatistiği** | $1.98$ | |
| **Kritik Değer** ($\alpha=0.05$) | $1.96$ | Reddetme bölgesinin başlangıç noktası. |

### Kritik Değer Kuralı:

Sağ Kuyruk Testinde:

$$\text{Test İstatistiği} > \text{Kritik Değer} \implies \text{H}_0 \text{ Reddedilir}$$

### Karar Verme 🛑

Hesaplanan değer ile kritik değer karşılaştırılır:

$$\mathbf{1.98 > 1.96}$$

Hesaplanan test istatistiği (1.98), kritik değer (1.96) eşiğini aşarak **reddetme bölgesine** düşmüştür.

---

## ✅ Sonuç

**Doğru Cevap:**

> **Yes, you reject the null hypothesis.**


<img width="803" height="314" alt="image" src="https://github.com/user-attachments/assets/3a364bbf-d403-4302-93b8-21641da90984" />

# ⚡️ 7. Enerji İçeceği Hipotez Testi: Test İstatistiği Hesabı

Bu soru, yeni bir enerji içeceğinin tepki sürelerini azalttığı iddiasını araştırmak için kullanılan tek örneklem $t$-testinin test istatistiğini hesaplamayı amaçlamaktadır.

---

## 🔍 Problemin Analizi

| Parametre | Değer | Açıklama |
| :--- | :--- | :--- |
| **İddia (Popülasyon Ortalaması, $\mu_0$)** | $1.05 \text{ saniye}$ | Enerji içeceği olmadan ortalama tepki süresi. |
| **Örneklem Ortalaması ($\bar{X}$)** | $0.95 \text{ saniye}$ | Enerji içeceği ile gözlemlenen ortalama. |
| **Örneklem Std. Sapması ($s$)** | $0.12 \text{ saniye}$ | Popülasyon $\sigma$ bilinmediği için $s$ kullanılır. |
| **Örneklem Büyüklüğü ($n$)** | $40$ | |

### Test İstatistiği Formülü

$\sigma$ bilinmediği için $t$-istatistiği formülü kullanılır:

$$t = \frac{\bar{X} - \mu_0}{s / \sqrt{n}}$$

### 🧮 Test İstatistiği Hesabı

Değerler formüle yerleştirilir:

$$t = \frac{0.95 - 1.05}{0.12 / \sqrt{40}}$$

$$t = \frac{-0.10}{0.12 / 6.3245}$$

$$t = \frac{-0.10}{0.01897}$$

$$t \approx \mathbf{-5.27}$$

---

## ✅ Doğru Cevap

Hesaplanan test istatistiği (t) yaklaşık **$-5.27$**'dir.

<img width="776" height="248" alt="image" src="https://github.com/user-attachments/assets/8d01fd4f-cdd1-4160-91b9-32e8f629812c" />


# 📉 8. P-Değeri Hesaplamasında Kullanılacak Dağılım

Bu soru, önceki problemde ($\sigma$ bilinmiyor, $n=40$) hesaplanan test istatistiğinin p-değerini bulmak için hangi olasılık dağılımının kullanılması gerektiğini sormaktadır.

---

## 🔍 Problemin Analizi ve Çözümü

### 1. Dağılımın Seçimi:

* **Kural:** Popülasyon standart sapması ($\sigma$) bilinmediğinde ve onun yerine örneklem standart sapması ($s$) kullanıldığında, test istatistiği ($T$) her zaman **$t$-Dağılımını** takip eder.

### 2. Serbestlik Derecesinin ($df$) Hesaplanması:

Tek örneklem $t$-testinde serbestlik derecesi şöyledir:

$$df = n - 1$$
$$\mathbf{df} = 40 - 1 = \mathbf{39}$$

### 3. Şıkların Değerlendirilmesi:

| Şık | İfade | Hata/Yorum |
| :--- | :--- | :--- |
| **Standard normal distribution** | Z dağılımı. | $\sigma$ bilinmediği için yanlış. |
| **$t$-Student distribution with 40 degrees of freedom** | $t$ dağılımı. | $df$ hatalı ($n$ yerine $n-1$ olmalı). |
| **Normal distribution with $\mu = 0.95$ and $\sigma = 0.12$** | Örneklem dağılımı. | Test istatistiği dağılımı değildir. |
| **$t$-Student distribution with 39 degrees of freedom** | **$t$ dağılımı.** | **Doğru $df$ ($40-1=39$).** |

---

## ✅ Doğru Cevap

**t-Student distribution with 39 degrees of freedom.**

<img width="792" height="305" alt="image" src="https://github.com/user-attachments/assets/a9a5ebcb-180f-4e9d-9ab8-c9d72b4d6cc3" />

# 📉 9. P-Değerinin Doğru Yorumu (p-Value Interpretation)

Bu soru, istatistiksel hipotez testlerinde p-değerinin ne anlama geldiğine dair doğru yorumu bulmayı amaçlamaktadır.

---

## 🔍 P-Değeri Tanımı

P-değeri, matematiksel olarak şu anlama gelir:

$$\text{p-value} = P(\text{Gözlemlenen veya daha aşırı sonuç} \mid H_0 \text{ Doğru})$$

* **$H_0$ (Sıfır Hipotezi):** Zarın adil olması.
* **p-value = 0.03:** Bu, zarın **adil olduğu varsayımı altında**, elde edilen sonuçları (veya daha aşırı sonuçları) rastgele görme olasılığının %3 olduğu anlamına gelir.

### Şık İncelemesi:

| Şık | İfade | Yorum |
| :--- | :--- | :--- |
| **1.** | Zarın adil olmama olasılığı %3'tür. | **Yanlış.** P-değeri hipotezin olasılığını ölçmez. |
| **2.** | Zarın adil olma olasılığı %3'tür. | **Yanlış.** P-değeri hipotezin olasılığını ölçmez. |
| **3.** | **Gözlemlenen sonuçları elde etme olasılığı (zarın adil olması şartıyla) %3'tür.** | **DOĞRU.** P-değerinin tanımına en uygun ifadedir ($P(\text{Veri} \mid H_0)$). |
| **4.** | Zarı atıp altı gelme olasılığı %97'dir. | **Yanlış.** Konuyla ilgisiz, alakasız bir olasılık değeridir. |

---

## ✅ Doğru Cevap

**The chance of producing the observer results (a fair die) is 3%.**


<img width="758" height="349" alt="image" src="https://github.com/user-attachments/assets/e3fe2319-f361-44f6-8118-0c556006591d" />


# 🔬 10. Bağımsız İki Örneklem $t$-Testi Senaryoları (Independent Two-Sample $t$-Test Scenarios)

Bu soru, **Bağımsız İki Örneklem $t$-Testi** (Independent Two-Sample $t$-Test) gerektiren senaryoları bulmayı amaçlamaktadır.

### Kural:

* **Bağımsız $t$-Testi:** Birbirinden **farklı ve bağımsız** iki grubun ortalamaları karşılaştırılır.
* **Eşli $t$-Testi:** **Aynı grubun** "önce/sonra" ölçümleri karşılaştırılır.

---

### Şık İncelemesi ve Test Kararı

| # | Senaryo | Grup İlişkisi | Doğru Test Türü |
| :---: | :--- | :--- | :--- |
| **1** | Aynı hastaların kan basıncı **önce/sonra**. | **Aynı grup / Bağımlı** | Eşli $t$-Testi |
| **2** | Aynı bireylerin tepki süresi **önce/sonra**. | **Aynı grup / Bağımlı** | Eşli $t$-Testi |
| **3** | İki **bağımsız** grubun **tıklama oranlarının** karşılaştırılması. | **Bağımsız** (Oran) | İki Oran Z-Testi (veya geniş $t$-testi kategorisi) |
| **4** | İki **bağımsız** öğrenci grubunun test skorlarının karşılaştırılması. | **Bağımsız** (Ortalama) | **Bağımsız İki Örneklem $t$-Testi** ✅ |
| **5** | Katılımcıların ağırlığı **önce/sonra**. | **Aynı grup / Bağımlı** | Eşli $t$-Testi |

---

## ✅ Doğru Cevaplar

Bağımsız iki örneklem $t$-Testinin temel tanımına en uygun senaryo 4'tür. Senaryo 3, bağımsız grupları karşılaştırdığı için mantıksal olarak bağımsız testler sınıfındadır.

* **Comparing the click-through rates of two independent groups of participants testing two different versions of a website homepage in an A/B testing environment.**
* **Comparing the test scores of two independent groups of students who received different teaching methods.**
