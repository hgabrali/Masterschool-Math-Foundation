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

---

# Bağımsız ve Bağımlı Olaylar (Independent and Dependent Events)

## Giriş

Olasılıkta, olaylar arasındaki ilişkiyi anlamak, sonuçların gerçekleşme olasılığını doğru bir şekilde hesaplamak için hayati öneme sahiptir. Olaylar, birinin gerçekleşmesinin diğerinin olasılığını etkileyip etkilemediğine bağlı olarak **bağımsız** veya **bağımlı** olarak sınıflandırılır.

---

## Bağımsız Olaylar (Independent Events)

İki olay, $A$ ve $B$, birinin gerçekleşmesinin diğerinin olasılığını **etkilememesi** durumunda **bağımsızdır**.

Matematiksel olarak bu, koşullu olasılık formülüyle ifade edilir:

$$\mathbf{P(A|B) = P(A)}$$

Yani, $B$ olayının gerçekleştiği bilgisi, $A$ olayının olasılığını değiştirmez.

### Bağımsızlık İçin Çarpma Kuralı

Koşullu olasılıktan gelen çarpma kuralında ($P(A \cap B) = P(A|B) \times P(B)$), $P(A|B)$ yerine $P(A)$ koyarsak, bağımsız olaylar için geçerli olan temel tanıma ulaşırız:

> 🎓 **Tanım:** $A$ ve $B$ olayları, ancak ve ancak aşağıdaki koşulu sağlıyorsa bağımsızdır:
>
> $$\mathbf{P(A \cap B) = P(A) \times P(B)}$$

### Örnek 1: Madeni Para ve Zar

Bir madeni parayı havaya attığımızı ve bir zar attığımızı düşünelim. $A$ olayı paranın "Tura" gelmesi, $B$ olayı ise zarın "4" gelmesi olsun. Parayı atmak zarın sonucunu etkilemediği için bu olaylar bağımsızdır.

* $P(A) = 1/2$
* $P(B) = 1/6$
* $P(A \cap B) = P(\text{Tura ve 4}) = P(A) \times P(B) = (1/2) \times (1/6) = 1/12$

### Örnek 2: Anket

Bir öğrenci anketine göre, öğrencilerin **%10'u** bisikletle işe/okula gidiyor ve **%40'ının** bir sevgilisi var. Bu iki olayın bağımsız olduğunu varsayarsak, öğrencilerin yüzde kaçı **hem** bisikletle gidiyor **hem de** sevgilisi var?

* $B$: Bisikletle gidiyor ($P(B) = 0.10$)
* $S$: Sevgilisi var ($P(S) = 0.40$)

Eğer $B$ ve $S$ bağımsız ise:
$$\mathbf{P(B \cap S) = P(B) \times P(S) = 0.10 \times 0.40 = 0.04}$$

Yani, öğrencilerin **%4'ü** hem bisikletle gidiyor hem de sevgilisi var.

---

## Bağımlı Olaylar (Dependent Events)

> 🎓 **Tanım:** İki olay, $A$ ve $B$, birinin gerçekleşmesinin diğerinin olasılığını **etkilemesi** durumunda **bağımlıdır**.

Bu ilişki, bağımsız olaylardaki eşitliğin bozulmasıyla ifade edilir:
$$\mathbf{P(A|B) \neq P(A)}$$

ve çarpma kuralında koşullu olasılık kullanılır:

$$\mathbf{P(A \cap B) = P(A|B) \times P(B)}$$

---

## Karşılıklı Hariç Olan Olaylar (Mutually Exclusive Events)

> 🎓 **Tanım:** İki olayın aynı anda gerçekleşmesi mümkün değilse, bu olaylara **karşılıklı hariç** (ayrık) olaylar denir.
>
> $$\mathbf{P(A \cap B) = 0}$$
>
> 🎯 **Önemli Not:** Bir olayın gerçekleşmesi, diğerinin gerçekleşmemesiyle sonuçlanacağından, **karşılıklı hariç olan olaylar daima bağımlıdır**. (Örn: Bir madeni paranın aynı anda hem Tura hem de Yazı gelmesi mümkün değildir.)

---

## Uygulama: Bağımlılık Kararı

Aşağıdaki örneklerde olayların bağımlı mı yoksa bağımsız mı olduğunu belirleyelim:

### Alıştırma 1: Hava Durumu ve Piknik

Bir aile piknik yapmayı planlıyor. $A$ olayı "yağmur yağması" ve $B$ olayı "ailenin piknik yapması" olsun. Olaylar bağımsız mı, bağımlı mı?

**Çözüm:** Bu olaylar **bağımlıdır**, çünkü ailenin piknik yapıp yapmaması ($B$), yağmur yağıp yağmamasına ($A$) bağlıdır.

### Alıştırma 2: Yerine Koymadan Top Çekme

