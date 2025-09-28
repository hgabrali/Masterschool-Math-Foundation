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

<img width="537" height="185" alt="image" src="https://github.com/user-attachments/assets/68c6bc6f-c3df-41fc-b899-4a6461e8bf00" />

<img width="580" height="299" alt="image" src="https://github.com/user-attachments/assets/0c12edc1-a32e-4a77-a520-45bece9a8c6e" />

<img width="514" height="281" alt="image" src="https://github.com/user-attachments/assets/5714b95e-92dc-4fda-8733-bbdbb57146c3" />

<img width="752" height="791" alt="image" src="https://github.com/user-attachments/assets/61211b37-7e29-437a-99cd-8afaa42c6e75" />

**Sıfır Hipotezi ($H_0$)** ve **Alternatif Hipotez ($H_a$ veya $H_1$)**, istatistiksel bir iddianın test edildiği bir hipotez testinin temelini oluşturan iki rakip beyandır.

Gelin bu iki kavramı, metaforlar ve karşılaştırmalarla detaylı bir şekilde inceleyerek bir özet tablosu oluşturalım.

### Ana Metaforlar: Mahkeme Duruşması ve Tıbbi Teşhis

Bu iki hata türünü anlamak için iki güçlü metafor kullanacağız:

* **Mahkeme Duruşması:** Bir sanığın suçlu olup olmadığına karar verdiğimiz bir senaryo.
    * **Sıfır Hipotezi ($H_0$):** "Sanık masumdur."
* **Tıbbi Teşhis:** Bir hastanın belirli bir hastalığa sahip olup olmadığına karar verdiğimiz bir senaryo.
    * **Sıfır Hipotezi ($H_0$):** "Hasta sağlıklıdır."

---
# Tip I Hata & Tip II Hata:

<img width="576" height="280" alt="image" src="https://github.com/user-attachments/assets/912b842b-f0c3-42c3-acfe-553a652a237f" />

<img width="676" height="358" alt="image" src="https://github.com/user-attachments/assets/26b9bc02-c0ed-4535-9d4a-8b95e11772b7" />


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

  #### Karşılaştırmalı Özet Tablosu

| Özellik | Tip I Hata | Tip II Hata |
| :--- | :--- | :--- |
| **Diğer Adı** | **Yalancı Pozitif** (False Positive) | **Yalancı Negatif** (False Negative) |
| **Tanım** | Doğru `$H_0$`'ı reddetmek. | Yanlış `$H_0$`'ı reddedememek. |
| **Mahkeme Metaforu** | **Masum Birini Mahkum Etmek** | **Suçlu Birini Serbest Bırakmak** |
| **Tıbbi Teşhis Metaforu**| Sağlıklı kişiye "hastasın" demek. | Hasta kişiye "sağlıklısın" demek. |
| **Bizim Kararımız** | "Bir etki/fark var!" | "Bir etki/fark olduğuna dair yeterli kanıt yok." |
| **Gerçek Durum** | Aslında bir etki/fark yoktu. | Aslında bir etki/fark vardı. |
| **Olasılığı** | $\alpha$ (Anlamlılık Düzeyi) | $\beta$ (Beta) |
| **Nasıl Kontrol Edilir?** | `$\alpha$` değerini düşürerek azaltılır. | Örneklem boyutunu artırarak azaltılır. |

---

En yaygın dijital pazarlama senaryolarından biri olan **A/B Testi** üzerinden Tip I ve Tip II Hataları incelemesi:

---

### Senaryo: "Sepete Ekle" Buton Rengini Değiştirmek 🎨

Bir e-ticaret siteniz olduğunu ve "Sepete Ekle" butonunun rengini mevcut **mavi** renkten, daha dikkat çekici olduğunu düşündüğünüz **yeşil** bir renge çevirmeyi test ettiğinizi varsayalım.

* **Sıfır Hipotezi ($H_0$):**
    > "Buton renginin tıklanma oranına bir etkisi **yoktur**. Yeşil ve mavi butonun performansları arasında bir fark yoktur."
* **Alternatif Hipotez ($H_a$):**
    > "Yeşil buton, tıklanma oranını **değiştirir** (artırır veya azaltır)."

Testi yapıp verileri analiz ettikten sonra varacağınız yanlış kararlar, Tip I ve Tip II hatalar olacaktır.

---

### Tip I Hata: Hayali Bir Başarıyı Kutlamak (Yalancı Pozitif)

* **Tanım:** Gerçekte bir etkisi olmamasına rağmen, test sonucunda "yeni yeşil buton daha iyi çalışıyor" diye yanlış bir karara varmak.

* **Senaryoda Ne Olur?** Test sonucunda yeşil butonun tıklanma oranı, mavi butondan istatistiksel olarak anlamlı derecede yüksek çıkar (düşük p-değeri). `$H_0$`'ı reddeder ve yeşil butonun daha iyi olduğuna karar verirsiniz.

* **Gerçek Durum:** Aslında iki buton arasında hiçbir performans farkı yoktur. Sizin test süreniz boyunca tamamen **şans eseri**, yeşil butonu gören kullanıcılar biraz daha fazla tıklama yapmıştır.

