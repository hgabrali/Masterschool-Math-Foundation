<img width="724" height="440" alt="image" src="https://github.com/user-attachments/assets/63b86a7d-c099-4337-b63e-8bf2e1d40f86" />

<img width="714" height="408" alt="image" src="https://github.com/user-attachments/assets/e7212cf1-bcda-4e16-90c9-cb0cc7438ce9" />

<img width="710" height="306" alt="image" src="https://github.com/user-attachments/assets/d7882cb4-e61d-478f-a70b-75249d6c0ab1" />

<img width="561" height="191" alt="image" src="https://github.com/user-attachments/assets/2bd8a1ad-1a73-487e-9f3e-7ebf609c5238" />

# Moments of a Discrete Probability Distribution

This table outlines the definitions, purpose, and formulas for the key moments of a **discrete random variable ($X$)**. These concepts quantify the central tendency and spread of the distribution.

| Concept | Alternative Name(s) | Purpose | Discrete Formula |
| :--- | :--- | :--- | :--- |
| **1. Mathematical Expectation** | Mean, Expected Value, $\mu$ or $E[X]$ | **Central Tendency:** Describes the long-run **average value** of the random variable. It is the weighted average of all possible outcomes. | $$\mathbf{E[X] = \sum x \cdot f(x)}$$ |
| **2. Variance** | $\sigma^2$ or $Var(X)$ | **Spread/Dispersion:** Quantifies the **average squared deviation** of values from the Mean ($\mu$). It measures how spread out the distribution is. | $$\mathbf{Var(X) = \sum (x - \mu)^2 \cdot f(x)}$$ **Alternative:** $E[X^2] - (E[X])^2$ |
| **3. Standard Deviation** | $\sigma$ | **Interpretability:** Measures the spread in the **original units** of the data (since variance is in squared units). Easier to interpret than variance. | $$\mathbf{\sigma = \sqrt{Var(X)}}$$ |

---

# Ayrık Olasılık Dağılımının Momentleri

Bu tablo, **ayrık rastgele değişkenin ($X$)** temel momentlerinin (merkez ve yayılım ölçüleri) tanımlarını, amaçlarını ve formüllerini özetlemektedir.

| Kavram | Alternatif İsim(ler) | Amaç | Ayrık Formül |
| :--- | :--- | :--- | :--- |
| **1. Matematiksel Beklenti** | Ortalama, Beklenen Değer, $\mu$ veya $E[X]$ | **Merkezi Eğilim:** Rastgele değişkenin uzun vadede ulaşacağı **ortalama değeri** tanımlar. Tüm olası sonuçların ağırlıklı ortalamasıdır. | $$\mathbf{E[X] = \sum x \cdot f(x)}$$ |
| **2. Varyans** | $\sigma^2$ veya $Var(X)$ | **Dağılım/Yayılım:** Değerlerin Ortalamadan ($\mu$) ne kadar **uzaklaştığını** (ortalama karesel sapmayı) nicel olarak ölçer. | $$\mathbf{Var(X) = \sum (x - \mu)^2 \cdot f(x)}$$ **Alternatif:** $E[X^2] - (E[X])^2$ |
| **3. Standart Sapma** | $\sigma$ | **Yorumlanabilirlik:** Yayılımı, verinin **orijinal birimleri** cinsinden ölçer (Varyans karesel birimlerdedir). Varyansa göre yorumlaması daha kolaydır. | $$\mathbf{\sigma = \sqrt{Var(X)}}$$ |

---

# Kavramsal Açıklamalar ve Kullanım Amaçları

## 1. Matematiksel Beklenti (Mean / Expected Value, $E[X]$)

| Amaç (Ne İşe Yarar) | Kullanım (Nerede/Ne Zaman) |
| :--- | :--- |
| **Merkezi Eğilimi Tanımlama:** Rastgele bir deneyin uzun vadede **ortalama sonucunun** ne olacağını gösterir. Dağılımın **merkez noktasını** belirtir. | Bir yatırımın ortalama getirisi, bir kumar oyununda uzun vadede beklenecek kayıp/kazanç miktarı, bir ürünün ortalama ömrü gibi **merkez değeri** bilmek istediğimiz her an kullanılır. |
| **Özet:** Olasılıkların ağırlıklı ortalamasıdır. | Veri setinin **tipik değerini** hızlıca görmek istediğinizde kullanırsınız. |


## 2. Varyans (Variance, $\sigma^2$)

| Amaç (Ne İşe Yarar) | Kullanım (Nerede/Ne Zaman) |
| :--- | :--- |
| **Dağılımı/Yayılımı Ölçme:** Rastgele değişkenin değerlerinin, Ortalamadan ($E[X]$) ne kadar **uzaklaştığını** veya **yayıldığını** gösterir. | **Risk Analizi:** Bir finansal varlığın (hisse senedi) getirilerinin ortalamadan ne kadar sapabileceğini, yani ne kadar **istikrarsız** olduğunu ölçmek için kullanılır. Yüksek varyans, yüksek risk demektir. |
| **Özet:** Ortalamadan olan sapmaların karesinin ortalamasıdır. | Bir dağılımın **ne kadar geniş** veya **dağınık** olduğunu merak ettiğinizde kullanırsınız. |