Bir kutuda 6 kırmızı ve 4 mavi top var. Art arda, **yerine koymadan** iki top çekiliyor. $A$ olayı birinci çekilişte kırmızı top gelmesi, $B$ olayı ise ikinci çekilişte kırmızı top gelmesi olsun. Olaylar bağımsız mı, bağımlı mı?

**Çözüm:** Bu olaylar **bağımlıdır**, çünkü birinci çekilişin sonucu, ikinci çekilişte kutuda kalan top sayısını (hem toplam sayıyı hem de kırmızı top sayısını) değiştirir ve dolayısıyla $P(B)$ olasılığını etkiler.

### Alıştırma 3: Zar Atma

İki adet adil altı yüzlü zar atılıyor. $A$ olayı birinci zarda 4 gelmesi, $B$ olayı ise ikinci zarda çift sayı gelmesi olsun. Olaylar bağımsız mı, bağımlı mı?

**Çözüm:** Bu olaylar **bağımsızdır**, çünkü birinci zarın sonucu, ikinci zarın sonucunu hiçbir şekilde etkilemez.

---

## Sonuç

🎉 Olayların bağımsız mı yoksa bağımlı mı olduğunu anlamak, olasılıkları doğru bir şekilde hesaplamak için çok önemlidir. Bağımsız olaylar, olasılıkların doğrudan çarpılmasına olanak tanırken, bağımlı olaylar koşullu olasılık kullanımını gerektirir. Bu ayrımı yapmak, gerçek dünya olasılık problemlerini etkili bir şekilde çözmenin anahtarıdır.

---
# Independent and Dependent Events in Probability

## Introduction

In probability theory, understanding the relationship between events is essential for accurately calculating the likelihood of outcomes. Events are primarily classified as **independent** or **dependent**, determined by whether the occurrence of one event affects the probability of another.

---

## Independent Events

**Definition:**
Two events, $A$ and $B$, are **independent** if the occurrence of one does not affect the probability of the other.

**Mathematical Expression:**
Independence is defined by the following multiplication rule:

$$\mathbf{P(A \cap B) = P(A) \cdot P(B)}$$

This formula is derived from the multiplication rule for probability, $P(A \cap B) = P(A|B) \cdot P(B)$, where the conditional probability simplifies to the marginal probability:

$$\mathbf{P(A|B) = P(A)}$$

### Example: Coin Flip and Die Roll

Consider flipping a fair coin and rolling a six-sided die.
* **Event A:** Getting Heads on the coin.
* **Event B:** Rolling a 4 on the die.

Since flipping a coin does not influence the outcome of rolling a die:

$$P(A) = \frac{1}{2}$$
$$P(B) = \frac{1}{6}$$

The probability of both events occurring is:
$$P(A \cap B) = P(A) \cdot P(B) = \frac{1}{2} \cdot \frac{1}{6} = \frac{1}{12}$$

### Example: Student Survey

A survey suggests that $10\%$ of students commute by bike and $40\%$ have a significant other. Assuming these events are independent, what percentage of students commute by bike **and** have a significant other?

* **Event B:** Student commutes by bike. ($P(B) = 0.10$)
* **Event S:** Student has a significant other. ($P(S) = 0.40$)

Since $B$ and $S$ are assumed independent:

$$P(B \cap S) = P(B) \cdot P(S) = 0.10 \cdot 0.40 = 0.04$$

**Solution:** $4\%$ of students commute by bike and have a significant other.

---

## Dependent Events

**Definition:**
Two events, $A$ and $B$, are **dependent** if the occurrence of one event **does** affect the probability of the other.

**Mathematical Expression:**
The relationship between dependent events is expressed using **conditional probability** and the general multiplication rule:

$$\mathbf{P(A \cap B) = P(A|B) \cdot P(B)}$$

Where $P(A|B)$ is the probability of $A$ given that $B$ has already occurred, and **$P(A|B) \neq P(A)$**.

---

## Mutually Exclusive Events (vs. Independence)

**Definition:**
Events are called **mutually exclusive** (or disjoint) when they **cannot occur at the same time**.

**Mathematical Expression:**
This is expressed by:

$$\mathbf{P(A \cap B) = 0}$$

**Key Distinction:**
Mutually exclusive events are a special type of **dependent** events. If $A$ and $B$ are mutually exclusive, the occurrence of $A$ makes the occurrence of $B$ impossible (probability becomes 0), thus affecting its probability. They are only independent if $P(A)$ or $P(B)$ (or both) is $0$.

---

## Practice Exercises

### Exercise 1: The Weather and a Picnic

A family is planning a picnic. Let **Event A** be "it rains," and **Event B** be "the family has a picnic." Are the events $A$ and $B$ independent or dependent?

**Solution:**
These events are **dependent** because the family's decision to have a picnic ($B$) is highly influenced by the weather condition ($A$). If it rains, the probability of having a picnic decreases significantly.