* **Sonuç ve Bedeli (İş Hayatındaki Etkisi):**
    * Bu "hayali" başarıya dayanarak, tüm web sitesindeki "Sepete Ekle" butonlarını yeşile çevirmek için bir karar alırsınız.
    * Tasarımcılar ve yazılımcılar saatlerini/günlerini bu değişikliği uygulamak için harcar.
    * Şirket, bu değişiklikten dolayı satışların artacağını bekler, ancak **beklenen artış asla gerçekleşmez**.
    * **Sonuç:** Kaynaklar (zaman ve para) boşa harcanmış olur.

---

### Tip II Hata: Masadaki Parayı Görmemek (Yalancı Negatif)

* **Tanım:** Yeni yeşil buton gerçekten daha iyi bir performansa sahipken, testin bu farkı tespit edememesi ve "iki buton arasında bir fark yoktur" diye yanlış karara varmak.

* **Senaryoda Ne Olur?** Test sonucunda iki buton arasındaki fark, istatistiksel olarak anlamlı çıkmaz (yüksek p-değeri). `$H_0$`'ı reddedemez ve "bir fark olduğuna dair yeterli kanıt yok" dersiniz.

* **Gerçek Durum:** Yeşil buton, aslında tıklanma oranını **gerçekten de %10 artırmaktadır**, ancak sizin örnekleminiz bu etkiyi net bir şekilde gösterecek kadar büyük veya uzun süreli olmamıştır.

* **Sonuç ve Bedeli (İş Hayatındaki Etkisi):**
    * "İşe yaramıyor" diye düşünüp, sitenin tamamında bu kârlı değişikliği yapmaktan vazgeçersiniz.
    * Düşük performanslı mavi butonu kullanmaya devam edersiniz.
    * Şirket, aslında kolayca elde edebileceği **potansiyel bir gelir artışını kaçırmış olur**.
    * **Sonuç:** Kaçırılmış bir fırsat ve masada bırakılmış bir para demektir.
 
  #### Karşılaştırmalı Özet Tablosu (A/B Testi Örneği)

| Özellik | Tip I Hata (Yalancı Pozitif) | Tip II Hata (Yalancı Negatif) |
| :--- | :--- | :--- |
| **Metafor** | **Hayali Bir Başarıyı Kutlamak** | **Masadaki Parayı Görmemek** |
| **Test Kararımız** | "Yeşil buton daha iyi!" | "Butonlar arasında fark yok." |
| **Gerçek Durum** | Yeşil ve mavi buton arasında fark yoktu. | Yeşil buton aslında daha iyiydi. |
| **Sonuç** | Gereksiz yere kaynak harcanır, beklenen kazanç gelmez. | Potansiyel bir kazanç fırsatı kaçırılır. |
| **Hangi Durumda Olur?**| Genellikle `$\alpha$` (anlamlılık) seviyesi çok esnek tutulduğunda veya tamamen şanssızlık. | Genellikle örneklem boyutu çok küçük olduğunda (testin gücü düşük olduğunda). |



# One-Tailed and Two-Tailed Tests:

<img width="524" height="268" alt="image" src="https://github.com/user-attachments/assets/89db017d-ef88-4589-a6dd-16498d6c9a8e" />

Hipotez testlerinde **Tek Kuyruklu (One-Tailed)** ve **İki Kuyruklu (Two-Tailed)** testler arasındaki farkı anlamak, testinizi doğru bir şekilde kurmanız ve sonuçlarınızı doğru yorumlamanız için kritik öneme sahiptir.

Gelin bu konuyu, metaforlar, karşılaştırmalar ve bir özet tablosuyla detaylı bir şekilde inceleyelim.

---

### Ana Metafor: Güvenlik Görevlisi ve Şüpheli Durum

Bir hipotez testini, önemli bir binanın önünde nöbet tutan bir **güvenlik görevlisi** olarak düşünebiliriz. Görevlinin amacı, "normal durumdan" (Sıfır Hipotezi, $H_0$) sapan "şüpheli durumları" (Alternatif Hipotez, $H_a$) tespit etmektir. Testin tek mi yoksa çift kuyruklu mu olacağı, görevlinin **nereye baktığını** ve **ne tür bir şüpheli durum aradığını** belirler.

---

### 1. İki Kuyruklu Test (Two-Tailed Test) – "Her İki Yöne de Dikkat Et!"

* **Nedir?**
  Örneklem ortalamasının, popülasyon ortalamasından **herhangi bir yönde** (yani daha büyük **veya** daha küçük) anlamlı bir şekilde farklı olup olmadığını test eden yöntemdir.

* **Metafor (Güvenlik Görevlisi):**
  > Görevli, binanın hem **giriş** hem de **çıkış** kapısını aynı anda gözlemekle görevlidir. Onun için şüpheli durum, birinin izinsiz girmesi **ya da** izinsiz çıkmasıdır. Hangi yönde olursa olsun, "normal durumdan" herhangi bir sapma alarmı tetikler.

