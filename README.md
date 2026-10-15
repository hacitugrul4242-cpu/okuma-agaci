# Okuma Ağacı — 21 Günlük Okuma Alışkanlığı 🌳

İnternetsiz kullanılabilen, iPhone ana ekranına kurulabilen, Türkçe 21 günlük okuma alışkanlığı uygulaması. Harici kütüphane ve sunucu gerektirmez. Animasyon, HTML Canvas üzerinde çalışır.

## GitHub Pages ile yayımlama

1. GitHub hesabında **public** `okuma-agaci` isimli yeni bir repository oluştur. Mevcut projelerin dosyalarını değiştirme.
2. Bu ZIP içindeki dosya ve klasörleri (ZIP'in kendisini değil) deponun **köküne** yükle. `index.html`, `manifest.webmanifest`, `service-worker.js`, `icons/` ve `.nojekyll` aynı düzeyde olmalı.
3. **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main → Folder: /(root) → Save** seç.
4. Sayfa yayımlanınca `https://KULLANICI.github.io/okuma-agaci/` adresine iPhone Safari'den git.
5. **Paylaş → Ana Ekrana Ekle** yolunu kullan. Varsa “Web Uygulaması Olarak Aç” seçeneğini aç.
6. İlk çevrimiçi açılıştan sonra çevrimdışı kullanım için gereken dosyalar cihaza önbelleklenir. Uçak modunda açarak test et.

## Özellikler

- Her iki günde bir artan hedef, 21. güne kadar toplam 21 hedef.
- Tarihe bağlı günlük tamamlamalar; ilerleme `localStorage` içinde saklanır (`okuma-agaci-v1`).
- 21 günlük büyümeyi hızlandırılmış izleme, bitişte ağaç, dinamik yapraklar.
- JSON yedeği indirme ve yedeği geri yükleme.
- Bildirim, hesap açma, verileri sunucuya gönderme veya üçüncü parti bağımlılığı yok.

## Önemli uyarılar

- GitHub Pages herkese açık sayfa yayımlar. Uygulama kodu genel kullanım için uygundur ama **kişisel JSON yedeğini asla GitHub deposuna yükleme**.
- Safari ile ana ekran uygulaması farklı depolama alanları kullanabilir; kayıtların otomatik taşınacağını varsayma. Yedekleme/geri yükleme kullan.
- Tarayıcı verileri veya uygulama silinirse yerel kayıtlar kaybolabilir. Yedek sakla.
- Service worker HTTPS ya da localhost üzerinde çalışır. HTML'yi doğrudan Dosyalar'dan açmak gerçek PWA deneyimi değildir.
- Güncelleme sonrası SW'yi yenilemek için uygulamayı kapatıp yeniden açmak gerekebilir.

## Proje dosyaları

- `index.html` — arayüz, kayıt takibi ve Canvas animasyonu
- `manifest.webmanifest` — ana ekran/standalone ayarları
- `service-worker.js` — çevrimdışı önbellek
- `icons/` — iOS ve standart PWA simgeleri
- `.nojekyll` — Pages'e statik dosyaları olduğu gibi sunmasını söyler

Projeyi yerel ortamda denemek için bu dizinde `python3 -m http.server 8000` çalıştırıp `http://localhost:8000` adresini aç.