# Normal Distribution

[Normal Distribution_Z-score-Codes](https://colab.research.google.com/drive/1jOaCghd9WhzMZOFUEfcvxxHEBH0Yo1h5#scrollTo=YUu0BJve-orF)


<img width="770" height="163" alt="image" src="https://github.com/user-attachments/assets/c49e213f-1f6a-4168-9b79-764e94674514" />

<img width="681" height="356" alt="image" src="https://github.com/user-attachments/assets/b0f4ed9a-aafa-412a-bfb7-f42b36530fc4" />

<img width="802" height="354" alt="image" src="https://github.com/user-attachments/assets/f560f8d2-a4ef-43d8-b638-f4deb30d04ec" />

<img width="687" height="331" alt="image" src="https://github.com/user-attachments/assets/62e00ab0-bcee-456b-a4a4-5357b5ca9677" />

<img width="708" height="241" alt="image" src="https://github.com/user-attachments/assets/13741dde-1755-42ff-acf7-4749b3e2a1a5" />

<img width="761" height="215" alt="image" src="https://github.com/user-attachments/assets/186a663d-41c8-4be8-b4f8-b93bd602f110" />

<img width="409" height="560" alt="image" src="https://github.com/user-attachments/assets/ba416e68-d1a0-4ac0-858a-0c37628f0173" />

<img width="769" height="332" alt="image" src="https://github.com/user-attachments/assets/d45caa67-565b-4ce7-91d4-0cafe818deb8" />

---


## Genel Bakış: İstatistiksel Bir Doğa Kanunu - Normal Dağılım

Normal Dağılım (veya Gauss Dağılımı), doğada ve insan hayatında o kadar sık karşımıza çıkar ki adeta bir doğa kanunu gibidir. İnsanların boyları, sınav notları, ölçüm hataları gibi birçok şey bu "Çan Eğrisi" şeklindeki dağılıma uyar.

Bu konuyu iki ana bölümde ele alacağız:

1.  **Normal Dağılımın Anatomisi:** Bu "Çan Eğrisi" ne anlama geliyor ve onu ne şekillendiriyor?
2.  **Python ile Gücü Kullanmak:** `scipy.stats.norm` kütüphanesini kullanarak bu teoriyi nasıl koda dökeriz?

### Bölüm 1: Normal Dağılımın Anatomisi (Bir Olasılık Dağı)

Normal dağılım eğrisini bir **olasılık dağı** gibi hayal edelim. Bu dağın şekli, bize her şeyin sırrını veren iki temel parametre tarafından yönetilir:

#### 1. Ortalama ($\mu$) - Dağın Konumu

* **Ne Olduğu:** Ortalama, dağılımın merkezidir. Verilerin etrafında toplandığı "ağırlık merkezi" veya en tepe noktasıdır.
* **Metafor:** Ortalama ($\mu$), olasılık dağımızın **nerede bulunduğunu** belirler. Eğer bir grup insanın ortalama boyu 175 cm ise, dağımızın zirvesi tam olarak 175 noktasındadır. Ortalama 180'e çıkarsa, dağımız sayı doğrusu üzerinde sağa doğru kayar.
* **Görseldeki Karşılaştırma:** İlk grafikteki gibi, ortalamayı değiştirmek dağı **sola veya sağa** kaydırır, ancak şeklini değiştirmez.

#### 2. Standart Sapma ($\sigma$) - Dağın Şekli

* **Ne Olduğu:** Standart sapma, verilerin ortalama etrafında ne kadar yayıldığının bir ölçüsüdür.
* **Metafor:** Standart sapma ($\sigma$), dağımızın ne kadar **sivri ve dar** veya ne kadar **yayvan ve basık** olduğunu belirler.
* **Düşük Standart Sapma:** Veriler ortalamaya çok yakındır. Bu, Everest gibi **sivri ve dar** bir dağ demektir. (Örn: Bir sınıftaki herkesin notu 70-80 arasındaysa).
* **Yüksek Standart Sapma:** Veriler geniş bir alana yayılmıştır. Bu, Ağrı Dağı gibi **geniş ve basık** bir dağ demektir. (Örn: Sınıfta 20 alan da 100 alan da varsa).
* **Görseldeki Karşılaştırma:** İkinci grafikteki gibi, standart sapmayı değiştirmek dağı **sivrileştirir veya basıklaştırır**, ancak merkezini değiştirmez.

### Bölüm 2: Python ile Gücü Kullanmak (`scipy.stats.norm`)

Bu olasılık dağını elle çizmek veya hesaplamak yerine, Python'daki `scipy` kütüphanesi bize bu dağılım için adeta bir **İsviçre çakısı** sunar: `scipy.stats.norm`. Bu araç setindeki temel fonksiyonları ve ne işe yaradıklarını inceleyelim.

#### Karşılaştırmalı Fonksiyonlar Tablosu

| Fonksiyon (Method) | Metaforik Adı | Cevapladığı Soru | Açıklama |
| :--- | :--- | :--- | :--- |
| `norm.pdf(x)` | **Yükseklik Ölçer** | "Tam `x` noktasında dağın yüksekliği (olasılık yoğunluğu) nedir?" | Bir noktanın doğrudan olasılığını vermez ama o bölgedeki olasılık yoğunluğunu gösterir. En yüksek değer dağın zirvesindedir. |
| `norm.cdf(x)` | **Alan Hesaplayıcı** | "`x` değerinden daha düşük bir sonuç alma olasılığım nedir?" | `x` noktasına kadar olan eğrinin altındaki toplam alanı (kümülatif olasılığı) hesaplar. İki değer *arasındaki* olasılığı bulmak için de bu fonksiyonu kullanırız. |
| `norm.ppf(q)` | **Ters Harita** | "Dağın en düşük %`q`'luk kısmını kapsayan `x` değeri nedir?" | Bir olasılık (alan) verirsiniz, o size o alana karşılık gelen `x` değerini söyler. Örneğin, "ilk %5'lik dilime giren not kaçtır?" sorusunun cevabıdır. |
| `norm.rvs(size=n)`| **Örneklem Jeneratörü** | "Bu dağın şekline uygun `n` tane rastgele örnek veri oluştur." | Bu dağılıma uyan rastgele sayılar üretir. Simülasyonlar için paha biçilmezdir. |

#### Pratik Örnekler

Diyelim ki bir sınıftaki notların ortalaması ($\mu$) **70**, standart sapması ($\sigma$) **10** olsun.

* **Soru 1: 80 puan civarındaki olasılık yoğunluğu nedir? (`pdf`)**
    * ```python
        norm.pdf(x=80, loc=70, scale=10)
        ```
    * Bu, çan eğrisinin 80 noktasındaki yüksekliğini verir.

* **Soru 2: Sınavdan 85'ten daha düşük not alma olasılığı nedir? (`cdf`)**
    * ```python
        norm.cdf(x=85, loc=70, scale=10)
        ```
    * Bu, 85'e kadar olan tüm alanın toplamını verir; yani öğrencilerin büyük bir yüzdesini.

* **Soru 3: Sınıfın en başarılı %10'luk dilimine girmek için en az kaç almak gerekir? (`ppf`)**
    * En başarılı %10, en düşük %90'ın üzerindedir. O zaman %90'lık sınırı buluruz.
    * ```python
        norm.ppf(q=0.90, loc=70, scale=10)
        ```
    * Bu fonksiyon size, örneğin, "82.8'den yüksek alanlar en başarılı %10'dadır" gibi bir sonuç verecektir.

* **Soru 4: Bu sınıfa benzer 5 kişilik rastgele bir öğrenci grubu oluştursak notları ne olurdu? (`rvs`)**
    * ```python
        norm.rvs(loc=70, scale=10, size=5)
        ```
    * Size `[75, 62, 81, 70, 68]` gibi ortalaması 70 civarında olan 5 rastgele not üretecektir.
