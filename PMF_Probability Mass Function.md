# Probability Mass Function (PMF)

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

[Probability Mass Function (PMF) - Vikipedi (Ayrıntılı Teknik Bilgi)](https://en.wikipedia.org/wiki/Probability_mass_function)

<img width="899" height="584" alt="image" src="https://github.com/user-attachments/assets/33cc0fb7-bd90-4270-bf40-0545ffb1c74c" />


<img width="698" height="748" alt="image" src="https://github.com/user-attachments/assets/cf344f2d-b864-470a-b44e-ad2cb32205ce" />