* **Alternatif Hipotez ($H_a$):**
  Her zaman bir "eşit değildir" (`$\neq$`) işareti içerir.
    * **Örnek:** "Yeni bir öğretim metodunun not ortalaması üzerindeki etkisi, eski metodun ortalamasından **farklıdır**." (`$\mu_{yeni} \neq \mu_{eski}$`). Notların artması da, azalması da bizim için anlamlı bir sonuçtur.

* **Risk Bölgesi ($\alpha$):**
  Belirlediğimiz anlamlılık düzeyi (`$\alpha$`, örn: 0.05), iki kuyruğa **eşit olarak bölünür**. Yani, %2.5'lik risk sol kuyruğa (çok düşük değerler), %2.5'lik risk de sağ kuyruğa (çok yüksek değerler) dağıtılır. Bu, testi daha **muhafazakar** yapar, çünkü aşırı bir sonucun bu küçük bölgelerden birine düşmesi daha zordur.

---

### 2. Tek Kuyruklu Test (One-Tailed Test) – "Tek Bir Yöne Odaklan!"

* **Nedir?**
  Örneklem ortalamasının, popülasyon ortalamasından **sadece belirli bir yönde** (yani **sadece daha büyük** veya **sadece daha küçük**) anlamlı bir şekilde farklı olup olmadığını test eden yöntemdir.

* **Metafor (Güvenlik Görevlisi):**
  > Görevli, artık sadece **"GİRİŞ YASAK"** levhası olan bir çıkış kapısında nöbet tutmaktadır. Onun için tek şüpheli durum, birinin bu kapıdan **içeri girmeye çalışmasıdır**. Birinin dışarı çıkması normaldir ve alarmı tetiklemez. Görevli, tüm dikkatini tek bir yöne odaklamıştır.

* **Alternatif Hipotez ($H_a$):**
  Her zaman bir "büyüktür" (`>`) veya "küçüktür" (`<`) işareti içerir.
    * **Örnek (Sağ Kuyruk Testi):** "Yeni bir gübre, bitki boyunu **artırır**." (`$\mu_{gübreli} > \mu_{gübresiz}$`). Burada bitki boyunun azalmasıyla ilgilenmiyoruz. Sadece artış olup olmadığını test ediyoruz.
    * **Örnek (Sol Kuyruk Testi):** "Yeni bir diyet programı, kilo **verdirir**." (`$\mu_{diyet\_sonrası} < \mu_{diyet\_öncesi}$`). Kilo alımıyla ilgilenmiyoruz.

* **Risk Bölgesi ($\alpha$):**
  Belirlediğimiz anlamlılık düzeyinin (`$\alpha$`, örn: 0.05) **tamamı tek bir kuyruğa** yerleştirilir. Bu, testi o yöndeki bir farkı tespit etme konusunda daha **güçlü** kılar. Çünkü aşırı bir sonucun %5'lik bir alana düşmesi, %2.5'lik bir alana düşmesinden daha kolaydır.

---

### Önemli Karşılaştırma ve Seçim Kriteri

* **Güç vs. Esneklik:**
  Tek kuyruklu testler, belirli bir yöndeki etkiyi tespit etmede **daha güçlüdür**, ancak diğer yöndeki bir etkiyi tamamen gözden kaçırırlar. İki kuyruklu testler ise her iki yöndeki etkiye de açık olduğu için **daha güvenli ve daha az varsayımsaldır**.

* **Ne Zaman Hangisi Seçilir?**
  Eğer bir etki olacağına ve bu etkinin yönüne dair **çok güçlü teorik veya geçmiş kanıtlarınız** varsa tek kuyruklu test kullanabilirsiniz (örneğin, bir ilacın zararlı bir yan etkisinin olmasının imkansız olduğunu biliyorsanız ve sadece faydasını test ediyorsanız). Emin değilseniz veya her iki yöndeki bir fark da sizin için önemliyse, **varsayılan ve daha güvenli olan seçenek her zaman iki kuyruklu testtir.**



| Özellik | İki Kuyruklu Test (Two-Tailed) | Tek Kuyruklu Test (One-Tailed) |
| :--- | :--- | :--- |
| **Ana Fikir** | "Bir fark var mı?" | "Belirli bir yönde (artış/azalış) bir fark var mı?" |
| **Alternatif Hipotez ($H_a$)**| Eşit değildir (`$\neq$`) | Büyüktür (`>`) veya Küçüktür (`<`) |
| **Metafor** | Hem giriş hem çıkışı gözleyen güvenlik görevlisi. | Sadece girişi (veya sadece çıkışı) gözleyen güvenlik görevlisi. |
| **Risk Bölgesi ($\alpha$)** | `$\alpha/2$` olarak iki kuyruğa **bölünür**. | `$\alpha$`'nın tamamı tek bir kuyruğa **yerleştirilir**. |
| **Güç** | Daha muhafazakar, daha az güçlü. | Belirtilen yöndeki bir etkiyi tespit etmede **daha güçlü**. |
| **Ne Zaman Kullanılır?**| Bir farkın yönü hakkında bir fikriniz olmadığında (standart yaklaşım). | Farkın yönü hakkında güçlü bir teorik beklenti olduğunda. |
| **Örnek Soru** | "Bu reklam kampanyası satışları **etkiledi mi**?" | "Bu indirim satışları **artırdı mı**?" | konusunu türkce olarak metaforlu ve tablolu aciklayacagiz.

