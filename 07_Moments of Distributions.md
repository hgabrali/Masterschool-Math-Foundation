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


* Beklenen Değer, Varyans ve Standart Sapma soyut formüller olmaktan çok, iş ve bilim dünyasında risk, güvenilirlik ve tahmin ile ilgili kararlar almamızı sağlayan ölçüm araçlarıdır.

# 1. Matematiksel Beklenti (Mean / Expected Value, $E[X]$)

Beklenen Değer, bir olayın uzun vadeli ortalama sonucunu tahmin etmenin matematiksel karşılığıdır.

| Data Science Uygulaması | Ne İşe Yarar? (Kullanım Amacı) | Neleri Bulmana Yardımcı Olur? |
| :--- | :--- | :--- |
| **Tahmin ve Bütçeleme** | **Merkezi Tahmin:** Olasılıkları kullanarak gelecekteki tipik sonucu tahmin etme. | **Ortalama Müşteri Ömrü Değeri (CLV):** Bir müşterinin şirkete ortalama ne kadar gelir getireceğini tahmin etme. **Optimizasyon:** Bir süreçte ortalama maliyet/kazanç noktasını belirleme. |
| **Örnek: E-Ticaret** | Bir müşterinin bir sonraki ziyaretinde yapacağı **ortalama harcama** miktarını tahmin etmek. (Bu, envanter ve pazarlama bütçesini ayarlamaya yardımcı olur.) | |

# 2. Varyans (Variance, $\sigma^2$) ve Standart Sapma (Standard Deviation, $\sigma$)

Varyans ve Standart Sapma, dağılımın yayılımını ölçerek, tahminlerimizin etrafındaki **belirsizliği ve riski** nicelleştirir.

| Data Science Uygulaması | Ne İşe Yarar? (Kullanım Amacı) | Neleri Bulmana Yardımcı Olur? |
| :--- | :--- | :--- |
| **Risk Analizi** | **Volatilite Ölçümü:** Verilerin merkezden ne kadar sapma eğiliminde olduğunu belirleme. Yüksek varyans = Yüksek **risk/belirsizlik**. | **Finansal Risk:** Bir yatırım portföyünün getirilerindeki **oynaklık** seviyesini ölçme. Yüksek $\sigma$, getiri ortalamadan hızla sapabilir demektir. |
| **Kalite Kontrolü** | **Güvenilirlik Aralığı:** Veri noktalarının %68'inin (1 Standart Sapma içinde) ve %95'inin (2 Standart Sapma içinde) hangi aralıkta kalacağını belirleme. | **Üretim Hataları:** Bir makinenin ürettiği parçaların boyutlarının ne kadar **tutarlı** olduğunu kontrol etme. |
| **Örnek: A/B Testi** | İki farklı reklam kampanyasının (A ve B) dönüşüm oranları aynı olabilir, ancak Kampanya A'nın varyansı çok daha düşükse, bu, A'nın sonucunun **daha güvenilir ve istikrarlı** olduğu anlamına gelir. | |


# Özet: Momentler Neden Hayati Önemdedir?

Bu momentler, bir veri bilimcinin sadece **"ne olacak?"** sorusunu değil, aynı zamanda **"ne kadar güvenle tahmin edebilirim?"** sorusunu yanıtlamasına yardımcı olur.

| Kavram | Temel Çıkarım | Karar Mekanizması |
| :--- | :--- | :--- |
| **$E[X]$ (Beklenti)** | Uzun vadeli kazanç. | **"Ortalamada bu iyidir."** (Elde edilecek tipik değer) |
| **$\sigma^2 / \sigma$ (Varyans/SS)** | Kazancın istikrarı. | **"Bu tahmin ne kadar risklidir?"** (Ortalamadan sapma payı) |

---

## İstatistiksel Momentler: Dağılımların Şeklini Anlamak

İstatistikte **momentler (moments)**, bir olasılık dağılımının şeklini ve karakterini tanımlayan bir dizi ölçüdür. Tıpkı bir nesnenin fiziksel özelliklerini (kütle merkezi, dengesi, vb.) tanımlamak gibi, istatistiksel momentler de bir veri dağılımının geometrisini ve davranışını anlamamızı sağlar.

Gelin bu konuyu, İngilizce terimlerini de belirterek ve akılda kalıcı bir ana metafor üzerinden detaylıca inceleyelim.

---

### Ana Metafor: Olasılık Dağılımı Bir Heykel Olsaydı...

Bir olasılık dağılımını, kütlesi farklı yerlerde yoğunlaşmış bir **metal heykel** gibi düşünün. Momentler, bu heykelin fiziksel özelliklerini tanımlamamıza yarayan ölçümlerdir.