## 3. Standart Sapma (Standard Deviation, $\sigma$)

| Amaç (Ne İşe Yarar) | Kullanım (Nerede/Ne Zaman) |
| :--- | :--- |
| **Yorumlanabilir Yayılım Ölçüsü:** Varyansın karesel birimler cinsinden ölçüldüğü bu durumu ortadan kaldırır. Varyansın **karekökünü** alarak yayılımı **orijinal veri birimine** geri çevirir. | **Karşılaştırma ve Yorumlama:** Risk analizinde Varyans yerine sıklıkla kullanılır, çünkü yorumlaması daha kolaydır. Örneğin, "Ortalama kazancımız $100$ TL ve standart sapmamız $20$ TL'dir." dendiğinde, bu $20$ TL'nin ortalamaya göre ne kadar sapma olduğunu anlarız. |
| **Özet:** Varyansın daha pratik, günlük hayata uyarlanmış halidir. | Risk veya yayılım ölçüsünü **verinin kendi biriminde** (TL, metre, adet vb.) ifade etmek istediğinizde kullanırsınız. |

# Metaforik Karşılaştırma: Aşçının Çorbası 🥣

Bu tablo, olasılığın üç temel anının (momentinin) günlük hayattaki karşılıklarını somutlaştırmaktadır.

| Kavram | Metaforik Karşılığı | Açıklama |
| :--- | :--- | :--- |
| **Matematiksel Beklenti ($E[X]$)** | **Çorbanın Ortalama Tadı** | Bir kaşık aldığınızda beklediğiniz **tipik lezzet** nedir? (Çok mu tuzlu, çok mu baharatlı?) Bu, çorbanın **merkezini** temsil eder. |
| **Varyans ($\sigma^2$)** | **Malzemelerin Karışma Düzeyinin Karesi** | Çorbanın ne kadar iyi karıştırıldığıdır. Bu değer **yüksekse**, bir kaşığınızda yoğun tuz, diğerinde sadece su bulursunuz. Tadı **istikrarsızdır** (yüksek risk). |
| **Standart Sapma ($\sigma$)** | **Tadın Ortalama Sapması** | Çorbayı karıştırmadan önce tuzun ve karabiberin ortalama tattan ne kadar **saptığını doğrudan hissettiğiniz** ölçüdür. (Çok tuzlu bir lokma ile karşılaşma riskiniz ne kadardır?) |

---

# Dağılımların Momentlerinin (E[X], Var[X]) Basitleşmesi

**Beklenti ($E[X]$), Varyans ve Standart Sapma** tanımları **tüm dağılımlar için aynıdır.** Yani, Beklenti her zaman merkezi eğilimi (merkezi) gösterir, Varyans her zaman yayılımı (riski) gösterir.

Ancak, her bir dağılımın (Binomial, Poisson, vb.) kendine ait benzersiz bir PMF (Olasılık Kütle Fonksiyonu) yapısı olduğu için, genel $\sum x f(x)$ formülünü uyguladığımızda, sonuç dağılımın parametrelerine dayalı çok daha basit bir formüle indirgenir.

Bu basitleştirilmiş formüller, dağılımların **"sınıflandırılma" biçimidir**.




# Moment Formüllerinden Kavramsal Çıkarımlar

**Basitleşme:** **Binomial dağılımda** Beklenti'yi ($E[X]$) bulmak için, $n$ denemenin tamamı için karmaşık toplamlar almak yerine, sadece parametreleri ($n$ ve $p$) çarpmanız yeterlidir ($\mathbf{E[X] = n \cdot p}$). Bu, matematiksel kanıtın gücüdür.

**Poisson'un Eşsizliği:** **Poisson dağılımında** Beklenti ($E[X]$) ve Varyans ($Var(X)$) birbirine eşittir ($\mathbf{E[X] = Var(X) = \lambda}$). Bu eşsiz özellik, bu dağılımın nadir ve rastgele olayları modellemedeki gücünü gösteren ayırt edici bir özelliğidir.

# Ayrık Dağılımlarda Momentlerin Sınıflandırılması

Aşağıdaki tablo, en yaygın kullanılan ayrık dağılımlar için Beklenti ($E[X]$) ve Varyansın ($Var(X)$) parametreler cinsinden nasıl basitleştiğini göstermektedir.

| Dağılım Adı | Parametreler | Beklenen Değer (Mean, $E[X]$) | Varyans ($Var(X)$) |
| :--- | :--- | :--- | :--- |
| **1. Bernoulli** | Başarı olasılığı ($p$) | $$\mathbf{p}$$ | $$\mathbf{p(1-p)}$$ |
| **2. Binomial** | Deneme sayısı ($n$), Başarı olasılığı ($p$) | $$\mathbf{n \cdot p}$$ | $$\mathbf{n \cdot p \cdot (1-p)}$$ |
| **3. Poisson** | Beklenen olay sayısı ($\lambda$) | $$\mathbf{\lambda}$$ | $$\mathbf{\lambda}$$ |
| **4. Geometrik** | Başarı olasılığı ($p$) | $$\mathbf{\frac{1}{p}}$$ | $$\mathbf{\frac{1-p}{p^2}}$$ |



