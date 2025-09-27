

[Point Estimate](https://colab.research.google.com/drive/1DDG5edu2A6xDJ78-zHiiySWaI3_o7qHC#scrollTo=ua2bXEZHAgyr)

## Point Estimate

### Introduction

In statistics, a **point estimate** is a single value or statistic used to estimate an unknown population parameter. Such estimates provide a "best guess" for the value of a population parameter, such as the population mean or population proportion.

---

### Types of Point Estimates

#### 1. Point Estimate of the Mean

The sample mean, $\bar{x}$, is often used as the point estimate for the population mean, $\mu$.
$$
\hat{\mu} = \bar{x}
$$
where $\hat{\mu}$ is the point estimate of the population mean, and $\bar{x}$ is the sample mean.

* **Example: Estimating the Mean Height of a Group of People**
    * Suppose you are conducting a survey to estimate the average height of adult women in a city. You randomly sample 50 women, and their heights (in cm) are recorded. The sample mean height is calculated to be 164 cm.
    * In this case, **164 cm** is the point estimate for the population mean height. This value is used as a "best guess" for the true average height of all adult women in the city.

#### 2. Point Estimate of the Proportion

The sample proportion, $\hat{p}$, is used to estimate the population proportion, $p$.
$$
\hat{p} = \frac{x}{n}
$$
where $x$ is the number of successes and $n$ is the sample size.

* **Example: Estimating the Proportion of Voters Who Support a Candidate**
    * You want to estimate the proportion of voters who support a particular candidate. You take a random sample of 200 voters, and 120 of them indicate support. The sample proportion is calculated as:
    * `120 / 200 = 0.60`
    * In this case, **0.60 (or 60%)** is the point estimate for the proportion of all voters who support the candidate.

#### 3. Point Estimate of the Variance

The sample variance, $s^2$, can be used to estimate the population variance, $\sigma^2$.
$$
\hat{\sigma}^2 = s^2 = \frac{\sum_{i=1}^{n}(x_i - \bar{x})^2}{n-1}
$$
where $\hat{\sigma}^2$ is the point estimate of the population variance, $\bar{x}$ is the sample mean, and $x_i$ represents each value in the sample.

* **Example: Estimating the Variance in Test Scores**
    * You are analysing the test scores of 30 students. After calculating the sample mean, you find the sample variance is 25.
    * In this case, **25** is the point estimate for the population variance of test scores for all students in the class.

#### 4. Variance of the Proportion Estimate

The variance of the proportion estimate is given by the formula:
$$
Var(\hat{p}) = \frac{\hat{p}(1-\hat{p})}{n}
$$
where $\hat{p}$ is the sample proportion and $n$ is the sample size.

---

### Properties of Point Estimates

* **Unbiased:** A point estimate is said to be unbiased if the expected value of the estimate equals the true population parameter.
* **Efficient:** A point estimate is efficient if it has the smallest possible variance among all unbiased estimators.
* **Consistent:** A point estimate is consistent if it converges to the true population parameter as the sample size increases.

--- 

# Example:  Estimating Mean and Variance using Python

"Nokta Tahmini" kavramının Python'da `numpy` kütüphanesi kullanılarak nasıl hayata geçirildiğini gösteriyor. Gelin bu kodu, çıktılarını ve arkasındaki mantığı adım adım, nelere dikkat etmemiz gerektiğini vurgulayarak açıklayalım.

---

### Problemin Amacı (Senaryo)

Elimizde gerçek bir popülasyon (örneğin bir okuldaki tüm öğrenciler) yok. Ancak bu popülasyonu temsil ettiğini varsaydığımız 50 kişilik bir **örneklemimiz** (bir sınıf) var. Amacımız, sadece bu 50 kişilik küçük grubun verilerine bakarak, okuldaki **tüm öğrencilerin** sınav notlarının ortalaması ve varyansı hakkında **en iyi tahminlerimizi** yapmaktır.

* **Metaforla Düşünelim:** Aşçı, dev çorba kazanının (popülasyon) tadını merak ediyor. Bütün kazanı tadamayacağı için, içinden bir kaşık dolusu (50 öğrenci) alıyor. Şimdi bu kaşığın içindekilere bakarak (veriyi analiz ederek), bütün kazanın tadı (popülasyon parametreleri) hakkında "en iyi tahminlerini" yapacak.

---

### Kodun Adım Adım Açıklaması

#### 1. Veri Simülasyonu (Kaşığı Doldurmak)

```python
import numpy as np

# Simulate the exam scores of 50 students (random sample)
np.random.seed(42) # For reproducibility
scores = np.random.randint(50, 100, size=50) # Generate random scores between 50 and 100
```

* **Ne Yapıyor?** Gerçek verimiz olmadığı için, 50 ile 100 arasında rastgele 50 adet tam sayı üreterek 50 öğrencinin sınav notunu simüle ediyoruz (taklit ediyoruz).

* **Nelere Dikkat Etmeli?** np.random.seed(42) satırı çok önemlidir. Bu, "rastgelelik" sürecini sabitler. Yani bu kodu kim çalıştırırsa çalıştırsın, herkesin scores listesi aynı "rastgele" sayılardan oluşur. Bu, deneylerin tekrarlanabilir olmasını sağlar.

#### 2.  Ortalama için Nokta Tahmini (Kaşıktaki Çorbanın Ortalama Tuzluluğu)

# Calculate the point estimate for the mean (sample mean)
mean_estimate = np.mean(scores)

* **Ne Yapıyor?** 50 öğrencinin notlarının aritmetik ortalamasını (Örneklem Ortalaması,  
x
ˉ
 ) hesaplıyor.

* **Yorum:** Bu, yapabileceğimiz en basit ve en sezgisel tahmindir. Popülasyonun gerçek ortalaması (μ) hakkında hiçbir bilgimiz yokken, en iyi tahminimiz elimizdeki örneklemin ortalamasıdır.

### 3. Varyans için Nokta Tahmini (Kaşıktaki Çorbanın Tat Dağınıklığı)

# Calculate the point estimate for the variance (sample variance)
variance_estimate = np.var(scores, ddof=1) # ddof=1 to calculate sample variance

* **Ne Yapıyor?** 50 öğrencinin notlarının **örneklem varyansını** ($s^2$) hesaplıyor.
* **NELERE DİKKAT ETMELİ? (En Kritik Kısım):** Buradaki en önemli parametre `ddof=1`'dir.
    * **`ddof` Nedir?** "Delta Degrees of Freedom" anlamına gelir ve varyans formülünün paydasındaki değeri belirler.
    * **`ddof=0` (Varsayılan):** Paydaya `$n$` yazar. Bu, elinizdeki verinin **popülasyonun tamamı** olduğunu varsaydığınızda kullanılır.
    * **`ddof=1` (Kullanmamız Gereken):** Paydaya `$n-1$` yazar. Bu, elinizdeki verinin bir **örneklem** olduğunu ve bu örneklemi kullanarak popülasyon varyansını **tahmin etmeye** çalıştığınızı belirtir. Matematiksel olarak, paydaya `$n-1$` yazmak, tahminimizin daha isabetli ve **yansız (unbiased)** olmasını sağlar.
* **Özetle:** Popülasyonu tahmin ediyorsak, `ddof=1` kullanarak daha "**ihtiyatlı**" bir tahmin yapmış oluruz.

### Çıktıların Yorumlanması

Kodun çıktısı:
* Point Estimate for Mean: 73.68
* Point Estimate for Variance: 192.96

Bu rakamları şu şekilde yorumlamalıyız:

* **Ortalama Yorumu:**
    > "Elimdeki 50 kişilik örnekleme dayanarak, popülasyonun (tüm öğrencilerin) gerçek not ortalaması ($\mu$) için **en iyi tekil tahminim 73.68'dir**."
* **Varyans Yorumu:**
    > "Elimdeki 50 kişilik örnekleme dayanarak, popülasyonun (tüm öğrencilerin) notlarının varyansı ($\sigma^2$) için **en iyi tekil tahminim 192.96'dır**."
* **Daha Anlaşılır Yorum:** Varyansın karekökü standart sapmadır. `$\sqrt{192.96} \approx 13.89$`. Bu bize şunu söyler:
    > "Tahminimize göre, popülasyondaki tipik bir öğrencinin notu, ortalama olan 73.68'den yaklaşık **13.89 puan sapma** göstermektedir." Bu, notların ne kadar yayvan olduğunun bir ölçüsüdür.

---

### Analiz ve Yorum için Kontrol Listeniz

#### 1. Veri Kaynağı Nedir?
* **Soru:** "Bu kod popülasyonla mı çalışıyor, yoksa bir örneklemle mi?"
* **Cevap:** Senaryo açıkça bir **örneklem** (`sample`) olduğunu belirtiyor. Bu, analiz yöntemimizi (özellikle varyans hesabını) doğrudan etkiler.

#### 2. Hangi Terimleri Kullanmalıyım?
* `73.68`, popülasyon ortalaması ($\mu$) için bir **nokta tahminidir (point estimate)**. Onu hesaplamak için **örneklem ortalamasını ($\bar{x}$)** kullandık.
* `192.96`, popülasyon varyansı ($\sigma^2$) için bir **nokta tahminidir**. Onu hesaplamak için **örneklem varyansını ($s^2$)** kullandık.

#### 3. Kodda Dikkat Edilmesi Gereken Kritik Nokta Nedir?
* `np.var()` fonksiyonunda, bir örneklemden popülasyon varyansını tahmin ederken **yansız bir tahmin** elde etmek için `ddof=1` parametresinin kullanılması zorunludur.

#### 4. Sonuçlar Ne Anlama Geliyor?
* Bu sayılar, popülasyonun *gerçek* değerleri değildir. Onlar, elimizdeki sınırlı veriye dayanarak yaptığımız **en iyi eğitimli tahminlerdir**. Tıpkı aşçının, bütün bir kazan hakkında sadece bir kaşık çorbaya bakarak bir fikir yürütmesi gibi.

--- 

### Python Kodu: Oran için Nokta Tahmini

Aşağıdaki kod, 300 öğrencinin sınav sonuçlarından oluşan bir örneklem oluşturur ve bu örneklemi kullanarak popülasyonun geçme oranı ve bu oranın varyansı için nokta tahminleri yapar.

```python
import numpy as np

# Simulate a sample of 
# 300 students' test results
n = 300  # Total sample size

# Create a random sample 
# where 1 represents passing 
# the test and 0 represents failing
# Let's assume 65% of students passed the test
np.random.seed(42) # For reproducible results
students = np.random.choice([0, 1], size=n, p=[0.35, 0.65])  # 65% pass the test

# Calculate the point
# estimate for the proportion (sample proportion)
p_estimate = np.mean(students)

# Calculate the variance
# of the proportion estimate using the formula: p̂ * (1 - p̂) / n
variance_estimate = p_estimate * (1 - p_estimate) / n

# Print the results
print(f"Point Estimate for Proportion: {p_estimate:.4f}")
print(f"Variance of the Proportion Estimate: {variance_estimate:.6f}")
```

### Kodun ve Çıktının Açıklaması

Bu kodun her bir parçasının ne anlama geldiğini ve sonuçları nasıl yorumlamamız gerektiğini inceleyelim.

#### 1. Oran için Nokta Tahmini (`p_estimate`)

* **Ne Yaptık?**
  `np.mean(students)` kodunu kullandık. `students` dizisi sadece 0 (kaldı) ve 1'lerden (geçti) oluştuğu için, bu dizinin ortalamasını almak, 1'lerin oranını (yani geçenlerin oranını) bulmak için zekice ve etkili bir yoldur.

* **Yorum:**
  Çıktıdaki `Point Estimate for Proportion: 0.6400` (veya sizin çalıştırdığınızda buna çok yakın bir değer) bizim **en iyi tekil tahminimizdir**.
  > "Elimdeki 300 kişilik örnekleme dayanarak, tüm popülasyonun (sınava giren tüm öğrencilerin) geçme oranının **%64** olduğunu tahmin ediyorum."

---

#### 2. Oran Tahmininin Varyansı (`variance_estimate`)

* **Ne Yaptık?**
  Görselde verilen formülü doğrudan Python koduna çevirdik:
  $$
  Var(\hat{p}) = \frac{\hat{p}(1-\hat{p})}{n}
  $$
  Bu, kodda `p_estimate * (1 - p_estimate) / n` olarak karşılık bulur.

* **Bu Formül Ne Anlama Geliyor? (Metafor)**
  Varyansı, tahminimizin **"güvenilirlik ölçüsü"** veya **"titreme payı"** olarak düşünebilirsiniz. Eğer bu deneyi (300 kişilik yeni bir örneklem seçmeyi) tekrar tekrar yapsaydık, bulacağımız oran tahmini her seferinde biraz farklı olurdu. İşte varyans, bu tahminlerin ne kadar "titreyeceğini" veya ne kadar küçük bir aralıkta değişeceğini ölçer.

* **Nelere Dikkat Etmeli?**
    * **Düşük Varyans (İyi):** Varyansın küçük olması, tahminimizin çok fazla "titremediğini", yani oldukça **güvenilir ve kararlı** olduğunu gösterir. Başka bir örneklem alsak bile sonucun çok farklı çıkmayacağını bekleyebiliriz.
    * **Yüksek Varyans (Kötü):** Varyansın büyük olması, tahminimizin çok "titrek" olduğunu ve başka bir örneklemde çok farklı bir sonuç bulabileceğimiz anlamına gelir.

* **Yorum:**
  Çıktıdaki `Variance of the Proportion Estimate: 0.000768` değeri **çok küçüktür**.
  > "Yaptığımız %64'lük tahmin oldukça sağlam. Örneklem boyutumuz (`n=300`) yeterince büyük olduğu için, bu tahminin 'titreme payı' çok düşüktür. Bu, tahminimize olan güvenimizi artırır." ✅

