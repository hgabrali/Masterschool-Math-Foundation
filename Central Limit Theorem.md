# Central Limit Theorem

[Central Limit Theorem](https://colab.research.google.com/drive/1ZELr-fJ9yJoFScAsgyjUwkx_q4Jbj8PJ#scrollTo=FPWLEBWBwBFg)

<img width="783" height="491" alt="image" src="https://github.com/user-attachments/assets/4efd717b-de65-4fc7-b7a7-e0dedb389038" />


<img width="795" height="558" alt="image" src="https://github.com/user-attachments/assets/96cca1ee-a75f-4c04-97a8-40186562a981" />

<img width="670" height="109" alt="image" src="https://github.com/user-attachments/assets/14a07158-325a-4c07-8330-0841c5d65cd7" />


### ÖRNEK GRAFIK:

<img width="513" height="302" alt="image" src="https://github.com/user-attachments/assets/0d19b36b-a05e-4691-bd5a-05bc9cfe6f58" />

<img width="678" height="479" alt="image" src="https://github.com/user-attachments/assets/363f843c-1af2-4b46-bb71-2c2922e53511" />

### Anahtar Prensip: Bu Grafik CLT'nin Kendisi Değil, Başlangıç Noktasıdır!

> Unutulmaması gereken en önemli şey şudur: Gördüğünüz bu **sağa çarpık (right-skewed)** grafik, Merkezi Limit Teoremi'nin sonucunu değil, **başlangıç koşulunu** gösteriyor.

* **Metaforla Hatırlayalım:** Bir önceki "Bilge Konseyi" metaforumuzda, bu grafik **kaotik fikirli krallığın kendisidir**. CLT'nin sihrinin işleyeceği ham madde budur. Henüz "Bilgeler Konseyi" (yani örneklem ortalamalarının dağılımı) toplanmadı.

---

### Grafiği ve Açıklamaları Yorumlama Adımları

Böyle bir grafikle karşılaştığınızda izlemeniz gereken yol haritası şöyledir:

#### Adım 1: Grafiğin Kimliğini Teşhis Etmek

İlk sormanız gereken soru: "Ben neye bakıyorum?"
* **Cevap:** Bu bir **popülasyonun histogramıdır**. Kod açıklaması da bunu doğrular:
    > *"Plot the histogram of the population..."*
* Bu, 10,000 veri noktasının tamamının dağılımıdır.

#### Adım 2: Grafiğin Şeklini Analiz Etmek (Karakter Tahlili)

Şimdi grafiğin kendisini, doğru terimleri kullanarak yorumlayalım:
* **Dağılımın Şekli:** Bu bir "Normal Dağılım" (Çan Eğrisi) **değildir**. Bu, **sağa çarpık (right-skewed / positively skewed)** bir dağılımdır.
* **Yorum:** Verilerin büyük bir kısmı sol tarafta (düşük değerlerde) toplanmış. Ancak az sayıda da olsa çok yüksek değerler var ve bunlar grafiğin kuyruğunu sağa doğru uzatıyor.
* **Merkez:** Veri yığılması kabaca 50-75 aralığında en yüksek görünüyor.
* **Yayılım:** Veriler 0'dan başlayıp 200'ün üzerine kadar geniş bir alana yayılıyor.

#### Adım 3: Kod Açıklaması ile Görseli Doğrulamak

Şimdi teoriyi ve pratiği birleştirelim:
* **Kodun Amacı:** Açıklama, `lognormal distribution` kullanarak **çarpık bir popülasyon** (`a skewed population`) yaratmayı amaçladığını açıkça belirtiyor.
* **Doğrulama:** Grafiğin şekli (sağa çarpık) ile kodun amacı (çarpık popülasyon yaratmak) **mükemmel bir şekilde örtüşüyor**. Bu, kodun beklendiği gibi çalıştığının görsel bir kanıtıdır.

#### Adım 4: Merkezi Limit Teoremi Bağlamını Kurmak (En Önemli Adım)

Bu noktada CLT devreye girer. Yorumunuzu şu şekilde yönlendirmelisiniz:

> "Elimizdeki bu popülasyon dağılımı normal olmasa da (sağa çarpık), Merkezi Limit Teoremi bize bir vaatte bulunur. Kod açıklamasında belirtilen parametreleri kullanarak (örneklem boyutu `n=30`, örneklem sayısı `1000`), bu popülasyondan 30'ar kişilik 1000 farklı örneklem alıp her birinin ortalamasını hesaplarsak, **bu 1000 adet ortalamanın dağılımı normal (Çan Eğrisi şeklinde) olacaktır.**"

* **Yani:**
    * **Bu Grafik:** Kaotik krallık.
    * **CLT'nin Öngörüsü:** Bu krallıktan seçeceğimiz temsilcilerin ("Bilgeler") oluşturacağı konseyin dağılımı düzenli ve normal olacaktır.

---

### Analiz ve Yorum için Kontrol Listeniz

Bir grafikle karşılaştığınızda şu soruları sorun ve bu terimleri kullanarak yorum yapın:

#### 1. Bu Grafik Neyi Temsil Ediyor?
> "Bu histogram, popülasyonun dağılımını mı gösteriyor, yoksa örneklem ortalamalarının dağılımını mı?"
* Cevabınız, CLT'yi nasıl yorumlayacağınızı belirler.

#### 2. Dağılımın Şekli Nedir? (Doğru Terimleri Kullanın)
* Normal Dağılım (Çan Eğrisi)
* Sağa Çarpık (Right-Skewed): Kuyruğun sağa uzadığı durum.
* Sola Çarpık (Left-Skewed): Kuyruğun sola uzadığı durum.
* Tek Tip (Uniform): Dikdörtgen şeklinde, her değer eşit olasılıklı.
* Çift Tepeli (Bimodal): İki belirgin tepe noktası var.

#### 3. CLT Bağlamı Nedir?
* **Eğer grafik popülasyonu gösteriyorsa (bu örnekteki gibi):**
    > "Bu popülasyon [şekli belirtin, örn: sağa çarpık] olmasına rağmen, CLT sayesinde, yeterince büyük örneklemlerin (`n > 30`) ortalamalarının dağılımının normale yakınsayacağını biliyoruz."
* **Eğer grafik örneklem ortalamalarını gösteriyorsa:**
    > "Bu grafik, Merkezi Limit Teoremi'nin bir kanıtıdır. Ana popülasyon çarpık olsa bile, örneklem ortalamalarının dağılımının öngörüldüğü gibi normale yakınsadığını görüyoruz."

#### 4. Parametreler Ne İfade Ediyor?
> "Kodda belirtilen örneklem boyutu (`n=30`), CLT'nin geçerli olması için genellikle yeterli kabul edilen bir sınırdadır. Bu nedenle, bu popülasyondan alınacak 30'luk örneklemlerin ortalamalarının normal dağılmasını bekleyebiliriz."

---

<img width="604" height="455" alt="image" src="https://github.com/user-attachments/assets/aa28c10c-271e-460b-991c-cbc81d3225a8" />

<img width="662" height="360" alt="image" src="https://github.com/user-attachments/assets/f8f0b7bb-209c-4184-8450-bc82a35b4929" />

### Anahtar Prensip: Bu Grafik CLT'nin Vaadinin Gerçekleşmiş Halidir!

> Bu gördüğünüz yeni grafik, Merkezi Limit Teoremi'nin bize söz verdiği şeyin ta kendisidir. Yani, çarpık bir popülasyondan alınan **örneklem ortalamalarının dağılımıdır**.

---

### Grafiği ve Açıklamaları Yorumlama Adımları

#### Adım 1: Kod Açıklamasını Anlamak (Sihrin Nasıl Yapıldığını Görmek)

Önce kodun ne yaptığını anlayalım. Bu adımlar, tam olarak "Bilge Konseyi" metaforumuzdaki süreci tarif ediyor:

* **`Initialise a list: sample_means`**: Konseyin toplanacağı boş bir salon hazırlıyoruz.
* **`Loop for sampling: Repeat 1000 times`**: 1000 defa temsilci ("Bilge") seçeceğimizi kararlaştırıyoruz.
* **`Draw a random sample: ...select 30 individuals`**: Her seferinde krallıktan rastgele **30 köylü** seçiyoruz (örneklem alıyoruz).
* **`Calculate the mean`**: Seçtiğimiz 30 köylünün ortalama görüşünü hesaplayıp "Bilge"yi belirliyoruz.
* **`Store the mean: ...add to the sample_means list`**: Belirlediğimiz her "Bilge"yi konsey salonuna (`sample_means` listesine) ekliyoruz.
* **`Plot the histogram`**: 1000 "Bilge" toplandıktan sonra, konseydeki genel görüş dağılımının resmini çekiyoruz.

#### Adım 2: Grafiğin Kimliğini Teşhis Etmek

Şimdi ortaya çıkan grafiğe (resme) bakalım:

* **Başlık (Sampling Distribution of Sample Means):** Başlık bize doğrudan neye baktığımızı söylüyor: **"Örneklem Ortalamalarının Örneklem Dağılımı"**.
* **X Ekseni (Sample Mean):** Bu eksen, bireysel köylülerin görüşlerini değil, 30'ar kişilik grupların **ortalama görüşlerini** ("Bilgeler"in görüşlerini) gösteriyor.
* **Y Ekseni (Frequency):** Belirli bir ortalama görüşe sahip kaç tane "Bilge" olduğunu gösteriyor.

#### Adım 3: Büyük Karşılaşma ve Analiz (En Önemli Adım)

Şimdi bir önceki grafikle bu grafiği **karşılaştıralım**:

| Özellik | Önceki Grafik (Popülasyon) | Şimdiki Grafik (Örneklem Ortalamaları) |
| :--- | :--- | :--- |
| **Neyi Temsil Ediyor?** | "Kaotik Krallık" (Bireyler) | "**Bilge Konseyi**" (Ortalamalar) |
| **Şekli** | Sağa Çarpık (Asimetrik) | **Normal Dağılım** (Simetrik Çan Eğrisi) |
| **Merkezi** | ~50 civarında yığılma var | **~50-55 civarında net bir merkez var** |


> **Yorum:** İşte bu, Merkezi Limit Teoremi'nin gücüdür! Başlangıçtaki popülasyonumuz çarpık olmasına rağmen, ondan aldığımız örneklemlerin ortalamaları **mükemmel bir çan eğrisi** oluşturdu. Kaostan düzen doğdu. Bu grafik, CLT'nin çalıştığının **canlı bir kanıtıdır**.

---

### Analiz ve Yorum için Kontrol Listeniz (Güncellenmiş Hali)

Bu yeni grafikle karşılaştığınızda, bir önceki kontrol listesindeki sorulara artık şu cevapları verebilirsiniz:

#### 1. Bu Grafik Neyi Temsil Ediyor?
* **Cevap:**
    > "Bu histogram, çarpık bir popülasyondan alınan **örneklem ortalamalarının dağılımını** gösteriyor."

#### 2. Dağılımın Şekli Nedir?
* **Cevap:** **Normal Dağılım (Çan Eğrisi)**. Simetrik, ortada tek bir tepe noktası var ve kenarlara doğru azalıyor.

#### 3. CLT Bağlamı Nedir?
* **Cevap:**
    > "Bu grafik, **Merkezi Limit Teoremi'nin bir kanıtıdır**. Ana popülasyon çarpık olsa bile, örneklem ortalamalarının dağılımının öngörüldüğü gibi normale yakınsadığını görüyoruz."

#### 4. Parametreler Ne İfade Ediyor?
* **Grafiğin Merkezi Hakkında Yorum:**
    > "Grafiğin tepe noktası (merkezi) kabaca 50-55 aralığındadır. Bu, ana popülasyonun ortalaması olan 50'ye çok yakındır. Bu durum, CLT'nin `$E[\bar{X}] = \mu$` kuralını görsel olarak doğrulamaktadır."

* **Grafiğin Yayılımı Hakkında Yorum:**
    > "Örneklem ortalamaları 40 ile 75 arasında bir aralığa yayılmış durumda. Bu yayılım, standart hata (`$SE = \sigma / \sqrt{n}$`) tarafından kontrol edilir ve popülasyonun kendisinden (0-250 aralığı) çok daha dardır. Bu, ortalama almanın aşırı değerleri nasıl yumuşattığını ve tahminleri nasıl daha tutarlı hale getirdiğini gösterir."


### SORU:

<img width="752" height="575" alt="image" src="https://github.com/user-attachments/assets/9cc64d78-03d7-4aba-bc1c-1f6c3f81ccf7" />

### Cözümün aciklamasi eklenecek

---

## Merkezi Limit Teoremi (Central Limit Theorem - CLT)

İstatistiğin belki de en güçlü ve en sihirli konsepti olan Merkezi Limit Teoremi'ni (CLT), neden bu kadar önemli olduğunu ve arkasındaki matematiği, detaylı bir metafor ve karşılaştırmalarla açıklayalım.

### Ana Metafor: Kaosun İçindeki Bilge Konsey

Merkezi Limit Teoremi'ni anlamak için, çok çeşitli ve kaotik görüşlere sahip bireylerden oluşan dev bir **krallık** hayal edin.

* **Popülasyon (Krallığın Kendisi):** Bu krallıktaki insanların fikirleri her türlü dağılımı gösterebilir. Bazı konularda fikirler ikiye bölünmüştür (çift tepeli dağılım), bazılarında herkes aynı şeyi düşünür (tek tip dağılım), bazılarında ise aşırı uç görüşler daha yaygındır (çarpık dağılım). Tam bir kaos hakimdir.
* **Örneklem (Rastgele Bir Grup Köylü):** Krallığın genel fikrini anlamak için, her seferinde rastgele 30 köylüyü bir araya getirip onlara fikirlerini soruyorsunuz.
* **Örneklem Ortalaması (Grubun Temsilcisi "Bilge"):** Her 30 kişilik grubun aşırı uç fikirleri (çok radikal veya çok pasif) birbirini bir miktar dengeler ve grubun bir **ortalama görüşü** ortaya çıkar. Bu ortalama görüş, o grubun temsilcisi olan bir "Bilge" gibidir.
* **Örneklem Ortalamalarının Dağılımı (Bilgeler Konseyi):** Şimdi, bu işlemi binlerce kez tekrarladığınızı ve her gruptan çıkan "Bilge"yi büyük bir **konseyde** topladığınızı hayal edin.

> **İşte Sihir Tam Burada Başlıyor:**
> Krallıktaki bireysel köylülerin fikirleri ne kadar kaotik ve farklı dağılımlara sahip olursa olsun, **Bilgeler Konseyi'ndeki ortalama görüşler her zaman mükemmel bir Çan Eğrisi (Normal Dağılım) şeklinde olacaktır!**

Görseldeki gibi, hangi kaotik dağılımdan başlarsanız başlayın, örneklem ortalamaları her zaman Normal Dağılıma yakınsar.

---

### Bölüm 1: Bilgeler Konseyi'nin Kuralları (CLT'nin Matematiksel Tanımı)

Bu sihirli sonucun arkasında üç temel kural vardır:

#### Kural 1: Konsey'in Merkezi (Ortalamaların Ortalaması)
Bilgeler Konseyi'nin ortalama görüşü, tüm krallığın **gerçek ortalama görüşüyle** birebir aynıdır.

* **Matematiksel Olarak:** `$E[\bar{X}] = \mu$`
* **Anlamı:** Örneklem ortalamalarının ortalaması, popülasyonun gerçek ortalamasını verir. Bu sayede, örneklemlerimize bakarak popülasyon hakkında çok isabetli bir merkez noktası tahmini yapabiliriz.

#### Kural 2: Konsey'deki Fikir Birliği (Standart Hata)
Konseydeki bilgelerin görüşlerinin ne kadar birbirine yakın olduğunun ölçüsüdür. Buna **Standart Hata (Standard Error)** denir.

* **Matematiksel Olarak:**
    $$SE = \frac{\sigma}{\sqrt{n}}$$
    (Burada $\sigma$ krallıktaki bireysel görüşlerin standart sapması, $n$ ise her bir gruptaki köylü sayısıdır.)
* **Karşılaştırmalı Anlamı:** Bu formül bize çok önemli bir şey söyler:
    * **Küçük Gruplar (düşük `$n$`):** Eğer bilge temsilcileri 5'er kişilik gruplardan seçseydik, şans eseri hep aşırı uç görüşlülerin bir araya gelme ihtimali olurdu. Bu yüzden konseydeki görüşler daha dağınık olurdu (yüksek standart hata).
    * **Büyük Gruplar (yüksek `$n$`):** Temsilcileri 100'er kişilik gruplardan seçtiğimizde, her grubun içindeki aşırılıklar birbirini daha iyi dengeler. Bu yüzden bilgelerin görüşleri birbirine çok daha yakın olur ve konseyde daha güçlü bir fikir birliği oluşur (düşük standart hata).
* **Sonuç:** **Örneklem boyutu ($n$) arttıkça, standart hata azalır** ve tahminlerimiz daha güvenilir hale gelir.

#### Kural 3: Konsey'in Şekli (Her Zaman Normal Dağılım)
En başta söylediğimiz sihirli kural: Krallıktaki bireylerin görüş dağılımı ne olursa olsun, yeterince büyük gruplardan (genellikle `$n > 30$` kabul edilir) seçilen bilgelerin oluşturduğu konseyin görüş dağılımı **her zaman Normal Dağılıma (Çan Eğrisi) uyar.**

---

### Bölüm 2: Bu Sihir Neden Bu Kadar Önemli?

CLT, istatistiksel çıkarımın temel taşıdır, çünkü bize şu gücü verir:

* **Problem:** Genellikle analiz ettiğimiz popülasyonun (krallığın) gerçek dağılım şeklini bilmeyiz. Verimiz normal dağılıma uymuyor olabilir.
* **CLT'nin Çözümü:** Popülasyonun şekli ne olursa olsun, biz **örneklem ortalamasının** dağılımının **normal olduğunu** biliriz. Bu sayede:
    * Bir örneklem ortalamasının ne kadar olası olduğunu hesaplayabiliriz.
    * Gerçek popülasyon ortalaması için **güven aralıkları** oluşturabiliriz.
    * **Hipotez testleri** yapabiliriz (tıpkı bir önceki Python alıştırmasında yaptığımız gibi).

CLT olmasaydı, popülasyonun dağılımını bilmediğimiz durumlarda ortalama hakkında güvenilir çıkarımlar yapmak neredeyse imkansız olurdu.

#### Karşılaştırmalı Özet Tablo

| Kavram | Metafordaki Karşılığı | Matematiksel Anlamı |
| :--- | :--- | :--- |
| **Popülasyon** | Krallığın tamamı (kaotik fikirler) | Üzerinde çalışılan grubun tamamı. Dağılımı bilinmeyebilir. |
| **Örneklem** | Rastgele seçilmiş bir grup köylü | Popülasyondan seçilen bir alt küme. |
| **Örneklem Ortalaması ($\bar{X}$)** | Grubun temsilcisi olan "Bilge" | Örneklemin ortalaması. Tek bir değerdir. |
| **Ortalamaların Dağılımı** | Bilgeler Konseyi | Çok sayıda örneklem ortalamasının oluşturduğu dağılım. |
| **CLT'nin Vaadi** | Konsey her zaman düzenli ve bilgedir. | Örneklem ortalamalarının dağılımı, `$n$` arttıkça **Normal Dağılıma** yakınsar. |



