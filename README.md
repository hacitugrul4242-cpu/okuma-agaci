# Okuma Ağacı — 21 Günlük Okuma Alışkanlığı 🌳

İnternetsiz kullanılabilen, iPhone ana ekranına kurulabilen, Türkçe 21 günlük okuma alışkanlığı uygulaması. Harici kütüphane ve sunucu gerektirmez. Animasyon, HTML Canvas üzerinde çalışır.

## GitHub Pages ile yayımlama

Bu depo PWA dosyalarını içerir; dosyalar `main` dalının köküne yüklenmiştir.

1. Depo sahibi **[Settings → Pages](https://github.com/hacitugrul4242-cpu/okuma-agaci/settings/pages)** bölümüne gitsin.
2. **Build and deployment → Source: Deploy from a branch** seçsin.
3. **Branch: main**, **Folder: /(root)** ayarlasın ve **Save** düğmesine bassın.
4. GitHub Pages etkinleşince adres: **https://hacitugrul4242-cpu.github.io/okuma-agaci/**
5. iPhone'da bu HTTPS adresini Safari'de açıp **Paylaş → Ana Ekrana Ekle** seç.
6. İlk açılışta internet bağlantısı gerekir; önbellek hazır olduktan sonra uçak modunda yeniden açarak çevrimdışı çalışmayı test et.

> GitHub Pages etkinleştirilmedikçe yukarıdaki uygulama adresi çalışmayabilir; kod yüklenmesi ve sitenin yayımlanması ayrı işlemlerdir.

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