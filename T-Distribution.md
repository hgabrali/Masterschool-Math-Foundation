# T-Distribution

[T-Distribution](https://colab.research.google.com/drive/1WC1F_PmLMNT99usidQHluykxCKRJsJxP#scrollTo=kUgw7xk1PUYg)

<img width="745" height="524" alt="image" src="https://github.com/user-attachments/assets/0781dc48-b180-4285-b4c0-ac01b375352c" />

<img width="772" height="646" alt="image" src="https://github.com/user-attachments/assets/319290b3-27e7-4167-bc07-76fd7c5c2ec5" />

<img width="749" height="332" alt="image" src="https://github.com/user-attachments/assets/e8f13bd2-dfa9-4c18-8dff-d83854527321" />

<img width="818" height="721" alt="image" src="https://github.com/user-attachments/assets/3c8baba8-f50f-460b-a35b-24986ff9556e" />


# Grafik Yorumu:

<img width="482" height="355" alt="image" src="https://github.com/user-attachments/assets/18d4f9ac-3c15-43a2-9df3-1f7cdbb04fd2" />

Bu grafik, **Normal (Z) Dağılımı** ile onun "**ihtiyatlı kuzeni**" olan **t-Dağılımı** arasındaki temel farkı görsel olarak mükemmel bir şekilde özetliyor. Verdiğiniz metindeki karakteristikleri kullanarak bu grafiği detaylı bir şekilde analiz edip yorumlayalım.

---

### Genel Bakış: İdeal Model vs. Gerçekçi Tahmin

Bu grafiğe bakarken şu hikayeyi düşünebiliriz:

* **Normal Dağılım (Mavi Çizgi):** Bu, popülasyon hakkında her şeyi (özellikle standart sapmasını, $\sigma$) bildiğimiz **ideal ve mükemmel** bir dünyayı temsil eder.
* **t-Dağılımı (Kırmızı Çizgi):** Bu ise, popülasyon standart sapmasını bilmediğimiz ve onu küçük bir örneklemden tahmin etmek zorunda kaldığımız **gerçekçi ama daha belirsiz** bir dünyayı temsil eder.

Grafik, bu "ekstra belirsizliğin" dağılımın şeklini nasıl değiştirdiğini gösterir.

---

### Grafik Analizi ve Yorumu

#### 1. Şekil: Benzer Aile, Farklı Bireyler

Metinde de belirtildiği gibi, her iki dağılım da **simetrik ve çan şeklindedir**. Grafiğe baktığımızda ikisinin de merkezinin 0 olduğunu ve her iki yana doğru simetrik bir şekilde azaldığını görüyoruz. Bu, t-dağılımının normal dağılım ailesinin bir üyesi olduğunu, ancak kendine özgü farklılıkları olduğunu gösterir.

#### 2. Kalın Kuyruklar (Heavier Tails): En Önemli Fark

Bu, grafikteki en çarpıcı ve en önemli özelliktir.

* **Grafikte Ne Görüyoruz?**
    * **Merkezde:** Kırmızı çizgi (t-Dağılımı), mavi çizgiden (Normal Dağılım) **daha basıktır**.
    * **Kuyruklarda:** Grafiğin uçlarına doğru (örneğin, -2'den küçük ve +2'den büyük bölgelerde), kırmızı çizgi mavi çizgiden **daha yüksektir**.

* **Bu Ne Anlama Geliyor? (Yorum)**
    Metindeki alıntı bunun görsel kanıtıdır:
    > "The t-distribution has heavier tails"

    "Kalın kuyruklar", **aşırı değerlerin (uç noktaların) t-dağılımında normal dağılıma göre daha olası olduğu** anlamına gelir.

* **Metafor:**
    > Bir zar attığınızı düşünün. Normal dağılım, hilesiz bir zar gibidir; 1 veya 6 gibi uç değerler gelir ama çoğunlukla orta değerler beklenir. Düşük serbestlik dereceli bir t-dağılımı ise, kenarları biraz daha ağırlaştırılmış bir zar gibidir; 1 veya 6 gelme ihtimali, yani **sürpriz bir sonuçla karşılaşma ihtimali** biraz daha fazladır. Bunun nedeni, küçük bir örneklemle çalışmanın getirdiği ekstra belirsizliktir.

#### 3. Serbestlik Derecesi (Degrees of Freedom - DF): Dağılımın Kaderini Belirleyen Faktör

* **Grafikte Ne Görüyoruz?**
  Kırmızı çizgi, özellikle **2 serbestlik derecesi (2 DF)** için çizilmiştir. Bu, çok küçük bir örneklemden (`$n = 3$`) geldiği anlamına gelir.

* **Bu Ne Anlama Geliyor? (Yorum)**
  Serbestlik derecesi (`df`), t-dağılımının normal dağılıma ne kadar benzeyeceğini belirleyen bir **ayar düğmesi** gibidir.
    * **Düşük `df` (Grafikteki Durum):** Örneklem boyutu küçük olduğunda (`$n$` küçük, dolayısıyla `df` düşük), popülasyonu tahmin etmedeki belirsizliğimiz çok yüksektir. t-dağılımı bu belirsizliği hesaba katmak için **kalın kuyruklu ve basık** hale gelir. Yani, "beklenmedik" sonuçlara daha fazla olasılık tanır.
    * **Yüksek `df`:** Örneklem boyutunu artırdıkça (`$n$` büyüdükçe, `df` de artar), tahminlerimizdeki belirsizlik azalır. Bu durumda t-dağılımının kuyrukları incelir, merkezi yükselir ve **giderek normal dağılıma (mavi çizgiye) yakınsar**. Genellikle `df > 30` olduğunda, t-dağılımı ile normal dağılım arasındaki fark neredeyse ayırt edilemez hale gelir.

Bu grafik, küçük örneklemlerle çalışırken neden t-dağılımını kullandığımızı özetler: t-dağılımı, bilmediğimiz popülasyon standart sapmasından kaynaklanan **ekstra belirsizliği** hesaba katan, daha **ihtiyatlı ve gerçekçi** bir modeldir.

---

### Ana Metafor: Uzman Rehber (Z) ve İhtiyatlı Gözcü (t)

Bilinmeyen bir hazineyi ( **popülasyonun gerçek ortalaması, $\mu$** ) aradığımızı hayal edelim. Bu arayışta bize iki farklı karakter yardımcı olabilir:

* **Normal (Z) Dağılımı - Uzman Rehber: 🗺️**
  Bu rehber, tüm bölgeyi avucunun içi gibi bilir. Bölgenin genel arazi değişkenliğini ( **popülasyon standart sapması, $\sigma$** ) gösteren mükemmel bir uydu haritasına sahiptir. Kendinden emindir ve hazinenin yerini tahmin ederken dar ve hassas bir arama alanı (güven aralığı) çizer.

* **t-Dağılımı - İhtiyatlı Gözcü: 🧭**
  Bu gözcü, tüm bölgenin haritasına sahip değildir. Yalnızca kendi gezdiği küçük bir alanın ( **örneklem** ) değişkenliğini ( **örneklem standart sapması, $s$** ) bilir. Bilgisinin eksik olduğunun farkındadır, bu yüzden daha **ihtiyatlı ve şüphecidir**.

İşte t-dağılımı, bu "ihtiyatlı gözcünün" haritasıdır.

---

### t-Dağılımının Karakteristikleri (Gözcünün Haritasının Özellikleri)

Metinde belirtilen özellikleri, metaforumuzla birleştirelim:

#### 1. Şekil: Aile Benzerliği

Hem uzman rehberin haritası hem de ihtiyatlı gözcünün haritası, hedefin merkezde olduğu **simetrik ve çan şeklinde** bir arama deseni kullanır. Bu, t-dağılımının da normal dağılım gibi davrandığını, ancak önemli farkları olduğunu gösterir.

#### 2. Kalın Kuyruklar (Heavier Tails): Genişletilmiş Arama Alanı

Bu, iki karakter arasındaki en temel farktır.

* **Anlamı:** İhtiyatlı Gözcü (t-dağılımı), bilgisindeki belirsizlikten dolayı daha temkinlidir. Bu yüzden arama alanının kenarlarına ( **kuyruklara** ) daha fazla pay bırakır.
    > "Hazine tam merkezde olmayabilir, biraz daha uç noktalarda olma ihtimali, uzman rehberin düşündüğünden biraz daha fazla."
    İşte bu "uç noktalara daha fazla olasılık tanıma" durumu, grafikte **kalın kuyruklar** olarak görünür.
* **Sonucu:** Bu ihtiyat, t-dağılımı ile oluşturulan güven aralıklarının Z-dağılımına göre **biraz daha geniş** olmasına neden olur. Bu, belirsizliğe karşı ödediğimiz bir bedeldir.

#### 3. Serbestlik Derecesi (Degrees of Freedom - DF): Gözcünün Deneyimi

Serbestlik derecesi (`df = n-1`), gözcümüzün ne kadar "deneyimli" olduğunu gösterir.

* **Düşük `df` (Acemi Gözcü):** Gözcü çok küçük bir alanı (`$n$` küçük) gezmişse, belirsizliği çok yüksektir. Bu yüzden haritası çok kalın kuyruklu ve basıktır. Çok geniş bir arama alanı çizer.
* **Yüksek `df` (Deneyimli Gözcü):** Gözcü çok büyük bir alanı (`$n$` büyük, örn: `$n > 30$`) gezmişse, artık bölgenin genel değişkenliği hakkında oldukça iyi bir fikri vardır. Tahminlerindeki belirsizlik azalır. Bu noktada gözcünün haritası, uzman rehberin haritasına o kadar çok benzer ki, aradaki fark neredeyse kaybolur.
* **Sonuç:** **Serbestlik derecesi arttıkça, t-dağılımı normal dağılıma yakınsar.**

### Hangi Haritayı Ne Zaman Kullanmalıyız? (Karşılaştırma Tablosu)

İşte karar verme sürecinizi basitleştirecek bir tablo:

| Durum | Popülasyon Standart Sapması ($\sigma$) | Örneklem Boyutu ($n$) | Kullanılacak Dağılım | Gerekçe |
| :--- | :--- | :--- | :--- | :--- |
| **İdeal Dünya** | **Biliniyor** | Fark etmez | **Normal (Z) Dağılımı** | Elimizde mükemmel bilgi (Uzman Rehber) var. |
| **Gerçek Dünya (Büyük Örneklem)** | Bilinmiyor | **Büyük** (`$n \ge 30$`) | **Normal (Z) Dağılımı** | Gözcü artık çok deneyimli (`df` yüksek) olduğu için haritası uzmanınkine çok benzer. |
| **Gerçek Dünya (Küçük Örneklem)**| Bilinmiyor | **Küçük** (`$n < 30$`) | **t-Dağılımı** | Gözcü acemi (`df` düşük) ve haritasındaki ekstra belirsizliği hesaba katmalıyız. |

---

### Özetle

**t-Dağılımı**, istatistiğin **"gerçek dünya" aracıdır**. Popülasyon hakkında tam bilgiye sahip olmadığımız (ki bu neredeyse her zaman geçerlidir) ve özellikle küçük veri setleriyle çalıştığımız durumlarda, tahminlerimize anlamlı bir **ihtiyat payı** ekleyerek daha dürüst ve güvenilir sonuçlar elde etmemizi sağlar.

---

<img width="672" height="129" alt="image" src="https://github.com/user-attachments/assets/06555c2a-69f3-4a13-a678-4e686e81c635" />

Bu şema, bir popülasyon ortalaması hakkında istatistiksel çıkarım yaparken (örneğin güven aralığı veya hipotez testi için) **Z-dağılımı mı yoksa t-dağılımı mı** kullanmanız gerektiğini belirleyen bir karar akış şemasıdır. 🧠

Bu, istatistikte doğru aracı seçmek için kullanılan pratik bir yol haritasıdır.

---

### Karar Verme Süreci Adım Adım

Şema, size üç kritik soru sorarak doğru yola yönlendirir:

#### Soru 1: Popülasyon Standart Sapması ($\sigma$) Biliniyor mu?

Bu, yolculuğun ilk ve en önemli yol ayrımıdır.

* **Evet ise ✅ → Z-Dağılımı Kullan**
    * Eğer popülasyonun standart sapmasını biliyorsanız, bu "ideal" bir durumdur. Örneklem boyutunuz ne olursa olsun, her zaman **Z-dağılımını** kullanabilirsiniz.

* **Hayır ise ❌ → Soru 2'ye Geç**
    * Gerçek hayatta popülasyonun standart sapmasını neredeyse hiçbir zaman bilmeyiz. Bu çok daha yaygın bir senaryodur. Bu durumda, bir sonraki soruya geçmelisiniz.

#### Soru 2: Örneklem Boyutu ($n$) Yeterince Büyük mü? (Genellikle `n > 30`)

Popülasyon standart sapmasını bilmediğiniz için, örnekleminizin büyüklüğü kritik hale gelir.

* **Evet ise ✅ → Z-Dağılımı Kullan**
    * Örneklem boyutunuz yeterince büyükse (genellikle 30'dan fazla kabul edilir), **Merkezi Limit Teoremi** sayesinde örneklem standart sapması ($s$), popülasyon standart sapmasının ($\sigma$) oldukça güvenilir bir tahmini haline gelir. Bu nedenle, pratikte yine **Z-dağılımını** kullanabilirsiniz.

* **Hayır ise ❌ → Soru 3'e Geç**
    * Eğer örneklem boyutunuz küçükse (30'dan az), belirsizlik artar. Bu durumda son bir kontrol daha yapmanız gerekir.

#### Soru 3: Popülasyon Normal Dağılıma Sahip mi?

Küçük bir örneklemle çalışırken, ana popülasyonun şekli önem kazanır.

* **Evet ise ✅ → t-Dağılımı Kullan**
    * Eğer örnekleminiz küçükse, popülasyon standart sapmasını bilmiyorsanız **AMA** popülasyonun normal dağıldığını biliyorsanız (veya varsayabiliyorsanız), o zaman **t-dağılımı** sizin için doğru araçtır. t-dağılımı, küçük örneklemlerin getirdiği ekstra belirsizliği hesaba katmak için tasarlanmıştır.

* **Hayır ise ❌ → Başka Yöntemler Kullan**
    * Eğer bu üç koşulun hiçbiri sağlanmıyorsa (popülasyon $\sigma$'sı bilinmiyor, örneklem küçük VE popülasyon normal dağılmıyor), Z veya t-dağılımını kullanamazsınız. Bu durumda, **parametrik olmayan testler (non-parametric tests)** gibi başka istatistiksel yöntemlere başvurmanız gerekir.

---

### Özetle

Bu şema, şu pratik kuralları özetler:

* **Z-Dağılımı:** "İdeal" veya "büyük örneklemli" senaryolar için.
* **t-Dağılımı:** "Küçük örneklemli, belirsiz ama düzenli" senaryolar için.
* **Diğer Yöntemler:** "Küçük örneklemli, belirsiz ve düzensiz" senaryolar için.

