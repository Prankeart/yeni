# Optik Transfer QR v0.3

İki cihaz arasında metni QR kod kareleriyle aktarır. Veri aktarımında internet, Bluetooth veya Wi‑Fi kullanılmaz; yalnızca verici ekranı ve alıcı kamerası kullanılır.

## Dosyalar
- `index.html`: ana menü
- `verici.html`: metni parçalara ayırır, QR kodları üretip sırayla gösterir
- `alici.html`: kamera ile QR kodlarını okur ve parçaları birleştirir

## Çalıştırma
1. Dosyaları aynı klasörde tutup HTTPS destekleyen bir statik web sunucusuna yükleyin (ör. GitHub Pages).
2. İki cihazda aynı siteyi açın.
3. Vericide metni girip **QR'ları hazırla**, ardından **Başlat**'a basın.
4. Alıcıda **Kamerayı aç** deyin ve verici ekranını ortadaki kareye hizalayın.
5. Aktarım tamamlanınca metin alıcıda görünür.

## Önemli
- Kamera erişimi için HTTPS gerekir (localhost istisnası).
- Verici QR kütüphanesini CDN'den yükler; ilk sayfa yüklenirken internet gerekebilir. Bu bağımlılığı tamamen çevrimdışı yapmak için kütüphaneyi yerel dosya olarak projeye eklemek gerekir.
- Alıcı `BarcodeDetector` API'sini kullanır; güncel Android Chrome'da desteklenir ancak her tarayıcıda yoktur.
- QR kareleri 1.8 saniyede bir değişir. Daha güvenilir okuma için alıcıyı sabit tutun; karakter sayısını 200–350 aralığında deneyin.
- Bu sürüm metin aktarımı içindir; resim/dosya aktarımı henüz ekli değildir.
