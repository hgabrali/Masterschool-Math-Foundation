# Population and Sampling

<img width="790" height="422" alt="image" src="https://github.com/user-attachments/assets/1731293b-80de-4347-9727-141add2e9286" />

<img width="772" height="509" alt="image" src="https://github.com/user-attachments/assets/da817bfa-a6e7-48b6-92ad-21f967f5c9fc" />

<img width="726" height="646" alt="image" src="https://github.com/user-attachments/assets/f065035d-68f8-4cfb-937f-ba1ab800bfb6" />

<img width="750" height="712" alt="image" src="https://github.com/user-attachments/assets/403ffe0e-1e89-41ca-a57f-e4d93572158d" />

<img width="784" height="383" alt="image" src="https://github.com/user-attachments/assets/887647cd-00fa-48c2-8788-b2a6579c7864" />


<img width="816" height="667" alt="image" src="https://github.com/user-attachments/assets/3164d5ab-49c8-416f-9465-939c958007a4" />

---

# Popülasyon (Evren) ve Örneklem 

### Ana Metafor: Aşçının Çorba İkilemi

Dev bir restoranda bir aşçı olduğunuzu hayal edin. Önünüzde devasa bir kazanda, günün spesiyali olan bir çorba var. Müşterilere servis etmeden önce çorbanın tuzunun tam kıvamında olup olmadığını anlamanız gerekiyor.

> **İkilem şudur:** Çorbanın *gerçek* tadını anlamak için bütün kazanı içemezsiniz. Ama sadece bir kaşık tadarak bütün kazan hakkında nasıl doğru bir karar verebilirsiniz? İşte istatistikteki temel problem tam olarak budur.

---

### Bölüm 1: Ana Kavramlar - Kazan ve Kaşık

#### Popülasyon (Evren) – Dev Çorba Kazanı

* **Ne Olduğu:** Üzerinde çalıştığımız, hakkında bilgi edinmek istediğimiz bireylerin veya nesnelerin **tamamıdır**. Araştırma sorumuzun hedefindeki **bütün grup**.
* **Metafordaki Karşılığı:** İçi çorba dolu **kazanın tamamı**.
* **Örnekler:**
    * Bir üniversitedeki **tüm öğrenciler**.
    * Bir yılda üretilen **tüm arabalar**.
    * Bir seçimdeki **tüm seçmenler**.
* **Popülasyon Parametreleri ($\mu$, $\sigma$):** Bunlar, popülasyonun tamamını tanımlayan "gerçek" ama genellikle bilmediğimiz değerlerdir.
    * **Metafordaki Karşılığı:** Bütün çorbanın **gerçek tuzluluk oranı ($\mu$)** ve tadının ne kadar homojen olduğu (**standart sapması $\sigma$**).

#### Örneklem (Sample) – Tatmak İçin Alınan Kaşık

* **Ne Olduğu:** Popülasyonun içinden analiz etmek için seçilmiş daha küçük bir **alt kümedir**.
* **Metafordaki Karşılığı:** Tadına bakmak için kazandan aldığınız **bir kaşık dolusu çorba**.
* **Örnek:** Üniversitedeki 10,000 öğrenci (popülasyon) arasından anket yapmak için seçilen 500 öğrenci (örneklem).
* **Örneklem İstatistiği ($\bar{x}$, $s$):** Bunlar, örneklemimizden hesapladığımız ve popülasyon parametrelerini *tahmin etmek* için kullandığımız değerlerdir.
    * **Metafordaki Karşılığı:** Kaşığınızdaki çorbanın **tuzluluk oranı ($\bar{x}$)**.

#### Süreç: Örnekleme ve Çıkarım

Görsellerdeki döngü, istatistiğin kalbini oluşturur:

1.  **Örnekleme (Sampling):** Popülasyondan bir örneklem seçme süreci. (Kazandan bir kaşık çorba almak).
2.  **Çıkarım (Inference):** Örneklemden elde ettiğimiz sonuçları kullanarak popülasyon hakkında genelleme yapma süreci. (Kaşığın tadına bakıp, "Bu kazanın tuzu biraz eksik" demek).

---

### Bölüm 2: Kaçınılmaz Gerçek - Örnekleme Hatası