---

Dijital pazarlama dünyasından çok yaygın bir senaryo olan **A/B testi** üzerinden Tek Kuyruklu ve İki Kuyruklu testleri karşılaştırmalı olarak açıklayalım.

---

### Pazarlama Senaryosu: İndirim Kuponu Kampanyası 💸

Bir e-ticaret siteniz olduğunu ve sattığınız bir online kurs için yeni bir pazarlama stratejisi denemek istediğinizi varsayalım. Mevcut durumda kursun ortalama günlük satışı **100 adet**. Satışları artırmak amacıyla, siteye yeni gelen ziyaretçilere **"%20 Hoş Geldin İndirimi"** sunan bir kampanya başlatıyorsunuz.

Testin sonunda sormanız gereken soru şudur: "Bu indirim kampanyası satışları etkiledi mi?" Bu soruyu sorma şekliniz, yapacağınız testin türünü belirler.

---

### 1. İki Kuyruklu Test (Two-Tailed) – İhtiyatlı Analistin Yaklaşımı

İhtiyatlı bir veri analisti olarak, kampanyanın olası tüm sonuçlarını düşünürsünüz.

* **Bakış Açısı:**
  > "İndirimler genellikle satışları artırır. Ancak, belki de bu indirim markamızın değerini düşürür ve insanlar 'ucuz mal kalitesizdir' diye düşünerek kursu daha **az** satın alır? Veya belki de hiçbir etkisi olmaz. Ben **her türlü değişime** hazırlıklı olmalıyım."

* **Sorulan Soru:**
  > "İndirim kampanyası, ortalama günlük satışları **değiştirdi mi**?"

* **Hipotezler:**
    * **$H_0$ (Sıfır Hipotezi):** İndirimli satışların ortalaması, eski ortalamaya eşittir. `$\mu_{indirimli} = 100$`
    * **$H_a$ (Alternatif Hipotez):** İndirimli satışların ortalaması, eski ortalamadan **farklıdır**. `$\mu_{indirimli} \neq 100$`

* **Metafor (Arama Alanı):**
  Analist, elindeki fenerle hem **sağdaki** (satışlarda beklenmedik bir artış) hem de **soldaki** (satışlarda beklenmedik bir düşüş) karanlık bölgeleri aydınlatmaya çalışır. Fenerin ışığını (anlamlılık düzeyi `$\alpha$`) iki yöne de paylaştırdığı için, herhangi bir yöndeki küçük bir hareketi görmesi biraz daha zordur.

* **Sonuç:**
  Bu test, satışlarda anlamlı bir artış **veya** azalış olup olmadığını size söyleyebilir.

---

### 2. Tek Kuyruklu Test (One-Tailed) – Odaklanmış Pazarlamacının Yaklaşımı

Odaklanmış bir pazarlamacı olarak, temel bir ekonomik varsayıma güvenirsiniz.

* **Bakış Açısı:**
  > "Fiyatı düşürmenin satışları düşürmesi için hiçbir mantıklı sebep yok. Bu, pazarlamanın doğasına aykırı. En kötü senaryo, indirimin hiçbir işe yaramamasıdır. Benim tek merak ettiğim şey, bu indirimin satışları **artırıp artırmadığıdır**."

* **Sorulan Soru:**
  > "İndirim kampanyası, ortalama günlük satışları **artırdı mı**?"

* **Hipotezler:**
    * **$H_0$ (Sıfır Hipotezi):** İndirimli satışların ortalaması, eski ortalamadan daha az veya eşittir. `$\mu_{indirimli} \le 100$`
    * **$H_a$ (Alternatif Hipotez):** İndirimli satışların ortalaması, eski ortalamadan **daha fazladır**. `$\mu_{indirimli} > 100$`

* **Metafor (Arama Alanı):**
  Pazarlamacı, elindeki fenerin tüm gücünü (anlamlılık düzeyi `$\alpha$`) sadece **sağdaki** (satışlarda artış olan) bölgeye odaklar. Sol tarafla (satışların düşmesiyle) hiç ilgilenmez. Tüm ışığı tek bir noktaya odakladığı için, o bölgedeki en ufak bir hareketi bile tespit etme gücü daha yüksektir.

* **Sonuç:**
  Bu test, satışlarda anlamlı bir artış olup olmadığını size daha yüksek bir güçle söyleyebilir. Ancak satışlar bir sebepten düşerse, bu test o düşüşün istatistiksel olarak anlamlı olup olmadığını size **söyleyemez**.


  #### Karşılaştırmalı Özet Tablosu (Pazarlama Örneği)

