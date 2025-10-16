# Paired t-Test
---
## 🔗 Eşli İki Örneklem $t$-Testi (Paired Two-Sample $t$-Test)

### 1. Paired $t$-Test'in Two-Sample $t$-Test'ten Farkı Nedir?

* Bu, iki test arasındaki temel ayrımdır ve görselde net bir şekilde gösterilmiştir:

# 🔄 Paired $t$-Test ve Bağımsız $t$-Test Farkı

Bu tablo, Eşli İki Örneklem $t$-Testi (Paired $t$-Test) ile Bağımsız İki Örneklem $t$-Testi (Independent Two-Sample $t$-Test) arasındaki temel yapısal ve analitik farkları özetlemektedir.

| Özellik | Paired $t$-Test (Eşli $t$-Testi) 🔗 | Independent Two-Sample $t$-Test (Bağımsız $t$-Testi) 👥 |
| :--- | :--- | :--- |
| **Grup İlişkisi** | **Bağımlıdır (Dependent).** Aynı bireyler veya birbiriyle doğal olarak eşleştirilmiş gruplar iki farklı durumda ölçülür. | **Bağımsızdır (Independent).** İki gruptaki bireyler birbirinden tamamen farklıdır. |
| **Örneklem Yapısı** | **"Öncesi/Sonrası"** veya **"Eşleştirilmiş Kontrol"** (Örn: Bir kişinin ilaç almadan önceki ve sonraki ağırlığı). | **"Kontrol Grubu"** vs. **"Deney Grubu"** (Örn: A ilacını alan farklı grup vs. B ilacını alan farklı grup). |
| **Temel Analiz** | İki örneklemi değil, her bir çiftin arasındaki **farkların dağılımını** ($d_i$) analiz eder. Tek bir veri seti (farklar) üzerinde işlem yapar. | İki örneklemin ortalamaları ($\bar{x}_1$ ve $\bar{x}_2$) arasındaki farkı analiz eder. |

<img width="1217" height="605" alt="image" src="https://github.com/user-attachments/assets/6c6f666b-6cd8-413c-8152-7f41da490e1f" />

<img width="1250" height="575" alt="image" src="https://github.com/user-attachments/assets/c656821b-354b-447e-9a3b-a8f039c4d533" />

* **Görseldeki İfade:** Görsel, eşleştirilmiş testte aynı kişilerin (alt oklarla gösterilen eşleştirmeler) zaman içinde (takvim simgesiyle gösterilen) takip edildiğini göstererek, grupların bağımlı olduğunu vurgular. Bağımsız grupta ise iki farklı insan kümesi karşılaştırılır.


* Sample:
  
<img width="793" height="126" alt="image" src="https://github.com/user-attachments/assets/e9bd164c-c9cb-4a32-973d-b4034cc0b5eb" />
# ❓ 2. Paired $t$-Test'in Örnekleminin Gaussian Olma Durumu Nedir? Neden Kaynaklanır?

Paired $t$-Test'in geçerli olması için, orijinal ölçümlerin ($x_i$ ve $y_i$) değil, **farkların ($d_i$) örnekleminin Normal (Gaussian) dağılıma sahip olması gerekir.**

### Neden Kaynaklanır:

* $t$-Test, temel olarak **Farkların Ortalaması ($\bar{d}$)** üzerinde çalıştığı için, bu ortalamanın dağılımının Normal olması beklenir.
* Eğer örneklem büyüklüğü ($n$) yeterince büyükse (Merkezi Limit Teoremi gereği), farkların ortalaması $\bar{d}$ zaten Normal dağılıma yaklaşacaktır.
* Ancak $n$ küçük olduğunda (Görselde $n=10$), **farkların kendisinin** Normal dağılıma yakın olması gerekir.

### Test Edilen Şey:

* Bizim hipotezimiz farkların popülasyon ortalaması ($\mu_D$) ile ilgilidir.
* Bu nedenle, test istatistiği ($T$) bir $t$-dağılımını takip etmesi için **farkların normal dağılması şarttır**.
* 
  
<img width="1210" height="573" alt="image" src="https://github.com/user-attachments/assets/95cbf731-953f-4066-8abf-22c367547485" />


# ❓ 3. Popülasyon Standart Sapması ($\sigma$) Bilinmediğinde Ne Yapılmalı? Neden Bilinmez?

Eşli $t$-Testi, yapısı gereği **her zaman $\sigma$ bilinmiyor varsayımıyla** çalışır.

### Neden Bilinmez: 🤯

