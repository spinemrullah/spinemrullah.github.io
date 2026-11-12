# EMRULLAH GAMING

Oyun temalı, mobil uyumlu video sitesi. YouTube bağlantıları ve doğrudan MP4/WebM yükleme desteği içerir.

## Dosyalar
- `index.html`: Site arayüzü, oynatıcı ve yönetici paneli
- `config.js`: Supabase bağlantı ayarları
- `supabase_setup.sql`: Veritabanı, depolama alanı ve erişim politikaları

## Yayına alma
1. Supabase üzerinde yeni bir proje oluştur.
2. SQL Editor bölümünde `supabase_setup.sql` dosyasının tamamını çalıştır.
3. Supabase Project Settings > API bölümünden Project URL ve `anon` / publishable public key değerini al.
4. `config.js` içindeki iki `BURAYA...` alanını bu bilgilerle değiştir.
5. Supabase Authentication > Users bölümünden kendin için bir kullanıcı oluştur. E-posta ve şifrenle site yönetici paneline giriş yap.
6. Dosyaları GitHub Pages deposunun kök dizinine koy. `index.html` ve `config.js` aynı dizinde olmalı.
7. GitHub Pages etkinleştirildiğinde siteni `https://KULLANICI_ADIN.github.io` adresinde aç.

## Video yükleme
Yönetici düğmesine basıp giriş yaptıktan sonra başlık, kategori ve video dosyası veya YouTube bağlantısı ekle. Doğrudan video yüklemeleri en fazla 500 MB olarak sınırlandırılmıştır. Supabase depolama kotası ve ücretleri kullanımına göre değişebilir.

## Güvenlik
- `service_role` anahtarını asla `config.js` dosyasına koyma. Yalnızca public `anon` / publishable key kullan.
- Yönetici hesabını Supabase Auth içinden oluştur.
- Bu başlangıç sürümünde yönetici kaydı açık değildir; ziyaretçiler giriş yapamaz.
- Herkese açık video depolama alanına yüklenen videolar herkes tarafından izlenebilir.
- 