| Özellik | İki Kuyruklu Test (İhtiyatlı Analist) | Tek Kuyruklu Test (Odaklanmış Pazarlamacı) |
| :--- | :--- | :--- |
| **Bakış Açısı** | "Her sonuca açığım." | "Sadece beklediğim sonuçla ilgileniyorum." |
| **Sorulan Soru** | "Kampanya satışları **değiştirdi mi**?" | "Kampanya satışları **artırdı mı**?" |
| **Alternatif Hipotez ($H_a$)**| `$\mu \neq 100$` | `$\mu > 100$` |
| **Risk Bölgesi ($\alpha$)** | `$\alpha/2$` olarak iki kuyruğa **bölünür**. | `$\alpha$`'nın tamamı tek bir yöne **odaklanır**. |
| **Güçlü Yönü** | Beklenmedik sonuçlara (örn: satışların düşmesi) karşı esnek ve güvenlidir. | Belirli bir yöndeki (örn: artış) etkiyi tespit etmede **daha güçlüdür**. |
| **Zayıf Yönü** | Tek bir yöndeki etkiyi tespit etme gücü biraz daha düşüktür. | Beklenmedik ters yöndeki bir etkiyi tamamen gözden kaçırır. |

# Significance Level:

<img width="363" height="208" alt="image" src="https://github.com/user-attachments/assets/1ab5f127-0eb1-4c19-87cf-d09a1ad81d6a" 

   **Anlamlılık Düzeyi (Significance Level)**, hipotez testlerinin kalbinde yer alan ve verdiğimiz kararların temelini oluşturan bir "**karar çizgisidir**". Gelin bu kavramı metaforlar, karşılaştırmalar ve bir özet tablosuyla detaylı bir şekilde inceleyelim.

---

### Ana Metaforlar: Yargıcın Standardı ve Limbo Dansı

Anlamlılık düzeyini anlamak için iki güçlü metafor kullanacağız:

* **Mahkeme Duruşması:** Anlamlılık düzeyi, duruşma başlamadan önce **yargıcın belirlediği kanıt standardıdır**. "Birini suçlu bulmak için, sunulan kanıtların masum birinin başına gelme olasılığı en fazla ne kadar olabilir?" sorusunun cevabıdır.
* **Limbo Dansı:** Bu, karar kuralını (`$p-değeri \le \alpha$`) akılda tutmak için harika bir yoldur. Anlamlılık düzeyi, altından geçmeniz gereken **limbo çubuğunun yüksekliğidir**.

---

### 1. Anlamlılık Düzeyi ($\alpha$) Nedir?

* **Tanım:** Anlamlılık düzeyi (alfa, `$\alpha$`), bir hipotez testinde **Tip I Hata** yapma riskini ne kadar göze aldığımızı gösteren, **deneyden önce** belirlediğimiz bir olasılık değeridir.
* **Ne İşe Yarar?** Gözlemlediğimiz sonuçların istatistiksel olarak "anlamlı" olup olmadığına karar vermek için bir **eşik değeri** veya **karar çizgisi** görevi görür.
* **Bize Ne Anlatır? (Mahkeme Metaforu)**
    > `$\alpha = 0.05$` demek, "Bu mahkemede, **masum birini mahkum etme riskini %5 olarak kabul ediyorum**" demektir. Bu, yargıcın adalet sistemindeki hatayı göze alma seviyesidir. Kısacası `$\alpha$`, bizim maksimum kabul edilebilir şüphe düzeyimizdir.

---

### 2. `$\alpha$` Değeri Nasıl Seçilir ve Yorumlanır? (Karşılaştırma)

En yaygın `$\alpha$` değerleri 0.05, 0.01 ve 0.10'dur. Seçimimiz, yaptığımız hatanın sonuçlarına ne kadar katlanabileceğimize bağlıdır.

#### A) Katı Standart: `$\alpha = 0.01` (%1 Risk)

