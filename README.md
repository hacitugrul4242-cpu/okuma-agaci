# Okuma Ağacı — Sakura 🌸

21 günde kitap okuma alışkanlığı edinmek için tasarlanmış, iPhone ana ekranına kurulabilen çevrimdışı PWA. Her gün ağaç gelişir; 11. günden itibaren kiraz çiçekleri açar.

## Canlı uygulama

https://hacitugrul4242-cpu.github.io/okuma-agaci/

iPhone Safari → Paylaş → Ana Ekrana Ekle. Güncellemeden sonra uygulamayı tamamen kapatıp tekrar aç.

## 24 saatlik seri kuralları

- Başlangıç anı, birinci 24 saatlik günün başlangıcıdır.
- Her 24 saatlik dilimde **yalnızca o gün** işaretlenebilir. Gelecek günler kilitlidir.
- Süresi biten herhangi bir gün eksikse seri **otomatik sıfırlanır**; yeni bir tohumla 1. gün başlar.
- 21/21 tamamlanırsa ağaç korunur, otomatik sıfırlanmaz.
- Örnek: Pazartesi 17.30'da başladıysan ikinci gün salı 17.30'da açılır; takvim gece yarısına bağlı değildir.
- Eski sürümdeki kayıtlar, geçmişte saat bilgisi bulunmadığından geriye dönük cezalandırılmaz; mevcut toplam korunur ve yeni kurallar güncellemeden itibaren uygulanır.

Bu zaman kontrolü çevrimdışı cihaz üzerinde çalışır; telefon saati veya yerel depolama kasıtlı değiştirilirse sunucu düzeyinde garanti verilemez.

## Gizlilik ve veri

- Okuma verileri sadece cihazda yerel olarak saklanır; GitHub'a gönderilmez.
- Yedekleme/geri yükleme v2 (tamamlanma saatleriyle) desteklenir. v1 yedekleri de aktarılır.
- JSON yedeklerini herkese açık GitHub'a yükleme.
- Safari ile Ana Ekran uygulaması farklı depolama alanları kullanabilir.
- Çevrimdışı kullanım ilk çevrimiçi açılıştan sonra önbelleğe alınır.

## Proje dosyaları

- `index.html`: arayüz, Canvas sakura, 21 günlük sistem ve zamanlama.
- `manifest.webmanifest`: PWA kurulumu.
- `service-worker.js`: sürümlü çevrimdışı önbellek.
- `icons/`: uygulama simgeleri.
- `.nojekyll`: GitHub Pages.

GitHub Pages ayarları: Settings → Pages → Deploy from a branch → main → /(root).
