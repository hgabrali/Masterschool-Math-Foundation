# 🔥Hypothesis Testing🔥

[Hypothesis Testing](https://colab.research.google.com/drive/1jA3-u4knu5kqdVWQ80fTSATXWe6nOwsb#scrollTo=OdfNyUqrWr6K)

### Hipotez Testi Süreci Karşılaştırma Tablosu (Tek Örneklemli t-Testi)

* **Ana Metafor:** İstatistiksel bir hipotez testini, bir **mahkeme salonu duruşması** gibi düşünebiliriz. Bir iddia var ve biz bu iddiayı elimizdeki kanıtlara (verilere) dayanarak yargılıyoruz.

* **Örnek Senaryo:** Bir cips firması, paketlerinin ortalama **500 gr** olduğunu iddia ediyor ($H_0$). Biz şüpheleniyoruz ve 10 paketten oluşan bir örneklem alıyoruz.

### Hipotez Testi Süreci Karşılaştırma Tablosu (Tek Örneklemli t-Testi)

**Ana Metafor:** İstatistiksel bir hipotez testini, bir **mahkeme salonu duruşması** gibi düşünebiliriz. Bir iddia var ve biz bu iddiayı elimizdeki kanıtlara (verilere) dayanarak yargılıyoruz.
**Örnek Senaryo:** Bir cips firması, paketlerinin ortalama **500 gr** olduğunu iddia ediyor ($H_0$). Biz şüpheleniyoruz ve 10 paketten oluşan bir örneklem alıyoruz.

| Kavram | Tanım | Metafor (Mahkeme Analojisi) | Örnek (Cips Paketi) | Pratik Anlamı ve Yorumu |
| :--- | :--- | :--- | :--- | :--- |
| **t-İstatistiği** | Örneklem ortalamasının, hipotez edilen popülasyon ortalamasından kaç standart hata uzakta olduğunu gösteren bir skordur. `$t = \frac{\bar{x} - \mu_0}{s / \sqrt{n}}$` | **Kanıtın Ağırlığı Skoru** | Örneklem ortalamamız 505 gr çıktı. Hesaplanan t-istatistiği **+2.5** olsun. | "Bulduğumuz sonuç (505 gr), iddia edilen değerden (500 gr) **2.5 standart hata birimi** uzakta. Bu fark ne kadar anlamlı?" sorusunu sayısallaştırır. |
| **Serbestlik Derecesi (df)** | Bir hesaplamada serbestçe değişebilen değerlerin sayısıdır. t-testi için `$n-1$` olarak hesaplanır. | **Jüri Deneyimi/Büyüklüğü** | 10 paketimiz olduğu için, `df = 10 - 1 = 9`'dur. | Testin hassasiyetini belirler. Düşük `df`, küçük örneklemden kaynaklanan daha fazla belirsizlik anlamına gelir ve bu da t-dağılımının şeklini etkiler. |
| **p-değeri (p-value)**| Sıfır hipotezi doğruyken, en az bizimki kadar aşırı bir test istatistiği gözlemleme olasılığıdır. | **Masumiyet Altında Şaşırtıcılık Olasılığı** | `t=2.5` ve `df=9` için p-değeri **0.034** olsun. | "Eğer cips paketleri gerçekten ortalama 500 gr olsaydı, bizimki gibi bir örneklemle karşılaşma olasılığımız sadece **%3.4** olurdu. Bu oldukça şaşırtıcı bir durum." |
| **Karar Verme (`$p \le \alpha$`)** | p-değeri, önceden belirlenen anlamlılık düzeyi ($\alpha$) ile karşılaştırılır. | **Yargıcın Kararı** | Anlamlılık düzeyimiz `$\alpha = 0.05$` olsun. `$p=0.034 < \alpha=0.05$` olduğu için `$H_0$`'ı reddederiz. | p-değeri, belirlediğimiz risk eşiğinden düşükse, sonuçlarımızın şans eseri olmadığına karar veririz ve iddiayı (örn: paketlerin 500 gr olduğu) reddederiz. |
| **Tip I Hata** | Gerçekte doğru olan bir sıfır hipotezini reddetmek. | **Masum Birini Mahkum Etmek** 😱 | Fabrika aslında doğru üretim yapıyordu ama bizim örneklemimiz şans eseri ağır paketlerden oluştu ve biz "paketler 500 gr değil" diye yanlış karar verdik. | Bu hatayı yapma olasılığı `$\alpha$`'ya eşittir. `$\alpha=0.05$` seçerek, bu tür bir hata yapma riskini **%5** olarak kabul etmiş oluruz. |
| **Tip II Hata**| Gerçekte yanlış olan bir sıfır hipotezini reddedememek. | **Suçlu Birini Serbest Bırakmak** | Fabrika gerçekten de 505 gr'lık paketler üretiyordu, ancak bizim örneklemimiz şans eseri hafif geldi ve bu sorunu tespit edemedik. | Yeterli kanıt (genellikle küçük örneklem boyutu nedeniyle) bulamadığımız için gerçek bir etkiyi veya farkı **gözden kaçırmak** anlamına gelir. |

---

**Sıfır Hipotezi ($H_0$)** ve **Alternatif Hipotez ($H_a$ veya $H_1$)**, istatistiksel bir iddianın test edildiği bir hipotez testinin temelini oluşturan iki rakip beyandır.

Gelin bu iki kavramı, metaforlar ve karşılaştırmalarla detaylı bir şekilde inceleyerek bir özet tablosu oluşturalım.

### Ana Metaforlar: Mahkeme Duruşması ve Tıbbi Teşhis

Bu iki hata türünü anlamak için iki güçlü metafor kullanacağız:

* **Mahkeme Duruşması:** Bir sanığın suçlu olup olmadığına karar verdiğimiz bir senaryo.
    * **Sıfır Hipotezi ($H_0$):** "Sanık masumdur."
* **Tıbbi Teşhis:** Bir hastanın belirli bir hastalığa sahip olup olmadığına karar verdiğimiz bir senaryo.
    * **Sıfır Hipotezi ($H_0$):** "Hasta sağlıklıdır."

---

### Tip I Hata: Masum Birini Mahkum Etmek (Yalancı Pozitif)

* **Tanım:**
  Gerçekte **doğru** olan bir sıfır hipotezini ($H_0$) **reddetmektir**. Yani, ortada bir etki veya fark yokken, "bir etki var" diye yanlış bir sonuca varmaktır.

* **Metaforlarla Açıklama:**
    * **Mahkeme Metaforu:**
        > Bu, **masum birini suçlu bulup hapse atmaktır** 😱. Duruşma sistemindeki en ciddi hata olarak kabul edilir. Elimizdeki kanıtlar bizi yanıltmış ve masumiyet varsayımını haksız yere çürütmüşüzdür.
    * **Tıbbi Teşhis Metaforu:**
        > Bu, **sağlıklı bir insana "hastasın" demektir (Yalancı Pozitif - False Positive)**. Bu teşhis, kişiyi gereksiz strese, masrafa ve hatta zararlı tedavilere maruz bırakabilir.

* **Olasılığı: Alfa ($\alpha$)**
  Bir Tip I hata yapma olasılığı, bizim en başta belirlediğimiz **anlamlılık düzeyine ($\alpha$)** eşittir. Eğer testimizi `$\alpha = 0.05$` ile yapıyorsak, en başından **%5 oranında masum birini mahkum etme riskini** kabul etmiş oluruz. `$\alpha$` değerini düşürerek bu riski azaltabiliriz.

* **Örnek Sonuç:**
  İşe yaramayan bir ilacın "etkili" olduğu sonucuna varılarak piyasaya sürülmesi.

---

### Tip II Hata: Suçlu Birini Serbest Bırakmak (Yalancı Negatif)

* **Tanım:**
  Gerçekte **yanlış** olan bir sıfır hipotezini ($H_0$) **reddedememektir**. Yani, ortada gerçek bir etki veya fark varken, bunu tespit etmek için yeterli kanıt bulamayıp "bir etki yoktur" sonucuna varmaktır.

* **Metaforlarla Açıklama:**
    * **Mahkeme Metaforu:**
        > Bu, **suçlu birini delil yetersizliğinden serbest bırakmaktır**. Sanık aslında suçludur, ama elimizdeki kanıtlar onu mahkum etmeye yetmemiştir.
    * **Tıbbi Teşhis Metaforu:**
        > Bu, **hasta bir insana "sağlıklısın, bir şeyin yok" demektir (Yalancı Negatif - False Negative)**. Bu teşhis, hastalığın ilerlemesine ve tedavi şansının kaçırılmasına neden olabileceği için çok tehlikelidir.

* **Olasılığı: Beta ($\beta$)**
  Bir Tip II hata yapma olasılığı **Beta ($\beta$)** ile gösterilir. Testin **gücü (power)** ise `$1 - \beta$`'dır ve gerçek bir etkiyi doğru bir şekilde tespit etme yeteneğini ölçer.

* **Örnek Sonuç:**
  Gerçekten işe yarayan bir kanser ilacının, testlerde "etkisiz" bulunarak rafa kaldırılması.

---

### İki Hata Arasındaki Denge

Bu iki hata arasında bir **ödünleşme (trade-off)** vardır:

* **Mahkeme Metaforu:** Masum birini hapse atmamak için kanıt standardını (`$\alpha$`yı düşürerek) çok yükseltirseniz, suçluların delil yetersizliğinden serbest kalma ihtimalini (Tip II hatayı) artırırsınız.
* **Çözüm:** Her iki hata türünü de aynı anda azaltmanın tek yolu, daha fazla ve daha iyi kanıt toplamaktır, yani **örneklem boyutunu artırmaktır**.

  

# One-Tailed and Two-Tailed Tests konusunu türkce olarak metaforlu ve tablolu aciklayacagiz.

# Significance Level konusunu türkce olarak metaforlu ve tablolu aciklayacagiz.

# P-value konusunu türkce olarak metaforlu ve tablolu aciklayacagiz.






---

<img width="739" height="409" alt="image" src="https://github.com/user-attachments/assets/fda9cdcc-a641-43d5-82cd-2cf633c9f710" />


<img width="761" height="682" alt="image" src="https://github.com/user-attachments/assets/45d003ed-6fa1-4ef2-85e4-4771654441b7" />

<img width="724" height="546" alt="image" src="https://github.com/user-attachments/assets/3c536c3f-895c-4052-949a-4c9b3fb4f19e" />


<img width="808" height="554" alt="image" src="https://github.com/user-attachments/assets/9532b805-66ba-46c1-9f80-008d72fd8501" />

<img width="875" height="550" alt="image" src="https://github.com/user-attachments/assets/acb6ce7c-b1cb-4f2a-9266-65f3c95d18a7" />

<img width="777" height="550" alt="image" src="https://github.com/user-attachments/assets/2f714f6d-8ac0-410e-b101-7e671f2fddba" />

<img width="782" height="369" alt="image" src="https://github.com/user-attachments/assets/e99e16c5-4027-4128-bc56-41998836e134" />

<img width="845" height="462" alt="image" src="https://github.com/user-attachments/assets/333bab45-d349-421c-9764-52dc94be8806" />

<img width="779" height="578" alt="image" src="https://github.com/user-attachments/assets/f5714dbd-c2cd-4c6b-be5c-2737582ded18" />

<img width="697" height="233" alt="image" src="https://github.com/user-attachments/assets/22c2064e-3396-4dc8-a523-767c8e54fb10" />

---





