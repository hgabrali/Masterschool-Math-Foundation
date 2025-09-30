# Z-score

[Normal Distribution_Z-score-Codes](https://colab.research.google.com/drive/1jOaCghd9WhzMZOFUEfcvxxHEBH0Yo1h5#scrollTo=YUu0BJve-orF)

<img width="774" height="663" alt="image" src="https://github.com/user-attachments/assets/3c899346-e388-4fb0-81cc-d98e1923763f" />

<img width="729" height="274" alt="image" src="https://github.com/user-attachments/assets/d0dca09a-14ee-46f9-8c03-5e54965007a6" />

<img width="680" height="130" alt="image" src="https://github.com/user-attachments/assets/e94e8cb1-ec92-4550-afa7-78834e638b5b" />

---

## Genel Bakış: Z-Skoru Nedir? (Veri Dünyasının Evrensel Cetveli)

En basit haliyle Z-Skoru, bir veri noktasına **bağlam kazandıran** sihirli bir araçtır. Tek başına bir skorun (örneğin bir sınav notunun) ne kadar iyi veya kötü olduğunu anlamak zordur. Z-Skoru bize bu skorun, ait olduğu grubun geri kalanına kıyasla nerede durduğunu gösterir.

> **Ana Metafor:** Z-Skorunu, farklı dilleri konuşan veriler için bir **evrensel tercüman** veya farklı ölçü birimlerini (inç, santimetre, kg, libre) tek bir standarda getiren **evrensel bir cetvel** gibi düşünebiliriz.

---

### Bölüm 1: Z-Skorunun Anatomisi (Veri Noktanızın GPS Koordinatları)

Z-Skoru, bir veri noktasının, grubun ortalamasından **kaç standart sapma uzakta olduğunu** söyler. Bu, onun veri dağılımı haritasındaki tam konumunu verir.

#### Formülün Anlamı
$$
z = \frac{x - \mu}{\sigma}
$$
Bu formülü bir yol tarifi gibi düşünelim:

* **$(x - \mu)$:** "Hedefim (`x`), başlangıç noktasından (ortalama, $\mu$) ne kadar uzakta?" Bu, ham mesafeyi verir.
* **/ $\sigma$ :** "Bu mesafeyi, standart adım büyüklüğüyle (standart sapma, $\sigma$) ölç." Bu, mesafeyi standart bir birime çevirir.

#### Z-Skorunun Yorumlanması

* **Pozitif Z-Skoru (+):** Veri noktası, ortalamanın **üzerindedir**. (Haritada merkezin sağında).
* **Negatif Z-Skoru (-):** Veri noktası, ortalamanın **altındadır**. (Haritada merkezin solunda).
* **Z-Skoru = 0:** Veri noktası, **tam olarak ortalamadadır**. (Haritanın tam merkezinde).

Örneğin, bir Z-Skorunun **+2.0** olması, o veri noktasının ortalamadan tam olarak 2 standart sapma yukarıda olduğunu gösterir ve bu oldukça iyi bir sonuçtur!

---

### Bölüm 2: Z-Skorunun Süper Güçleri (Uygulama Alanları)

Görsellerde Z-Skorunun üç temel süper gücü vurgulanıyor. Gelin bunları karşılaştırmalı olarak inceleyelim.

#### 1. Süper Güç: Elmalarla Armutları Karşılaştırmak (Farklı Veri Setlerini Kıyaslama)

* **Problem:** Ali, Fizik sınavından 80 aldı. Ayşe ise Edebiyat sınavından 90 aldı. Kim daha başarılı? Sadece notlara bakarak karar veremeyiz çünkü sınavların zorlukları farklı olabilir.
* **Z-Skoru Çözümü:** Her öğrencinin notunu, kendi sınıfının ortalamasına ve standart sapmasına göre "standart bir başarı puanına" çeviririz.

| Öğrenci | Sınav | Notu ($x$) | Sınıf Ortalaması ($\mu$) | Standart Sapma ($\sigma$) | Z-Skoru Hesabı | Sonuç |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Ali** | Fizik | 80 | 70 | 5 | `$z = \frac{80 - 70}{5}$` | **+2.0** |
| **Ayşe** | Edebiyat| 90 | 85 | 10 | `$z = \frac{90 - 85}{10}$` | **+0.5** |

* **Karar:** Ali'nin Z-Skoru (+2.0), Ayşe'nin Z-Skorundan (+0.5) çok daha yüksek. Bu demektir ki Ali, kendi sınıfına göre **çok daha üstün bir başarı** göstermiştir. Z-Skoru, elmalarla armutları "**standart başarı meyvesi**"ne dönüştürerek adil bir kıyaslama yapmamızı sağladı.

---

#### 2. Süper Güç: Kalabalıktaki Aykırıları Tespit Etmek (Aykırı Değer Tespiti)

* **Problem:** Bir veri setinde, genel eğilime uymayan ve analizimizi yanıltabilecek "garip" veya "aşırı" değerler var mı?
* **Z-Skoru Çözümü:** Her veri noktasının Z-Skorunu hesaplarız.
* **Metafor:** Veri setini bir kalabalık olarak düşünün. Çoğu insan ortalama boydadır (Z-Skorları -2 ile +2 arasındadır). Ancak biri olağanüstü uzun veya kısaysa hemen göze çarpar.
* **Pratik Kural:** Genellikle mutlak değeri 3'ten büyük olan Z-Skorları (`$z > 3$` veya `$z < -3$`) aykırı değer olarak kabul edilir. Çünkü bir veri noktasının ortalamadan 3 standart sapmadan daha fazla uzaklaşması **çok nadir bir durumdur** (%99.7'si bu aralıktadır).