* **Limbo Dansı Metaforu:** Limbo çubuğu **çok alçaktadır**. Altından geçmek (yani `$H_0$`'ı reddetmek) çok zordur. Sadece çok "etkileyici" sonuçlar başarılı olabilir.
* **Anlamı:** Sadece çok güçlü kanıtlar karşısında "bir etki vardır" demeye razıyız. Tip I Hata yapmaktan (masum birini mahkum etmekten) çok korkuyoruz.
* **Ne Zaman Kullanılır?** Bir hatanın bedelinin çok ağır olduğu durumlarda.
    * **Örnek:** Ciddi yan etkileri olabilecek yeni bir ilacın "etkili" olduğunu iddia etmek. Hatalı bir şekilde "etkili" demek felaket olabilir, bu yüzden kanıt standardı çok yüksek olmalıdır.

#### B) Altın Standart: `$\alpha = 0.05` (%5 Risk)

* **Limbo Dansı Metaforu:** Limbo çubuğu **standart bir yüksekliktedir**. Altından geçmek zorlayıcıdır ama imkansız değildir.
* **Anlamı:** Bilimsel çalışmaların çoğunda kabul edilen standart dengedir. Tip I ve Tip II hatalar arasında makul bir denge kurar.
* **Ne Zaman Kullanılır?** Çoğu bilimsel ve akademik araştırma, A/B testleri gibi genel amaçlı analizler için.

#### C) Esnek Standart: `$\alpha = 0.10` (%10 Risk)

* **Limbo Dansı Metaforu:** Limbo çubuğu **oldukça yüksektedir**. Altından geçmek (yani `$H_0$`'ı reddetmek) daha kolaydır.
* **Anlamı:** Olası bir etkiyi veya farkı "kaçırmamak" bizim için daha önemlidir. Tip I Hata yapma riskini biraz daha fazla göze alıp, Tip II Hata (gerçek bir etkiyi gözden kaçırma) yapma riskini azaltmaya çalışırız.
* **Ne Zaman Kullanılır?** Bir hatanın bedelinin düşük olduğu, keşif amaçlı ön analizlerde.
    * **Örnek:** Bir web sitesinde yeni bir buton renginin "etkili olabileceğine" dair en ufak bir sinyali bile kaçırmak istemediğimiz bir ön analiz.

---

### 3. Karar Verme Süreci: p-değeri vs. `$\alpha$`

Karar anı, bu iki değerin karşılaştırılmasıdır.

* **p-değeri:** Sizin deneyinizden elde ettiğiniz kanıtın ne kadar "şaşırtıcı" olduğunun ölçüsüdür. (Limbo dansçısının ne kadar eğilebildiği).
* **$\alpha$:** Sizin deneyden önce belirlediğiniz "karar çizgisidir". (Limbo çubuğunun yüksekliği).

> **Altın Kural:**
> * Eğer `$p-değeri \le \alpha$` ise → **$H_0$ Reddedilir**. (Dansçı, çubuğun altından başarıyla geçti! Sonuçlar istatistiksel olarak anlamlıdır.)
> * Eğer `$p-değeri > \alpha$` ise → **$H_0$ Reddedilemez**. (Dansçı, çubuğu devirdi. Sonuçlar istatistiksel olarak anlamlı değildir.)

### Understanding Significance Level & Confidence Level:

<img width="554" height="452" alt="image" src="https://github.com/user-attachments/assets/0231b339-c1af-4348-8e49-1685883bb447" />

<img width="460" height="201" alt="image" src="https://github.com/user-attachments/assets/a6bc6892-e44f-4c28-a0d2-4d01abf97f65" />

<img width="565" height="407" alt="image" src="https://github.com/user-attachments/assets/871b5d7f-5144-423c-9435-5fd1d1faa322" />

#### Karşılaştırmalı Özet Tablosu

| Anlamlılık Düzeyi ($\alpha$) | Metafor (Limbo Çubuğu) | Tip I Hata Riski | Tip II Hata Riski | Ne Zaman Kullanılır? |
| :--- | :--- | :--- | :--- | :--- |
| **Katı (`$\alpha = 0.01$`)** | Çok Alçak | **Çok Düşük** | Yüksek | Hatalı pozitif sonucun bedeli çok ağır olduğunda (ilaç güvenliği vb.). |
| **Standart (`$\alpha = 0.05$`)** | Normal Yükseklik | **Düşük** | Orta | Genel bilimsel araştırmalar, A/B testleri. |
| **Esnek (`$\alpha = 0.10$`)** | Yüksek | **Orta** | Düşük | Olası bir etkiyi kaçırma riskinin yüksek olduğu öncü çalışmalar. |


# P-value:

<img width="972" height="837" alt="image" src="https://github.com/user-attachments/assets/6bf0dfd3-5e10-44a8-87ac-5e96c807dd67" />

### Ana Fikir: p-değeri Bir "Şaşırtıcılık Ölçer"dir, "Doğruluk Ölçer" Değil

Bu görselin temel mesajı şudur: **p-değeri, bir hipotezin doğru olup olmadığını söylemez.** Sadece, "eğer hipotezimiz doğru olsaydı, elimizdeki sonuçları görmek ne kadar şaşırtıcı olurdu?" sorusunu cevaplar.

---

### Bölüm 1: Grafiğin Yorumu - p-değeri Nedir?

Grafik, bir hipotez testinin dünyasını haritalandırır:

* **Eğri (Normal Dağılım):** Bu, **Sıfır Hipotezinin ($H_0$)** doğru olduğu bir evreni temsil eder. Yani, "hiçbir özel durum yok, her şey normal" varsayımındaki tüm olası sonuçları gösterir.
* **Eğrinin Ortası (More likely observation):** `$H_0$` evreninde en sık beklenen, sıradan ve "sıkıcı" sonuçlardır.
* **Eğrinin Kuyrukları (Very un-likely observations):** `$H_0$` evreninde gerçekleşmesi çok nadir, şaşırtıcı ve "şüpheli" sonuçlardır.
* **Kırmızı Nokta (Observed data point):** Bu, bizim deneyimiz sonucunda **elde ettiğimiz gerçek veridir**. Grafikte bu nokta, şüpheli bir bölge olan kuyruk kısmına düşmüştür.
* **Yeşil Alan (P-value):** İşte bu, p-değerinin kendisidir. Anlamı şudur:
    > "Eğer Sıfır Hipotezi doğru olsaydı (yani her şey normal olsaydı), bizim bulduğumuz bu kırmızı nokta kadar veya ondan **daha da aşırı** (daha da şüpheli) bir sonucu **sırf şans eseri** görme olasılığımız, bu yeşil alan kadardır."

Eğer bu yeşil alan (p-değeri) çok küçükse, sonucumuzun "normal" bir evrende şans eseri ortaya çıkmasının çok düşük bir ihtimal olduğunu anlarız.

---

### Bölüm 2: Mantıksal Hata - p-değeri Ne Değildir?

Görselin en üstündeki "Önemli" kutusu, istatistikte en sık yapılan hatayı vurgular.

**Matematiksel Olarak:**
$$
P(\text{Gözlem | Hipotez}) \neq P(\text{Hipotez | Gözlem})
$$
Bu karmaşık görünen ifadeyi basit bir metaforla açıklayalım:

#### Yağmur ve Islak Zemin Metaforu

* **Hipotez:** Yağmur yağıyor.
* **Gözlem:** Yerdeki çimenler ıslak.

Şimdi iki farklı olasılık sorusu soralım:

* **Soru A (p-değerinin mantığı): `$P(\text{Gözlem | Hipotez})$`**
    > **Soru:** "Eğer yağmurun yağdığını **BİLİYORSAK**, çimenlerin ıslak olma olasılığı nedir?"
    > **Cevap:** Çok yüksektir, neredeyse %100. Yağmur yağıyorsa, çimenler ıslanır.
    >
    > **p-değeri de tam olarak bu mantıkla çalışır.** `$H_0$`'ın doğru olduğunu **varsayar** ve bu varsayım altında bizim veriyi (gözlemi) bulma olasılığımızı hesaplar.

* **Soru B (Sık yapılan hata): `$P(\text{Hipotez | Gözlem})$`**
    > **Soru:** "Eğer çimenlerin ıslak olduğunu **GÖRÜYORSAK**, yağmur yağıyor olma olasılığı nedir?"
    > **Cevap:** %100 değildir. Belki de fıskiyeler çalıştı, biri hortumla bir yeri suladı veya kar eridi. Çimenlerin ıslak olması, kesin olarak yağmur yağdığı anlamına gelmez.

**İşte En Büyük Hata (Transposed Conditional Fallacy):**
Bir deney yapıp düşük bir p-değeri bulmak (yani "şaşırtıcı" bir gözlem yapmak), **Durum A**'daki gibi bir durumdur. Ancak buradan yola çıkarak **Durum B** hakkında kesin bir yargıya varmak hatadır.

> **Yani,** "Eğer `$H_0$` doğru olsaydı, bu veriyi görmem çok düşük bir ihtimaldi" (düşük p-değeri) demek, "**Öyleyse `$H_0$`'ın doğru olma olasılığı çok düşüktür**" demekle **aynı şey değildir!**

---

### Özetle

Bu görsel bize şunu anlatır:

* p-değeri, hipotezinizin doğru veya yanlış olma ihtimalini **söylemez**.
* p-değeri, sadece verilerinizin, "hiçbir şey olmuyor" diyen varsayımsal bir dünya ile ne kadar uyumsuz olduğunu, yani ne kadar "şaşırtıcı" olduğunu söyler.
* Düşük bir p-değeri, `$H_0$`'a karşı bir **şüphe uyandıran kırmızı bir bayraktır**, ancak `$H_0$`'ın yanlış olduğunun kesin bir kanıtı veya olasılığı değildir.

**p-değeri (p-value)**, hipotez testlerinin en önemli ama aynı zamanda en sık yanlış anlaşılan kavramıdır. Bir sonucun istatistiksel olarak "anlamlı" olup olmadığına karar vermemizi sağlayan kilit bir kanıttır.

Gelin bu kavramı metaforlar, karşılaştırmalar ve bir özet tablosuyla detaylı bir şekilde inceleyelim.

---

### Ana Metafor: Mahkeme Duruşmasındaki "Şaşırtıcılık" Kanıtı

Bir hipotez testini bir **mahkeme duruşması** olarak düşünmeye devam edelim:

* **Sıfır Hipotezi ($H_0$):** "Sanık masumdur." Bu, testin başındaki varsayımımızdır.
* **Kanıt:** Olay yerinde bulunan bir parmak izi.
* **p-değeri:** Bu, savcının yargıca sunduğu en güçlü argümandır ve şunu söyler:
    > "Sayın yargıç, eğer sanık **gerçekten masum olsaydı**, bu parmak izinin olay yerinde **sırf şans eseri** bulunma ihtimali işte bu kadardır."

p-değeri, bir sonucun varsayılan durum (masumiyet) altında ne kadar **şaşırtıcı veya beklenmedik** olduğunun bir ölçüsüdür.

---

### 1. p-değeri Nedir?

* **Tanım:**
  p-değeri, **sıfır hipotezi ($H_0$) doğruyken**, en az bizim deneyimizde gözlemlediğimiz kadar aşırı (veya daha da aşırı) bir sonucun **şans eseri** ortaya çıkma olasılığıdır.

* **Ne İşe Yarar?**
  Bize, gözlemlediğimiz sonucun sadece rastlantısal bir dalgalanma mı, yoksa sıfır hipotezine karşı gerçek bir kanıt mı olduğunu değerlendirme imkanı sunar.

* **Bize Ne Anlatır?**
  Düşük bir p-değeri, "Eğer `$H_0$` doğru olsaydı, bu sonucu görmek çok büyük bir tesadüf olurdu. Belki de `$H_0$` doğru değildir?" dedirtir. Yüksek bir p-değeri ise, "Bu sonucu görmek şaşırtıcı değil, `$H_0$` doğru olsa bile bu tür sonuçlar şans eseri sık sık görülebilir" anlamına gelir.

---

### 2. p-değeri Nasıl Yorumlanır? (Karşılaştırma)

p-değerinin kendisi tek başına bir anlam ifade etmez; onu önceden belirlediğimiz **Anlamlılık Düzeyi ($\alpha$)** ile karşılaştırarak bir karara varırız.

#### A) Düşük p-değeri (örn: `$p < 0.05$`)

* **Anlamı:** Gözlemlediğimiz sonuç, `$H_0$`'ın doğru olduğu varsayımı altında **çok beklenmedik ve şaşırtıcıdır**.
* **Mahkeme Metaforu:** Olay yerinde bulunan parmak izinin, masum olduğu varsayılan sanığa ait olma ihtimali çok düşüktür. Bu durum, "masumiyet" varsayımına karşı **güçlü bir şüphe** oluşturur.
* **Karar:** Bu, sıfır hipotezine karşı **güçlü bir kanıttır**. Genellikle `$H_0$`'ı reddederiz.

#### B) Yüksek p-değeri (örn: `$p > 0.05$`)

* **Anlamı:** Gözlemlediğimiz sonuç, `$H_0$`'ın doğru olduğu varsayımı altında **beklenen, şaşırtıcı olmayan** bir durumdur.
* **Mahkeme Metaforu:** Olay yeri bir kütüphaneyse ve sanık da orada çalışan bir kütüphaneciyse, parmak izinin orada bulunması hiç şaşırtıcı değildir. Bu kanıt, "masumiyet" varsayımını çürütmek için **zayıftır**.
* **Karar:** Bu, sıfır hipotezine karşı **zayıf bir kanıttır**. `$H_0$`'ı reddetmek için yeterli nedenimiz yoktur.

#### Karşılaştırmalı Özet Tablosu: p-değeri vs. Anlamlılık Düzeyi ($\alpha$)

Bu iki kavram sıkça karıştırılır, ancak rolleri tamamen farklıdır.

| Özellik | p-değeri (p-value) | Anlamlılık Düzeyi ($\alpha$) |
| :--- | :--- | :--- |
| **Tanım** | `$H_0$` doğruyken, gözlemlenen sonucun ortaya çıkma olasılığı. | `$H_0$` doğruyken onu reddetme hatasını yapmayı göze aldığımız risk. |
| **Metafor (Mahkeme)**| **Kanıtın gücü/şaşırtıcılığı.** | Yargıcın önceden belirlediği **kanıt standardı**. |
| **Kökeni** | Deney verilerinden **hesaplanır**. | Deneyden önce araştırmacı tarafından **seçilir**. |
| **Rolü** | Karar vermek için kullanılan **kanıt**. | Karar vermek için kullanılan **eşik/sınır**. |
| **Kullanımı** | Değeri `$\alpha$` ile karşılaştırılır. | Değeri `p-değeri` ile karşılaştırmak için bir referans noktasıdır. |

### Çok Önemli Notlar: p-değerinin Yanlış Yorumları

---

❌ **YANLIŞ:** p-değeri, sıfır hipotezinin doğru olma olasılığıdır.

✅ **DOĞRU:** p-değeri, `$H_0$` **doğru varsayıldığında** verilerin ortaya çıkma olasılığıdır.

---

❌ **YANLIŞ:** Yüksek bir p-değeri (örn: 0.80), sıfır hipotezinin doğru olduğunu kanıtlar.

✅ **DOĞRU:** Yüksek bir p-değeri, sadece `$H_0$`'ı reddetmek için **yeterli kanıtımız olmadığı** anlamına gelir. Bu, "delil yetersizliğinden beraat" kararı gibidir, "masumiyetin kanıtı" değil.

---

❌ **YANLIŞ:** İstatistiksel olarak anlamlı bir sonuç (düşük p-değeri), pratik olarak da önemli bir sonuçtur.

✅ **DOĞRU:** Çok büyük bir örneklemle, pratik olarak hiçbir anlamı olmayan çok küçük bir fark bile istatistiksel olarak anlamlı çıkabilir. Anlamlılık, **etkinin büyüklüğünü göstermez**.

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