### Exercise 2: Drawing Balls Without Replacement

A box contains 6 red balls and 4 blue balls. Two balls are drawn one after the other **without replacement**. Let **Event A** be drawing a red ball on the first draw, and **Event B** be drawing a red ball on the second draw. Are $A$ and $B$ independent or dependent?

**Solution:**
These events are **dependent**. The outcome of the first draw changes the composition of the remaining balls (the sample space) for the second draw. Specifically, if a red ball is drawn first ($A$), the probability of drawing another red ball on the second draw ($P(B|A)$) decreases from $6/10$ to $5/9$.

### Exercise 3: Rolling Dice

Two fair six-sided dice are rolled. Let **Event A** be rolling a 4 on the first die, and **Event B** be rolling an even number on the second die. Are $A$ and $B$ independent or dependent?

**Solution:**
These events are **independent**. The physical action and outcome of the first die roll have absolutely no influence on the physical action and outcome of the second die roll.

---

## Conclusion

Understanding whether events are **independent** or **dependent** is crucial for accurately calculating probabilities. **Independent events** allow for the direct multiplication of probabilities, while **dependent events** require the use of conditional probability. Mastering this distinction is key to solving real-world probability problems effectively.

# Bağımsız ve Bağımlı Olaylar Karşılaştırması

Aşağıdaki tablo, olasılık teorisindeki **Bağımsız Olaylar** ve **Bağımlı Olaylar** arasındaki temel farkları, formülleri ve örnekleriyle özetlemektedir.

| Özellik | Bağımsız Olaylar (Independent Events) | Bağımlı Olaylar (Dependent Events) |
| :--- | :--- | :--- |
| **Tanım** | Bir olayın gerçekleşmesi, diğer olayın gerçekleşme olasılığını **kesinlikle değiştirmez**. | Bir olayın gerçekleşmesi, diğer olayın gerçekleşme olasılığını **değiştirir**. |
| **Koşullu Olasılık** | $A$ olayının olasılığı, $B$ olayının gerçekleşip gerçekleşmemesinden etkilenmez. | $A$ olayının olasılığı, $B$ olayının gerçekleşmesine **bağlıdır**. |
| **Koşullu Formül** | $$\mathbf{P(A|B) = P(A)}$$ | $$\mathbf{P(A|B) \neq P(A)}$$ |
| **Çarpma Kuralı (Birlikte Olma)** | İki olayın birlikte gerçekleşme olasılığı, tek tek olasılıklarının çarpımıdır. | İki olayın birlikte gerçekleşme olasılığı, koşullu olasılık kullanılarak hesaplanır. |
| **Genel Formül** | $$\mathbf{P(A \cap B) = P(A) \cdot P(B)}$$ | $$\mathbf{P(A \cap B) = P(A|B) \cdot P(B)}$$ |
| **Gündelik Örnek** | Bir madeni paranın tura gelmesi ve bir zarın 6 gelmesi. (Birbirini etkilemezler) | Yağmur yağması ve bir şemsiye almayı unuttuğun için ıslanma olasılığın. (Yağmur, ıslanma olasılığını artırır) |
| **Kutu Örneği** | Bir top çekip, topu **geri koyarak** tekrar çekmek (Replacement). | Bir top çekip, topu **geri koymadan** tekrar çekmek (Without Replacement). |

---

## Formül Detayları ve Uygulaması

### Bağımsız Olaylar Örneği: Para Atma ve Zar Atma

* **Olay A:** Madeni paranın Tura gelmesi ($P(A) = 1/2$)
* **Olay B:** Zarın 4 gelmesi ($P(B) = 1/6$)

İki olayın aynı anda gerçekleşme olasılığı:
$$\mathbf{P(A \cap B) = P(A) \cdot P(B) = \frac{1}{2} \cdot \frac{1}{6} = \frac{1}{12}}$$

### Bağımlı Olaylar Örneği: Geri Koymadan Top Çekme

Bir kutuda 5 Kırmızı (K) ve 5 Mavi (M) top var (Toplam 10 top). Ardışık iki top, geri koyulmadan çekiliyor.

1.  **Olay B:** İlk çekilen topun Kırmızı olması ($P(B) = 5/10$)
2.  **Olay A:** İkinci çekilen topun Kırmızı olması

**$P(A|B)$ Hesaplaması:** İlk top Kırmızı çekilirse, geriye 4 Kırmızı ve toplam 9 top kalır.
$$P(A|B) = \frac{\text{Kalan Kırmızı Top Sayısı}}{\text{Kalan Toplam Sayısı}} = \frac{4}{9}$$

İki Kırmızı topun ardışık çekilme olasılığı:
$$\mathbf{P(A \cap B) = P(A|B) \cdot P(B) = \frac{4}{9} \cdot \frac{5}{10} = \frac{20}{90} = \frac{2}{9}}$$
