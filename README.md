## LSB Image Steganography
# Yazılım Güvenliği dersi dönem ödevi — Python ile görsel tabanlı steganografi uygulaması.

## Proje Hakkında
Bu proje, LSB (Least Significant Bit) yöntemi kullanarak bir görsel dosyasının piksel verilerine gizli metin mesajı gömmek ve bu mesajı geri çıkarmak amacıyla geliştirilmiştir. Google Colab ortamında çalışacak şekilde tasarlanmıştır.

## Steganografi Nedir?
Steganografi, bir bilginin (metin, ses, görsel vb.) başka bir bilginin içine gizlenerek iletilmesini inceleyen bilim dalıdır. Kriptografiden farkı şudur: kriptografi verinin içeriğini şifrelerken, steganografi verinin var olduğunu gizler.
# LSB Yöntemi
Her pikselin RGB değeri 8 bit ile ifade edilir. Bu 8 bitin en az anlamlı biti (LSB) değiştirildiğinde görselde gözle görülür bir fark oluşmaz. Bu özelliği kullanarak piksel başına 1 bit veri gizlenebilir.
Örnek piksel değeri : 11001010  (202)
Gizlenecek bit      : 1
Sonuç               : 11001011  (203)  ← fark edilmez

 ## 📁 Proje Yapısı
LSB-Image-Steganography/
│
├── steganography.ipynb   # Ana Colab notebook
├── input.png             # Giriş görseli (örnek)
├── output.png            # Encode edilmiş çıktı görseli
└── README.md

##  Kurulum ve Kullanım
Google Colab'da Çalıştırma

steganography.ipynb dosyasını Google Colab'da aç
Blokları sırayla çalıştır:

BlokİşlevBlok 1Kütüphaneleri import etBlok 2Görselini yükleBlok 3Encode fonksiyonunu tanımlaBlok 4Decode fonksiyonunu tanımlaBlok 5AGörsele mesaj göm (Encode)Blok 5BGörselden mesaj çıkar (Decode)Blok 6Encode/Decode testiBlok 7Çıktı görselini indir

##  Kullanılan Teknolojiler

Python 3
Pillow (PIL) — görsel işleme
NumPy — piksel dizisi manipülasyonu
Google Colab — çalışma ortamı



⚠️ ##  Sınırlamalar

Yalnızca PNG formatı desteklenir (JPG sıkıştırması LSB verilerini bozar)
Görselin boyutu, gömülebilecek maksimum mesaj uzunluğunu belirler
Piksel sayısı × 3 ÷ 8 = maksimum karakter sayısı

# Sümeyye Polat 
