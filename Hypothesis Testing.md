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

---

### Ana Metafor: Mahkeme Salonu ve Bilimsel Deney

Bu iki hipotezi anlamak için iki güçlü metafor kullanabiliriz:

* **Mahkeme Salonu:** Bir iddiayı yargıladığımız bir duruşma.
* **Bilimsel Deney:** Yeni bir fikrin işe yarayıp yaramadığını test ettiğimiz bir laboratuvar.

---

#### 1. Sıfır Hipotezi ($H_0$) – Statükonun Savunucusu

* **Nedir?**
  Sıfır hipotezi, testin başında doğru olarak kabul edilen varsayımdır. Genellikle "bir etki yoktur," "bir fark yoktur," veya "bir değişiklik olmamıştır" gibi ifadeler içerir. Çürütülmeye çalışılan mevcut durum veya genel kanıdır.

* **Rolü:**
  Değişime karşı bir "şeytanın avukatı" rolü oynar. Bir etkinin veya farkın, sadece şans eseri ortaya çıkmadığından emin olmamızı sağlar.

* **Metaforları:**
    * **Mahkeme Salonu:** "**Sanık masumdur.**" Duruşma başladığında, sanığın masum olduğu varsayılır. Onu suçlu bulmak için bu varsayımın "makul şüphenin ötesinde" çürütülmesi gerekir.
    * **Bilimsel Deney:** "**Yeni gübrenin bitki büyümesine bir etkisi yoktur.**" Deneye başlarken, yeni tedavinin veya yöntemin mevcut durumdan farksız olduğunu varsayarız.

* **Matematiksel İpucu:**
  Her zaman bir eşitlik içerir (`$=$, `$\le$`, veya `$\ge$`).

#### 2. Alternatif Hipotez ($H_a$ veya $H_1$) – Değişimin Habercisi

* **Nedir?**
  Alternatif hipotez, araştırmacının kanıtlamaya çalıştığı iddiadır. Bu, "bir etki vardır," "bir fark vardır," veya "bir değişiklik olmuştur" diyen yeni ve "heyecan verici" fikirdir.

* **Rolü:**
  Statükoya meydan okur. Eğer sıfır hipotezini çürütecek kadar güçlü kanıt bulursak, alternatif hipotezi kabul ederiz.

* **Metaforları:**
    * **Mahkeme Salonu:** "**Sanık suçludur.**" Bu, savcının kanıtlamaya çalıştığı iddiadır.
    * **Bilimsel Deney:** "**Yeni gübre bitki büyümesini artırır.**" Bu, araştırmacının keşfetmeyi umduğu yeniliktir.

* **Matematiksel İpucu:**
  Her zaman bir eşitsizlik içerir (`$\ne$`, `$>$`, veya `$<$`).

# Asagidaki tabloyu markdown formatina cevircez:

<img width="664" height="447" alt="image" src="https://github.com/user-attachments/assets/aed7c1e2-0da4-4f9e-9604-67dc93e997ad" />




# Type I and Type II Errors konusunu türkce olarak metaforlu ve tablolu aciklayacagiz. 


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





