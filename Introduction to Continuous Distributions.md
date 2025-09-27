# Introduction to Continuous Distributions
<img width="730" height="417" alt="image" src="https://github.com/user-attachments/assets/7fd55c10-9097-4ec4-8143-2f65c634c7d8" />
<img width="811" height="711" alt="image" src="https://github.com/user-attachments/assets/2e6c86d1-aa90-46cf-b10d-58d999bf4ef1" />
<img width="812" height="455" alt="image" src="https://github.com/user-attachments/assets/e39c1617-8ebf-4dcc-adb8-28db52b0f9ac" />
<img width="763" height="622" alt="image" src="https://github.com/user-attachments/assets/62d63364-b096-45cc-a4b0-3630727d41aa" />
<img width="767" height="652" alt="image" src="https://github.com/user-attachments/assets/d8c106eb-92e7-45b5-bc75-ded24e9fbcb5" />
<img width="743" height="452" alt="image" src="https://github.com/user-attachments/assets/2b6f9f8e-6a66-4d55-bc90-4e9799808f1d" />
<img width="777" height="537" alt="image" src="https://github.com/user-attachments/assets/cd6639b4-311c-4e6f-8d5d-80a6df19d879" />
<img width="747" height="404" alt="image" src="https://github.com/user-attachments/assets/1c6cda6b-bd58-4e3f-b2c0-e3debb17c337" />

---

## Genel Bakış: Olasılığın İki Farklı Dünyası

Olasılık dünyasını iki ana krallığa ayırabiliriz: **Kesikli (Discrete)** ve **Sürekli (Continuous)**. Aralarındaki temel fark, ölçtüğümüz şeyin "sayılabilir" mi yoksa "ölçülebilir" mi olduğudur.

---

## Karşılaştırma ve Metaforlar

### 1. Kesikli Dağılım vs. Sürekli Dağılım

Görsellerde bu ikili arasındaki fark net bir şekilde gösteriliyor.

* **Kesikli Dağılım (Bilye Torbası Metaforu):**
    * **Ne Olduğu:** Elinizde bir torba olduğunu ve içinde 3 kırmızı, 5 mavi bilye olduğunu hayal edin. Torbadan bir bilye çektiğinizde gelebilecek sonuçlar **sayılabilir** ve **sınırlıdır**: ya kırmızıdır ya da mavidir. "Yarı kırmızı, yarı mavi" bir bilye çekemezsiniz.
    * **Örnekler:** Zar atışı (1, 2, 3, 4, 5, 6 gelebilir), yazı-tura (yazı veya tura), bir saatte gelen müşteri sayısı (10, 11, 12... ama 10.5 müşteri gelemez).
    * **Grafiği (PMF - Olasılık Kütle Fonksiyonu):** Her bir olayın (örneğin 3 gelmesi) olasılığını gösteren ayrı **çubuklardan** oluşur. Her çubuğun yüksekliği, tam olarak o değerin gerçekleşme olasılığını verir. Örneğin, `$P(X = 3)$` yani "zarın tam 3 gelme olasılığı" anlamlıdır ve bir değeri vardır (1/6).
 
* **Sürekli Dağılım (Su Bardağı Metaforu):**
    * **Ne Olduğu:** Şimdi de elinizde bir su bardağı olduğunu düşünün. Bardağı ne kadar doldurdunuz? 150 ml olabilir, 150.1 ml olabilir, 150.112345... ml olabilir. İki değer arasında **sonsuz sayıda** olası değer vardır. Değerler "sayılamaz", ancak bir aralıkta **"ölçülebilir"**.
    * **Örnekler:** Bir insanın boyu, bir arabanın hızı, bir odanın sıcaklığı.
    * **Grafiği (PDF - Olasılık Yoğunluk Fonksiyonu):** Ayrı çubuklar yerine **kesintisiz bir eğri** şeklindedir. Burada kritik bir fark var: Eğrinin bir noktadaki yüksekliği doğrudan olasılığı vermez! Tek bir noktanın olasılığı sıfırdır. Neden mi? Çünkü *tam olarak* 175.00000... cm boyunda biri olma ihtimali, sonsuz olasılık içinde matematiksel olarak sıfırdır.
    * **Anlamlı Olan Nedir?** "Boyunun 175 cm ile 176 cm *arasında* olma olasılığı" gibi bir aralığın olasılığı anlamlıdır. Bu olasılık, eğrinin altında kalan **alandır**.
 
  ### 2. Sürekli Dağılımların Araçları: PDF ve CDF

