# Permütasyon ve Kombinasyon Problemleri

Aşağıda, kombinatorik alanında sıkça karşılaşılan permütasyon ve kombinasyon problemlerine dair çözümler bulunmaktadır.

---

### 1. 7 koşucunun bir yarışta ilk 3 sıraya kaç farklı şekilde yerleşebileceği?

Bu, bir **permütasyon (sıralama)** problemidir, çünkü ilk 3 pozisyondaki sıralama önemlidir. (Örneğin, 1. Ayşe, 2. Bora farklı bir sonuçtur; 1. Bora, 2. Ayşe farklı bir sonuçtur.)

Permütasyon formülü $P(n, k) = \frac{n!}{(n-k)!}$ şeklindedir.
Burada $n=7$ (toplam koşucu sayısı) ve $k=3$ (ilk 3 pozisyon) olarak verilmiştir.

**Hesaplama:**
$$P(7, 3) = \frac{7!}{(7-3)!} = \frac{7!}{4!} = 7 \times 6 \times 5 = 210$$

Yani, 7 koşucu bir yarışta ilk 3 sıraya **210** farklı şekilde yerleşebilir.

---

### 2. A, B, C, D, E harfleri kullanılarak, tekrar etmeden kaç farklı 5 harfli şifre oluşturulabilir?

Bu da bir **permütasyon (sıralama)** problemidir, çünkü bir şifrede harflerin sırası önemlidir ve tekrar yoktur.

Toplam 5 harf (A, B, C, D, E) var ve 5 harfli bir şifre oluşturulacak. Tekrar olmadığı için her harf sadece bir kez kullanılabilir.

Bunu hesaplamanın iki yolu vardır:

**Yol 1: Çarpım Kuralı**
* İlk konum için 5 seçeneğiniz var.
* İkinci konum için kalan 4 seçeneğiniz var.
* Üçüncü konum için kalan 3 seçeneğiniz var.
* Dördüncü konum için kalan 2 seçeneğiniz var.
* Beşinci konum için kalan 1 seçeneğiniz var.

Toplam yol sayısı:
$$5 \times 4 \times 3 \times 2 \times 1 = 120$$

**Yol 2: Permütasyon Formülü**
Bu, $n$ farklı öğenin tümünün sıralandığı özel bir permütasyon durumudur, yani $P(n, n) = n!$.
Burada $n=5$ olduğundan:
$$P(5, 5) = 5! = 120$$

Yani, 5 harf kullanılarak, tekrar etmeden **120** farklı 5 harfli şifre oluşturulabilir.

---

### 3. 10 kişilik bir gruptan 4 kişilik bir takım kaç farklı şekilde oluşturulabilir?

Bu bir **kombinasyon** problemidir, çünkü bir takım oluşturulurken kişilerin seçilme sırası önemli değildir; önemli olan takımın kendisidir. Yani, "Ayşe, Bora, Cem, Derya" takımını seçmek ile "Bora, Ayşe, Derya, Cem" takımını seçmek aynı takımdır.

Kombinasyon formülü $C(n, k) = \binom{n}{k} = \frac{n!}{k!(n-k)!}$ şeklindedir.
Burada $n=10$ (toplam kişi sayısı) ve $k=4$ (takıma seçilecek kişi sayısı) olarak verilmiştir.

**Hesaplama:**
$$C(10, 4) = \frac{10!}{4!(10-4)!} = \frac{10!}{4!6!}$$

Faktöriyelleri açalım ve sadeleştirelim:
$$C(10, 4) = \frac{10 \times 9 \times 8 \times 7 \times 6!}{4! \times 6!} = \frac{10 \times 9 \times 8 \times 7}{4 \times 3 \times 2 \times 1}$$
$$C(10, 4) = \frac{5040}{24}$$

Sadeleştirmeleri yapalım:
$$C(10, 4) = 10 \times 3 \times 7 = 210$$

Yani, 10 kişilik bir gruptan **210** farklı 4 kişilik takım oluşturulabilir.

---

### 4. Bir torbada 6 farklı renk top bulunmaktadır. Bu 6 topun hepsini çekip bir sıraya kaç farklı şekilde dizebilirsiniz?

Bu bir **permütasyon (sıralama)** problemidir, çünkü topları hem çekiyor hem de **bir sıra halinde düzenliyorsunuz**, bu da sıranın önemli olduğu anlamına gelir. Ayrıca, 6 farklı top olduğu ve tüm 6 topu düzenlediğiniz belirtiliyor.

Toplam $n=6$ farklı top var ve bu 6 topun hepsini sıralamak istiyoruz ($k=6$).

Bu, $n$ farklı öğenin tümünün sıralanması durumudur ve $n!$ (n faktöriyel) ile hesaplanır.

**Hesaplama:**
$$6! = 6 \times 5 \times 4 \times 3 \times 2 \times 1 = 720$$

Yani, 6 farklı topu çekip bir sıraya **720** farklı şekilde dizebilirsiniz.

---

### 5. 52 kartlık bir desteden, bir iskambil oyununda eliniz için 5 kartı kaç farklı şekilde seçebilirsiniz?

Bu bir **kombinasyon** problemidir, çünkü bir kart oyununda elinize gelen 5 kartın sırası önemli değildir; önemli olan hangi 5 kartın elinizde olduğudur.

Kombinasyon formülü $C(n, k) = \binom{n}{k} = \frac{n!}{k!(n-k)!}$ şeklindedir.
Burada $n=52$ (toplam kart sayısı) ve $k=5$ (seçilecek kart sayısı) olarak verilmiştir.

**Hesaplama:**
$$C(52, 5) = \frac{52!}{5!(52-5)!} = \frac{52!}{5!47!}$$

Faktöriyelleri açıp sadeleştirelim:
$$C(52, 5) = \frac{52 \times 51 \times 50 \times 49 \times 48 \times 47!}{5 \times 4 \times 3 \times 2 \times 1 \times 47!}$$
$$C(52, 5) = \frac{52 \times 51 \times 50 \times 49 \times 48}{5 \times 4 \times 3 \times 2 \times 1}$$

Paydadaki değer: $5 \times 4 \times 3 \times 2 \times 1 = 120$.

Şimdi sadeleştirmeleri yapalım:
* $\frac{50}{5 \times 2} = \frac{50}{10} = 5$
* $\frac{48}{4 \times 3} = \frac{48}{12} = 4$
* $\frac{51}{1} \rightarrow \text{Bu adımda sadeleştirme için 3'ü kullanabiliriz, 51/3 = 17.}$

Yani çarpım:
$$C(52, 5) = 52 \times \frac{51}{3} \times \frac{50}{5 \times 2} \times 49 \times \frac{48}{4}$$
$$C(52, 5) = 52 \times 17 \times 5 \times 49 \times 4$$

Bu çarpımın sonucu:
$$C(52, 5) = 2,598,960$$

Yani, 52 kartlık bir desteden, bir iskambil oyununda eliniz için **2,598,960** farklı şekilde 5 kart seçebilirsiniz.
