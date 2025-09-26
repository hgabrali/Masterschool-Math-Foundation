# Probability Mass Function (PMF)

<img width="698" height="390" alt="image" src="https://github.com/user-attachments/assets/5b3c013f-3bd8-4702-bab5-21a5c7d635fc" />

 <img width="865" height="580" alt="image" src="https://github.com/user-attachments/assets/1bd69202-e3b8-474d-8863-11177890d336" />

<img width="1098" height="666" alt="image" src="https://github.com/user-attachments/assets/cab28747-0a90-46ee-b5c8-ff51d30c4313" />

<img width="1163" height="564" alt="image" src="https://github.com/user-attachments/assets/76e728ea-0a88-4f8f-92e1-e43982ac0e34" />

### Kaynaklar (Resources)

* [Probability Mass Function - GeeksforGeeks](https://www.geeksforgeeks.org/maths/probability-mass-function/)

  ---
  
# Olasılık Kütle Fonksiyonu (Probability Mass Function - PMF)

**PMF**, **ayrık olasılık dağılımlarının (Discrete Probability Distributions)** kalbidir. Bir rastgele değişkenin ($X$), olası bir $x$ değerini alma olasılığını tanımlayan fonksiyondur ve genellikle $P(X=x)$ veya $f(x)$ olarak gösterilir.

Bir fonksiyonun geçerli bir PMF (Olasılık Kütle Fonksiyonu) sayılabilmesi için, olasılık teorisinin temel **aksiyomlarından (axioms)** gelen üç temel **formel gereksinimi (formal requirements)** karşılaması gerekir.

---

## 1. PMF'nin Formel Tanımı

**Tanım:** Bir ayrık rastgele değişken $X$ için, **Olasılık Kütle Fonksiyonu** ($f(x)$ veya $P(X=x)$), $X$'in alabileceği her bir $x$ değeri için $P(X=x)$ olasılığını veren fonksiyondur.

---

## 2. PMF'nin Formel Gereksinimleri (Formal Requirements)

### Gereksinim 1: Negatif Olmama Koşulu (Non-negativity)

Hiçbir olayın olasılığı sıfırın altında olamaz.

* **Tanım:** Olasılık Kütle Fonksiyonu'nun alabileceği tüm değerler sıfıra eşit veya sıfırdan büyük olmalıdır.
* **Formel Gösterim:**
    $$\mathbf{f(x) \ge 0}$$
    (Tüm $x$ değerleri için)

### Gereksinim 2: Toplamın Bir Olması Koşulu (Summation to Unity)

Rastgele değişkenin alabileceği **tüm olası değerlerin** olasılıkları toplandığında, bu toplam kesinlikle $1$'e eşit olmalıdır. (Evrensel örneklem uzayının (sample space) olasılığı $100\%$ olduğu anlamına gelir.)

* **Tanım:** Rastgele değişkenin ($X$) alabileceği tüm $x$ değerleri üzerindeki olasılıkların toplamı $1$ olmalıdır.
* **Formel Gösterim:**
    $$\mathbf{\sum_{x} f(x) = 1}$$
    (Buradaki $\sum_{x}$ ifadesi, $X$'in alabileceği tüm $x$ değerleri üzerindeki toplamı temsil eder.)

### Gereksinim 3: Tanımlı Değerler Dışında Sıfır Olması Koşulu (Defined only for Countable Values)

PMF, sadece rastgele değişkenin alabileceği **ayrık** ve **sayılabilir** değerler için bir olasılık atar; bu değerler dışındaki tüm değerler için olasılık sıfırdır.

* **Tanım:** Eğer bir $x$ değeri, rastgele değişken $X$'in alabileceği olası değerler kümesine ait değilse ($x \notin X$), bu değeri alma olasılığı sıfırdır.
* **Formel Gösterim:**
    $$\mathbf{f(x) = 0}$$
    (Eğer $x$ değeri, $X$'in değer kümesine ait değilse.)

  # Olasılık Kütle Fonksiyonu (PMF) Gereksinimleri Özeti

PMF'nin (Probability Mass Function) bir fonksiyon sayılabilmesi için karşılaması gereken üç temel koşul.

| Gereksinim | İngilizce Karşılığı | Açıklama | Formel Gösterim |
| :--- | :--- | :--- | :--- |
| **1. Negatif Olmama** | Non-negativity | Hiçbir olasılık negatif olamaz. | $$\mathbf{f(x) \ge 0}$$ |
| **2. Toplamın Bir Olması** | Summation to Unity | Tüm olası ayrık sonuçların olasılıklarının toplamı 1'dir. | $$\mathbf{\sum_{x} f(x) = 1}$$ |
| **3. Tanımlı Küme Dışı** | Defined only for $X$'s values | Rastgele değişkenin almadığı değerler için olasılık $0$'dır. | $$\mathbf{f(x) = 0 \quad (\text{eğer } x \notin X)}$$ |

* Bu gereksinimler, zar atma, yazı tura atma veya arızalı ürün sayısını modelleme gibi tüm ayrık olayların matematiksel olarak tutarlı bir şekilde temsil edilmesini sağlar.
----
  # Dağılım ve Fonksiyon Farkı

* Poisson, Binomial ve Geometrik, olasılık olaylarını modelleyen **Dağılım** türleridir.

* PMF (Olasılık Kütle Fonksiyonu) ve CDF (Kümülatif Dağılım Fonksiyonu) ise bu dağılımları matematiksel olarak tanımlayan **Fonksiyonlardır** (araçlardır).

# Olasılık Kavramlarının Rolleri: Bir Analoji (Dağılım, PMF, CDF)

Bu tablo, Olasılık Dağılımı, PMF ve CDF arasındaki ilişkileri bir yemek tarifi analojisiyle netleştirmektedir.

| Kavram | İngilizce Karşılığı | Rolü (Yemek Analojisi) | Açıklama |
| :--- | :--- | :--- | :--- |
| **Dağılım** | Distribution | **Tarif Kitabı** 📖 | Olası sonuçların listesi ve bu sonuçların oluşma kurallarını belirleyen genel matematiksel model. |
| **PMF** | Probability Mass Function | **Malzeme Listesi/Teknik Adımlar** 🧾 | Dağılımın kuralına göre, **tam olarak tek bir sonuca** ulaşma olasılığını hesaplayan fonksiyon. |
| **CDF** | Cumulative Distribution Function | **Toplam Porsiyon Sayısı** 📈 | Belirli bir değere (veya ona kadar olan) tüm sonuçların olasılıklarını **toplayarak (biriktirerek)**, o ana kadarki kümülatif olasılığı hesaplayan fonksiyon. |


# Ayrık Dağılımların PMF ve CDF Karşılaştırması

Bu tablo, temel ayrık olasılık dağılımlarının PMF (Olasılık Kütle Fonksiyonu) ve CDF (Kümülatif Dağılım Fonksiyonu) ile olan somut ilişkisini göstermektedir.

| Dağılım Adı | PMF Ne İşe Yarar? (Tek Bir Değer) | CDF Ne İşe Yarar? (Kümülatif Değer) |
| :--- | :--- | :--- |
| **Bernoulli ($p$)** | Tek bir denemede **tam olarak 1 başarı** olasılığını ($p$) veya **tam olarak 0 başarı** olasılığını ($1-p$) verir. | Olasılığın $0$'dan $1$'e yükselişini gösterir. $P(X \le 0)$ ve $P(X \le 1)$'i verir. |
| **Binomial ($n, p$)** | $n$ denemede **tam olarak $k$ tane başarı** olma olasılığını ($P(X = k)$) hesaplar. | $n$ denemede **$k$ veya daha az** başarı olma olasılığını ($P(X \le k)$) hesaplar. |
| **Poisson ($\lambda$)** | Sabit bir aralıkta **tam olarak $k$ tane olay** gerçekleşme olasılığını ($P(X = k)$) hesaplar. | Sabit bir aralıkta **$k$ veya daha az** olay gerçekleşme olasılığını ($P(X \le k)$) hesaplar. |
| **Geometrik ($p$)** | **Tam olarak $k$. denemede ilk başarıyı** elde etme olasılığını ($P(X = k)$) hesaplar. | **$k$ veya daha az** denemede ilk başarıyı elde etme olasılığını ($P(X \le k)$) hesaplar. |

---

[Probability Mass Function (PMF) - Vikipedi (Ayrıntılı Teknik Bilgi)](https://en.wikipedia.org/wiki/Probability_mass_function)

<img width="899" height="584" alt="image" src="https://github.com/user-attachments/assets/33cc0fb7-bd90-4270-bf40-0545ffb1c74c" />


<img width="698" height="748" alt="image" src="https://github.com/user-attachments/assets/cf344f2d-b864-470a-b44e-ad2cb32205ce" />



