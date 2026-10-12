# YDS Kelime Akademisi – Telefona Uygulama Olarak Kurulum

Bu klasördeki dosyalar uygulamanın telefona yüklenebilen (PWA) sürümüdür.
İnternet olmadan da çalışır, ana ekranda kendi simgesiyle açılır.

## 1. Adım: Uygulamayı ücretsiz olarak internete koy (GitHub Pages)
1. github.com adresinde ücretsiz bir hesap aç.
2. Sağ üstteki "+" > "New repository" ile yeni bir depo oluştur. Adı örneğin: yds-akademi. "Public" seçili olsun.
3. Depo sayfasında "uploading an existing file" bağlantısına tıkla ve bu klasördeki TÜM dosyaları
   (index.html, manifest.json, sw.js ve 4 simge dosyası) sürükleyip bırak. "Commit changes" de.
4. Depoda "Settings" > "Pages" bölümüne gir. "Branch" olarak "main" ve "/ (root)" seç, "Save" de.
5. 1–2 dakika sonra uygulamanın adresi görünür:
   https://KULLANICI-ADIN.github.io/yds-akademi/

## 2. Adım: Telefona yükle
- Android (Chrome): Adresi aç > sağ üstteki üç nokta > "Uygulamayı yükle" veya "Ana ekrana ekle".
- iPhone (Safari): Adresi aç > Paylaş simgesi > "Ana Ekrana Ekle".
Artık uygulama ana ekranda kendi simgesiyle durur ve tam ekran açılır.
E�inle paylaşmak için bu adresi göndermen yeterli.

## 3. Adım: Eski ilerlemeni taşı
1. Eski sürümde (Claude linki): Ana ekran > "İlerlemeyi yedekle / geri yükle" > "Yedek kodunu kopyala".
2. Yeni uygulamada aynı ekrana gir, kodu "Geri yükle" kutusuna yapıştır ve "Geri yükle"ye bas.

## (İsteğe bağlı) Play Store'a yüklemek
1. pwabuilder.com adresine git, uygulamanın GitHub Pages adresini yaz.
2. "Package for stores" > "Android" ile Play Store'a uygun paketi indir.
3. Google Play Console'da geliştirici hesabı aç (tek seferlik ücretli) ve paketi yükle.
   Not: Yeni kişisel hesaplarda yayına almadan önce en az 12 test kullanıcısıyla 14 gün kapalı test şartı vardır.

## Güncelleme
Yeni kelimeler veya özellikler eklendiğinde sadece yeni index.html dosyasını GitHub'daki deponun
üzerine yüklemen yeterli. sw.js içindeki "yds-akademi-v1" yazısını "v2" yapmak, telefonların
yeni sürümü hemen almasını sağlar.

## Güncelleme butonu
Uygulamada "🔄 Uygulamayı güncelle" butonu var (YDS Akademi: ana ekranın altı; Dil Atölyesi: Defter › Uygulama).
Basınca en yeni sürüm indirilir ve uygulama yenilenir. İlerleme silinmez.
Yeni sürüm yayınlandığında uygulama bunu kendisi fark eder ve altta "Yeni güncelleme var" uyarısı çıkar.

Yeni sürüm yayınlarken: index.html içindeki APP_VER ile version.json içindeki "v" değerini
aynı yeni değere getir (örn. 2026.10.20-1). Uyarı bu iki değer farklı olunca çıkar.