---

#### 3. Süper Güç: Veriyi Terbiye Etmek (Makine Öğrenmesi için Standardizasyon)

* **Problem:** Makine öğrenmesi algoritmaları, özellikle mesafeye dayalı olanlar (k-NN, SVM gibi), farklı ölçeklerdeki verilerden olumsuz etkilenir. Örneğin, bir veri özelliği maaşı (örn: 50,000-150,000 aralığında), diğeri ise tecrübe yılını (örn: 1-20 aralığında) temsil ediyorsa, algoritma büyük sayılara sahip olan maaş özelliğine **daha fazla ağırlık verme** eğiliminde olur.
* **Z-Skoru Çözümü:** Tüm veri özelliklerini Z-Skoruna dönüştürerek standardize ederiz. Bu işleme "**Standardizasyon**" denir.
* **Metafor:** Farklı spor dallarından (örneğin halter ve maraton) gelen sporcuları tek bir etkinlikte yarıştırmak gibidir. Doğrudan karşılaştıramazsınız. Ama her birinin kendi branşındaki performansını Z-Skoruna çevirirseniz, kimin göreceli olarak daha iyi bir atlet olduğunu anlayabilirsiniz. Standardizasyon, tüm veri özelliklerini aynı "**yarış pistine**" getirerek adil bir modelleme ortamı sağlar.

#### Özet Tablo: Z-Skorunun Kullanım Alanları

| Uygulama Alanı | Çözdüğü Problem | Metafor |
| :--- | :--- | :--- |
| **Farklı Veri Setlerini Kıyaslama** | Farklı ölçek ve bağlamdaki değerleri nasıl adil karşılaştırabilirim? | Elmalarla Armutları Karşılaştırmak |
| **Aykırı Değer Tespiti** | Veri setimdeki olağandışı veya "garip" noktaları nasıl bulabilirim? | Kalabalıktaki Aykırıları Bulmak |
| **Veri Standardizasyonu (ML)** | Farklı ölçeklerdeki özelliklerin modelimi domine etmesini nasıl engellerim? | Veriyi Aynı Yarış Pistine Getirmek |

---
