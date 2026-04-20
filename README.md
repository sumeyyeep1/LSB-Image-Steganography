# 🛡️ LSB Image Steganography
## Yazılım Güvenliği Dersi Dönem Ödevi — Python ile Görsel Tabanlı Stenografi Uygulaması

### 📌 Proje Hakkında
Bu proje, **LSB (Least Significant Bit)** yöntemi kullanarak bir görsel dosyasının piksel verilerine gizli metin mesajı gömmek ve bu mesajı geri çıkarmak amacıyla geliştirilmiştir. Proje, özellikle **Google Colab** ortamında çalışacak şekilde optimize edilmiştir.

---

### 🧠 Stenografi Nedir?
Stenografi, bir bilginin (metin, ses, görsel vb.) başka bir bilginin içine gizlenerek iletilmesini inceleyen bilim dalıdır. 

> **Kriptografiden Farkı:** Kriptografi verinin içeriğini şifreleyerek okunmaz hale getirirken; stenografi, verinin var olduğunu tamamen gizleyerek dikkat çekmemeyi amaçlar.

#### LSB (En Az Öneme Sahip Bit) Yöntemi
Dijital görsellerde her pikselin RGB değerleri 8 bit (0-255 arası) ile ifade edilir. Bu 8 bitin en sağındaki bit (LSB) değiştirildiğinde, renk değerindeki değişim insan gözüyle fark edilemeyecek kadar küçüktür.

**Örnek:**
* **Orijinal Piksel (Kırmızı):** `11001010` (202)
* **Gizlenecek Bit:** `1`
* **Yeni Piksel:** `11001011` (203)  
* *Sonuç: Görselde herhangi bir bozulma veya renk farkı oluşmaz.*

---

### 📁 Proje Yapısı
Ödev talimatlarına uygun olarak hazırlanan klasör yapısı:
```text
SumeyyePolat/
│
├── steganography.ipynb   # Tüm Python kodlarını içeren notebook
├── input.png             # Orijinal (temiz) görsel dosyası
├── stego_output.png      # Mesaj gömülmüş (şifreli) görsel dosyası
└── README.md             # Proje dökümantasyonu
```
### 🚀 Kurulum ve Kullanım
Uygulamayı Google Colab üzerinde şu adımlarla çalıştırabilirsiniz:

1. **Notebook'u Açın:** `steganography.ipynb` dosyasını Google Colab ortamına yükleyin.
2. **Blokları Sırayla Çalıştırın:**

| Blok | İşlev |
| :--- | :--- |
| **Blok 1** | Gerekli kütüphanelerin (OpenCV, NumPy, PIL) yüklenmesi. |
| **Blok 2** | Görselin sisteme yüklenmesi ve PNG formatına dönüştürülmesi. |
| **Blok 3** | **Encode:** Mesajın piksellerin LSB katmanına gizlenmesi. |
| **Blok 4** | **Decode:** Görselden gizli mesajın ayıklanması. |
| **Blok 5** | CLI arayüzü ile işlemin test edilmesi ve dosyanın indirilmesi. |

---

### ⚙️ Kullanılan Teknolojiler
* **Python 3**
* **OpenCV:** Piksel düzeyinde erişim ve görüntü işleme.
* **Pillow (PIL):** Format dönüştürme ve görsel yönetimi.
* **NumPy:** Verilerin matris bazlı manipülasyonu.

---

### 📊 Değerlendirme Kriterleri
| Kriter | Puan |
| :--- | :--- |
| Teorik kısmın içeriği ve açıklığı | 20 |
| Kodun doğruluğu ve çalışabilirliği | 30 |
| Encode / Decode fonksiyonlarının başarımı | 30 |
| Raporun düzeni ve içeriği | 20 |

---

### ⚠️ Önemli Sınırlamalar
* **Format Desteği:** Veri bütünlüğü için yalnızca **PNG** formatı kullanılmalıdır. JPG formatı LSB verilerini bozan "kayıplı" bir sıkıştırma yapar.
* **Kapasite:** Gömülebilecek maksimum mesaj uzunluğu şu formülle hesaplanır:

$$\frac{\text{Piksel Sayısı} \times 3}{8} = \text{Maksimum Karakter Sayısı}$$

---
**Hazırlayan:** Sümeyye Polat  
**Ders:** Yazılım Güvenliği  
**Kurum:** Kırklareli Üniversitesi
