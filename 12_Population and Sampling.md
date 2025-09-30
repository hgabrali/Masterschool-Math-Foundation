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


<img width="805" height="168" alt="image" src="https://github.com/user-attachments/assets/d187af7c-72ff-4f7b-baa9-e616ae7780d2" />

Sayısal bir sonuç bekleyen bir problemden çok, istatistiksel bir problemin **nasıl çözüleceğine dair bir yol haritası (süreç)** sunuyor.

Bu örneğin "çözümü", bir sonuç bulmak değil, doğru adımları izleyerek o sonuca nasıl ulaşılacağını planlamaktır. Gelin bu süreci adım adım, pratik bir şekilde ele alalım.

---

### Problemin Analizi

* **Popülasyon:** Üniversitedeki 1,000 öğrencinin tamamı.
* **Bilmek İstediğimiz Değer (Popülasyon Parametresi):** Bu 1,000 öğrencinin *gerçek* boy ortalaması ($\mu$).
* **Zorluk:** Herkesi tek tek ölçmek çok zor (zaman, maliyet, lojistik).
* **Önerilen Çözüm:** Daha küçük bir grup olan 100 kişilik bir **örneklem** seçmek ve bu grubun ortalamasını ($\bar{x}$) kullanarak tüm üniversite hakkında bir **tahmin (çıkarım)** yapmak.

---

### Çözüm Süreci: Adım Adım İlerleme

Bu problemi çözmek için izlenmesi gereken adımlar şunlardır:

#### Adım 1: Doğru Örnekleme Yöntemini Seçmek

Bu, **en kritik adımdır**. Eğer 100 kişilik örnekleminiz tüm üniversiteyi iyi temsil etmezse, tahmininiz tamamen yanlış olabilir. (Örneğin, sadece basketbol takımından 100 kişi seçerseniz, ortalama boy çok yüksek çıkar!)

Burada birkaç yöntem düşünülebilir:

* **Basit Rastgele Örnekleme:** En kolayı. 1,000 öğrencinin hepsinin ismini bir listeye yazıp, tamamen rastgele 100 kişi seçersiniz. Herkesin eşit şansı vardır.
* **Tabakalı Örnekleme (En İyi Yöntem):** Daha doğru bir sonuç için bu yöntem daha iyidir. Üniversiteyi doğal alt gruplara (yani **tabakalara**) ayırırsınız. Örneğin:
    * Fakültelere göre (Mühendislik, Tıp, Sosyal Bilimler vb.)
    * Cinsiyete göre (Kadın/Erkek)
    * Sınıf seviyelerine göre (1. sınıf, 2. sınıf vb.)

    Sonra, her bir tabakadan, o tabakanın popülasyondaki oranı kadar rastgele öğrenci seçersiniz. Mesela üniversitenin %60'ı kadın, %40'ı erkek ise; 100 kişilik örnekleminizin 60'ını kadınlardan, 40'ını erkeklerden rastgele seçersiniz. Bu, örnekleminizin popülasyonun demografik yapısını yansıtmasını sağlar.

#### Adım 2: Veriyi Toplamak

Seçtiğiniz 100 öğrenciyi bulup boylarını tek tek ölçersiniz. Elinizde artık 100 adet boy verisi olur.

#### Adım 3: Örneklem İstatistiğini Hesaplamak

Topladığınız 100 boy verisinin aritmetik ortalamasını alırsınız. Bu, sizin **örneklem ortalamanızdır ($\bar{x}$)**.

* **Örnek Hesaplama:** Diyelim ki 100 öğrencinin boylarını ölçtünüz ve ortalamasını **172.5 cm** buldunuz. `$\bar{x}$ = 172.5 cm`

#### Adım 4: Çıkarım Yapmak ve Sonucu Raporlamak

Bu adımda, kaşığınızdaki çorbanın tadına bakıp (örneklem), bütün kazan (popülasyon) hakkında bir yorum yaparsınız.

* **Nokta Tahmini (Point Estimate):** En basit tahmin, "Örneklem ortalamamız 172.5 cm olduğuna göre, 1,000 öğrencinin tamamının ortalama boyunun da yaklaşık 172.5 cm olduğunu tahmin ediyoruz" demektir.
* **Daha İyi Yöntem: Güven Aralığı (Confidence Interval):** İstatistikte tek bir sayı vermek yerine, bir "hata payı" ekleyerek bir aralık vermek çok daha doğrudur. Çünkü örneklememizin şans eseri biraz daha uzun veya kısa kişilerden oluşmuş olabileceğini biliriz. Şöyle bir sonuç raporlanır:
    > "Yaptığımız analize göre, üniversitedeki 1,000 öğrencinin gerçek boy ortalamasının **%95 güvenle 170.5 cm ile 174.5 cm arasında** olduğunu tahmin ediyoruz."

    Bu aralığa **Güven Aralığı** denir ve tahminimizin ne kadar kesin olduğu hakkında bir fikir verir. Bu, istatistiksel çıkarımın en güçlü yönüdür.

---

### Özetle Çözüm

Bu örnek, şu 4 adımlı süreç ile "çözülür":

1.  **Planla:** Popülasyonu en iyi temsil edecek örnekleme yöntemini (örn: Tabakalı Örnekleme) seç.
2.  **Uygula:** Seçilen 100 öğrencinin boy verisini topla.
3.  **Hesapla:** Toplanan verinin ortalamasını ($\bar{x}$) bul.
4.  **Tahmin Et:** Bulunan örneklem ortalamasını kullanarak, popülasyon ortalaması ($\mu$) için bir tahmin (tercihen bir güven aralığı ile) raporla.

