# Course Structure Overview

## 1: Foundations of Probability
- Learn the core concepts of probability, including random variables, sample spaces, and probability distributions.
- Build a strong foundation for understanding uncertainty and making data-driven decisions.

## 2: Conditional Probability and Distributions
- Explore conditional probability and how it relates to distributions.
- Learn how to calculate and interpret conditional probabilities in various scenarios.

## 3: Continuous Distributions
- Understand continuous probability distributions, such as the normal and exponential distributions.
- Learn how to apply these distributions to real-world data analysis problems.

## 4: Statistical Inference
- Dive into statistical inference, including hypothesis testing, confidence intervals, and point estimates.
- Use your knowledge of probability to make conclusions about populations based on sample data.

  ---

  # Kurs Yapısına Genel Bakış

## 1: Olasılığın Temelleri
- Olasılığın temel kavramlarını, rastgele değişkenler, örneklem uzayları ve olasılık dağılımları dahil olmak üzere öğrenin.
- Belirsizliği anlamak ve veriye dayalı kararlar vermek için güçlü bir temel oluşturun.

## 2: Koşullu Olasılık ve Dağılımlar
- Koşullu olasılığı ve dağılımlarla nasıl ilişkili olduğunu keşfedin.
- Çeşitli senaryolarda koşullu olasılıkları nasıl hesaplayacağınızı ve yorumlayacağınızı öğrenin.

## 3: Sürekli Dağılımlar
- Normal ve üstel dağılımlar gibi sürekli olasılık dağılımlarını anlayın.
- Bu dağılımları gerçek dünya veri analizi problemlerine nasıl uygulayacağınızı öğrenin.

##  4: İstatistiksel Çıkarım
- Hipotez testi, güven aralıkları ve nokta tahminleri gibi istatistiksel çıkarıma derinlemesine dalın.
- Örneklem verilerine dayanarak popülasyonlar hakkında sonuçlar çıkarmak için olasılık bilginizi kullanın.

  ---
# Introduction to Probability

### What is Probability?

Probability is a branch of mathematics that deals with calculating the likelihood of an event occurring. In simple terms, it helps us understand and quantify uncertainty. Probability is widely used in fields like statistics, finance, science, and even everyday decision-making. It provides a mathematical framework for modelling random phenomena and making predictions about outcomes.

For example:
- What is the likelihood of flipping a coin and it landing heads up?
- What is the chance of drawing an ace from a deck of cards?
- What is the probability that a person will pass an exam?

# Olasılığa Giriş

### Olasılık Nedir?

Olasılık, bir olayın meydana gelme ihtimalini hesaplayan bir matematik dalıdır. Basit terimlerle, belirsizliği anlamamıza ve nicel olarak belirlememize yardımcı olur. Olasılık, istatistik, finans, bilim ve hatta gündelik karar alma gibi alanlarda yaygın olarak kullanılır. Rastgele olayları modellemek ve sonuçlar hakkında tahminlerde bulunmak için matematiksel bir çerçeve sunar.

Örneğin:
- Bir madeni parayı attığınızda yazı gelme olasılığı nedir?
- Bir iskambil destesinden as çekme şansı nedir?
- Bir kişinin sınavı geçme olasılığı nedir?

  # Key Terms in Probability

- **Experiment:** An action or process that leads to one of several possible outcomes. For example, rolling a die or drawing a card from a deck.
- **Sample Space:** The set of all possible outcomes of an experiment. For example, when rolling a die, the sample space is {1, 2, 3, 4, 5, 6}.
- **Event:** A specific outcome or set of outcomes of an experiment. For example, rolling an even number on a die is an event.
- **Outcome:** A single result from the sample space. For example, getting a 3 when rolling a die is an outcome.

### Olasılıkta Anahtar Terimler

| İngilizce Terim | Türkçe Karşılığı | Açıklama |
| :--- | :--- | :--- |
| **Experiment** | **Deney** | Birkaç olası sonuçtan birine yol açan eylem veya süreç. Örneğin, bir zar atmak veya desteden bir kart çekmek. |
| **Sample Space** | **Örneklem Uzayı** | Bir deneyin tüm olası sonuçlarının kümesi. Örneğin, bir zar atıldığında örneklem uzayı {1, 2, 3, 4, 5, 6} olur. |
| **Event** | **Olay** | Bir deneyin belirli bir sonucu veya sonuçlar kümesi. Örneğin, bir zarda çift sayı gelmesi bir olaydır. |
| **Outcome** | **Sonuç** | Örneklem uzayından çıkan tek bir sonuç. Örneğin, bir zar atıldığında 3 gelmesi bir sonuçtur. |


### Olasılık ve Yemek Yapma Sanatı

| İngilizce Terim | Türkçe Karşılığı | Yemek Tarifi Metaforu |
| :--- | :--- | :--- |
| **Experiment** | **Deney** | Yeni bir kek tarifi deneme eylemi. Ne kadar çaba harcarsanız harcayın, her zaman birkaç olası sonuç vardır (enfes, fena değil, yenmez). |
| **Sample Space** | **Örneklem Uzayı** | Tüm olası sonuçların listesi: Kekin mükemmel bir şekilde kabarması, ortasının çökmesi veya tadının çok şekerli olması. |
| **Event** | **Olay** | Mükemmel bir kek yapma gibi, belirli ve arzu edilen bir sonuç. Bu, tüm olası sonuçlardan sadece bir tanesidir. |
| **Outcome** | **Sonuç** | Fırından çıkan tek, nihai sonuç. Örneğin, 'ortası çökmüş kek'. Bu, örneklem uzayındaki tek bir noktadır. |

### Events

For a given random experiment, the outcome space (or sample space) **S** is the collection of all possible outcomes of the random experiment.

**Example:**
Suppose we randomly select a person and ask them, "How many books do you own?" In this case, our sample space is:

$S = \{0, 1, 2, 3, 4, 5, ...\}$

We could set a practical upper limit, but some people might own hundreds or even thousands of books. So, we'll leave the sample space open to be as accurate as possible. Now, let's define some events:

- Let A be the event that a randomly selected person owns no books:
  $A = \{0\}$

- Let B be the event that a person owns at least one book:
  $B = \{1, 2, 3, 4, ...\}$

- Let C be the event that a person owns no more than 10 books:
  $C = \{0, 1, 2, 3, ..., 10\}$

- Let D be the event that a person owns an even number of books:
  $D = \{0, 2, 4, 6, ...\}$

  ### Basic Set Operations

1.  ∅ is the **null set** or **empty set**. This set does not contain any elements.

2.  $A \cup B$ = **union**. The union contains all of the elements of set A and all elements of set B.

3.  $A \cap B$ = **intersection**. The intersection contains all elements that are present in **both** A and B.

   <img width="359" height="257" alt="image" src="https://github.com/user-attachments/assets/c2ef307a-0a20-4fa7-9a20-0f6b0fa98f73" />


4.  If $A \cap B = ∅$, then A and B are called **mutually exclusive events**.

   <img width="435" height="262" alt="image" src="https://github.com/user-attachments/assets/6dac48b5-6bbd-4d22-8cbb-627d19aad1e6" />

   1.  $A' = A^C$ = **complement**. When we consider all of the possible elements, the complement to the set A is all elements that do not belong to A.
      
<img width="473" height="243" alt="image" src="https://github.com/user-attachments/assets/ec6eff4f-055b-41f6-9350-0bb6c6eb329a" />

      