* Hipotez testi genellikle, popülasyon hakkında kesin bilgiye sahip olmadığımız durumlarda yapılır.
* İki farklı popülasyon (öncesi/sonrası) olsa bile, farkların popülasyon standart sapmasını ($\sigma_D$) bilmek neredeyse imkansızdır.

### Ne Yapılmalı: 🛠️

* $\sigma_D$ yerine, örneklemden hesaplanan **farkların örneklem standart sapması ($s_D$)** kullanılır.
* $\sigma$ yerine $s_D$ kullanıldığı anda, standart normal dağılım ($Z$) yerine **$t$-dağılımı** kullanılır.
* Bu nedenle test istatistiği $T$ olarak adlandırılır ve $t$-dağılımını takip eder.

<img width="1203" height="587" alt="image" src="https://github.com/user-attachments/assets/49c913f8-51c9-42de-bedf-31aa548192c0" />

# 🔬 4. İkinci Görseldeki Gözlemleri Açıklama (Observations)

<img width="1244" height="583" alt="image" src="https://github.com/user-attachments/assets/fa25f3ee-c3d9-4a9c-85c7-4e4e9d4ca09d" />

İkinci görselde, bir deneye ait **eşli veriler** ve $t$-testinin nasıl hesaplandığı adım adım gösterilmiştir (Muhtemelen bir ağırlık kaldırma programının kas gücüne etkisi veya kilo değişimi gibi).

### Gözlemler ($x_i$ ve $y_i$):

* $x_i$: İlk ölçüm (Örn: Program **Öncesi**).
* $y_i$: İkinci ölçüm (Örn: Program **Sonrası**).
* Her $x_i$ ve $y_i$ birbiriyle **eşleştirilmiştir** (aynı kişiye aittir).

### Farkların Hesaplanması ($d_i$): ➖

$d_i = x_i - y_i$ (veya $y_i - x_i$, tutarlılık önemlidir). Görselde $x_i - y_i$ yapılmış gibi görünüyor, ancak sonuçlara bakarsak **$y_i - x_i$** yapılmış olması daha olasıdır, zira $\bar{d}$ pozitif çıkmıştır. (Örn: $d_1 = 251.5 - 251.9 = -0.4$, oysa tablonun altında $d_1=0.4$ yazıyor. Bu da $y_i - x_i$ yapıldığını gösterir: $251.9 - 251.5 = 0.4$).

### Farkların Ortalaması ($\bar{d}$):

Tüm $d_i$ değerlerinin ortalaması.
$$\bar{d} = \mathbf{1.09}$$

### Farkların Standart Sapması ($s_D$):

$d_i$ değerlerinin standart sapması.
$$s_D = \mathbf{1.485}$$

### t-İstatistiği Hesaplanması: 📊

$$t = \frac{\bar{d} - 0}{s_D/\sqrt{n}} = \frac{1.09 - 0}{1.485/\sqrt{10}} \approx \mathbf{2.321}$$

# 📈 5. Sağ Kuyruk Testi Sonuçlarını Yorumlama (Right-Tailed Test Interpretation)

* <img width="1233" height="590" alt="image" src="https://github.com/user-attachments/assets/381930bd-56ce-45cd-b59c-6d76f4d6f3d0" />


İlk görselde gösterilen **Sağ Kuyruk Testi** sonuçları aşağıdaki gibidir:

### Hipotezler: 📜

* **$H_0: \mu_D = 0$** (Ortalamalar arasında fark yok)
* **$H_1: \mu_D > 0$** (Farkın ortalaması pozitif, yani ikinci ölçüm (sonrası) birinci ölçümden (öncesi) anlamlı olarak daha büyüktür).

### Test İstatistiği: 🔢

* **$T = 2.321$**
* $T$ istatistiği $t$-dağılımını takip eder ($df = n-1 = 9$).

### Anlamlılık Seviyesi:

* **$\alpha = 0.05$**

### P-Değeri Hesaplama: 📉

$$\text{p-value} = P(T > 2.321 \mid \mu_D = 0) = \mathbf{0.0227}$$

*(Grafikteki turuncu alan)*

---

## Karar ve Yorum: ✅

### Karşılaştırma:

$$\text{p-value} (0.0227) < \alpha (0.05)$$

### Sonuç:

$H_0$ **Reddedilir** (**Reject $H_0$**) ve $H_1$ kabul edilir.

### Yorum: 💬

\%5 anlamlılık seviyesinde, ikinci ölçümün (Program Sonrası) birinci ölçümden (Program Öncesi) **anlamlı derecede daha yüksek olduğuna dair yeterli istatistiksel kanıt vardır.** Programın **pozitif ve anlamlı bir etkisi** olmuştur.
