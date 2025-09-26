# Cumulative Distribution Function ( CDF)

<img width="706" height="263" alt="image" src="https://github.com/user-attachments/assets/456cb4d0-6bc8-4970-abc6-1d1d3ef7212d" />

<img width="680" height="485" alt="image" src="https://github.com/user-attachments/assets/98aee107-9dee-4569-8ee3-10b3170d54ee" />

<img width="738" height="287" alt="image" src="https://github.com/user-attachments/assets/eae05593-0c5f-4176-affd-f87bb272264d" />

<img width="727" height="519" alt="image" src="https://github.com/user-attachments/assets/04498180-4911-419a-9c89-f6f472fb5101" />

# Olasılık Problemlerine Yaklaşım: 3 Adımlı Plan

| Adım | Amaç | Hesaplama Aracı |
| :--- | :--- | :--- |
| **1. Rastgele Değişkeni Tanımlama** | Değişkenin alabileceği **tüm olası ayrık değerleri** listeleriz. Bu, örneklem uzayını ($X$) sayısal olarak sınırlar. | Mantıksal Çıkarım |
| **2. PMF'yi Hesaplama** | Her bir ayrık değerin **tam olarak** gerçekleşme olasılığını buluruz. Bu, problemin **neden-sonuç** ilişkisini kurar. | Olasılık (Seçim Kuralları) |
| **3. CDF'yi Hesaplama** | PMF değerlerini toplayarak **kümülatif (birikimli) olasılıkları** buluruz. Bu, olasılıkların bir eşiği aşmama durumunu gösterir. | Toplama (PMF'lerin Toplamı) |

---

# Kümülatif Dağılım Fonksiyonu (Cumulative Distribution Function - CDF) Nedir?

**CDF**, $F(x)$ olarak gösterilir ve **Olasılık Kütle Fonksiyonu'nun (PMF)** yaptığı gibi tek bir değeri hesaplamak yerine, birikimli (**kümülatif**) olasılığı hesaplamak için kullanılır.

---

## Temel Amaç: Kümülatif Olasılık

CDF'nin temel amacı, bir rastgele değişkenin ($X$) belirli bir $x$ değerine **eşit veya ondan küçük olma olasılığını** bulmaktır.

* **Matematiksel Gösterim:**
    $$\mathbf{F(x) = P(X \le x)}$$

---

## Ayrık Değişkenlerde CDF'nin Çalışma Prensibi

Ayrık bir rastgele değişken için **CDF**, PMF değerlerinin bir toplamıdır. Belirli bir $x$ değerindeki CDF, o noktaya kadar olan tüm PMF değerlerinin toplanmasıyla elde edilir.

* **Formel Bağlantı:**
    $$\mathbf{F(x) = \sum_{t \le x} f(t)}$$
    (Burada $f(t)$, $X$'in alabileceği tüm $t$ değerleri üzerindeki PMF'yi temsil eder.)

  # CDF Neden Önemlidir? (PMF ile Farkı)

| Fonksiyon | Olasılığı Hesapladığı Aralık | Amacı |
| :--- | :--- | :--- |
| **PMF ($f(x)$)** | **Tam olarak $x$ değeri** | Bir olayın tam olarak o sonucu vermesi olasılığı. ($P(X = x)$) |
| **CDF ($F(x)$)** | $x$ değerine **kadar olan tüm** değerler | Olası sonuçların belirli bir eşiği **aşmama** olasılığı. ($P(X \le x)$) |

### Örnek (Binomial Dağılım)

Binomial dağılımda $P(X \le 3)$ ifadesini hesaplamak istediğimizde (yani 10 denemede 3 veya daha az başarı), CDF aslında bu tek tek olasılıkları toplar:

$$\mathbf{F(3) = P(X=0) + P(X=1) + P(X=2) + P(X=3)}$$

---

**Çıkarım:** Bu, CDF'nin **Toplam Porsiyon Sayısı** analojisine karşılık geldiğini açıklar. CDF bize "Şimdiye kadar kaç başarı (veya arıza, veya çağrı) görme olasılığımız nedir?" sorusunun cevabını verir.