Sürekli verilerle çalışmak için özel araçlara ihtiyacımız var.

* **PDF (Probability Density Function - Olasılık Yoğunluk Fonksiyonu):**

<img width="440" height="543" alt="image" src="https://github.com/user-attachments/assets/4b0923ac-5e10-4715-86b2-8c7ff46c9d95" />


<img width="440" height="543" alt="image" src="https://github.com/user-attachments/assets/e9aee059-308f-4f99-b702-49f43a38e829" />

* Geometric visualisation of the mode, median and mean of an arbitrary unimodal probability density function.

<img width="1023" height="738" alt="image" src="https://github.com/user-attachments/assets/459157ad-a5c0-45e0-b377-7d3f2d6c33f5" />

* Examples of four continuous probability density functions.

    * **Metafor (Manzara Tepeleri):** PDF eğrisini bir dağ veya tepe manzarası gibi düşünün.
    * **Tepenin Yüksekliği ($f(x)$):** Manzaranın herhangi bir noktasındaki yükseklik, o bölgede bir değerin ortaya çıkmasının ne kadar "yoğun" veya "olası" olduğunu gösterir. Zirveler, en olası değerlerin kümelendiği yerlerdir. Ancak bu yükseklik, tek başına bir olasılık değildir.
    * **Alan (Olasılık):** Belirli bir aralıktaki olasılığı bulmak için o aralıktaki tepenin altında kalan alanı hesaplamamız gerekir ($P(a < X < b)$). Tüm manzaranın (tüm tepelerin) altındaki toplam alan her zaman 1'dir (%100).
 
