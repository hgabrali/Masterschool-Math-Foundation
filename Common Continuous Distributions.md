# Common Continuous Distributions

<img width="675" height="127" alt="image" src="https://github.com/user-attachments/assets/5c7f654b-273e-4aaa-9c2b-145f04d2d757" />


<img width="858" height="673" alt="image" src="https://github.com/user-attachments/assets/586ed94c-117e-4198-aa88-0b28244ddaa5" />

<img width="580" height="368" alt="image" src="https://github.com/user-attachments/assets/828ec00d-d78a-442e-8114-1d81e900c0ea" />

<img width="778" height="308" alt="image" src="https://github.com/user-attachments/assets/5298fb09-c902-4f51-a9c0-059da9c8e52d" />

<img width="789" height="517" alt="image" src="https://github.com/user-attachments/assets/d7c6694d-b933-4c94-82cf-4df668e83423" />


<img width="558" height="263" alt="image" src="https://github.com/user-attachments/assets/d34fe46d-0771-40b3-b7fc-70b58c2cc966" />

<img width="501" height="335" alt="image" src="https://github.com/user-attachments/assets/f8d02573-6a0f-45ec-993a-d5b41d407ea4" />

<img width="791" height="248" alt="image" src="https://github.com/user-attachments/assets/e489ca37-c5dc-48d2-8961-b83ef955fccd" />

---


# Düzgün Dağılım (Uniform Distribution) ve Üstel Dağılım (Exponential Distribution)

## Genel Bakış: İki Farklı Rastgelelik Hikayesi

Bu iki dağılımı, rastgele olayları anlatan iki farklı hikaye anlatıcısı gibi düşünebiliriz:

* **Düzgün Dağılım:** Bu anlatıcı, "Belirlenen sınırlar içinde her şey olabilir ve her sonucun şansı tamamen eşittir" der. Tam bir **eşitlik ve belirsizlik** hikayesidir.
* **Üstel Dağılım:** Bu anlatıcı ise, "Bir sonraki olayın *her an* olması muhtemeldir, ancak en çok *hemen şimdi* olması olasıdır" der. Bu, bir **bekleyiş ve aciliyet** hikayesidir.

---

### Bölüm 1: Düzgün Dağılım – "Adil Fırsatlar Dünyası"

Bu dağılım, en basit ve en öngörülemez rastgelelik türüdür.

* **Metafor:** Düzgün dağılımı, mükemmel bir şekilde karıştırılmış bir **tombala torbası** veya **kusursuz bir piyango makinesi** gibi düşünün. Belirli bir aralıktaki (örneğin 1'den 100'e kadar) her bir topun çekilme olasılığı kesinlikle aynıdır. 5 gelmesi ne kadar olasıysa, 95 gelmesi de o kadar olasıdır.

* **Ne Zaman Kullanılır?** Bir olayın belirli sınırlar ($a$ ve $b$) içinde gerçekleşeceğini bildiğiniz, ancak bu sınırlar içinde herhangi bir sonuca öncelik vermek için hiçbir nedeninizin olmadığı durumları modellemek için kullanılır.

* **Görsel Hikayesi (PDF Grafiği):** Grafiği bir **dikdörtgen** veya **düz bir platodur**. Bu platonun yüksekliği ($\frac{1}{b-a}$) tüm aralık boyunca sabittir. Bu, olasılığın aralığın her noktasına "adil" bir şekilde dağıtıldığı anlamına gelir.

* **Örnek Senaryo:** Bir bilgisayarın 0 ile 1 arasında rastgele bir sayı üretmesi. Veya bir otobüsün durağa saat 10:00 ile 10:10 arasında herhangi bir anda gelebileceğini ve bu aralıktaki her saniyenin eşit olasılıklı olduğunu varsaymak.

---

### Bölüm 2: Üstel Dağılım – "Her An Olabilir Dünyası"

Bu dağılım, olaylar arasındaki **bekleme süresini** modellemek için kullanılır ve Düzgün Dağılımın tam tersi bir mantığa sahiptir.