2.  If $E \cup F \cup G ... = Ω$, then E, F, G, and so on are called **exhaustive events**. So when the union of the sets makes the complete set of all the possible elements, they are called exhaustive events.

3.  The union of events C and D is the event that a randomly selected person either owns **no more than 10 books** or owns an **even number of books**. That is:

    $C \cup D = \{0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 12, 14, 16, ...\}$

    - The **intersection** of events $A$ and $B$ is the event that a person owns **both no books and at least one book** at the same time. This is impossible, so:
  $A \cap B = \emptyset$

- The **complement** of event $D$ is the event that a person owns an **odd number of books**. That is:
  $D^c = \{1, 3, 5, 7, ...\}$

- If we define events $E_0, E_1, E_2,...$ such that
  $E_0 = \{0\}, E_1 = \{1\}, E_2 = \{2\}, ...$
  then the events $E_0, E_1, E_2, ...$ are **exhaustive events**, meaning they cover all possible outcomes in the sample space.

  ### Basic Set Operations

| Operation | Symbol | Description | Example |
| :--- | :--- | :--- | :--- |
| **Union** | $A \cup B$ | The set of all elements that are in **set A**, in **set B**, or in **both**. | If $A = \{1, 2, 3\}$ and $B = \{3, 4, 5\}$, then $A \cup B = \{1, 2, 3, 4, 5\}$. |
| **Intersection** | $A \cap B$ | The set of elements that are **common to both** set A and set B. | If $A = \{1, 2, 3\}$ and $B = \{3, 4, 5\}$, then $A \cap B = \{3\}$. |
| **Complement** | $A'$ or $A^c$ | The set of all elements in the **universal set** that are **not** in set A. | If the universal set $U = \{1, 2, 3, 4, 5\}$ and $A = \{1, 2\}$, then $A^c = \{3, 4, 5\}$. |
| **Difference** | $A - B$ | The set of elements that are in **set A** but **not** in set B. | If $A = \{1, 2, 3\}$ and $B = \{3, 4, 5\}$, then $A - B = \{1, 2\}$. |
| **Empty Set** | $\emptyset$ or {} | A set that contains **no elements**. | The intersection of two disjoint sets (with no common elements) is the empty set. |

---
### Olaylar (Events)

Bir olay, örneklem uzayının (tüm olası sonuçların kümesinin) bir alt kümesidir. Yani, bir deneyin olası sonuçlarından belirli bir kısmını ifade eder.

### Günlük Hayattan Örnekler:

**Örnek: Bir Alışveriş Merkezi Ziyaretçisi**
- **Rastgele Deney:** Rastgele bir alışveriş merkezi ziyaretçisi seçmek ve ona kaç tane mağaza gezdiğini sormak.
- **Örneklem Uzayı (S):** $\{0, 1, 2, 3, 4, ...\}$ (Sonsuz bir küme)
- **Olay A:** Ziyaretçinin en az 5 mağaza gezmesi.
- Bu olayın elemanları: $A = \{5, 6, 7, 8, ...\}$
- **Olay B:** Ziyaretçinin çift sayıda mağaza gezmesi.
- Bu olayın elemanları: $B = \{0, 2, 4, 6, 8, ...\}$

**Örnek: Hava Durumu Tahmini**
- **Rastgele Deney:** Yarınki hava durumunun ne olacağını tahmin etmek.
- **Örneklem Uzayı (S):** $\{Güneşli, Bulutlu, Yağmurlu, Karlı, Rüzgarlı\}$
- **Olay C:** Yarınki havanın "yağışlı" olması.
- Bu olayın elemanları: $C = \{Yağmurlu, Karlı\}$

**Örnek: Öğrenci Sınavı**
- **Rastgele Deney:** Bir öğrencinin sınavdan alacağı notu (100 üzerinden) tahmin etmek.
- **Örneklem Uzayı (S):** $\{0, 1, 2, ..., 100\}$
- **Olay D:** Öğrencinin geçme notu alması. (Geçme notu 60 ise)
- Bu olayın elemanları: $D = \{60, 61, 62, ..., 100\}$
  
### Temel Küme İşlemleri

| İşlem | Sembol | Açıklama | Örnek |
| :--- | :--- | :--- | :--- |
| **Birleşim** | $A \cup B$ | **A kümesinde**, **B kümesinde** veya **her ikisinde** de bulunan tüm elemanların kümesi. | Eğer $A = \{1, 2, 3\}$ ve $B = \{3, 4, 5\}$ ise, $A \cup B = \{1, 2, 3, 4, 5\}$ olur. |
| **Kesişim** | $A \cap B$ | Hem A kümesinde hem de B kümesinde **ortak olarak** bulunan elemanların kümesi. | Eğer $A = \{1, 2, 3\}$ ve $B = \{3, 4, 5\}$ ise, $A \cap B = \{3\}$ olur. |
| **Tümleme** | $A'$ veya $A^c$ | Evrensel kümedeki (uzaydaki) ancak A kümesinde **bulunmayan** tüm elemanların kümesi. | Eğer evrensel küme $U = \{1, 2, 3, 4, 5\}$ ve $A = \{1, 2\}$ ise, $A^c = \{3, 4, 5\}$ olur. |
| **Fark** | $A - B$ | **A kümesinde olan**, ancak B kümesinde **olmayan** elemanların kümesi. | Eğer $A = \{1, 2, 3\}$ ve $B = \{3, 4, 5\}$ ise, $A - B = \{1, 2\}$ olur. |
| **Boş Küme** | $\emptyset$ veya {} | Hiçbir eleman içermeyen bir küme. | Kesişimi olmayan (ortak elemanları olmayan) iki kümenin kesişimi boş kümedir. |

---

# Probabilities of the events

Understanding probability is essential for answering questions that involve making conclusions about a larger population based on a sample. Questions like "How likely is it...?" or "What is the probability...?" are at the core of research and data analysis. To answer them accurately, we need a solid grasp of probability concepts, rules, and models.

Informally we can define a probability as following:

### Probability
- a number between 0 and 1
- a number closer to 0 means **not likely**
- a number closer to 1 means **quite likely**
- if probability of an event is exactly 0, then the event **can't occur**
- if the probability of an event is exactly 1, then the event will **definitely occur**

  ### An Event That Cannot Occur

This is an event with a probability of exactly 0. It is also known as an **impossible event**.

**Example:**
- **Experiment:** Rolling a standard six-sided die.
- **Impossible Event:** Rolling a 7. Since a standard die only has the numbers 1 through 6, it is impossible to roll a 7. The probability of this event is $0/6 = 0$.

---

### An Event That Will Definitely Occur

This is an event with a probability of exactly 1. It is also known as a **certain event**.

**Example:**
- **Experiment:** Rolling a standard six-sided die.
- **Certain Event:** Rolling a number less than 7. Since all possible outcomes (1, 2, 3, 4, 5, 6) are less than 7, this event will always happen. The probability of this event is $6/6 = 1$.

  ### The relative frequency approach

A very common and practical approach to calculating probabilities is the **relative frequency approach**. By observing how often an event occurs over many repeated trials, we can estimate its probability based on actual data rather than assumptions. This approach is done in a following steps:

1.  **Perform an experiment** a large number of times $n$.
2.  **Count the number of times event A occurs** - $N(A)$.
3.  Then, the probability of event A equals:

    $P(A) = \frac{N(A)}{n}$

