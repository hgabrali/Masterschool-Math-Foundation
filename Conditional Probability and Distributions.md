# Conditional Probability and Distributions



## Introduction
In many real-world situations, the probability of an event depends on whether another event has occurred. This relationship is captured by **conditional probability**. Conditional probability measures the likelihood of an event occurring given that another event has already happened.

## Definition of Conditional Probability
The conditional probability of event $A$ given that event $B$ has occurred is denoted as $P(A|B)$ and is defined as:

$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

<img width="746" height="465" alt="image" src="https://github.com/user-attachments/assets/d5ec7885-e288-4e78-a99b-e15a55da9713" />


---

# Example 1: Drawing a Ball

A box contains 6 white balls and 4 red balls. We randomly (and without replacement) draw two balls from the box. What is the probability that the second ball selected is red, given that the first ball selected is white?

## Solution
Let $A$ be an event drawing a red ball; and $B$ be an event drawing a white ball. The probability of first drawing a white ball is given by:

$$P(B) = \frac{6}{10} = 0.6$$

Now, we have 9 balls left in the box, and if the first drawn ball was white, we have 5 white and 4 red balls in the box. Hence,

$$P(A|B) = \frac{4}{9} \approx 0.44$$

---

# Example 2: Deck of Cards

What is the probability that two cards drawn from a 36-card deck belong to the same suit?

## Solution
Let $A$ be an event of drawing a card of a given suit and event $B$ - an event of drawing a card of the same suit. Hence,

* $P(A) = 0.25$
* $P(B|A) = 8/35 \approx 0.23$ since among the 35 cards left only 8 cards have the same suit as the first card drawn.

---

# Multiplication Rule

The probability that two events $A$ and $B$ both occur is given by:

$$P(A \cap B) = P(A|B) \times P(B)$$

or by

$$P(A \cap B) = P(B|A) \times P(A)$$

---

# Example: Drawer of Socks

A drawer contains 6 black socks and 4 white socks. Two socks are drawn randomly, one after the other without replacement.

* a) What is the probability that the first sock is black and the second sock is also black?
* b) Use the multiplication rule to calculate the joint probability of both events.

## Solution
Let event $A$ be drawing a black sock and event $B$ - drawing a black sock the second time in a row. Then

* $P(A) = 6/10 = 0.6$
* $P(B|A) = 5/9 \approx 0.56$

And the joint probability, which is drawing black socks two times in a row, is given by

$$P(A \cap B) = P(A) \cdot P(B|A) \approx 0.6 \cdot 0.56 \approx 0.33$$

---

# Practice

Now it is time for you to practice calculating conditional and joint probabilities.

## Exercise 1
A bag contains 5 red, 3 blue, and 2 green marbles. If a marble is drawn and is known to be **not red**, what is the probability that it is **blue**?

### Solution
We have 3 blue and 2 green marbles, so a total of 5 not red marbles. Then the probability of drawing a blue marble given that it is known not to be red, is:

$$P(A|B) = \frac{3}{5} = 0.6$$

---

## Exercise 2
A company has 60 employees, 20 of whom are in management. If a randomly selected employee is in a meeting and 15 managers are currently in meetings while 25 non-managers are also in meeting, what is the probability that the employee is a **manager**?

### Solution
The probability of selecting an employee, who is a manager, under the condition they are at the meeting, is

$$P(A|B) = \frac{15}{15+25} = 0.375$$

---

## Exercise 3
A factory produces 100 lightbulbs, of which 10 are defective. Two lightbulbs are selected randomly, one after the other without replacement.

* a) What is the probability that the first lightbulb selected is defective and the second lightbulb is not defective?
* b) Use the multiplication rule to calculate the joint probability of these two events.

### Solution
We have 10 defective and 90 non defective bulbs before the experiment. The probability of the first lightbulb to be defective is

$$P(A) = \frac{10}{100} = 0.1$$

We have 99 bulbs left, 90 of which are not defective. The probability of the second lightbulb not to be defective is

$$P(B|A) = \frac{90}{99} \approx 0.91$$

And the joint probability, which stands for selecting a defective lightbulb and a non-defective one right after it is

$$P(A \cap B) = P(A) \cdot P(B|A) \approx 0.1 \cdot 0.91 = 0.091$$

* Conditional probability helps us understand how the likelihood of an event changes when we know that another event has occurred. This concept is fundamental in making informed decisions under uncertainty.

---

# Koşullu Olasılık (Conditional Probability) Nedir?

Koşullu olasılık, bir olayın, **başka bir olayın zaten gerçekleştiği bilindiğinde** ortaya çıkma olasılığını ifade eder. Başka bir deyişle, bir olayın gerçekleşme ihtimalini, elimizdeki **ek bilgiye** dayanarak yeniden hesaplamaktır.

## Örnekle Açıklama: Zar Atma

Bu durumu bir örnekle açıklayalım:

Farz edelim ki, bir zar atıyorsunuz. Normalde "zarın 6 gelme olasılığı" $1/6$'dır. Bu, hiçbir ek bilginin olmadığı durumdaki olasılıktır.

Peki, size **"zarın çift sayı geldiği bilindiğinde, zarın 6 gelme olasılığı nedir?"** diye sorsam?

1.  **İlk Durumdaki Tüm Olasılıklar (Örneklem Uzayı):**
    $$S = \{1, 2, 3, 4, 5, 6\} \quad \text{(6 durum)}$$

2.  **Yeni Durum (Verilen Ek Bilgi):**
    "Zarın **çift sayı** geldiği bilgisi." Bu durumda, olasılık uzayımız küçülür. Sadece çift sayıların olduğu kümeye odaklanıyoruz:
    $$\text{Yeni Durum} = \{2, 4, 6\} \quad \text{(3 durum)}$$