1.  **Birinci Moment (First Moment):** Heykelin **denge noktasını** bulur.
2.  **İkinci Moment (Second Moment):** Heykelin bu denge noktası etrafında ne kadar kolay **döneceğini** (yani ne kadar yayvan olduğunu) ölçer.
3.  **Üçüncü Moment (Third Moment):** Heykelin ne kadar **dengesiz veya tek tarafa yığılmış** olduğunu ölçer.
4.  **Dördüncü Moment (Fourth Moment):** Heykelin kütlesinin merkezde ne kadar **sivri** ve uçlarda ne kadar **ağır** olduğunu ölçer.

---

### Terimlerin Pratik Anlamları

* **Ortalama (Mean):**
  Veri setinizin merkezi konumunu söyler.

* **Standart Sapma (Standard Deviation):**
  Verilerinizin bu merkezden tipik olarak ne kadar uzakta olduğunu söyler. **Düşük** standart sapma, verilerin tutarlı ve birbirine yakın olduğunu; **yüksek** standart sapma ise verilerin dağınık ve değişken olduğunu gösterir.

* **Çarpıklık (Skewness):**
  Dağılımınızın kuyruğunun hangi yöne uzun olduğunu söyler.
    * **Pozitif (Sağa Çarpık):** Kuyruk sağa doğrudur. Çoğu veri düşük değerlerde toplanmıştır, ancak birkaç tane çok yüksek "aykırı" değer ortalamayı yukarı çeker (örn: insanların maaşları).
    * **Negatif (Sola Çarpık):** Kuyruk sola doğrudur. Çoğu veri yüksek değerlerde toplanmıştır, ancak birkaç tane çok düşük değer ortalamayı aşağı çeker (örn: kolay bir sınavdan alınan notlar).

* **Basıklık (Kurtosis):**
  Dağılımınızın ne kadar "**aykırı değere eğilimli**" olduğunu söyler.
    * **Yüksek Basıklık (Leptokurtic):** Normal dağılıma göre daha sivri bir tepeye ve daha "kalın" kuyruklara sahiptir. Bu, aşırı değerlerin (outlier) beklenenden daha olası olduğu anlamına gelir (örn: hisse senedi getirileri).
    * **Düşük Basıklık (Platykurtic):** Normal dağılıma göre daha basık bir tepeye ve daha "ince" kuyruklara sahiptir. Aşırı değerler daha az olasıdır.
 
### Ayrıntılı ve Karşılaştırmalı Momentler Tablosu

| Moment | İngilizce Karşılığı | Teknik Tanım | Metafor (Heykel Analojisi) | Bize Ne Anlatır? (Yorumu) |
| :--- | :--- | :--- | :--- | :--- |
| **1. Moment: Ortalama ($\mu$)** | **Mean, Expected Value** | Bir dağılımın "ağırlık merkezidir". Her bir değerin, gerçekleşme olasılığı ile ağırlıklandırılmış ortalamasıdır. | **Denge Noktası (Center of Gravity)** | Heykeli hangi noktadan parmağınızın ucuna koyarsanız dengede durur? Bu nokta, dağılımın "merkezini" veya "tipik" değerini gösterir. |
| **2. Moment: Varyans ($\sigma^2$) / Standart Sapma ($\sigma$)** | **Variance / Standard Deviation**| Verilerin ortalamadan ne kadar uzakta yayıldığının bir ölçüsüdür. Varyans, ortalamadan sapmaların karesinin ortalamasıdır. Standart sapma ise varyansın kareköküdür. | **Dönme Eylemsizliği (Rotational Inertia)** | Heykeli denge noktasından döndürmek ne kadar zor? Kütlesi merkeze yakın, **kompakt bir küre** (düşük varyans) mi, yoksa kolları iki yana açılmış **geniş bir heykel** (yüksek varyans) mi? |
| **3. Moment: Çarpıklık ($\beta_1$)** | **Skewness** | Dağılımın simetriden ne kadar saptığının bir ölçüsüdür. Simetrik bir dağılımda (örn: Normal Dağılım) çarpıklık sıfırdır. | **Dengesizlik / Tek Tarafa Yığılma (Lopsidedness)**| Heykel mükemmel simetrik mi? Yoksa bir tarafında diğerine göre daha uzun ve ağır bir kolu var mı? Bu dengesizlik, heykelin hangi yöne "eğilim" gösterdiğini anlatır. |
| **4. Moment: Basıklık/Sivrilik ($\beta_2$)**| **Kurtosis** | Dağılımın kuyruklarının "ağırlığını" ve merkezinin "sivriliğini" normal dağılıma göre ölçer. | **Uçların Ağırlığı / Sivrilik (Weight of the Extremes / Peakedness)** | Heykelin kütlesi nasıl dağılmış? Kütlenin çoğu merkezde toplanıp **sivri bir tepe** mi oluşturuyor ve uçlarda çok ince ama ağır **kuyrukları** (yüksek basıklık) mı var? Yoksa kütle daha eşit dağılıp **düz bir plato** (düşük basıklık) mu oluşturuyor? |
