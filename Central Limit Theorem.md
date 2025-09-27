# Central Limit Theorem

[Central Limit Theorem](https://colab.research.google.com/drive/1ZELr-fJ9yJoFScAsgyjUwkx_q4Jbj8PJ#scrollTo=FPWLEBWBwBFg)

<img width="783" height="491" alt="image" src="https://github.com/user-attachments/assets/4efd717b-de65-4fc7-b7a7-e0dedb389038" />


<img width="795" height="558" alt="image" src="https://github.com/user-attachments/assets/96cca1ee-a75f-4c04-97a8-40186562a981" />

<img width="670" height="109" alt="image" src="https://github.com/user-attachments/assets/14a07158-325a-4c07-8330-0841c5d65cd7" />


### ÖRNEK GRAFIK:

<img width="513" height="302" alt="image" src="https://github.com/user-attachments/assets/0d19b36b-a05e-4691-bd5a-05bc9cfe6f58" />

<img width="678" height="479" alt="image" src="https://github.com/user-attachments/assets/363f843c-1af2-4b46-bb71-2c2922e53511" />


<img width="604" height="455" alt="image" src="https://github.com/user-attachments/assets/aa28c10c-271e-460b-991c-cbc81d3225a8" />

<img width="662" height="360" alt="image" src="https://github.com/user-attachments/assets/f8f0b7bb-209c-4184-8450-bc82a35b4929" />

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