3.  **Koşullu Olasılık Hesaplaması:**
    Bu yeni "olasılık uzayında" 6 gelme olasılığı nedir?
    * İstenen durum sayısı (6 gelmesi): 1 durum
    * Toplam durum sayısı (Yeni Durum): 3 durum

    Bu yüzden, **"zarın çift sayı geldiği bilindiğinde, zarın 6 gelme olasılığı"** $1/3$'tür.

Gördüğün gibi, ek bilgi sayesinde olasılık değeri $1/6$'dan $1/3$'e yükseldi.

---

## Formül ve Gösterim

Koşullu olasılık genellikle şu şekilde gösterilir ve okunur:

$$\mathbf{P(A|B)}$$

Bu, "$B$ olayı gerçekleştiği bilindiğinde $A$ olayının olasılığı" anlamına gelir.

**Formülü** ise şöyledir:

$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

### Formül Bileşenleri

* **$P(A|B)$:** B olayı gerçekleştiğinde A olayının koşullu olasılığı.
* **$P(A \cap B)$:** Hem $A$ olayının hem de $B$ olayının **birlikte** gerçekleşme olasılığı (Kesişim Kümesi).
* **$P(B)$:** $B$ olayının gerçekleşme olasılığı.

---

## Formülü Örnekle Uygulama

Yukarıdaki zar örneğini formül ile doğrulayalım:

* **$A$:** Zarın 6 gelmesi olayı.
* **$B$:** Zarın çift sayı gelmesi olayı.

1.  **$P(A \cap B)$ Hesaplaması:**
    * Zarın hem 6 **hem de** çift sayı gelme olasılığı. Bu sadece 6 gelmesi olayıdır.
    * $$P(A \cap B) = 1/6$$

2.  **$P(B)$ Hesaplaması:**
    * Zarın çift sayı gelme olasılığı. (Olasılık kümesi $\{2, 4, 6\}$)
    * $$P(B) = 3/6 = 1/2$$

3.  **Formülde Yerine Koyma:**
    $$P(A|B) = \frac{P(A \cap B)}{P(B)} = \frac{1/6}{1/2}$$

4.  **Sonuç:**
    $$P(A
# Gündelik Hayattan Koşullu Olasılık Örnekleri

Koşullu olasılık, günlük kararlarımızın ve çıkarımlarımızın birçoğunda farkında olmadan kullandığımız bir kavramdır. İşte bu kavramı daha iyi anlamak için bazı basit örnekler:

---

## Örnek 1: Trafik ve Yağmur

**Senaryo:** Sabah işe giderken iki farklı yol kullanma seçeneğin var. Normalde her iki yolda da trafik olasılığı aynıdır. Ancak, hava durumunu kontrol ettiğinde yağmur yağdığını görüyorsun.

* **Olay A:** Trafikte kalma olasılığın.
* **Olay B:** Yağmur yağması olayı.

Normalde $P(A)$ olasılığı, yani trafikte kalma olasılığın, yağmur bilgisi olmadan değerlendirilir. Ancak, **yağmurun (B olayı) gerçekleştiği bilindiğinde**, yani $P(A|B)$ koşullu olasılığına baktığımızda, trafikte kalma olasılığın artar. Çünkü yağmur, insanların daha yavaş sürmesine veya kaza yapmasına neden olabilir.

---

## Örnek 2: Hastalık Teşhisi ve Test Sonuçları

**Senaryo:** Belirli bir hastalığı taşıma riskin var. Normalde bu hastalığın toplumdaki görülme sıklığı $P(H)$'dir. Ancak bir test yaptırdın ve sonuç pozitif çıktı.

* **Olay H:** Hastalığı taşıma olasılığın.
* **Olay P:** Test sonucunun pozitif çıkması olayı.

Test yapılmadan önce hastalığı taşıma olasılığın $P(H)$ idi. Ancak **testin pozitif çıktığı bilindiğinde**, yani $P(H|P)$ koşullu olasılığına baktığımızda, hastalığı taşıma olasılığın önemli ölçüde artar. Bu yeni bilgi, başlangıçtaki olasılığı değiştirecektir.

---

## Örnek 3: Kart Oyunları ve El Seçimi

**Senaryo:** Bir iskambil destesinde bir kart çekiyorsun.

* **Olay A:** Çektiğin kartın karo (maça, kupa, sinek gibi bir tür) olması olasılığı.
* **Olay B:** Çektiğin kartın bir as olması olasılığı.

Normalde desteden rastgele bir kart çektiğinde, bir as gelme olasılığı $P(B) = 4/52$'dir. Ancak birisi sana **"çekilen kartın kırmızı renkte (kupa veya karo) olduğu"** bilgisini verdiğinde, as çekme olasılığın değişir. Çünkü artık tüm kartlar yerine, sadece kırmızı kartlar arasından bir as çekme olasılığını düşünmen gerekir.

Bu durumda:
* Kırmızı kart sayısı: 26 (13 kupa, 13 karo)
* Kırmızı as sayısı: 2 (Kupa Ası, Karo Ası)

Yeni durumda as çekme olasılığın $2/26$'dır, yani $1/13$. Gördüğün gibi, ek bilgi olasılığı $4/52$'den $2/26$'ya yükseltti.

---

Bu örnekler, koşullu olasılığın günlük hayatımızda nasıl işlediğini gösteriyor. Verilerimize yeni bir bilgi eklendiğinde, olayların olasılıklarını yeniden değerlendirmemiz gerektiğini hatırlatıyor.