[Probability Density Function - Wikipedia](https://en.wikipedia.org/wiki/Probability_density_function)

* **CDF (Cumulative Distribution Function - Kümülatif Dağılım Fonksiyonu):**

<img width="381" height="344" alt="image" src="https://github.com/user-attachments/assets/3900d3ec-a1de-4a4a-999c-31765523da76" />

<img width="378" height="305" alt="image" src="https://github.com/user-attachments/assets/79018f58-facb-4e20-a53a-baa0b173a700" />

<img width="322" height="372" alt="image" src="https://github.com/user-attachments/assets/4723ef95-cb4b-4ca4-b9aa-73ff08898a45" />

   * **Metafor (Tırmanış Rotası):** CDF, bu manzarada en soldan başlayıp sağa doğru ilerlerken, o ana kadar arkanızda bıraktığınız toplam alanı (yani toplam olasılığı) gösteren bir fonksiyondur.
  * Yolculuğun en başında (en solda) arkanızda hiç alan yoktur, yani CDF = 0.
  * Yolculuğun sonunda (en sağda) tüm manzarayı geçtiğiniz için toplam alan 1 olur, yani CDF = 1.
  * Bu araç çok kullanışlıdır. Çünkü iki nokta arasındaki alanı (olasılığı) bulmak için integral ile uğraşmak yerine, sadece o noktalardaki kümülatif değerleri birbirinden çıkarırız: `$P(a < X < b) = CDF(b) - CDF(a)$`.
 

[Cumulative Distribution Function - Wikipedia](https://en.wikipedia.org/wiki/Cumulative_distribution_function) 
 
### 3. Dağılımın Karakterini Anlamak: Ortalama ve Varyans

Her manzara (dağılım) farklıdır. Onları tanımlamak için iki temel ölçütümüz var:

* **Ortalama (Mean / Expected Value, $\mu$):**
    * **Metafor (Denge Noktası):** Manzara şeklini bir kartondan kestiğinizi hayal edin. Ortalama ($\mu$), bu kartonu parmağınızın ucunda **dengeleyebileceğiniz** noktadır. Dağılımın "ağırlık merkezidir".

* **Varyans ve Standart Sapma ($\sigma^2$ ve $\sigma$):**
    * **Metafor (Manzaranın Yayılımı):** Bu değerler, manzaranın ne kadar **yayvan** veya ne kadar **sivri** olduğunu anlatır.
    * **Düşük Standart Sapma:** Değerler ortalamaya çok yakındır. Manzaramız sivri ve dar bir tepe gibidir (örneğin Fuji Dağı). Herkesin boyu birbirine çok yakınsa standart sapma düşük olur.
    * **Yüksek Standart Sapma:** Değerler ortalamadan çok uzağa yayılmıştır. Manzaramız geniş ve basık bir tepe veya yayla gibidir. Sınıfta çok uzun ve çok kısa boylu öğrenciler varsa standart sapma yüksek olur.
 

### 4. Tanışılması Gereken İki Önemli Aile Üyesi

Görsellerde iki popüler dağılım türü tanıtılıyor:

* **1. Düzgün Dağılım (Uniform Distribution):**
---

<img width="353" height="552" alt="image" src="https://github.com/user-attachments/assets/40ae3eea-a0d7-4f2b-8b10-438635bd8c4e" />


   * **Metafor (Mükemmel Düz Bir Plato):** Bu dağılım, belirli bir aralıktaki her sonucun **eşit derecede olası** olduğu durumları tanımlar. PDF grafiği, bir **dikdörtgen** şeklindedir.
   * **Örnek:** Bir bilgisayarın 0 ile 1 arasında rastgele bir sayı üretmesi. 0.2 gelme olasılığı ile 0.8 gelme olasılığı tamamen aynıdır. Hiçbir bölgenin diğerine üstünlüğü yoktur.
      
 **Uniform distribution** may refer to:

* Continuous uniform distribution
* Discrete uniform distribution
* Uniform distribution (ecology)
* Equidistributed sequence

### Sürekli Düzgün Dağılım (Continuous Uniform Distribution)

Bu, istatistikte en yaygın bilinen türdür. Belirli bir aralıktaki (örneğin 0 ile 10 arası) her bir sonucun gerçekleşme olasılığının **tamamen aynı** olduğu durumları ifade eder.

* **Metafor:** Bir otobüsün her saat başı 0 ila 30. dakikalar arasında herhangi bir anda gelebildiğini ve her anın eşit olasılıklı olduğunu düşünün. Durağa rastgele bir zamanda gittiğinizde otobüsün 5. ile 10. dakikalar arasında gelme olasılığı, 20. ile 25. dakikalar arasında gelme olasılığı ile aynıdır.

---

### Kesikli Düzgün Dağılım (Discrete Uniform Distribution)

Bu, **sayılabilir** sayıda ve sonlu olan her bir sonucun gerçekleşme olasılığının eşit olduğu durumları tanımlar.

* **Metafor:** Hilesiz bir zarı attığınızda 1, 2, 3, 4, 5 veya 6 gelme olasılıklarının hepsi birbirine eşittir (1/6). Sonuçlar belirli ve ayrı değerlerdir.

---

### Düzgün Dağılım (Ekoloji)

Bu terim, istatistiksel bir kavram değil, **ekolojik** bir gözlemdir. Bir popülasyondaki bireylerin bir yaşam alanı üzerinde nasıl yayıldığını ifade eder.

* **Açıklama:** Düzgün dağılım, bireylerin birbirinden **eşit uzaklıklarda** bulunduğu bir yerleşim düzenidir. Bu durum genellikle bireyler arası rekabetin (örneğin kaynaklar veya alan için) yüksek olduğu durumlarda görülür.
* **Örnek:** Kendi bölgelerini savunan penguenlerin yuvaları veya su için rekabet eden çöl bitkileri genellikle düzgün bir dağılım sergiler. 🐧

---

### Dengeli Dağılımlı Dizi (Equidistributed Sequence)

Bu, daha çok matematik ve sayı teorisiyle ilgili bir kavramdır. Bir aralıktaki sayıların oluşturduğu bir dizinin, o aralığı ne kadar **"adil" veya "eşit"** bir şekilde doldurduğunu ifade eder.

* **Açıklama:** Basitçe, bir dizideki elemanlar ilerledikçe, herhangi bir alt aralığa düşen eleman sayısının, o aralığın uzunluğuyla orantılı hale gelmesidir. Yani dizi, zamanla aralığın her yerine **eşit bir şekilde yayılır**.

### Düzgün Dağılım Kavramları Karşılaştırma Tablosu

| Kavram | Alan | Temel Fikir | Veri Tipi / Yapı | Örnek / Metafor |
| :--- | :--- | :--- | :--- | :--- |
| **Sürekli Düzgün Dağılım** | İstatistik | Belirli bir aralıktaki her sonucun olasılığı eşittir. | Sürekli (ölçülebilir) aralık | Bir otobüsün 0-30 dk. arasında herhangi bir anda gelmesi. |
| **Kesikli Düzgün Dağılım** | İstatistik | Sonlu sayıdaki her bir ayrık sonucun olasılığı eşittir. | Kesikli (sayılabilir) değerler | Hilesiz bir zar atışı (1, 2, 3, 4, 5, 6). |
| **Düzgün Dağılım (Ekoloji)** | Ekoloji | Bireylerin bir alanda birbirinden eşit uzaklıkta yayılması. | Coğrafi / Fiziksel alan | Rekabet nedeniyle eşit aralıklı penguen yuvaları. 🐧 |
| **Dengeli Dağılımlı Dizi** | Matematik | Bir dizinin elemanlarının bir aralığı adil ve orantılı olarak doldurması. | Sayı dizisi (sequence) | Dizinin zamanla aralığın her yerine eşit yayılması. |

* **2. Normal Dağılım (Gaussian Distribution):**
  
  ---
    * **Metafor (Çan Eğrisi Tepesi):** Doğada ve sosyal bilimlerde en sık karşılaşılan dağılımdır. Simetrik bir **çan** şeklindedir.
    * **Özellikleri:** Değerlerin çoğu ortalama ($\mu$) etrafında toplanır. Ortalamadan uzaklaştıkça bu değerlerin görülme sıklığı hızla azalır.
    * **Örnek:** İnsanların boyları, zeka seviyeleri (IQ), ölçüm hataları. Çoğu insan ortalama boydadır; çok uzun veya çok kısa insanlar çok daha azdır.
 
  | Özellik | Kesikli Dağılım (Bilye Torbası) | Sürekli Dağılım (Su Bardağı) |
| :--- | :--- | :--- |
| **Veri Türü** | Sayılabilir (1, 2, 3...) | Ölçülebilir (1.5, 2.71, ...) |
| **Olasılık Fonk.** | PMF (Olasılık Kütle Fonksiyonu) | PDF (Olasılık Yoğunluk Fonksiyonu) |
| **Grafik** | Çubuk Grafik | Sürekli Eğri |
| **Tek Nokta Olasılığı**| `$P(X = c) > 0$` (Anlamlıdır) | `$P(X = c) = 0$` (Anlamsızdır) |
| **Aralık Olasılığı**| `$P(a \le X \le b)$` (Noktalar toplanır) | `$P(a \le X \le b)$` (Eğri altındaki alan) |
| **Örnekler** | Zar atışı, müşteri sayısı | Boy, kilo, sıcaklık, zaman |


 ---

 ## Olasılığın İki Farklı Dünyası: Kesikli ve Sürekli ( MINI-ÖZET)

Olasılık dünyası, ölçülen verinin doğasına göre iki ana krallığa ayrılır. Temel ayrım, değerlerin **sayılabilir** mi yoksa **ölçülebilir** mi olduğudur.

---

### 1. Kesikli (Discrete) Dünya

* **Metafor:** Bilye Torbası
* **Temel Fikir:** Değerler arasında geçiş yoktur. Sonuçlar yalnızca belirli, ayrı ve sayılabilir değerler alabilir.
    * *Örnek: Bir torbada sadece kırmızı ve mavi bilyeler vardır; "yarı kırmızı" bir bilye yoktur.*
* **Veri Tipi:** Genellikle tam sayılarla ifade edilir.
    * *Örnekler: Atılan bir zarın sonucu (1, 2, 3, 4, 5, 6), bir saatte gelen müşteri sayısı (10, 11, 12).*
* **Olasılık Sorusu:** "Bir olayın **tam olarak** gerçekleşme olasılığı nedir?" sorusu anlamlıdır.
    * *Örnek: `$P(\text{Zar} = 3)$` (Zarın tam 3 gelme olasılığı)*

### 2. Sürekli (Continuous) Dünya

* **Metafor:** Su Bardağı
* **Temel Fikir:** İki değer arasında sonsuz sayıda başka değer bulunabilir. Değerler bir aralık boyunca kesintisiz bir şekilde akar.
    * *Örnek: Bardaktaki su miktarı 150ml ile 151ml arasında herhangi bir değer olabilir (150.1, 150.11, 150.112...).*
* **Veri Tipi:** Genellikle bir aralıktaki reel sayılarla ifade edilir.
    * *Örnekler: Bir kişinin boyu, bir odanın sıcaklığı, bir işin tamamlanma süresi.*
* **Olasılık Sorusu:** "Bir sonucun **belirli bir aralıkta** olma olasılığı nedir?" sorusu anlamlıdır.
    * *Örnek: `$P(175 \le \text{Boy} \le 176)$` (Boyun 175cm ile 176cm arasında olma olasılığı).*

> **Önemli Not:** Tek bir noktanın olasılığı sıfır kabul edilir, çünkü sonsuz olasılık içinde tek bir noktayı tam isabet ettirmek imkansızdır.