* **Metafor:** Üstel dağılımı, yoğun bir caddede **boş bir taksi beklemek** gibi düşünün. En olası senaryo, bir taksinin *hemen şimdi* veya çok kısa bir süre içinde geçmesidir. 5 dakika bekledikten sonra hala taksi geçmediyse, umudunuzu yitirmeye başlarsınız. 30 dakika sonra bir taksinin geçme olasılığı oldukça düşüktür.

* **Ne Zaman Kullanılır?** Olayların sabit bir ortalama oranda gerçekleştiği bir süreçte, bir sonraki olaya kadar geçecek süreyi modellemek için kullanılır.
    * Bir web sitesine bir sonraki kullanıcının gelmesine kadar geçecek süre.
    * Bir ampulün patlamasına kadar geçecek ömür.
    * Bir müşteri hizmetleri temsilcisinin bir sonraki çağrıyı almasına kadar geçen süre.

* **Görsel Hikayesi (PDF Grafiği):** Grafiği, yüksek bir noktadan başlayıp hızla aşağı inen bir **kaydırak** gibidir. En yüksek noktası sıfırdadır, çünkü bekleme süresinin kısa olma olasılığı en yüksektir. Bekleme süresi uzadıkça, olasılık (eğrinin yüksekliği) hızla sıfıra yaklaşır.

* **Anahtar Karakter: Lambda ($\lambda$):** Bu dağılımın kaderini **oran parametresi** olan Lambda ($\lambda$) belirler. $\lambda$, bir zaman biriminde olayın ne sıklıkla gerçekleştiğini gösterir.
    * **Yüksek $\lambda$:** Olaylar sık olur (örneğin, yoğun bir kafeye dakikada 3 müşteri gelir). Bekleme süresi kısadır, bu yüzden kaydırak **çok diktir**.
    * **Düşük $\lambda$:** Olaylar nadirdir (sakin bir kütüphaneye saatte 2 kişi gelir). Bekleme süresi uzundur, bu yüzden kaydırak **daha yatıktır**.

* **Hafızasızlık Özelliği (Memorylessness):** Bu, Üstel Dağılımın en ilginç ve karşı-sezgisel özelliğidir. "Geçmişin önemi yoktur" der.
    * **Örnek:** Ortalama ömrü 1000 saat olan bir ampul düşünün. Eğer bu ampul 800 saattir yanıyorsa, "yorulduğu" için yakında patlama olasılığının daha yüksek olduğunu düşünebilirsiniz. Ancak Üstel Dağılıma göre bu yanlıştır! Ampulün "hafızası" yoktur. 800 saattir yanıyor olması, önümüzdeki 100 saat daha yanma olasılığını, sıfır kilometre bir ampulün ilk 100 saat yanma olasılığından farklı kılmaz.
 
  #### Karşılaştırmalı Özet Tablosu

| Özellik | Düzgün Dağılım (Uniform) | Üstel Dağılım (Exponential) |
| :--- | :--- | :--- |
| **Metafor** | Adil Fırsatlar / Kusursuz Piyango | Her An Olabilir / Taksi Bekleme Oyunu |
| **Cevapladığı Soru** | "Bu aralıkta herhangi bir sonucun olasılığı nedir?" | "Bir sonraki olaya kadar ne kadar beklemem gerekecek?" |
| **PDF Grafiği** | **Dikdörtgen** (Olasılık sabit) | **Kaydırak** (Olasılık zamanla azalır) |
| **Ana Parametre(ler)**| Başlangıç ($a$) ve Bitiş ($b$) noktaları | Oran Parametresi ($\lambda$) |
| **Örnek Senaryo** | 0-100 arasında rastgele sayı seçimi. | Bir sonraki depreme kadar geçecek süre. |
| **Hafıza?** | Uygulanamaz | **Hafızasızdır** (Geçmiş, geleceği etkilemez) |

