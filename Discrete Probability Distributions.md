# Discrete Probability Distributions

## Introduction

In probability theory, a **discrete probability distribution** describes the likelihood of outcomes for a **random variable ($X$)** that can take on a **finite** or **countably infinite** set of distinct values. These distributions are fundamental for understanding random processes and are widely used in statistics, engineering, and machine learning.

---

## Defining the Discrete Random Variable ($X$)

A random variable is a formal way to assign numerical values to the outcomes of a random experiment.

### Formal Definition

Given a random experiment with a **sample space $S$**, a **random variable $X$** is a set function that assigns one and only one real number to each element $s$ that belongs in the sample space $S$.

### Condition for Discrete Variables

A random variable $X$ is a **discrete random variable** if:

* There are a **finite** number of possible outcomes of $X$, or
* There are a **countably infinite** number of possible outcomes of $X$.

As shown in the examples below, the number of all possible outcomes for a discrete variable must be countable.

---

## Examples of Discrete Random Variables

### Example 1: Flipping a Coin (Bernoulli Variable)

Consider flipping a fair coin. Let the random variable $X$ represent the outcome of a single flip.

* $X = 1$ if the outcome is **Heads**
* $X = 0$ if the outcome is **Tails**

This is an example of a **Bernoulli random variable**, which takes only two distinct values.

**Probabilities:**
$$P(X = 1) = 0.5, \quad P(X = 0) = 0.5$$

The sum of probabilities equals 1:
$$P(X = 1) + P(X = 0) = 0.5 + 0.5 = 1$$

### Example 2: Rolling a Single Die

Imagine rolling a single six-sided die. Let $X$ represent the number shown on the die after the roll. The possible values of $X$ are $\{1, 2, 3, 4, 5, 6\}$.

Each side of the die has an equal probability of $1/6$. This simple example demonstrates a discrete random variable where all outcomes are equally likely.

**Probabilities:**
$$P(X = x) = \frac{1}{6}, \quad x \in \{1, 2, 3, 4, 5, 6\}$$
$$\sum_{x=1}^{6} P(X = x) = \frac{1}{6} + \frac{1}{6} + \frac{1}{6} + \frac{1}{6} + \frac{1}{6} + \frac{1}{6} = 1$$

---

# Discrete Probability Distributions: Key Concepts

This summary provides an overview of the core concepts, types, and importance of discrete probability distributions, based on technical and financial analysis.

---

## 1. Overview and Definition

| Feature | Description |
| :--- | :--- |
| **Definition** | A discrete probability distribution counts occurrences for a **random variable** that can only take on a **finite** or **countably infinite** set of distinct, specific values (e.g., $1, 2, 3$, or true/false). |
| **Contrast** | It contrasts with **continuous distributions**, where outcomes can fall anywhere on a continuum (e.g., all real numbers in a range). |
| **Core Concept** | These distributions often involve statistical analysis of "**counts**" or "**how many times**" an event occurs. |
| **Example** | The **Binomial Distribution** evaluates the probability of a "yes" or "no" outcome over a given number of trials (e.g., coin flips). |

---

## 2. Why Discrete Distributions Matter

