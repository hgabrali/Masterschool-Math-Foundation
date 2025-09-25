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

### Temel Küme İşlemleri

| İşlem | Sembol | Açıklama | Örnek |
| :--- | :--- | :--- | :--- |
| **Birleşim** | $A \cup B$ | **A kümesinde**, **B kümesinde** veya **her ikisinde** de bulunan tüm elemanların kümesi. | Eğer $A = \{1, 2, 3\}$ ve $B = \{3, 4, 5\}$ ise, $A \cup B = \{1, 2, 3, 4, 5\}$ olur. |
| **Kesişim** | $A \cap B$ | Hem A kümesinde hem de B kümesinde **ortak olarak** bulunan elemanların kümesi. | Eğer $A = \{1, 2, 3\}$ ve $B = \{3, 4, 5\}$ ise, $A \cap B = \{3\}$ olur. |
| **Tümleme** | $A'$ veya $A^c$ | Evrensel kümedeki (uzaydaki) ancak A kümesinde **bulunmayan** tüm elemanların kümesi. | Eğer evrensel küme $U = \{1, 2, 3, 4, 5\}$ ve $A = \{1, 2\}$ ise, $A^c = \{3, 4, 5\}$ olur. |
| **Fark** | $A - B$ | **A kümesinde olan**, ancak B kümesinde **olmayan** elemanların kümesi. | Eğer $A = \{1, 2, 3\}$ ve $B = \{3, 4, 5\}$ ise, $A - B = \{1, 2\}$ olur. |
| **Boş Küme** | $\emptyset$ veya {} | Hiçbir eleman içermeyen bir küme. | Kesişimi olmayan (ortak elemanları olmayan) iki kümenin kesişimi boş kümedir. |

