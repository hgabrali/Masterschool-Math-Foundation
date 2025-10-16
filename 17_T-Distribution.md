# T-Distribution

[T-Distribution](https://colab.research.google.com/drive/1WC1F_PmLMNT99usidQHluykxCKRJsJxP#scrollTo=kUgw7xk1PUYg)

<img width="745" height="524" alt="image" src="https://github.com/user-attachments/assets/0781dc48-b180-4285-b4c0-ac01b375352c" />

<img width="772" height="646" alt="image" src="https://github.com/user-attachments/assets/319290b3-27e7-4167-bc07-76fd7c5c2ec5" />

<img width="749" height="332" alt="image" src="https://github.com/user-attachments/assets/e8f13bd2-dfa9-4c18-8dff-d83854527321" />

<img width="818" height="721" alt="image" src="https://github.com/user-attachments/assets/3c8baba8-f50f-460b-a35b-24986ff9556e" />


# Grafik Yorumu:

<img width="482" height="355" alt="image" src="https://github.com/user-attachments/assets/18d4f9ac-3c15-43a2-9df3-1f7cdbb04fd2" />

Bu grafik, **Normal (Z) Dağılımı** ile onun "**ihtiyatlı kuzeni**" olan **t-Dağılımı** arasındaki temel farkı görsel olarak mükemmel bir şekilde özetliyor. Verdiğiniz metindeki karakteristikleri kullanarak bu grafiği detaylı bir şekilde analiz edip yorumlayalım.

---

### Genel Bakış: İdeal Model vs. Gerçekçi Tahmin

Bu grafiğe bakarken şu hikayeyi düşünebiliriz:

* **Normal Dağılım (Mavi Çizgi):** Bu, popülasyon hakkında her şeyi (özellikle standart sapmasını, $\sigma$) bildiğimiz **ideal ve mükemmel** bir dünyayı temsil eder.
* **t-Dağılımı (Kırmızı Çizgi):** Bu ise, popülasyon standart sapmasını bilmediğimiz ve onu küçük bir örneklemden tahmin etmek zorunda kaldığımız **gerçekçi ama daha belirsiz** bir dünyayı temsil eder.

Grafik, bu "ekstra belirsizliğin" dağılımın şeklini nasıl değiştirdiğini gösterir.

---

### Grafik Analizi ve Yorumu

#### 1. Şekil: Benzer Aile, Farklı Bireyler

Metinde de belirtildiği gibi, her iki dağılım da **simetrik ve çan şeklindedir**. Grafiğe baktığımızda ikisinin de merkezinin 0 olduğunu ve her iki yana doğru simetrik bir şekilde azaldığını görüyoruz. Bu, t-dağılımının normal dağılım ailesinin bir üyesi olduğunu, ancak kendine özgü farklılıkları olduğunu gösterir.

#### 2. Kalın Kuyruklar (Heavier Tails): En Önemli Fark

Bu, grafikteki en çarpıcı ve en önemli özelliktir.

* **Grafikte Ne Görüyoruz?**
    * **Merkezde:** Kırmızı çizgi (t-Dağılımı), mavi çizgiden (Normal Dağılım) **daha basıktır**.
    * **Kuyruklarda:** Grafiğin uçlarına doğru (örneğin, -2'den küçük ve +2'den büyük bölgelerde), kırmızı çizgi mavi çizgiden **daha yüksektir**.

* **Bu Ne Anlama Geliyor? (Yorum)**
    Metindeki alıntı bunun görsel kanıtıdır:
    > "The t-distribution has heavier tails"

    "Kalın kuyruklar", **aşırı değerlerin (uç noktaların) t-dağılımında normal dağılıma göre daha olası olduğu** anlamına gelir.

* **Metafor:**
    > Bir zar attığınızı düşünün. Normal dağılım, hilesiz bir zar gibidir; 1 veya 6 gibi uç değerler gelir ama çoğunlukla orta değerler beklenir. Düşük serbestlik dereceli bir t-dağılımı ise, kenarları biraz daha ağırlaştırılmış bir zar gibidir; 1 veya 6 gelme ihtimali, yani **sürpriz bir sonuçla karşılaşma ihtimali** biraz daha fazladır. Bunun nedeni, küçük bir örneklemle çalışmanın getirdiği ekstra belirsizliktir.

#### 3. Serbestlik Derecesi (Degrees of Freedom - DF): Dağılımın Kaderini Belirleyen Faktör

* **Grafikte Ne Görüyoruz?**
  Kırmızı çizgi, özellikle **2 serbestlik derecesi (2 DF)** için çizilmiştir. Bu, çok küçük bir örneklemden (`$n = 3$`) geldiği anlamına gelir.

* **Bu Ne Anlama Geliyor? (Yorum)**
  Serbestlik derecesi (`df`), t-dağılımının normal dağılıma ne kadar benzeyeceğini belirleyen bir **ayar düğmesi** gibidir.
    * **Düşük `df` (Grafikteki Durum):** Örneklem boyutu küçük olduğunda (`$n$` küçük, dolayısıyla `df` düşük), popülasyonu tahmin etmedeki belirsizliğimiz çok yüksektir. t-dağılımı bu belirsizliği hesaba katmak için **kalın kuyruklu ve basık** hale gelir. Yani, "beklenmedik" sonuçlara daha fazla olasılık tanır.
    * **Yüksek `df`:** Örneklem boyutunu artırdıkça (`$n$` büyüdükçe, `df` de artar), tahminlerimizdeki belirsizlik azalır. Bu durumda t-dağılımının kuyrukları incelir, merkezi yükselir ve **giderek normal dağılıma (mavi çizgiye) yakınsar**. Genellikle `df > 30` olduğunda, t-dağılımı ile normal dağılım arasındaki fark neredeyse ayırt edilemez hale gelir.

Bu grafik, küçük örneklemlerle çalışırken neden t-dağılımını kullandığımızı özetler: t-dağılımı, bilmediğimiz popülasyon standart sapmasından kaynaklanan **ekstra belirsizliği** hesaba katan, daha **ihtiyatlı ve gerçekçi** bir modeldir.

---

### Ana Metafor: Uzman Rehber (Z) ve İhtiyatlı Gözcü (t)

Bilinmeyen bir hazineyi ( **popülasyonun gerçek ortalaması, $\mu$** ) aradığımızı hayal edelim. Bu arayışta bize iki farklı karakter yardımcı olabilir:

* **Normal (Z) Dağılımı - Uzman Rehber: 🗺️**
  Bu rehber, tüm bölgeyi avucunun içi gibi bilir. Bölgenin genel arazi değişkenliğini ( **popülasyon standart sapması, $\sigma$** ) gösteren mükemmel bir uydu haritasına sahiptir. Kendinden emindir ve hazinenin yerini tahmin ederken dar ve hassas bir arama alanı (güven aralığı) çizer.

* **t-Dağılımı - İhtiyatlı Gözcü: 🧭**
  Bu gözcü, tüm bölgenin haritasına sahip değildir. Yalnızca kendi gezdiği küçük bir alanın ( **örneklem** ) değişkenliğini ( **örneklem standart sapması, $s$** ) bilir. Bilgisinin eksik olduğunun farkındadır, bu yüzden daha **ihtiyatlı ve şüphecidir**.

İşte t-dağılımı, bu "ihtiyatlı gözcünün" haritasıdır.

---

### t-Dağılımının Karakteristikleri (Gözcünün Haritasının Özellikleri)

Metinde belirtilen özellikleri, metaforumuzla birleştirelim:

#### 1. Şekil: Aile Benzerliği

Hem uzman rehberin haritası hem de ihtiyatlı gözcünün haritası, hedefin merkezde olduğu **simetrik ve çan şeklinde** bir arama deseni kullanır. Bu, t-dağılımının da normal dağılım gibi davrandığını, ancak önemli farkları olduğunu gösterir.

#### 2. Kalın Kuyruklar (Heavier Tails): Genişletilmiş Arama Alanı

Bu, iki karakter arasındaki en temel farktır.

* **Anlamı:** İhtiyatlı Gözcü (t-dağılımı), bilgisindeki belirsizlikten dolayı daha temkinlidir. Bu yüzden arama alanının kenarlarına ( **kuyruklara** ) daha fazla pay bırakır.
    > "Hazine tam merkezde olmayabilir, biraz daha uç noktalarda olma ihtimali, uzman rehberin düşündüğünden biraz daha fazla."
    İşte bu "uç noktalara daha fazla olasılık tanıma" durumu, grafikte **kalın kuyruklar** olarak görünür.
* **Sonucu:** Bu ihtiyat, t-dağılımı ile oluşturulan güven aralıklarının Z-dağılımına göre **biraz daha geniş** olmasına neden olur. Bu, belirsizliğe karşı ödediğimiz bir bedeldir.

#### 3. Serbestlik Derecesi (Degrees of Freedom - DF): Gözcünün Deneyimi

Serbestlik derecesi (`df = n-1`), gözcümüzün ne kadar "deneyimli" olduğunu gösterir.

* **Düşük `df` (Acemi Gözcü):** Gözcü çok küçük bir alanı (`$n$` küçük) gezmişse, belirsizliği çok yüksektir. Bu yüzden haritası çok kalın kuyruklu ve basıktır. Çok geniş bir arama alanı çizer.
* **Yüksek `df` (Deneyimli Gözcü):** Gözcü çok büyük bir alanı (`$n$` büyük, örn: `$n > 30$`) gezmişse, artık bölgenin genel değişkenliği hakkında oldukça iyi bir fikri vardır. Tahminlerindeki belirsizlik azalır. Bu noktada gözcünün haritası, uzman rehberin haritasına o kadar çok benzer ki, aradaki fark neredeyse kaybolur.
* **Sonuç:** **Serbestlik derecesi arttıkça, t-dağılımı normal dağılıma yakınsar.**

### Hangi Haritayı Ne Zaman Kullanmalıyız? (Karşılaştırma Tablosu)

İşte karar verme sürecinizi basitleştirecek bir tablo:

| Durum | Popülasyon Standart Sapması ($\sigma$) | Örneklem Boyutu ($n$) | Kullanılacak Dağılım | Gerekçe |
| :--- | :--- | :--- | :--- | :--- |
| **İdeal Dünya** | **Biliniyor** | Fark etmez | **Normal (Z) Dağılımı** | Elimizde mükemmel bilgi (Uzman Rehber) var. |
| **Gerçek Dünya (Büyük Örneklem)** | Bilinmiyor | **Büyük** (`$n \ge 30$`) | **Normal (Z) Dağılımı** | Gözcü artık çok deneyimli (`df` yüksek) olduğu için haritası uzmanınkine çok benzer. |
| **Gerçek Dünya (Küçük Örneklem)**| Bilinmiyor | **Küçük** (`$n < 30$`) | **t-Dağılımı** | Gözcü acemi (`df` düşük) ve haritasındaki ekstra belirsizliği hesaba katmalıyız. |

---

### Özetle

**t-Dağılımı**, istatistiğin **"gerçek dünya" aracıdır**. Popülasyon hakkında tam bilgiye sahip olmadığımız (ki bu neredeyse her zaman geçerlidir) ve özellikle küçük veri setleriyle çalıştığımız durumlarda, tahminlerimize anlamlı bir **ihtiyat payı** ekleyerek daha dürüst ve güvenilir sonuçlar elde etmemizi sağlar.

---

<img width="672" height="129" alt="image" src="https://github.com/user-attachments/assets/06555c2a-69f3-4a13-a678-4e686e81c635" />

Bu şema, bir popülasyon ortalaması hakkında istatistiksel çıkarım yaparken (örneğin güven aralığı veya hipotez testi için) **Z-dağılımı mı yoksa t-dağılımı mı** kullanmanız gerektiğini belirleyen bir karar akış şemasıdır. 🧠

Bu, istatistikte doğru aracı seçmek için kullanılan pratik bir yol haritasıdır.

---

### Karar Verme Süreci Adım Adım

Şema, size üç kritik soru sorarak doğru yola yönlendirir:

#### Soru 1: Popülasyon Standart Sapması ($\sigma$) Biliniyor mu?

Bu, yolculuğun ilk ve en önemli yol ayrımıdır.

* **Evet ise ✅ → Z-Dağılımı Kullan**
    * Eğer popülasyonun standart sapmasını biliyorsanız, bu "ideal" bir durumdur. Örneklem boyutunuz ne olursa olsun, her zaman **Z-dağılımını** kullanabilirsiniz.

* **Hayır ise ❌ → Soru 2'ye Geç**
    * Gerçek hayatta popülasyonun standart sapmasını neredeyse hiçbir zaman bilmeyiz. Bu çok daha yaygın bir senaryodur. Bu durumda, bir sonraki soruya geçmelisiniz.

#### Soru 2: Örneklem Boyutu ($n$) Yeterince Büyük mü? (Genellikle `n > 30`)

Popülasyon standart sapmasını bilmediğiniz için, örnekleminizin büyüklüğü kritik hale gelir.

* **Evet ise ✅ → Z-Dağılımı Kullan**
    * Örneklem boyutunuz yeterince büyükse (genellikle 30'dan fazla kabul edilir), **Merkezi Limit Teoremi** sayesinde örneklem standart sapması ($s$), popülasyon standart sapmasının ($\sigma$) oldukça güvenilir bir tahmini haline gelir. Bu nedenle, pratikte yine **Z-dağılımını** kullanabilirsiniz.

* **Hayır ise ❌ → Soru 3'e Geç**
    * Eğer örneklem boyutunuz küçükse (30'dan az), belirsizlik artar. Bu durumda son bir kontrol daha yapmanız gerekir.

#### Soru 3: Popülasyon Normal Dağılıma Sahip mi?

Küçük bir örneklemle çalışırken, ana popülasyonun şekli önem kazanır.

* **Evet ise ✅ → t-Dağılımı Kullan**
    * Eğer örnekleminiz küçükse, popülasyon standart sapmasını bilmiyorsanız **AMA** popülasyonun normal dağıldığını biliyorsanız (veya varsayabiliyorsanız), o zaman **t-dağılımı** sizin için doğru araçtır. t-dağılımı, küçük örneklemlerin getirdiği ekstra belirsizliği hesaba katmak için tasarlanmıştır.

* **Hayır ise ❌ → Başka Yöntemler Kullan**
    * Eğer bu üç koşulun hiçbiri sağlanmıyorsa (popülasyon $\sigma$'sı bilinmiyor, örneklem küçük VE popülasyon normal dağılmıyor), Z veya t-dağılımını kullanamazsınız. Bu durumda, **parametrik olmayan testler (non-parametric tests)** gibi başka istatistiksel yöntemlere başvurmanız gerekir.

---

### Özetle

Bu şema, şu pratik kuralları özetler:

* **Z-Dağılımı:** "İdeal" veya "büyük örneklemli" senaryolar için.
* **t-Dağılımı:** "Küçük örneklemli, belirsiz ama düzenli" senaryolar için.
* **Diğer Yöntemler:** "Küçük örneklemli, belirsiz ve düzensiz" senaryolar için.




# 💡 t-Dağılımı: Motivasyon ve Rolü (t-Distribution: Motivation and Role)

## 🎯 Hipotez Testinde t-Dağılımının Rolü Nedir?

* Bu görsel, istatistikte $t$-Dağılımının (t-Distribution) neden ortaya çıktığını ve hipotez testindeki temel rolünü mükemmel bir şekilde özetliyor.

<img width="1207" height="573" alt="image" src="https://github.com/user-attachments/assets/7ce1909c-4ecc-4685-9299-a7ea79447a73" />


* Eger Sigma bilinmezse ne olur? 


<img width="1203" height="563" alt="image" src="https://github.com/user-attachments/assets/30b19a24-6499-4ca4-a531-30b78cc5115a" />

* Degrees of freedom artarsa ne olur?
* 

<img width="1210" height="557" alt="image" src="https://github.com/user-attachments/assets/0d932907-0f43-41fc-82e4-a726acd99484" />



<img width="1207" height="582" alt="image" src="https://github.com/user-attachments/assets/ccddc7f0-596a-4558-9590-6c751504b14a" />



$t$-Dağılımının (Student's t-Distribution) hipotez testindeki temel rolü, **anakütle standart sapması ($\sigma$) bilinmediğinde** veya örneklem boyutu ($n$) küçük olduğunda ($\approx n < 30$) standart normal dağılım ($Z$-dağılımı) yerine kullanılmasıdır.

* **Rasyonel:** Bir hipotez testi yaparken bir test istatistiği hesaplamamız gerekir. Anakütle standart sapması ($\sigma$) biliniyorsa, $Z$-istatistiğini kullanırız. Ancak $\sigma$ bilinmiyorsa, $t$-dağılımını kullanırız.
* **Amaç:** $t$-dağılımı, $\sigma$'nın bilinmemesinden kaynaklanan ek belirsizliği hesaba katar. Bu, $Z$-dağılımına göre **daha geniş kuyruklara** sahip olması anlamına gelir, bu da daha **muhafazakâr (conservartive)** sonuçlar elde etmemizi sağlar.

---

## ❓ Eğer Sigma ($\sigma$) Bilinmezse Ne Olur? (Population Unknown $\sigma$)

Görsel, $\sigma$'nın bilinmediği durumda ne olduğunu açıkça göstermektedir:

### Z İstatistiği (If $\mu, \sigma$ are known):

$$Z = \frac{\bar{X} - \mu}{\sigma/\sqrt{n}} \sim N(0, 1^2)$$

Eğer anakütle standart sapması ($\sigma$) ve anakütle ortalaması ($\mu$) biliniyorsa, standartlaştırılmış örneklem ortalaması ($Z$ istatistiği) standart normal dağılımı ($N(0,1)$) takip eder.

### $\sigma$ Bilinmezse (What if $\sigma$ is unknown?):

$\sigma$ bilinmediğinde, onun yerine örneklemden hesaplanan bir tahmini değer olan **örneklem standart sapması ($S$)** kullanılır (**Replace $\sigma$ with its estimate**).

### T İstatistiği:

$$T = \frac{\bar{X} - \mu}{S/\sqrt{n}}$$

$\sigma$ yerine $S$ kullanıldığı anda, elde edilen test istatistiği artık $Z$ istatistiği değil, **$T$ istatistiği** olur ve **$t$-dağılımını** takip eder. Bu durum, istatistiğe **ek bir değişkenlik (variability)** getirir.

---

## 🛠️ $t$-Dağılımının Parametreleri Nelerdir?

$t$-Dağılımının temel tek bir parametresi vardır:

### Serbestlik Derecesi (Degrees of Freedom / $df$):

$t$-dağılımının şeklini belirleyen parametredir. Genellikle örneklem büyüklüğü ($n$) kullanılarak hesaplanır.

$$df = n - 1$$

Görseldeki örneklem büyüklüğü $n=10$ olduğu için ($i=1$'den $10$'a kadar toplam), serbestlik derecesi $df = 10 - 1 = 9$ olacaktır.

---

## ⬆️ Serbestlik Derecesi ($df$) Artarsa Ne Olur?

Serbestlik derecesi ($df$) $t$-dağılımının şekli üzerinde kritik bir etkiye sahiptir:

* **$df$ küçükken:** $t$-dağılımı, standart normal dağılıma göre daha basık (platykurtic) ve **daha kalın, geniş kuyruklara** sahiptir. Bu, uç değerlerin (outliers) ortaya çıkma olasılığının daha yüksek olduğu anlamına gelir.
* **$df$ arttıkça ($n$ büyüdükçe):** $t$-dağılımının şekli, kuyrukları incelterek ve merkezi tepe noktasını yükselterek **standart normal dağılıma ($Z$-Distribution) yaklaşır.**
* **$df \to \infty$ olduğunda:** $t$-dağılımı, pratik olarak standart normal dağılım ile aynı hale gelir. (Genellikle $df > 30$ olduğunda $t$ yerine $Z$ kullanılabilir.)

### 📝 Özetle:

Örneklem boyutu büyüdükçe, $\sigma$'nın tahmini ($S$) daha güvenilir hale gelir ve **$t$-dağılımı $Z$-dağılımı ile birleşir.**

# t-Tests: Gaussian Veri (Bilinmeyen $\sigma$)

<img width="1219" height="589" alt="image" src="https://github.com/user-attachments/assets/25ad45f0-8a79-4100-9f6b-ddfb6eb45207" />


# 📊 Sağ Kuyruk Testi: Gaussian Veri (Bilinmeyen $\sigma$)

Bu analiz, ABD'de 1970'lerde 18 yaşındaki bireylerin ortalama boyunun günümüzde artıp artmadığını, $\sigma$ bilinmediği için $t$-Dağılımı kullanarak test etmektedir.

---

## 1. Hipotezler ve Seviyeler

| Parametre | Değer/İfade | Açıklama |
| :--- | :--- | :--- |
| **Sıfır Hipotezi** ($H_0$) | $\mu = 66.7$ in. | Ortalama boyun değişmediği varsayımı. |
| **Alternatif Hipotez** ($H_1$) | $\mu > 66.7$ in. | Ortalama boyun arttığı hipotezi (Sağ Kuyruk Testi). |
| **Örneklem Büyüklüğü** ($n$) | $n=10$ | |
| **Anlamlılık Seviyesi** ($\alpha$) | $\alpha = 0.05$ | Reddetme bölgesi için belirlenen risk seviyesi (%5). |

---

## 2. Örneklem İstatistikleri ve t-İstatistiği Hesaplama

| İstatistik | Değer | Açıklama |
| :--- | :--- | :--- |
| **Örneklem Ortalaması** ($\bar{x}$) | $68.442$ | |
| **Örneklem Standart Sapması** ($s$) | $3.113$ | |

### 🚀 t-İstatistiği

Örneklem standart sapması ($s$) kullanılarak $t$-istatistiği hesaplanır:

$$t = \frac{\bar{x} - \mu}{s/\sqrt{n}} = \frac{68.442 - 66.7}{3.113/\sqrt{10}} \approx \mathbf{1.770}$$

---

## 3. P-Değeri (p-value) Hesaplama

Hesaplanan $t=1.770$ değerinin, $H_0$'ın doğru olduğu varsayımıyla elde edilme olasılığı bulunur.

$$\text{p-value: } P\left(\frac{\bar{X} - 66.7}{S/\sqrt{10}} > 1.770 \mid \mu = 66.7\right)$$

Hesaplanan p-değeri: 
$$\mathbf{0.0552}$$

*(Bu değer, $t$-dağılımının $1.770$ değerinden sonraki sağ kuyruk alanını temsil eder - Grafikteki turuncu bölge)*

---

## 4. Karar ve Sonuç

P-değeri ($\mathbf{0.0552}$) $\alpha$ ($\mathbf{0.05}$) ile karşılaştırılır:

$$0.0552 > 0.05$$

* **Karar Kuralı:** Eğer $\text{p-value} > \alpha$ ise $H_0$ **redd edilmez**.
* **Sonuç:** $\implies$ **Do not reject $H_0$** (Null hypothesis reddedilmez).

### Yorum 💬

%5 anlamlılık seviyesinde, ortalama boyun $66.7$ inçten daha büyük olduğuna dair **yeterli istatistiksel kanıt yoktur

<img width="1210" height="603" alt="image" src="https://github.com/user-attachments/assets/6d26c2d9-4b18-4e38-90eb-ea0ef0ead229" />

# 🧮 Çift Kuyruk Testi: Gaussian Veri (Bilinmeyen $\sigma$)

Bu analiz, ABD'de 1970'lerde 18 yaşındaki bireylerin ortalama boyunun **değişip değişmediğini** test etmektedir. Anakütle standart sapması ($\sigma$) bilinmediği için $t$-Dağılımı kullanılmıştır.

---

## 1. Hipotezler ve Seviyeler

| Parametre | Değer/İfade | Açıklama |
| :--- | :--- | :--- |
| **Sıfır Hipotezi** ($H_0$) | $\mu = 66.7$ in. | Ortalama boyun değişmediği varsayımı. |
| **Alternatif Hipotez** ($H_1$) | $\mu \neq 66.7$ in. | Ortalama boyun değiştiği hipotezi (**Çift Kuyruk Testi**). |
| **Örneklem Büyüklüğü** ($n$) | $n=10$ | |
| **Anlamlılık Seviyesi** ($\alpha$) | $\alpha = 0.05$ | Reddetme bölgesi için belirlenen risk seviyesi. |

---

## 2. Örneklem İstatistikleri ve t-İstatistiği Hesaplama

| İstatistik | Değer | Açıklama |
| :--- | :--- | :--- |
| **Örneklem Ortalaması** ($\bar{x}$) | $68.442$ | |
| **Örneklem Standart Sapması** ($s$) | $3.113$ | |

### 🚀 t-İstatistiği

Örneklem standart sapması ($s$) kullanılarak $t$-istatistiği hesaplanır:

$$t = \frac{\bar{x} - \mu}{s/\sqrt{n}} = \frac{68.442 - 66.7}{3.113/\sqrt{10}} \approx \mathbf{1.770}$$

---

## 3. P-Değeri (p-value) Hesaplama

Çift kuyruk testinde, $t$'nin mutlak değerinin her iki yönde de elde edilme olasılığı bulunur.

$$\text{p-value: } P\left(\left|\frac{\bar{X} - 66.7}{S/\sqrt{10}}\right| > 1.770 \mid \mu = 66.7\right)$$

*p-değeri, tek kuyruk testinin p-değerinin iki katıdır ($\approx 0.0552 \times 2$).*

Hesaplanan p-değeri: 
$$\mathbf{0.1105}$$

*(Bu değer, $t$-dağılımının $1.770$'ın sağında ve $-1.770$'ın solunda kalan iki kuyruk alanının toplamını temsil eder - Grafikteki turuncu bölgeler)*

---

## 4. Karar ve Sonuç

P-değeri ($\mathbf{0.1105}$) $\alpha$ ($\mathbf{0.05}$) ile karşılaştırılır:

$$0.1105 > 0.05$$

* **Karar Kuralı:** Eğer $\text{p-value} > \alpha$ ise $H_0$ **redd edilmez**.
* **Sonuç:** $\implies$ **Do not reject $H_0$** (Null hypothesis reddedilmez).

### Yorum 💬

%5 anlamlılık seviyesinde, ortalama boyun $66.7$ inçten **farklı olduğuna** dair **yeterli istatistiksel kanıt yoktur**.


<img width="1217" height="597" alt="image" src="https://github.com/user-attachments/assets/8cab2ac3-821a-435a-92d2-1fb15e018d1e" />

# 📉 Sol Kuyruk Testi: Gaussian Veri (Bilinmeyen $\sigma$)

Bu analiz, ABD'de 1970'lerdeki 18 yaşındaki bireylerin ortalama boyunun **azalıp azalmadığını** test etmektedir. Anakütle standart sapması ($\sigma$) bilinmediği için $t$-Dağılımı kullanılmıştır.

---

## 1. Hipotezler ve Seviyeler

| Parametre | Değer/İfade | Açıklama |
| :--- | :--- | :--- |
| **Sıfır Hipotezi** ($H_0$) | $\mu = 66.7$ in. | Ortalama boyun değişmediği varsayımı. |
| **Alternatif Hipotez** ($H_1$) | $\mu < 66.7$ in. | Ortalama boyun azaldığı hipotezi (**Sol Kuyruk Testi**). |
| **Örneklem Büyüklüğü** ($n$) | $n=10$ | |
| **Anlamlılık Seviyesi** ($\alpha$) | $\alpha = 0.05$ | Reddetme bölgesi için belirlenen risk seviyesi. |

---

## 2. Örneklem İstatistikleri ve t-İstatistiği Hesaplama

| İstatistik | Değer | Açıklama |
| :--- | :--- | :--- |
| **Örneklem Ortalaması** ($\bar{x}$) | $64.252$ | |
| **Örneklem Standart Sapması** ($s$) | $3.113$ | |

### 🚀 t-İstatistiği

Örneklem standart sapması ($s$) kullanılarak $t$-istatistiği hesaplanır:

$$t = \frac{\bar{x} - \mu}{s/\sqrt{n}} = \frac{64.252 - 66.7}{3.113/\sqrt{10}} \approx \mathbf{-2.487}$$

---

## 3. P-Değeri (p-value) Hesaplama

Hesaplanan negatif $t=-2.487$ değerinin, $H_0$'ın doğru olduğu varsayımıyla elde edilme olasılığı bulunur.

$$\text{p-value: } P\left(\frac{\bar{X} - 66.7}{S/\sqrt{10}} < -2.487 \mid \mu = 66.7\right)$$

Hesaplanan p-değeri: 
$$\mathbf{0.0173}$$

*(Bu değer, $t$-dağılımının $-2.487$ değerinden önceki sol kuyruk alanını temsil eder - Grafikteki turuncu bölge)*

---

## 4. Karar ve Sonuç

P-değeri ($\mathbf{0.0173}$) $\alpha$ ($\mathbf{0.05}$) ile karşılaştırılır:

$$0.0173 < 0.05$$

* **Karar Kuralı:** Eğer $\text{p-value} < \alpha$ ise $H_0$ **reddedilir**.
* **Sonuç:** $\implies$ **Conclusion: reject $H_0$** (Sıfır hipotezi reddedilir).

### Yorum 💬

%5 anlamlılık seviyesinde, ortalama boyun $66.7$ inçten **azaldığına** dair **yeterli istatistiksel kanıt bulunmuştur**.

<img width="752" height="638" alt="image" src="https://github.com/user-attachments/assets/4e5d9888-b600-41c4-8343-f1312195322d" />

<img width="750" height="343" alt="image" src="https://github.com/user-attachments/assets/fa18b80f-9034-48df-a068-fbc3b799f532" />

<img width="795" height="708" alt="image" src="https://github.com/user-attachments/assets/f50d12ca-db64-468a-a767-234cc94d1a40" />

<img width="784" height="423" alt="image" src="https://github.com/user-attachments/assets/951f01e0-15e5-4fb1-a5de-0af61a8288e5" />

<img width="798" height="367" alt="image" src="https://github.com/user-attachments/assets/18c758a6-f575-4e94-b84e-b6ae95552833" />


<img width="788" height="591" alt="image" src="https://github.com/user-attachments/assets/93c22c26-2a9d-440a-a0ab-ae41b2a01493" />

---

# 🚀 Bağımsız İki Örneklem $t$-Testi (Independent Two Sample $t$-Test)

* Farkli populasyon ve örneklemde- Independent  two sample t-Test, t-testle olan iliskisi nedir?
* Burada degree of freedom´in önemi nedir?, Independent  two sample t-Test´te right, left and two tailed testlere nasil karar verecegim?
* Hangi parametrelere bakmam gerekli?, Independent  two sample t-Test´te P-valunun durumu nedir? Ne zaman ve ne etkilerde degisir? ve significance level ile olan iliskilerini nasil incelememiz gereki?
* Hipotezlerin karar/ kabul durumlari ne olur? ve Nelere bakarak degerlendirmemiz gerekli? Hangi parametreler karsilastirilmali?
* ML´de   Two Sample t -Test nerede ve nasil kullanilir?


<img width="1211" height="573" alt="image" src="https://github.com/user-attachments/assets/97284ce1-115d-4d28-8368-c5f62720c992" />


<img width="1127" height="583" alt="image" src="https://github.com/user-attachments/assets/5966f711-7191-4b8b-81f8-3a6388a1cade" />

* Then:

<img width="1103" height="583" alt="image" src="https://github.com/user-attachments/assets/94379043-f75d-41f7-acfd-0a8542491901" />


<img width="1208" height="602" alt="image" src="https://github.com/user-attachments/assets/5a5918d1-bb12-4f7b-b9fb-447503bfb5f2" />


<img width="1214" height="592" alt="image" src="https://github.com/user-attachments/assets/997f524c-358e-439c-b10a-c8c76a1bdc7a" />

<img width="1207" height="577" alt="image" src="https://github.com/user-attachments/assets/e2c93fa9-3023-4cc3-ab70-428e4f83c8e3" />



<img width="1233" height="600" alt="image" src="https://github.com/user-attachments/assets/1375fe30-2745-4bbe-8fe5-c2a779c69489" />


<img width="1226" height="603" alt="image" src="https://github.com/user-attachments/assets/71875565-485c-4ba8-bbc4-4875402c198c" />


# 🤝 1. Farklı Popülasyon ve Örneklemde - İlişkisi Nedir?

Bağımsız iki örneklem $t$-Testi (Independent Two Sample $t$-Test), adından da anlaşılacağı gibi, **birbirinden bağımsız iki farklı popülasyonun (anakütlenin) ortalamaları arasında anlamlı bir fark olup olmadığını** test etmek için kullanılır.

| Kavram | Açıklama |
| :--- | :--- |
| **Popülasyonlar** | İki ayrı ve bağımsız grup varsayılır (Örn: A Reklamını görenler ve B Reklamını görenler). Popülasyon parametreleri $\mu_1$ ve $\mu_2$'dir. |
| **Örneklemler** | Her popülasyondan bağımsız olarak veri toplanır. Örneklem istatistikleri $\bar{X}_1$ ve $\bar{X}_2$'dir. |
| **$t$-Test ile İlişkisi** | Tek örneklem $t$-Testi, bir örneklemin ortalamasını bilinen bir popülasyon ortalamasıyla ($\mu$) karşılaştırırken; **İki Örneklem $t$-Testi, iki örneklem ortalaması arasındaki farkı $(\bar{X}_1 - \bar{X}_2)$, bu farkın sıfır olup olmadığına göre** (yani $\mu_1 = \mu_2$ olup olmadığına göre) test eder. |

### Test İstatistiği (Genel Formül):

$$t = \frac{(\bar{X}_1 - \bar{X}_2) - (\mu_1 - \mu_2)}{SE(\bar{X}_1 - \bar{X}_2)}$$
*Sıfır hipotezi ($H_0: \mu_1 = \mu_2$) altında, formüldeki $(\mu_1 - \mu_2)$ terimi $0$ kabul edilir.*

# 👥 İki Örneklem $t$-Testi Temel Kavramları

Bu tablo, Bağımsız İki Örneklem $t$-Testinde yer alan temel istatistiksel kavramları ve testin amacını açıklamaktadır.

---

| Kavram | Açıklama |
| :--- | :--- |
| **Popülasyonlar** | İki ayrı ve bağımsız grup varsayılır (Örn: A Reklamını görenler ve B Reklamını görenler). Popülasyon parametreleri $\mu_1$ ve $\mu_2$'dir. |
| **Örneklemler** | Her popülasyondan bağımsız olarak veri toplanır. Örneklem istatistikleri $\bar{X}_1$ ve $\bar{X}_2$'dir. |
| **$t$-Test ile İlişkisi** | Tek örneklem $t$-Testi, bir örneklemin ortalamasını bilinen bir popülasyon ortalamasıyla ($\mu$) karşılaştırırken; **İki Örneklem $t$-Testi, iki örneklem ortalaması arasındaki farkı ($\bar{X}_1 - \bar{X}_2$), bu farkın sıfır olup olmadığına göre** (yani $\mu_1 = \mu_2$ olup olmadığına göre) test eder. |


# 🛠️ Test İstatistiği ve $df$ Hesaplaması

## Test İstatistiği (Genel Formül)

Bağımsız İki Örneklem $t$-Testinin genel formülü aşağıdaki gibidir:

$$t = \frac{(\bar{X}_1 - \bar{X}_2) - (\mu_1 - \mu_2)}{SE(\bar{X}_1 - \bar{X}_2)}$$

* Sıfır hipotezi ($H_0: \mu_1 = \mu_2$) altında, formüldeki $(\mu_1 - \mu_2)$ terimi $\mathbf{0}$ kabul edilir.

---

## 2. Serbestlik Derecesinin Önemi ve Test Türüne Karar Verme

### Serbestlik Derecesinin ($df$) Önemi 📐

Bağımsız iki örneklem $t$-Testinde **serbestlik derecesi ($df$)**, hesaplanan $t$-değerinin hangi $t$-dağılımını takip edeceğini belirler. İki farklı örneklem olduğu için $df$ hesaplaması daha karmaşıktır ve **varyansların eşit olup olmamasına (Homogeneity of Variances)** göre değişir:

#### 1. Varyanslar Eşit Kabul Edilirse (Pooled t-Test):

$$df = n_1 + n_2 - 2$$

#### 2. Varyanslar Eşit Kabul Edilmezse (Welch's t-Test):

* $df$ için karmaşık bir formül (Welch-Satterthwaite denklemi) kullanılır.
* Genellikle istatistiksel yazılımlar bunu otomatik hesaplar ve $df$ tam sayı olmayabilir.
* **Bu, pratikte daha yaygın kullanılan ve varsayımlara daha az hassas olan yöntemdir.**

$df$'in önemi, **testin gücünü ve p-değerini doğru hesaplamak için doğru dağılımı seçmeyi** sağlamasıdır.

### Test Türüne Karar Verme (Right, Left and Two-Tailed) 🚪

Test türüne, kurulan **Alternatif Hipotez ($H_1$)** ile karar verilir:

| Test Türü | Alternatif Hipotez ($H_1$) | Anlamı |
| :--- | :--- | :--- |
| **Çift Kuyruk (Two-Tailed)** | $\mu_1 \neq \mu_2$ | Ortalamalar arasında **fark var** mı? |
| **Sağ Kuyruk (Right-Tailed)** | $\mu_1 > \mu_2$ | Birinci popülasyonun ortalaması, ikinciden **daha büyük** mi? |
| **Sol Kuyruk (Left-Tailed)** | $\mu_1 < \mu_2$ | Birinci popülasyonun ortalaması, ikinciden **daha küçük** mü? |

# 🚀 Bağımsız İki Örneklem $t$-Testi (Independent Two Sample $t$-Test)

Harika bir konu! Bağımsız İki Örneklem $t$-Testi (Independent Two Sample $t$-Test), makine öğrenimi ve veri biliminde A/B testlerinden deney analizlerine kadar birçok yerde kullanılan temel bir istatistiksel araçtır.

Aşağıda, istediğiniz başlıkları teknik, kapsamlı ve anlaşılır bir şekilde ele alarak sunuyorum.

---

## 1. Farklı Popülasyon ve Örneklemde - İlişkisi Nedir? 🤝

Bağımsız iki örneklem $t$-Testi, adından da anlaşılacağı gibi, **birbirinden bağımsız iki farklı popülasyonun (anakütlenin) ortalamaları arasında anlamlı bir fark olup olmadığını** test etmek için kullanılır.

| Kavram | Açıklama |
| :--- | :--- |
| **Popülasyonlar** | İki ayrı ve bağımsız grup varsayılır (Örn: A Reklamını görenler ve B Reklamını görenler). Popülasyon parametreleri $\mu_1$ ve $\mu_2$'dir. |
| **Örneklemler** | Her popülasyondan bağımsız olarak veri toplanır. Örneklem istatistikleri $\bar{X}_1$ ve $\bar{X}_2$'dir. |
| **$t$-Test ile İlişkisi** | Tek örneklem $t$-Testi, bir örneklemin ortalamasını bilinen bir popülasyon ortalamasıyla ($\mu$) karşılaştırırken; **İki Örneklem $t$-Testi, iki örneklem ortalaması arasındaki farkı $(\bar{X}_1 - \bar{X}_2)$, bu farkın sıfır olup olmadığına göre** (yani $\mu_1 = \mu_2$ olup olmadığına göre) test eder. |

### Test İstatistiği (Genel Formül): 📈

$$t = \frac{(\bar{X}_1 - \bar{X}_2) - (\mu_1 - \mu_2)}{SE(\bar{X}_1 - \bar{X}_2)}$$

Sıfır hipotezi ($H_0: \mu_1 = \mu_2$) altında, formüldeki $(\mu_1 - \mu_2)$ terimi $\mathbf{0}$ kabul edilir.

---

## 2. Serbestlik Derecesinin Önemi ve Test Türüne Karar Verme 📐

### Serbestlik Derecesinin ($df$) Önemi

Bağımsız iki örneklem $t$-Testinde **serbestlik derecesi ($df$)**, hesaplanan $t$-değerinin hangi $t$-dağılımını takip edeceğini belirler. İki farklı örneklem olduğu için $df$ hesaplaması daha karmaşıktır ve **varyansların eşit olup olmamasına (Homogeneity of Variances)** göre değişir:

#### Varyanslar Eşit Kabul Edilirse (Pooled t-Test):

$$df = n_1 + n_2 - 2$$

#### Varyanslar Eşit Kabul Edilmezse (Welch's t-Test):

* $df$ için karmaşık bir formül (Welch-Satterthwaite denklemi) kullanılır.
* Genellikle istatistiksel yazılımlar bunu otomatik hesaplar ve $df$ tam sayı olmayabilir.
* Bu, **pratikte daha yaygın kullanılan ve varsayımlara daha az hassas olan yöntemdir**.

$df$'in önemi, **testin gücünü ve p-değerini doğru hesaplamak için doğru dağılımı seçmeyi** sağlamasıdır.

### Test Türüne Karar Verme (Right, Left and Two-Tailed) 🚪

Test türüne, kurulan **Alternatif Hipotez ($H_1$)** ile karar verilir:

| Test Türü | Alternatif Hipotez ($H_1$) | Anlamı |
| :--- | :--- | :--- |
| **Çift Kuyruk (Two-Tailed)** | $\mu_1 \neq \mu_2$ | Ortalamalar arasında **fark var** mı? ($H_0: \mu_1 = \mu_2$ reddedilir.) |
| **Sağ Kuyruk (Right-Tailed)** | $\mu_1 > \mu_2$ | Birinci popülasyonun ortalaması, ikinciden **daha büyük** mü? |
| **Sol Kuyruk (Left-Tailed)** | $\mu_1 < \mu_2$ | Birinci popülasyonun ortalaması, ikinciden **daha küçük** mü? |

---

## 3. Parametreler, P-Değeri ve Anlamlılık Seviyesi ($\alpha$) İlişkisi 🧐

### Hangi Parametrelere Bakmam Gerekli?

* **Örneklem Ortalamaları ($\bar{X}_1, \bar{X}_2$):** Ortalamalar arasındaki farkın büyüklüğü.
* **Örneklem Büyüklükleri ($n_1, n_2$):** Testin gücünü ve $df$'yi belirler.
* **Örneklem Standart Sapmaları ($S_1, S_2$):** Varyansı ve dolayısıyla Test İstatistiğinin paydasını ($SE$) belirler.
* **Varyans Eşitliği Testi Sonucu (Örn: Levene Testi):** Hangi $t$-Test formülünün kullanılacağına (Pooled vs. Welch's) karar vermek için gereklidir.

### P-Değerinin Durumu ve Etkileyen Faktörler 📉

**P-Değeri (p-value):** Sıfır hipotezi ($H_0$) doğruyken, elimizdeki veriler kadar veya daha ekstrem bir sonuç görme olasılığıdır.

#### Değişim Nedenleri ve Etkileri:

* **Ortalamalar Arasındaki Farkın Büyüklüğü ($\bar{X}_1 - \bar{X}_2$):** Fark ne kadar büyükse, $t$-değeri o kadar büyük olur ve p-değeri o kadar **küçülür** (Daha anlamlı bir sonuç).
* **Standart Hata ($SE$):** $SE$ ne kadar küçükse, $t$-değeri o kadar büyük olur ve p-değeri o kadar **küçülür**. $SE$'yi küçülten faktörler:
    * Örneklem büyüklüğünün ($n$) artması.
    * Örneklem varyansının ($S^2$) azalması.
* **Serbestlik Derecesi ($df$):** $df$ arttıkça, $t$-dağılımı normal dağılıma yaklaşır ve bu durum p-değeri üzerinde küçük bir etki yaratabilir.

### P-Değeri ve Anlamlılık Seviyesi ($\alpha$) İlişkisi 🚦

* **Anlamlılık Seviyesi ($\alpha$ / Significance Level):** Testi yapmadan önce belirlenen ve reddetme bölgesini tanımlayan eşik değerdir. Genellikle $\mathbf{0.05}$ (%5) olarak ayarlanır. Bu, Birinci Tip Hata (Type I Error) yapma riskini (doğru $H_0$'ı reddetme riski) temsil eder.
* **İlişki:** Test kararı bu iki değerin karşılaştırılmasına dayanır:
    * Eğer $\text{p-value} \leq \alpha$ ise: Sonuç istatistiksel olarak **anlamlıdır**. $H_0$ reddedilir.
 
# ✍️ 4. Hipotezlerin Karar/Kabul Durumları

Hipotez testinde kullanılan parametreler ve karar verme süreci:

| Durum | Karşılaştırma | İstatistiksel Karar | Yorum |
| :--- | :--- | :--- | :--- |
| **Anlamlı Fark Var** ✅ | p-value $\leq \alpha$ | $H_0$ **Reddedilir** | $\mu_1$ ve $\mu_2$ arasında anlamlı bir fark olduğuna dair yeterli kanıt var. $\mathbf{H_1}$ kabul edilir. |
| **Anlamlı Fark Yok** ❌ | p-value $ > \alpha$ | $H_0$ **Reddedilemez** | $\mu_1$ ve $\mu_2$ arasında anlamlı bir fark olduğuna dair yeterli kanıt yok. Fark, tesadüfü olabilir. |

### Karşılaştırılacak Temel Parametreler:

1.  **$p$-Değeri** vs. **$\alpha$ seviyesi** (En yaygın karar mekanizması).
2.  **Hesaplanan $t$-Değeri** vs. **Kritik $t$-Değeri** ($df$ ve $\alpha$'ya dayalı tablo değeri).

### Karşılaştırılacak Temel Parametreler: 🎯

1.  **$p$-Değeri** vs. **$\alpha$ seviyesi** (En yaygın karar mekanizması).
2.  **Hesaplanan $t$-Değeri** vs. **Kritik $t$-Değeri** ($df$ ve $\alpha$'ya dayalı tablo değeri).

---

## 5. ML'de Two Sample $t$-Test Nerede ve Nasıl Kullanılır? 🤖

Bağımsız iki örneklem $t$-Testi, Makine Öğrenimi (ML) ve Veri Bilimi bağlamında, özellikle **karşılaştırmalı analiz** ve **deney tasarımı** aşamalarında hayati bir rol oynar:

| Kullanım Alanı | Senaryo | Nasıl Kullanılır? |
| :--- | :--- | :--- |
| **A/B Testi** | Bir e-ticaret sitesinde A tasarımının B tasarımından daha iyi dönüşüm (Conversion Rate) sağlayıp sağlamadığını test etmek. | $H_0: \mu_{A} = \mu_{B}$. İki grubun dönüşüm ortalaması $(\bar{X}_A, \bar{X}_B)$ karşılaştırılarak hangi tasarımın daha iyi olduğu kararlaştırılır. |
| **Model Değerlendirme** | İki farklı ML modelinin (Örn: Model 1 vs. Model 2) aynı veri seti üzerinde elde ettiği performans metriklerinin (Örn: F1 Skoru, RMSE) ortalamaları arasında fark var mı? | Modellerin k-katlamalı çapraz doğrulama (k-fold cross-validation) ile elde edilen metriklerinin ortalamaları karşılaştırılır. Eğer fark anlamlıysa, modellerden biri diğerinden daha iyidir. |
| **Özellik Seçimi** | Bir özelliğin (feature) eklendiği modelin performansının, eklenmediği modele göre anlamlı bir fark yaratıp yaratmadığını test etmek. | Özelliğin etkisini nicel olarak test ederek gereksiz özelliklerin elenmesine yardımcı olur. |
| **Ön İşleme Etkisi** | İki farklı veri ön işleme yönteminin (Örn: Normalizasyon vs. Standardizasyon) nihai model başarısı üzerindeki etkisini karşılaştırmak. | İki ön işleme yöntemiyle eğitilmiş modellerin test seti performansları karşılaştırılır. |

# 🤖 5. ML'de Two Sample $t$-Test Nerede ve Nasıl Kullanılır?

Bağımsız iki örneklem $t$-Testi, Makine Öğrenimi (ML) ve Veri Bilimi bağlamında, özellikle **karşılaştırmalı analiz** ve **deney tasarımı** aşamalarında hayati bir rol oynar:

| Kullanım Alanı | Senaryo | Nasıl Kullanılır? |
| :--- | :--- | :--- |
| **A/B Testi** 🛒 | Bir e-ticaret sitesinde A tasarımının B tasarımından daha iyi dönüşüm (Conversion Rate) sağlayıp sağlamadığını test etmek. | $H_0: \mu_{A} = \mu_{B}$. İki grubun dönüşüm ortalaması ($\bar{X}_A, \bar{X}_B$) karşılaştırılarak hangi tasarımın daha iyi olduğu kararlaştırılır. |
| **Model Değerlendirme** ✨ | İki farklı ML modelinin (Örn: Model 1 vs. Model 2) aynı veri seti üzerinde elde ettiği performans metriklerinin (Örn: F1 Skoru, RMSE) ortalamaları arasında fark var mı? | Modellerin k-katlamalı çapraz doğrulama (k-fold cross-validation) ile elde edilen metriklerinin ortalamaları karşılaştırılır. Eğer fark anlamlıysa, modellerden biri diğerinden daha iyidir. |
| **Özellik Seçimi** 🧩 | Bir özelliğin (feature) eklendiği modelin performansının, eklenmediği modele göre anlamlı bir fark yaratıp yaratmadığını test etmek. | Özelliğin etkisini nicel olarak test ederek gereksiz özelliklerin elenmesine yardımcı olur. |
| **Ön İşleme Etkisi** ⚙️ | İki farklı veri ön işleme yönteminin (Örn: Normalizasyon vs. Standardizasyon) nihai model başarısı üzerindeki etkisini karşılaştırmak. | İki ön işleme yöntemiyle eğitilmiş modellerin test seti performansları karşılaştırılır. |