---

### Example

Suppose you want to estimate the probability that it will rain on any given day in your city. Using the **relative frequency approach**, you decide to look at historical weather data.

1.  **Perform the experiment:** You review the weather records for the past 365 days.
2.  **Count the occurrences:** You find that it rained on 90 of those days.
3.  **Calculate the probability:** Using the relative frequency formula:

    $P(Rain) = \frac{N(Rainy Days)}{N(Total Days)} = \frac{90}{365} \approx 0.247$

So, based on past data, the probability that it will rain on any given day is approximately **24.7%**.

### Classical approach

As long as the outcomes in the sample space are **equally likely**, the probability of event $A$ is:

$P(A) = \frac{N(A)}{N(S)}$

where:
* $N(A)$ is the number of elements in the event $A$.
* $N(S)$ is the number of elements in the sample space $S$.

---

### Example

Suppose you roll a fair six-sided die. The sample space for this experiment is:

$S = \{1, 2, 3, 4, 5, 6\}$

Since the die is fair, each outcome is equally likely.

Let event $A$ be rolling an even number. The outcomes that satisfy this event are:

$A = \{2, 4, 6\}$

Using the **classical approach**, the probability of rolling an even number is:

$P(A) = \frac{N(A)}{N(S)} = \frac{3}{6} = 0.5$

---

### Olayların Olasılığı

Olasılığı anlamak, bir örnekleme dayanarak daha geniş bir popülasyon hakkında sonuç çıkarmayı içeren soruları yanıtlamak için çok önemlidir. "Ne kadar olası?" veya "Olasılığı nedir?" gibi sorular, araştırma ve veri analizinin merkezinde yer alır.

Gayriresmi Olarak Olasılığı Şu Şekilde Tanımlayabiliriz:

- Olasılık, 0 ile 1 arasında bir sayıdır.
- 0'a yakın bir sayı, olayın pek olası olmadığını gösterir.
- 1'e yakın bir sayı, olayın oldukça olası olduğunu gösterir.
- Bir olayın olasılığı tam olarak 0 ise, o olay gerçekleşemez.
- Bir olayın olasılığı tam olarak 1 ise, o olay kesinlikle gerçekleşir.

#### Günlük Hayattan Örnekler:

- **Gerçekleşemeyen Olay (Olasılık = 0):** Hava durumu bugün güneşli iken aynı anda yağmur yağması. Bu iki olayın aynı anda gerçekleşme olasılığı sıfırdır.
- **Kesinlikle Gerçekleşen Olay (Olasılık = 1):** Bir futbol maçının sonunda ya bir takımın kazanması ya da maçın berabere bitmesi. Başka bir sonuç olamayacağı için bu olay kesinlikle gerçekleşir.

---

### Göreceli Frekans Yaklaşımı

Olasılık hesaplamanın çok yaygın ve pratik bir yolu, göreceli frekans yaklaşımıdır. Bir olayın birçok tekrarlanan deneme boyunca ne sıklıkta meydana geldiğini gözlemleyerek, olasılığını varsayımlar yerine gerçek verilere dayanarak tahmin edebiliriz.

Bu yaklaşım aşağıdaki adımlarda yapılır:

1.  Bir deneyi çok sayıda ($n$) kez gerçekleştirin.
2.  A olayının meydana geldiği sayı olan $N(A)$'yı sayın.
3.  Ardından, A olayının olasılığı: $P(A) = \frac{N(A)}{n}$ olur.

#### Günlük Hayattan Örnek:

Bir kahve makinesinin siparişleri ne sıklıkta yanlış hazırladığını tahmin etmek istediğinizi varsayalım.

- **Deneyi gerçekleştirin:** Makinenin son 100 siparişini inceleyin.
- **Meydana gelme sayısını sayın:** Makinenin 100 siparişten 5'ini yanlış hazırladığını buldunuz.
- **Olasılığı hesaplayın:** Formülü kullanarak, makinenin yanlış hazırlama olasılığı $P(\text{Yanlış Hazırlama}) = \frac{5}{100} = 0.05$ veya %5'tir.

---

### Klasik Yaklaşım

Örneklem uzayındaki sonuçların eşit derecede olası olduğu durumlarda, A olayının olasılığı:

$P(A) = \frac{N(A)}{N(S)}$

Burada:

- $N(A)$, A olayındaki eleman sayısıdır.
- $N(S)$, S örneklem uzayındaki eleman sayısıdır.

#### Günlük Hayattan Örnek:

Arkadaşlarınızla bir kart oyunu oynadığınızı varsayalım.

- **Deney:** Bir desteden rastgele bir kart çekmek.
- **Örneklem Uzayı (S):** Destedeki tüm kartlar, yani 52 kart. Bu nedenle $N(S)=52$'dir.
- **Olay A:** As (Ace) kartı çekmek.
- A olayını sağlayan sonuçlar: Destede 4 tane as kartı vardır. Bu nedenle $N(A)=4$'tür.
- **Olasılığı hesaplayın:** Klasik yaklaşımı kullanarak as çekme olasılığı: $P(A)=\frac{4}{52}\approx0.077$ veya yaklaşık %7.7'dir.

  ### Olayların Olasılığı: Farklı Yaklaşımlar

| Yaklaşım | Göreceli Frekans Yaklaşımı | Klasik Yaklaşım |
| :--- | :--- | :--- |
| **Temel Tanım** | Bir deneyin çok sayıda tekrarlanmasına dayanır. Bir olayın olasılığı, o olayın gerçekleştiği sayının toplam deneme sayısına oranıdır. | Bir deneyin tüm sonuçlarının eşit derecede olası olduğu varsayımına dayanır. Bir olayın olasılığı, o olayı sağlayan sonuç sayısının, tüm olası sonuçların sayısına oranıdır. |
| **Formül** | $P(A) = \frac{\text{A Olayının Gerçekleşme Sayısı}}{\text{Toplam Deneme Sayısı}}$ | $P(A) = \frac{\text{A Olayını Sağlayan Sonuç Sayısı}}{\text{Toplam Olası Sonuç Sayısı}}$ |
| **Ne Zaman Kullanılır?** | Sonuçların eşit derecede olası olup olmadığının bilinmediği veya varsayılamadığı durumlarda, genellikle geçmiş verilerle tahmin yapmak için kullanılır. Örneğin, bir fabrika üretim hatasının olasılığını bulmak. | Sonuçların eşit derecede olası olduğu, teorik olarak bilinen durumlar için kullanılır. Örneğin, zar atma, madeni para atma, kart çekme gibi deneyler. |
| **Avantajı** | Gerçek dünya verilerine dayanarak olasılık tahmini yapmamızı sağlar ve teorik varsayımlar gerektirmez. | Hesaplaması daha basittir ve deney yapılmadan olasılık değeri bulunabilir. |
| **Dezavantajı** | Doğru bir tahmin için çok sayıda deneme gerektirir. Küçük bir örneklemle yapılan hesaplamalar yanıltıcı olabilir. | Yalnızca tüm sonuçların eşit olasılıklı olduğu deneyler için geçerlidir. Gerçek hayattaki birçok durum için uygun değildir. |
| **Günlük Hayattan Örnek** | Bir basketbolcunun serbest atış isabet olasılığını hesaplamak. Basketbolcu geçmişte 1000 serbest atıştan 750'sini başarılı attıysa, olasılığı $750/1000 = 0.75$ (%75) olarak tahmin edilir. | Bir parayı havaya attığımızda tura gelme olasılığı. Tüm sonuçlar (yazı, tura) eşit olasılıklı olduğundan, olasılık $1/2 = 0.5$ (%50) olarak hesaplanır. |

