# Okuma Ağacı — Sakura 🌸

iPhone ana ekranına kurulabilen, internet bağlantısı olmadan çalışabilen 21 günlük okuma alışkanlığı PWA'sı. Tamamlanan her gün kiraz ağacı gelişir ve çiçeklenir.

**Uygulama:** https://hacitugrul4242-cpu.github.io/okuma-agaci/

## Yerel takvim günü kuralları

- İlk kullanımda başlangıç günü seçilir: **bugün veya ilerideki bir tarih**. Geçmiş günler seçilip sonradan işaretlenemez.
- Gün hesabı **telefonun geçerli yerel tarihi ve saat dilimiyle** yapılır. Günler **00.00–23.59:59** aralığıdır; 24 saat bekleme zorunluluğu yoktur.
- Örnek: 15 Ekim günü 23.59'da görevi tamamlayan kişi, 16 Ekim günü saat 00.00'dan itibaren sonraki görevi işaretleyebilir.
- Gelecek günler ve geçmiş günler işaretlenemez; yalnızca bugünkü görev tamamlanabilir veya aynı gün geri alınabilir.
- Bir takvim günü tamamlanmadan sona ererse saat 00.00'dan sonra seri otomatik sıfırlanır; **yeni tohum, 1. gün**. Tüm 21 gün tamamlanırsa ağaç kalıcıdır.
- 23/25 saatlik yaz-kış saati geçişlerinde de **yerel takvim** kullanılır.
- Önceki PWA sürümlerinin kayıtları korunur, geçmişteki 24 saat pencereleri geriye dönük cezalandırılmaz. Zamanlama bu sürümden itibaren takvim günlerine göre işler.

Bu kurallar çevrimdışı olarak cihaz üzerinde çalışır; kullanıcı saat dilimini, sistem saatini veya yerel depolamayı kasıtlı değiştirirse sunucu düzeyinde güvenlik garantisi yoktur.

## iPhone kurulumu

1. Yukarıdaki bağlantıyı Safari'de aç.
2. Paylaş → Ana Ekrana Ekle → (varsa) Web Uygulaması Olarak Aç → Ekle.
3. Güncellemeden sonra siteyi çevrimiçi bir kez açıp tamamen kapat; yeniden başlat ve çevrimdışı test et.
4. Kayıtlarını kaybetmemek için **Yedeği indir** seçeneğini kullan. JSON yedeğini herkese açık GitHub'a yükleme.

## Dosyalar

- `index.html`: tüm HTML/CSS/Canvas çizimi, tarih seçimi, serinin takibi ve yedekleme
- `manifest.webmanifest`: PWA kurulumu
- `service-worker.js`: çevrimdışı önbellek
- `icons/`: iPhone ve diğer cihazlar için simgeler

GitHub Pages: **Settings → Pages → Deploy from a branch → main → /(root)**.