Kaşığınızdaki çorbanın tadı, kazanın genel tadına çok yakın olabilir ama **asla birebir aynısı olmayacaktır**. Belki sizin kaşığınıza şans eseri bir tane fazla havuç veya bir tane eksik karabiber tanesi denk geldi. İşte bu küçük farka **Örnekleme Hatası (Sampling Error)** denir. Bu bir "hata" olmasına rağmen, kötü bir şey değildir; örneklemeyle çalışmanın doğal bir sonucudur.

* **Nasıl Azaltılır?** Daha büyük bir kaşık kullanarak! Yani, **örneklem boyutunu artırarak** örnekleme hatasını azaltabiliriz.

---

### Bölüm 3: Kaşığı Kazana Nasıl Daldırırsın? (Örnekleme Yöntemleri)

Doğru bir çıkarım yapabilmek (çorbanın tadını doğru tahmin edebilmek) için kaşığı kazana doğru bir şekilde daldırmak gerekir. İşte görsellerde anlatılan temel yöntemler:

1.  **Basit Rastgele Örnekleme (Simple Random Sampling)**
    * **Ne Olduğu:** Popülasyondaki her bireyin seçilme şansının eşit olduğu yöntem.
    * **Çorba Metaforu:** Gözlerinizi kapatıp, kaşığı kazanın **herhangi bir yerine rastgele** daldırmak. Bu, çorbanın her yerinin iyi karıştığını varsayar.

2.  **Sistematik Örnekleme (Systematic Sampling)**
    * **Ne Olduğu:** Popülasyon bir listeye dizilir ve her *k*-ıncı eleman seçilir (örn: her 10. kişi).
    * **Çorba Metaforu:** Çorbayı karıştırırken, **her 5 turda bir, bir kaşık** almak.

3.  **Tabakalı Örnekleme (Stratified Sampling)**
    * **Ne Olduğu:** Popülasyon, kendi içinde homojen olan alt gruplara (tabakalara) ayrılır ve **her bir tabakanın içinden rastgele** örnekler alınır.
    * **Çorba Metaforu:** Çorbanızın üç ayrı katmandan (tabakadan) oluştuğunu düşünün: en altta etler, ortada sebzeler, en üstte de suyu var. Çorbanın tam tadını alabilmek için kaşığınızı **her üç katmandan da geçecek şekilde daldırarak** her bileşenden bir parça alırsınız. Bu, popülasyonun tüm segmentlerinin temsil edilmesini sağlar.

4.  **Küme Örneklemesi (Cluster Sampling)**
    * **Ne Olduğu:** Popülasyon, coğrafi veya mantıksal kümelere ayrılır ve bu kümelerden birkaçı **rastgele seçilerek, seçilen kümelerin içindeki herkes** analize dahil edilir.
    * **Çorba Metaforu:** Çorbanızın içinde birçok küçük **mantı (küme)** olduğunu düşünün. Çorbanın tadına bakmak için rastgele **birkaç tane mantıyı bütün olarak** seçip tadına bakarsınız.
  
  #### Karşılaştırmalı Özet Tablo: Örnekleme Yöntemleri

| Yöntem | Temel Fikir | Çorba Metaforu | Ne Zaman İdealdir? |
| :--- | :--- | :--- | :--- |
| **Basit Rastgele** | Herkesin eşit şansı var. | Gözü kapalı, rastgele bir yerden kaşık almak. | Popülasyon homojen olduğunda ve tam bir liste mevcutsa. |
| **Sistematik** | Belirli bir aralıkla seçim yapılır. | Her 5 karıştırmada bir kaşık almak. | Popülasyon sıralı bir listede olduğunda ve periyodik bir desen yoksa. |
| **Tabakalı** | Her alt gruptan örnek alınır. | Kaşığı çorbanın tüm katmanlarından geçirmek. | Popülasyonda önemli ve belirgin alt gruplar (kadın/erkek, yaş grupları) varsa. |
| **Küme** | Bütün alt gruplar örnek olarak alınır. | Birkaç tane mantıyı bütün olarak seçip tatmak. | Popülasyon coğrafi olarak çok dağınık olduğunda ve bireylere tek tek ulaşmak zorsa. |