### Çikolata Kutusu Metaforu

Bir kutu dolusu farklı çikolatan olduğunu düşün. Bu kutuda toplam **52** tane çikolata var ve her birinin içindeki dolgu eşit olasılığa sahip (çilekli, karamelli, fındıklı vb.).

- **Toplam Olası Sonuçlar:** Elindeki bütün çikolataların sayısı. Yani, **52** çikolata. Bu, olasılık formülündeki paydadır.
- **İstediğin Sonuçlar:** Kutudan çekmek istediğin çikolata türlerinin sayısı. Örneğin, fındıklı çikolataların tamamı. Bu, olasılık formülündeki paydır.

**Klasik Yaklaşımın Kuralı:** Olasılığı hesaplamak için istediğin sonuçların sayısını, tüm olası sonuçların sayısına bölersin.

$P(\text{İstenen Sonuç}) = \frac{\text{İstediğin Çikolata Sayısı}}{\text{Tüm Çikolataların Sayısı}}$

---

Şimdi bu mantıkla kart destesi sorusunu çözelim:

Bir iskambil destesindeki tüm kartlar (52 kart) eşit olasılığa sahiptir. Yani, tüm hesaplamalarda paydamız 52 olacak.

**a) Sinek (Heart) Çekme Olasılığı:**
- İstediğin sonuçlar: Destede 13 tane sinek kartı var.
- Hesaplama: $\frac{13}{52} = \frac{1}{4} = 0.25$

**b) Papaz (King) Çekme Olasılığı:**
- İstediğin sonuçlar: Destede 4 tane papaz var (sinek, maça, karo, kupa).
- Hesaplama: $\frac{4}{52} = \frac{1}{13} \approx 0.077$

**c) Kırmızı Kart Çekme Olasılığı:**
- İstediğin sonuçlar: Kırmızı kartlar sinek (hearts) ve karo (diamonds) türüdür. Her birinden 13 tane olduğu için toplamda 26 kırmızı kart vardır.
- Hesaplama: $\frac{26}{52} = \frac{1}{2} = 0.5$

**d) Resimli Kart (Face Card) Çekme Olasılığı:**
- İstediğin sonuçlar: Resimli kartlar Vale (Jack), Kız (Queen) ve Papaz'dır (King). Her birinden 4'er tane olduğu için toplam 12 resimli kart vardır.
- Hesaplama: $\frac{12}{52} = \frac{3}{13} \approx 0.231$

---
### Probability: Definition and Properties

We previously defined probability informally. Now, let's take a look at a formal definition using the axioms of probability:

Probability is defined as a set function $P$ that assigns to each event $A$ in the sample space $S$ a non-negative value called the probability of the event $A$, such that the following hold:

- The probability of any event $A$ is non-negative: $P(A) \ge 0$.
- The probability of the sample space is 1: $P(S) = 1$.
- Given mutually exclusive events $A_1, A_2, ...$, the probability of the union of these events equals the sum of their individual probabilities: $P(A_1 \cup A_2 \cup ...) = P(A_1) + P(A_2) + ...$.

---

### Theorem 1