* **Modeling Countable Data:** They are essential because they provide the mathematical framework for modeling data that consists only of distinct, countable outcomes.
* **Statistical Differentiation:** Unlike the continuous Normal Distribution, a discrete distribution is specifically designed for data that cannot take on infinite values between two points (e.g., you can't have 1.5 coin flips or 3.7 customers).
* **Finance Applications:** In finance, they are critical for applications like **options pricing** (using binomial tree models) and **forecasting** market shocks or recessions.

---

## 3. Types of Discrete Probability Distributions

The most common types used in statistics, data science, and finance include:

| Distribution Type | Characteristic | Primary Use |
| :--- | :--- | :--- |
| **Binomial** | Only **two possible outcomes** (success/failure) over repetitive trials. | Modeling outcomes of repeatable binary events (e.g., success rate in A/B testing). |
| **Bernoulli** | Similar to binomial, but for only a **single trial**. Outcomes are $0$ (failure) or $1$ (success). | Viewing the probability that a single investment or event will succeed or fail. |
| **Poisson** | Expresses the probability of a given **number of events** occurring over a **fixed period or space**. Outcomes are integers ($\ge 0$). | Modeling rare event frequency, like the number of transactions per minute or the number of claims received. |
| **Multinomial** | Occurs when there is a probability of **more than two outcomes** with multiple counts. | Estimating the probability that a specific set of financial events (e.g., stock price moves up, down, or stays flat) will occur. |

---

## 4. Discrete Distribution vs. Continuous Distribution

| Feature | Discrete Distribution | Continuous Distribution |
| :--- | :--- | :--- |
| **Outcomes** | Countable values (integers, binary). | Any value within a range (real numbers, fractions). |
| **Graph** | Represented by **separate bars** because there are gaps between possible values. | Represented by a **continuous curve or line** (e.g., the bell curve) because all values are possible. |
| **Function** | **Probability Mass Function (PMF)**: Gives the probability of a specific point. | **Probability Density Function (PDF)**: Gives the probability over an interval. |

---

# Ayrık Olasılık Dağılımları Neden Önemlidir?

Ayrık olasılık dağılımlarının temel önemi, **sayılabilir** ve **belirli** sonuçlara sahip gerçek dünya olaylarını modellemek ve analiz etmek için gerekli matematiksel çerçeveyi sağlamalarından kaynaklanmaktadır.

---

## 1. Sayılabilir Olguların Doğru Modellenmesi

Ayrık dağılımlar, ara (kesirli) değerlerin mantıksal olarak imkansız olduğu verileri doğru bir şekilde temsil ettikleri için hayati öneme sahiptir.

### Tam Sayıların Ele Alınması
* **Doğru Temsil:** Gerçek dünyadaki birçok sonuç tam, negatif olmayan sayılar (tamsayılar) olmak zorundadır. Örneğin, $2.5$ arabanız veya $3.3$ arızanız olamaz.
* **Özel Araçlar:** **Poisson** ve **Binomial** dağılımları gibi ayrık dağılımlar, bu **sayılabilir veri noktalarını** işlemek üzere özel olarak tasarlanmıştır, bu da yüksek doğrulukta ve eyleme geçirilebilir tahminler sağlar.

### İkili Sonuçların Modellenmesi
* **Temel Veri Türü:** Yalnızca iki sonucu olan olaylar (Başarı/Başarısızlık, Evet/Hayır, $0/1$), ayrık verinin en temel türüdür.
* **Temel Modeller:** **Bernoulli** ve **Binomial** dağılımları, tek bir yazı tura denemesinden, çok sayıda denemede bir web sitesinin dönüşüm oranını hesaplamaya kadar her şeyi modellemek için zorunludur.

---

## 2. İstatistiksel Çıkarım ve Hipotez Testlerinin Temeli

Ayrık dağılımlar, örnek verilere dayanarak popülasyonlar hakkında kanıta dayalı kararlar almak ve teorileri titizlikle test etmek için temel oluşturur.

* **Hipotez Testi:** İstatistikçiler bir oran veya sayı hakkındaki iddiayı test ederken (örneğin, "Kusur oranı %1'den yüksek mi?"), örnek sonuçları gözlemleme olasılığını hesaplamak için **Binomial dağılımı** gibi dağılımlara güvenirler. Bu süreç, bulgunun istatistiksel olarak anlamlı olup olmadığını belirler.
* **Popülasyon Parametrelerini Çıkarım:** Bir örneklemdeki sayılabilir sonuçları gözlemleyerek, bu dağılımlar daha büyük popülasyonun özelliklerini çıkarmamıza ve tahmin etmemize olanak tanır (örneğin, tüm ürün grubu için gerçek başarı olasılığını tahmin etmek).

---

## 3. Makine Öğrenimi ve Veri Biliminde Esas

Modern veri odaklı alanlarda, ayrık olasılık, güçlü sınıflandırma algoritmaları ve olay sıklıklarını modelleme açısından kritiktir.

* **Naive Bayes Sınıflandırıcısı:** Makine öğrenimindeki en ünlü algoritmalardan biri olan **Naive Bayes Sınıflandırıcısı**, doğrudan ayrık olasılık kullanarak Bayes Teoremi prensipleri üzerine inşa edilmiştir. Metin sınıflandırma (spam filtreleme, duygu analizi) görevlerinde, özellikler kelime sayıları gibi ayrık veriler olduğu için son derece etkilidir.
* **Nadir Olayların Modellenmesi (Poisson):** **Poisson dağılımı**, sabit bir aralıkta nadir olayların sıklığını tahmin etmek için hayati öneme sahiptir. Bu, aşağıdaki durumları modellemek için kullanılır:
    * Bir çağrı merkezine dakikada gelen müşteri çağrısı sayısı.
    * Bir günde meydana gelen sunucu çökmelerinin sayısı.
    * Belirli bir dönemde açılan sigorta taleplerinin sıklığı.

---

## 4. Risk Yönetimi ve Finansı Yönlendirme

Risk miktarının belirlenmesinin çok önemli olduğu finansta, ayrık dağılımlar potansiyel kazanç ve kayıpları değerlendirmek için yapılandırılmış yollar sunar.

* **Opsiyon Fiyatlandırması (Binomial Ağaç Modeli):** **Binomial Ağaç Modeli**, opsiyon değerlemesi için temel bir araçtır. Bir hisse senedi fiyatının yalnızca iki farklı, **ayrık değere** (yukarı veya aşağı) hareket edebileceği varsayımına dayanarak karmaşık fiyat hareketlerini basitleştirir ve sağlam bir risk analizi yöntemi sağlar.
* **Portföy Riski:** Ayrık dağılımlar, bir şirketin temerrüde düşme veya ani bir piyasa şoku olayı gibi, bir portföy içinde meydana gelen ayrık risklerin olasılığını ölçmeye yardımcı olur.

---

**Özetle:** Ayrık dağılımlar, **sayıları, sıklıkları ve ikili kararları** analiz etmek için matematiksel bir temeldir. Bu dağılımlar, bizi basit sayılabilir sonuçları gözlemlemekten, hemen hemen her nicel alanda karmaşık ve rasyonel çıkarımlar yapmaya taşır.

---

# Temel Ayrık Olasılık Dağılımları (Discrete Probability Distributions)

Bu dağılımlar, sayılabilir sonuçlara sahip rastgele olayları analiz etmek için kullanılan en önemli matematiksel araçlardır.

## 1. Bernoulli Dağılımı (Bernoulli Distribution)

| Özellik | Açıklama |
| :--- | :--- |
| **Tanım** | Bir deneyin yalnızca iki olası sonucu olduğunda (başarı veya başarısızlık) kullanılır. Tek bir denemeyi modeller. |
| **Sonuçlar** | $X=1$ (Başarı) veya $X=0$ (Başarısızlık). |
| **Parametre** | Başarı olasılığı ($p$) |
| **Olasılıklar** | $P(X=1) = p$ ve $P(X=0) = 1 - p$ |
| **Kullanım Alanı** | Atılan bir paranın sonucu veya tek bir müşteri işleminin başarılı olup olmadığı gibi ikili (binary) sonuçlu durumlar. |

---

## 2. Binomial Dağılım (Binomial Distribution)

| Özellik | Açıklama |
| :--- | :--- |
| **Tanım** | Bernoulli deneyinin ardışık, bağımsız $n$ kez tekrar edilmesi durumunda, bu $n$ denemeden kaç tanesinin başarılı olacağını ($k$ başarılı deneme sayısı) modeller. |
| **Koşullar** | Deneme sayısı ($n$) sabit, denemeler bağımsız, her denemede iki sonuç var ve başarı olasılığı ($p$) sabittir. |
| **Parametreler** | Deneme sayısı ($n$) ve başarı olasılığı ($p$). |
| **Kullanım Alanı** | $100$ kişiden kaçının bir ürünü satın alacağını veya $50$ üründen kaçının kusurlu olacağını tahmin etmek. |

---

## 3. Poisson Dağılımı (Poisson Distribution)

| Özellik | Açıklama |
| :--- | :--- |
| **Tanım** | Belirli bir zaman aralığında veya sabit bir alanda **nadir olayların** kaç kez gerçekleşeceğini modeller. |
| **Koşullar** | Olaylar bağımsızdır, gerçekleşme hızı ($\lambda$) sabittir ve aynı anda birden fazla olay olasılığı çok düşüktür. |
| **Sonuçlar** | Sonsuz sayıda olası sonuç ($0, 1, 2, 3, \dots$) olabilir. |
| **Parametre** | Beklenen olay sayısı ($\lambda$, lambda). |
| **Kullanım Alanı** | Bir çağrı merkezine bir saat içinde gelen çağrı sayısı veya bir web sitesine bir dakikada gelen ziyaretçi sayısı gibi sıklık veya hız ile ilgili olayları modellemek. |

---

## 4. Geometrik Dağılım (Geometric Distribution)

| Özellik | Açıklama |
| :--- | :--- |
| **Tanım** | Bir Bernoulli deneyi dizisinde, **ilk başarının elde edilmesi için gereken deneme sayısını** modeller. |
| **Sonuçlar** | $X = 1, 2, 3, \dots$ (Denemeler sonsuza kadar sürebilir). |
| **Parametre** | Başarının olasılığı ($p$). |
| **Kullanım Alanı** | Bir ürünün kalite kontrolünden ilk geçtiği deneme sayısını bulmak. |

---

Bu dört temel dağılım, olasılık ve istatistikte en sık kullanılanlardır. Şimdi istersen, bu dağılımlardan birini daha derinlemesine inceleyebiliriz.