The probability of an event $A$ occurring is equal to one minus the probability of its complement:
$P(A) = 1 - P(A')$
<img width="727" height="380" alt="image" src="https://github.com/user-attachments/assets/d5dc168d-5821-41de-8d50-2bccd454ced9" />


**Example:**
Consider a standard deck of 52 cards. Let event $A$ be drawing a Heart from the deck. There are 13 Hearts in the deck, so:
$P(A) = \frac{13}{52} = \frac{1}{4}$
The complement of A, denoted as $A'$, is drawing any card that is not a Heart. There are 39 non-Heart cards, so:
$P(A') = \frac{39}{52} = \frac{3}{4} = 1 - P(A)$

---

### Theorem 2

The probability of the empty set is zero:
$P(\emptyset) = 0$

**Example:**
Consider rolling a standard 6-sided die. Let event $A$ be rolling a number greater than 6. Since the die only has numbers from 1 to 6, there are no outcomes where the result is greater than 6. This means: $A = \emptyset$. Therefore, the probability of this event is:
$P(A) = 0$

---

### Theorem 3

If event $A$ is a subset of event $B$, then the probability of $A$ is less than or equal to the probability of $B$:
If $A \subseteq B$ then $P(A) \le P(B)$.

<img width="723" height="386" alt="image" src="https://github.com/user-attachments/assets/ad56126b-d5d9-4c2d-bb57-1f0f2b70f620" />


**Example:**
Consider drawing a card from a standard deck of 52 cards.
Let event $B$ be drawing a red card. There are 26 red cards (Hearts and Diamonds), so: $P(B) = \frac{26}{52} = \frac{1}{2}$
Let event $A$ be drawing a red Queen. There are only 2 red Queens (Queen of Hearts and Queen of Diamonds), so: $P(A) = \frac{2}{52}$
Drawing a red Queen is a more specific outcome that is fully contained within the event of drawing any red card ($A \subseteq B$), so: $P(A) \le P(B)$

---

### Theorem 4

The probability of any event $A$ is always less than or equal to 1:
$P(A) \le 1$

**Example:**
Consider rolling a standard 6-sided die.
Let event $A$ be rolling a number less than 7. Since all possible outcomes ({1, 2, 3, 4, 5, 6}) satisfy this condition, the probability is: $P(A) = \frac{6}{6} = 1$
Let event $B$ be rolling an even number. The even outcomes are {2, 4, 6}, so: $P(B) = \frac{3}{6} = \frac{1}{2}$
In both cases, the probability of each event is less than or equal to 1: $P(A) = 1$ and $P(B) = 0.5 \le 1$

---

### Theorem 5

The probability of the union of two events $A$ and $B$ is equal to the sum of their individual probabilities minus the probability of their intersection:
$P(A \cup B) = P(A) + P(B) - P(A \cap B)$

<img width="533" height="226" alt="image" src="https://github.com/user-attachments/assets/6d3b81a3-de76-4936-adc0-1cab499563ff" />


**Example:**
Consider a classroom of 30 students.
Let event $A$ be a student playing a musical instrument. Suppose 18 students play a musical instrument: $P(A) = \frac{18}{30} = \frac{3}{5}$
Let event $B$ be


---

### Olasılık: Tanım ve Özellikler

Daha önce olasılığı gayriresmi olarak tanımlamıştık. Şimdi olasılığın aksiyomlarını kullanarak resmi bir tanıma göz atalım:

Olasılık, örneklem uzayı S'deki her A olayı için P(A) adı verilen negatif olmayan bir değer atayan bir küme fonksiyonu olarak tanımlanır, öyle ki aşağıdaki koşullar geçerlidir:

- Herhangi bir A olayının olasılığı negatif değildir: $P(A) \ge 0$.
- Örneklem uzayının olasılığı 1'dir: $P(S) = 1$.
- Karşılıklı dışlayıcı (mutually exclusive) olaylar $A_1, A_2, ...$ verildiğinde, bu olayların birleşiminin olasılığı, bireysel olasılıklarının toplamına eşittir: $P(A_1 \cup A_2 \cup ...) = P(A_1) + P(A_2) + ...$.

---

### Teorem 1

Bir A olayının gerçekleşme olasılığı, onun tümleyeninin olasılığının birden çıkarılmasına eşittir:
$P(A) = 1 - P(A')$

**Örnek:**
Standart 52 kartlık bir desteyi düşünün. A olayı, desteden bir Sinek (Heart) çekmek olsun. Destede 13 adet Sinek vardır, bu yüzden:
$P(A) = \frac{13}{52} = \frac{1}{4}$
A'nın tümleyeni, $A'$ olarak gösterilir, Sinek olmayan herhangi bir kartı çekmektir. Destede 39 adet Sinek olmayan kart vardır, bu yüzden:
$P(A') = \frac{39}{52} = \frac{3}{4} = 1 - P(A)$

---

### Teorem 2

Boş kümenin olasılığı sıfırdır:
$P(\emptyset) = 0$

**Örnek:**
Standart 6 yüzlü bir zar atmayı düşünün. A olayı, 6'dan büyük bir sayı atmak olsun. Zarın sadece 1'den 6'ya kadar sayıları olduğundan, sonuç 6'dan büyük olan hiçbir sonuç yoktur. Bu, $A = \emptyset$ anlamına gelir. Bu nedenle, bu olayın olasılığı şudur:
$P(A) = 0$

---

### Teorem 3

Eğer A olayı B olayının bir alt kümesi ise, A'nın olasılığı B'nin olasılığından küçük veya eşittir:
Eğer $A \subseteq B$ ise $P(A) \le P(B)$.

**Örnek:**
Standart 52 kartlık bir desteden kart çekmeyi düşünün.
B olayı, kırmızı bir kart çekmek olsun. Destede 26 kırmızı kart (Sinek ve Karo) vardır, bu yüzden: $P(B) = \frac{26}{52} = \frac{1}{2}$
A olayı, kırmızı bir Kız (Queen) çekmek olsun. Sadece 2 kırmızı Kız (Sinek Kız ve Karo Kız) vardır, bu yüzden: $P(A) = \frac{2}{52}$
Kırmızı Kız çekmek, kırmızı kart çekme olayının daha spesifik bir sonucudur ve bu olayın tamamen içinde yer alır ($A \subseteq B$), bu yüzden: $P(A) \le P(B)$

---

### Teorem 4

Herhangi bir A olayının olasılığı daima 1'den küçük veya eşittir:
$P(A) \le 1$

**Örnek:**
Standart 6 yüzlü bir zar atmayı düşünün.
A olayı, 7'den küçük bir sayı atmak olsun. Tüm olası sonuçlar ({1, 2, 3, 4, 5, 6}) bu koşulu sağladığı için, olasılık şudur: $P(A) = \frac{6}{6} = 1$
B olayı, çift sayı atmak olsun. Çift sayılar {2, 4, 6}'dır, bu yüzden: $P(B) = \frac{3}{6} = \frac{1}{2}$
Her iki durumda da, her bir olayın olasılığı 1'den küçük veya eşittir: $P(A) = 1$ ve $P(B) = 0.5 \le 1$

---

### Teorem 5

İki olay A ve B'nin birleşiminin olasılığı, bireysel olasılıklarının toplamından kesişimlerinin olasılığının çıkarılmasına eşittir:
$P(A \cup B) = P(A) + P(B) - P(A \cap B)$

**Örnek:**
30 öğrencili bir sınıfı düşünün.
A olayı, bir öğrencinin müzik aleti çalması olsun. 18 öğrencinin müzik aleti çaldığını varsayalım: $P(A) = \frac{18}{30} = \frac{3}{5}$
B olayı, bir öğrencinin ikinci bir dil konuşması olsun. 15 öğrencinin ikinci bir dil konuştuğunu varsayalım: $P(B) = \frac{15}{30} = \frac{1}{2}$
10 öğrencinin hem müzik aleti çaldığını hem de ikinci bir dil konuştuğunu varsayalım. Bu, A ve B'nin kesişimidir: $P(A \cap B) = \frac{10}{30} = \frac{1}{3}$
İki olayın birleşimi formülünü kullanarak: $P(A \cup B) = P(A) + P(B) - P(A \cap B) = \frac{3}{5} + \frac{1}{2} - \frac{1}{3} = \frac{23}{30}$
Dolayısıyla, rastgele seçilen bir öğrencinin ya müzik aleti çalması ya da ikinci bir dil konuşması olasılığı 23/30'dur.

### Olasılığın Beş Temel Teoremi

Olasılık teorisinin bu beş temel teoremi, olaylar arasındaki ilişkileri ve olasılıkların nasıl hesaplandığını anlamak için kritik öneme sahiptir. Aşağıda, her bir teorem karşılaştırmalı olarak ve örneklerle açıklanmıştır.

---

#### Teorem 1 ve 2: Tümleme ve Boş Küme

Bu iki teorem, bir olayın gerçekleşme ve gerçekleşmeme durumları arasındaki ilişkiyi kurar.

| Teorem | Formül | Açıklama | Örnek |
| :--- | :--- | :--- | :--- |
| **Teorem 1**<br>(Tümleme Kuralı) | $P(A) = 1 - P(A')$ | Bir olayın olma olasılığı, olmama olasılığının ($A'$), 1'den çıkarılmasına eşittir. Bu, tüm olasılıkların toplamının 1 olduğu gerçeğine dayanır. | Bir desteden kupa çekme olasılığı $13/52$ ise, kupa çekmeme olasılığı $1 - 13/52 = 39/52$'dir. |
| **Teorem 2**<br>(Boş Küme) | $P(\emptyset) = 0$ | Gerçekleşmesi imkansız bir olayın olasılığı sıfırdır. Boş küme ($∅$), sonuçlar kümesinde hiçbir elemanı olmayan bir olayı temsil eder. | Altı yüzlü bir zar attığınızda, 7 gelme olasılığı 0'dır, çünkü bu imkansız bir sonuçtur. |

### Teorem 3 ve 4: Alt Küme ve Maksimum Olasılık

Bu teoremler, olasılıkların büyüklükleri ve birbiriyle ilişkileri hakkında temel kısıtlamalar getirir.

| Teorem | Formül | Açıklama | Örnek |
| :--- | :--- | :--- | :--- |
| **Teorem 3**<br>(Alt Küme Kuralı) | Eğer $A \subseteq B$ ise $P(A) \le P(B)$ | Eğer bir olay ($A$) başka bir olayın ($B$) alt kümesi ise, $A$'nın olma olasılığı $B$'nin olma olasılığından daha küçük veya eşittir. | Bir desteden kırmızı kız (red queen) çekme olasılığı ($A$), kırmızı kart çekme olasılığından ($B$) daha düşüktür, çünkü tüm kırmızı kızlar kırmızı karttır. |
| **Teorem 4**<br>(Maksimum Olasılık) | $P(A) \le 1$ | Herhangi bir olayın olasılığı asla 1'den büyük olamaz. Olasılıklar, en fazla tüm olası sonuçları kapsayan kesin olay kadar olabilir. | Bir zar attığınızda, 7'den küçük bir sayı gelme olasılığı 1'dir. Başka bir sonuç olamayacağı için olasılık 1'i geçemez. |

### Teorem 5: Birleşim Kuralı

Bu teorem, iki olayın birleşiminin olasılığını hesaplamak için kullanılır ve en karmaşık olanıdır.

| Teorem | Formül | Açıklama | Örnek |
| :--- | :--- | :--- | :--- |
| **Teorem 5**<br>(Birleşim Kuralı) | $P(A \cup B) = P(A) + P(B) - P(A \cap B)$ | İki olayın birleşim olasılığı, bireysel olasılıklarının toplamından, her ikisinin de aynı anda gerçekleşme olasılığının ($A \cap B$) çıkarılmasına eşittir. Bu çıkarma işlemi, ortak durumların iki kez sayılmasını önler. | 30 kişilik bir sınıfta, 18 kişinin enstrüman çaldığını ($A$) ve 15 kişinin Almanca konuştuğunu ($B$) düşünün. 10 kişi her ikisini de yapıyorsa, ya enstrüman çalan ya da Almanca konuşan birini seçme olasılığı $P(A) + P(B) - P(A \cap B) = 18/30 + 15/30 - 10/30 = 23/30$ olur. |

### Additive and Multiplication Principles

The **Additive Principle** is used when selecting between two distinct options that cannot occur at the same time. It states: If object A can be chosen in *n* ways, and object B can be chosen in *m* ways, then choosing either A or B can be done in *n + m* ways.

For example, when selecting a snack, if you can choose from 3 types of fruit (apple, banana, orange) and 2 types of granola bars, the total number of choices is $3 + 2 = 5$.

The **Multiplication Principle** applies when making sequential or independent choices. It states: If object A can be chosen in *n* ways, and object B can be chosen in *m* ways, then choosing both A and B can be done in *n x m* ways.

For example, when selecting an outfit, if you have 4 shirts and 3 pairs of pants, the total number of combinations to choose one shirt and one pair of pants is $4 \times 3 = 12$.

In a more complex scenario, such as choosing a meal, both principles can be combined. If a cafeteria offers a sandwich (5 options) or a salad (3 options), and you also want to choose a drink (4 types), the total number of combinations is calculated in two steps:
- Choosing either a sandwich or a salad: $5 + 3 = 8$
- Choosing a meal and a drink: $8 \times 4 = 32$

### Exercise

Imagine a school event where students can choose between participating in a science fair or a sports competition. There are 5 science fair categories and 4 sports activities. Additionally, each participant must choose one of 3 available T-shirt colors for the event.

How many combinations are there for choosing an activity and a T-shirt?

### Çözüm

Bu soru, kombinasyon sayısını bulmak için hem **Toplama Prensibi**'ni hem de **Çarpma Prensibi**'ni bir arada kullanmayı gerektirir.

#### Çözüm Adımları

1.  **Aktivite Seçimi:** Öğrencinin seçebileceği toplam aktivite sayısını bulmak için **Toplama Prensibi**'ni kullanırız. Çünkü öğrenci, ya bir bilim fuarı etkinliğine ya da bir spor etkinliğine katılabilir, ikisine birden katılamaz.
    - Bilim fuarı kategorileri: 5
    - Spor aktiviteleri: 4
    - Toplam Aktivite: $5 + 4 = 9$ farklı aktivite seçeneği vardır.

2.  **Kıyafet Seçimi:** Öğrenci, bir aktivite seçtikten sonra, bu aktivite seçimiyle bağımsız olarak bir tişört rengi de seçmelidir. Bu yüzden **Çarpma Prensibi**'ni kullanırız.
    - Toplam aktivite seçeneği: 9
    - Tişört rengi seçeneği: 3
    - Toplam Kombinasyon: $9 \times 3 = 27$

Yani, bir aktivite ve bir tişört rengi seçmek için toplamda **27 farklı kombinasyon** vardır.

---

### Toplama ve Çarpma İlkeleri

Toplama ve Çarpma İlkeleri, olasılık ve kombinatorik alanında bir dizi seçimin toplam olası sonucunu bulmak için kullanılan temel kurallardır.

---

### Toplama İlkesi (Additive Principle)

Bu ilke, aynı anda gerçekleşemeyen veya birbirini dışlayan iki ayrı olayın toplam olası sonucunu bulmak için kullanılır.

* **Ne Zaman Kullanılır?** Seçenekler arasında bir **VEYA (OR)** ilişkisi olduğunda. Yani, "ya A'yı ya da B'yi seçerim" dediğinizde bu ilkeyi kullanırsınız.
* **Kural:** Eğer bir olayın *$n$* farklı sonucu varsa ve diğer bir olayın *$m$* farklı sonucu varsa, bu iki olaydan birinin gerçekleşme toplam yolu *$n + m$*'dir.

#### Günlük Hayattan Örnek:

Bir kafe menüsünde sandviç veya salata seçeneğiniz olduğunu düşünün.
* Sandviç seçeneği: 5
* Salata seçeneği: 3
* Toplam Seçim Sayısı: $5 + 3 = 8$ farklı seçim yapabilirsiniz.

---

### Çarpma İlkesi (Multiplication Principle)

Bu ilke, ardışık veya bağımsız seçimlerin toplam olası sonucunu bulmak için kullanılır. Bir dizi karar alırken, her bir kararın sonucu diğer kararları etkilemediğinde bu ilke geçerlidir.

* **Ne Zaman Kullanılır?** Seçenekler arasında bir **VE (AND)** ilişkisi olduğunda. Yani, "hem A'yı hem de B'yi seçerim" dediğinizde bu ilkeyi kullanırsınız.
* **Kural:** Eğer bir olayın *$n$* farklı sonucu varsa ve ikinci bir olayın *$m$* farklı sonucu varsa, bu iki olayın arka arkaya gerçekleşme toplam yolu *$n \times m$*'dir.

#### Günlük Hayattan Örnek:

Bir kıyafet kombinasyonu yaptığınızı düşünün.
* Gömlek seçeneği: 4
* Pantolon seçeneği: 3
* Toplam Kombinasyon Sayısı: $4 \times 3 = 12$ farklı kombinasyon oluşturabilirsiniz.

---

### Birleşik Örnek: Her İki İlkenin Birlikte Kullanımı

Bazı durumlarda her iki ilkeyi de kullanmanız gerekebilir.

#### Günlük Hayattan Örnek:

Bir kafeteryada yemek ve içecek seçimi yapıyorsunuz.
* **Adım 1: Yemeği Seçme (Toplama İlkesi)**
    * Sandviç: 5 seçenek
    * Salata: 3 seçenek
    * Toplam Yemek Seçeneği: $5 + 3 = 8$
* **Adım 2: Yemek ve İçeceği Seçme (Çarpma İlkesi)**
    * Toplam Yemek Seçeneği: 8
    * İçecek Seçeneği: 4
    * Toplam Kombinasyon: $8 \times 4 = 32$

Sonuç olarak, 32 farklı yemek ve içecek kombinasyonu yapabilirsiniz.


### Toplama ve Çarpma İlkeleri Karşılaştırması

| Özellik | Toplama İlkesi | Çarpma İlkesi |
| :--- | :--- | :--- |
| **Kullanım Amacı** | Birbirini dışlayan, **aynı anda gerçekleşemeyen** olayların toplam sonucunu bulmak. | **Ardışık veya bağımsız** olayların toplam kombinasyon sayısını bulmak. |
| **Mantıksal Bağ** | Seçenekler arasında **"VEYA" (`OR`)** ilişkisi vardır. (Ya A ya da B) | Seçenekler arasında **"VE" (`AND`)** ilişkisi vardır. (Hem A hem B) |
| **Matematiksel İşlem** | **Toplama** (`+`) | **Çarpma** (`*`) |
| **Teknik Kural** | Eğer olay $A$, $n$ farklı şekilde ve olay $B$, $m$ farklı şekilde gerçekleşiyorsa, ikisinden birinin gerçekleşme sayısı $n + m$'dir. | Eğer olay $A$, $n$ farklı şekilde ve olay $B$, $m$ farklı şekilde gerçekleşiyorsa, ikisinin de gerçekleşme sayısı $n \times m$'dir. |
| **Günlük Hayattan Örnek** | Bir restoranda, **ya** bir pizza (**10 çeşit**) **ya da** bir makarna (**8 çeşit**) seçme sayısı: $10 + 8 = 18$ farklı seçim. | Bir restoranda, **hem** bir ana yemek (**10 çeşit**) **hem de** bir içecek (**8 çeşit**) seçme sayısı: $10 \times 8 = 80$ farklı kombinasyon. |
| **Önemli Not** | Seçimler arasında bir kesişim olamaz. Bir pizza seçtiğinizde, bir makarna seçemezsiniz. | Seçimler birbirinden bağımsızdır. Bir ana yemek seçimi, içecek seçimi sayısını etkilemez. |

### Permutations

#### Introduction
Permutations refer to the number of ways to arrange a set of distinct objects in a specific order. The **order of arrangement matters** in permutations.

Let's take a look at the example.

#### Example: Arranging Books on a Shelf
Suppose you have 4 different books and you want to arrange them on a shelf.
- For the first position, you have 4 choices.
- For the second position, you have 3 remaining choices.
- For the third position, 2 choices.
- For the last position, 1 choice.

By the Multiplication Principle, the total number of ways to arrange the books is: $P_4 = 4 \times 3 \times 2 \times 1 = 24$.
So, there are 24 different ways to arrange 4 books.

#### A Generalisation of the Multiplication Principle
Suppose there are $n$ positions to be filled with $n$ different objects, in which there are:
- $n$ choices for the 1st position;
- $n-1$ choices for the 2nd position;
- $n-2$ choices for the 3rd position;
- ... and ...
- 1 choice for the last position.

The Multiplication Principle tells us there are then in general: $P_n = n \times (n-1) \times (n-2) \times ... \times 1 = n!$

> Permutation of $n$ objects is an ordered arrangement of $n$ objects and is denoted as $P_n$.

---

### Exercise
What is the number of ways to line up 5 students for a class photo?

#### Solution
$P_5 = 5! = 120$

> Permutations are used when the order of arrangement is important. The total number of ways to arrange distinct objects is given by $n!$, which is the product of all positive integers up to $n$, following the Multiplication Principle.
---

### Permütasyon

Permütasyon, belirli sayıda nesnenin, belirli bir sıraya göre dizilme şekillerinin sayısıdır. Bu konunun en önemli özelliği, **sıranın önemli olmasıdır**.

#### Permütasyon Nedir?

Permütasyon, bir kümedeki elemanların farklı sıralanışlarını inceler. Eğer sıralama değiştiğinde sonuç da değişiyorsa, permütasyondan bahsedilir.

#### Günlük Hayattan Örnek:

- **Şifre Belirleme:** Bir telefonun 4 haneli şifresini düşünün. "1234" şifresi ile "4321" şifresi aynı değildir. Rakamların sırası önemlidir, bu yüzden bu bir permütasyondur.
- **Yarış Sıralaması:** 10 kişinin katıldığı bir koşu yarışında, ilk 3'e girenlerin sıralaması önemlidir (birinci, ikinci ve üçüncü). Ahmet'in birinci, Mehmet'in ikinci olması ile tam tersi durum aynı değildir.

---

### Permütasyon Nasıl Hesaplanır?

Permütasyon, "Çarpma İlkesi"nin özel bir halidir. Elinizdeki nesne sayısı ($n$) kadar farklı pozisyon varsa, her bir pozisyon için bir önceki pozisyonda kullanılamayan elemanlar kalır. Bu durum, faktöriyel ($!$) ile gösterilir.

#### Günlük Hayattan Örnek:

Elinizde 4 farklı kitap (A, B, C, D) var ve bunları bir rafa dizmek istiyorsunuz.
- 1. pozisyon için: 4 kitabın hepsi bir seçenek. (4 tercih)
- 2. pozisyon için: İlk kitabı koyduğunuz için geriye 3 kitap kaldı. (3 tercih)
- 3. pozisyon için: Geriye 2 kitap kaldı. (2 tercih)
- 4. pozisyon için: Son kitap kaldı. (1 tercih)
Bu durumda, toplam sıralama sayısı $4 \times 3 \times 2 \times 1 = 24$'tür. Bu, matematiksel olarak $4!$ (4 faktöriyel) olarak ifade edilir.

---

### Formül:

- Birbirinden farklı $n$ nesnenin sıralanma sayısı $P_n$ ile gösterilir ve $P_n = n!$'dir.
- Eğer belirli bir sayıdaki nesneden ($n$), daha az sayıda nesneyi ($r$) sıralamak istiyorsanız, formül şöyledir: $P(n,r) = \frac{n!}{(n-r)!}$

#### Örnek:
10 kişilik bir sınıftan 3 kişilik bir başkanlık divanı (başkan, başkan yardımcısı, sekreter) seçmek. Sıralama önemli olduğu için bu bir permütasyon problemidir.
$P(10,3) = \frac{10!}{(10-3)!} = \frac{10!}{7!} = 10 \times 9 \times 8 = 720$'dir.
Yani 720 farklı şekilde başkanlık divanı oluşturulabilir.

---

### Arrangements (k-Permutations)

#### Introduction
**Arrangements**, also known as **placements** or **k-permutations**, refer to the number of ways to arrange a subset of *k* objects selected from a larger set of *n* distinct objects, where the **order of arrangement matters**.

Let's look at an example to illustrate this principle.

#### Example: Arranging Students for Awards
Imagine you have 8 students competing, and you need to select and arrange 3 of them to receive gold, silver, and bronze medals.
- For the first place (gold), you have 8 choices.
- For the second place (silver), you have 7 choices remaining.
- For the third place (bronze), you have 6 choices left.

<img width="360" height="295" alt="image" src="https://github.com/user-attachments/assets/676d141a-c5e7-418a-baf0-2614a051fc49" />



By applying the **Multiplication Principle**, the total number of ways to arrange the awards is: $8 \times 7 \times 6 = 336$.
Therefore, there are **336** possible ways to award medals to 3 out of 8 students.

---

### The General Formula
For situations involving an arrangement of *k* objects selected from a set of *n* distinct objects, the total number of arrangements, denoted as $P(n,k)$ or $A(n,k)$, can be generalized with the following formula:

$P(n,k) = \frac{n!}{(n-k)!}$

This formula represents the product of the first *k* terms of *n* factorial, which is: $n \times (n-1) \times (n-2) \times ... \times (n-k+1)$.

#### Connection to Permutations
A **permutation** is a special case of an arrangement where the number of selected objects is equal to the total number of available objects (i.e., when $n=k$). In this scenario, the formula simplifies to $P(n,n) = n!$.

---

### Exercise
Imagine you need to create a 4-character password using distinct digits from 0 to 9. How many unique ways can you do this?

#### Solution
This is an arrangement problem because the **order of the digits matters**, and we are selecting a subset of 4 digits from a larger set of 10.
- Total objects ($n$): 10 (digits 0-9)
- Objects to be arranged ($k$): 4

Using the arrangement formula, the total number of unique passwords is:
$P(10,4) = \frac{10!}{(10-4)!} = \frac{10!}{6!} = 10 \times 9 \times 8 \times 7 = 5040$
Thus, there are **5,040** unique ways to create a 4-digit password using distinct digits.

---

# Combinations: Selecting Items Without Regard to Order

## 1. Introduction to Combinatorial Selection

In various fields, from probability theory and statistics to computer science and daily decision-making, we frequently encounter situations where we need to select a subset of items from a larger collection. These selection processes can broadly be categorized into two main types: those where the **order of selection matters** (permutations or arrangements) and those where the **order of selection does not matter** (combinations). This lesson focuses exclusively on the latter: **combinations**.

A **combination** refers to the selection of items from a larger set where the sequence or arrangement of the chosen items is irrelevant. The emphasis is solely on the *composition* of the chosen group, not the chronological order in which the elements were picked. This fundamental distinction sets combinations apart from permutations, where every different ordering of the same set of items is considered a unique outcome.

To illustrate this core concept, let us consider a concrete example.

## 2. Differentiating Combinations from Permutations: An Illustrative Example

### Example: Selecting Fruits from a Basket

Imagine you have a basket containing 5 distinct types of fruits: Apple (A), Banana (B), Cherry (C), Date (D), and Elderberry (E). You are asked to choose 3 types of fruit from this basket. How many unique selections of 3 fruits can you make?

Let's begin by approaching this problem from the perspective of **arrangements (permutations)**, as a preliminary step to understanding combinations.

* **First Selection:** You have 5 distinct options for the first fruit.
* **Second Selection:** After choosing the first, 4 distinct options remain for the second fruit.
* **Third Selection:** Finally, 3 distinct options are left for the third fruit.

Using the multiplication principle for permutations, the total number of ordered arrangements of 3 fruits chosen from 5 is given by:

$$P(n, k) = n \times (n-1) \times \dots \times (n-k+1) = \frac{n!}{(n-k)!}$$

In our case, $P(5, 3) = 5 \times 4 \times 3 = 60$ possible arrangements.

However, a crucial point of divergence arises here. In the context of arrangements, selecting (Apple, Banana, Cherry) is considered a distinct outcome from selecting (Banana, Apple, Cherry), or (Cherry, Apple, Banana), and so forth. All six possible orderings of these three specific fruits are counted as separate entities in permutations.

To clarify, for any given set of 3 distinct fruits (e.g., Apple, Banana, Cherry), there are $3!$ (3 factorial) ways to arrange them:

$$3! = 3 \times 2 \times 1 = 6$$

These 6 arrangements are:

* (Apple, Banana, Cherry)
* (Apple, Cherry, Banana)
* (Banana, Apple, Cherry)
* (Banana, Cherry, Apple)
* (Cherry, Apple, Banana)
* (Cherry, Banana, Apple)

Each unique group of 3 fruits, when considered as a combination, has been overcounted precisely $3!$ times in our permutation calculation. To correct this overcounting and derive the number of unique combinations, we must divide the total number of arrangements by the number of ways to arrange the chosen items.

Therefore, the number of distinct ways to select 3 fruits from a basket of 5, where the order of selection does not matter, is:

$$\text{Number of Combinations} = \frac{\text{Number of Permutations}}{\text{Number of arrangements of chosen items}} = \frac{60}{3!} = \frac{60}{6} = 10$$

Thus, there are 10 distinct ways to choose 3 fruits from 5 when the order is not a factor.

🎓 **Key Concept:** Combinations deal with the selection of items where the internal order of the selected subset is irrelevant. This distinguishes them from permutations, which are concerned with ordered arrangements.

## 3. The General Formula for Combinations

The general formula for calculating the number of ways to choose $k$ items from a set of $n$ distinct items, without regard to the order of selection, is given by the binomial coefficient, often read as "n choose k":

$$C(n, k) = \binom{n}{k} = \frac{n!}{k!(n-k)!}$$

Where:

* $n$ represents the total number of distinct items available in the set.
* $k$ represents the number of items to be chosen from the set.
* $n!$ (n factorial) is the product of all positive integers up to n ($n \times (n-1) \times \dots \times 1$).
* $0!$ is defined as 1.

This formula essentially takes the total number of permutations $P(n, k) = \frac{n!}{(n-k)!}$ and divides it by $k!$ to account for the redundant orderings within each selected group of $k$ items.

## 4. Applying the Combination Formula: An Advanced Example

### Example: Selecting Novels for Summer Reading

A library possesses a collection of 7 distinct novels, and you intend to borrow 4 of them to read over the summer holiday. Given that the sequence in which you choose the books does not influence the set of books you ultimately take home (i.e., picking Novel A then B is the same as picking Novel B then A), this scenario constitutes a combination problem.

Using the general combinations formula with $n=7$ (total novels) and $k=4$ (novels to choose):

$$C(7, 4) = \binom{7}{4} = \frac{7!}{4!(7-4)!} = \frac{7!}{4!3!}$$

Let's compute the factorials:

* $7! = 7 \times 6 \times 5 \times 4 \times 3 \times 2 \times 1 = 5040$
* $4! = 4 \times 3 \times 2 \times 1 = 24$
* $3! = 3 \times 2 \times 1 = 6$

Substitute these values back into the formula:

$$C(7, 4) = \frac{5040}{24 \times 6} = \frac{5040}{144} = 35$$

Therefore, there are 35 distinct ways to choose 4 novels from the 7 available in the library.

## 5. Practice Exercise

Now, it's your opportunity to apply this knowledge.

🤔 **Exercise:**
A gourmet bakery offers a selection of 8 distinct types of muffins. You wish to purchase a box containing 3 different muffins to share with your friends. Assuming the order in which you pick the muffins does not matter for the final composition of your box, how many different combinations of 3 muffins can you choose?

### Solution:

Identify $n$ (total items) and $k$ (items to choose).
$n = 8$ (types of muffins)
$k = 3$ (muffins to choose)

Apply the combination formula:

$$C(8, 3) = \binom{8}{3} = \frac{8!}{3!(8-3)!} = \frac{8!}{3!5!}$$

Calculate factorials:

* $8! = 8 \times 7 \times 6 \times 5 \times 4 \times 3 \times 2 \times 1 = 40320$
* $3! = 3 \times 2 \times 1 = 6$
* $5! = 5 \times 4 \times 3 \times 2 \times 1 = 120$

Substitute into the formula:

$$C(8, 3) = \frac{40320}{6 \times 120} = \frac{40320}{720} = 56$$

There are **56** different combinations of 3 muffins you can choose from the 8 available types.

## 6. Conclusion and Future Outlook

🎉 In this comprehensive lesson, we have thoroughly explored the concept of combinations, emphasizing their distinction from permutations by focusing on selections where the order is irrelevant. We've defined the general formula and applied it to practical scenarios, demonstrating its utility in calculating the number of unique groups that can be formed. A strong grasp of combinations is foundational for advanced topics in probability, statistics, and discrete mathematics. In subsequent lessons, we will delve into more complex problems and variations, further solidifying your understanding and enhancing your combinatorial problem-solving skills.
