# 🤖 FiveM Bot - Kullanım Kılavuzu

## 📋 İçindekiler
- [Genel Bakış](#genel-bakış)
- [Kurulum](#kurulum)
- [Komutlar](#komutlar)
- [Yetki Sistemi](#yetki-sistemi)
- [Ayarlar Paneli](#ayarlar-paneli)
- [Whitelist Sistemi](#whitelist-sistemi)
- [Ticket Sistemi](#ticket-sistemi)
- [Log Sistemi](#log-sistemi)
- [İşletme/Oluşum/Departman](#işletmeoluşumdepartman)

---

## 🎯 Genel Bakış

FiveM Bot, Discord sunucunuzda otomatik moderasyon, whitelist yönetimi, ticket sistemi ve log takibi sağlayan kapsamlı bir bot sistemidir.

### ✨ Özellikler
- 🎫 **Ticket Sistemi** - Destek talepleri için otomatik kanal oluşturma
- 📝 **Whitelist Yönetimi** - Başvuru ve mülakat sistemi
- 📊 **Log Sistemi** - Tüm sunucu aktivitelerini takip
- 🏢 **İşletme/Oluşum/Departman** - Organizasyon yönetimi
- 👥 **Rol Yönetimi** - Yetki sistemi kontrolü
- 🛡️ **Moderasyon** - Ban/unban ve ceza sistemi

---

## 🚀 Kurulum

### 1. Gereksinimler
- Node.js 16.9.0 veya üzeri
- MongoDB veritabanı
- MySQL veritabanı
- Discord Bot Token

### 2. Kurulum Adımları
```bash
# Projeyi klonlayın
git clone [repository-url]

# Bağımlılıkları yükleyin
npm install

# Config dosyasını düzenleyin
cp core/config.js.example core/config.js

# Botu başlatın
node .
```

### 3. Discord Kurulumu
1. Discord Developer Portal'da yeni bot oluşturun
2. Bot token'ını `core/config.js` dosyasına ekleyin
3. Gerekli izinleri verin:
   - `Send Messages`
   - `Manage Channels`
   - `Manage Roles`
   - `Embed Links`
   - `Read Message History`

---

## 💬 Komutlar

### 🔧 Yönetim Komutları

#### `/setup`
**Açıklama:** Bot kurulum paneli  
**Yetki:** Owner  
**Kullanım:** Temel bot ayarlarını yapılandırır

#### `/settings`
**Açıklama:** Bot ayarları görüntüleme paneli  
**Yetki:** Owner  
**Kullanım:** Detaylı ayarları görüntüler ve düzenler

#### `/system`
**Açıklama:** Sistem bilgileri  
**Yetki:** Owner  
**Kullanım:** Bot durumu ve sistem bilgilerini gösterir

#### `/topreset`
**Açıklama:** Top istatistiklerini sıfırla  
**Yetki:** Owner  
**Kullanım:** Tüm istatistikleri sıfırlar

### 🎫 Ticket Komutları

#### `/ticketsetup`
**Açıklama:** Ticket sistemi kurulumu  
**Yetki:** Owner  
**Kullanım:** Ticket kanalına kurulum mesajı gönderir

### 🛡️ Moderasyon Komutları

#### `/ban`
**Açıklama:** Kullanıcıyı yasakla  
**Yetki:** Banhammer  
**Kullanım:** `/ban @kullanıcı sebep`

#### `/unban`
**Açıklama:** Yasak kaldır  
**Yetki:** Banhammer  
**Kullanım:** `/unban kullanıcı_id`

#### `/baninfo`
**Açıklama:** Yasak bilgisi  
**Yetki:** Staff  
**Kullanım:** `/baninfo kullanıcı_id`

### 👥 Staff Komutları

#### `/ceza`
**Açıklama:** Ceza ver  
**Yetki:** Staff  
**Kullanım:** `/ceza @kullanıcı sebep`

#### `/cezakaldir`
**Açıklama:** Ceza kaldır  
**Yetki:** Staff  
**Kullanım:** `/cezakaldir @kullanıcı`

#### `/rolver`
**Açıklama:** Rol ver  
**Yetki:** Staff  
**Kullanım:** `/rolver @kullanıcı @rol`

#### `/rolal`
**Açıklama:** Rol al  
**Yetki:** Staff  
**Kullanım:** `/rolal @kullanıcı @rol`

#### `/rolkontrol`
**Açıklama:** Rol kontrol et  
**Yetki:** Staff  
**Kullanım:** `/rolkontrol @kullanıcı`

### 📝 Whitelist Komutları

#### `/başvuru`
**Açıklama:** Başvuru yap  
**Yetki:** Herkes  
**Kullanım:** Whitelist başvurusu yapar

#### `/basvuruform`
**Açıklama:** Başvuru formu gönder  
**Yetki:** Staff  
**Kullanım:** Başvuru formu gönderir

#### `/mülakat`
**Açıklama:** Mülakat yap  
**Yetki:** Mülakat Sorumlusu  
**Kullanım:** `/mülakat @kullanıcı sonuç`

### 📊 İstatistik Komutları

#### `/destekstats`
**Açıklama:** Destek istatistikleri  
**Yetki:** Staff  
**Kullanım:** Ticket istatistiklerini gösterir

#### `/başvurustats`
**Açıklama:** Başvuru istatistikleri  
**Yetki:** Staff  
**Kullanım:** Başvuru istatistiklerini gösterir

#### `/mülakatstats`
**Açıklama:** Mülakat istatistikleri  
**Yetki:** Staff  
**Kullanım:** Mülakat istatistiklerini gösterir

### 🏢 Organizasyon Komutları

#### `/işletme`
**Açıklama:** İşletme oluştur  
**Yetki:** İşletme Müdürü  
**Kullanım:** Yeni işletme oluşturur

#### `/olusum`
**Açıklama:** Oluşum oluştur  
**Yetki:** Boss  
**Kullanım:** Yeni oluşum oluşturur

#### `/departman`
**Açıklama:** Departman oluştur  
**Yetki:** High Command  
**Kullanım:** Yeni departman oluşturur

---

## 👑 Yetki Sistemi

### 🔴 Owner (En Yüksek Yetki)
- **Rol ID:** `1222303283385729044`
- **Yetkiler:**
  - Tüm bot ayarlarını değiştirme
  - Sistem yönetimi
  - Diğer tüm rollere sahip
- **Komutlar:** `/setup`, `/settings`, `/system`, `/topreset`

### 🟠 Staff (Yönetim)
- **Rol ID:** `1222303180088676412`
- **Yetkiler:**
  - Ceza verme/kaldırma
  - Rol yönetimi
  - Ticket yönetimi
  - İstatistik görüntüleme
- **Komutlar:** `/ceza`, `/cezakaldir`, `/rolver`, `/rolal`, `/rolkontrol`, `/destekstats`

### 🟡 Supervisor (Denetim)
- **Rol ID:** `1222303138124533821`
- **Yetkiler:**
  - Staff işlemlerini denetleme
  - Rapor görüntüleme
- **Komutlar:** Tüm Staff komutları + denetim yetkileri

### 🔵 Banhammer (Moderasyon)
- **Rol ID:** `1222599530315251773`
- **Yetkiler:**
  - Ban/unban işlemleri
  - Yasak bilgisi sorgulama
- **Komutlar:** `/ban`, `/unban`, `/baninfo`

### 🟢 Başvuru Sorumlusu
- **Rol ID:** `1424076465909137429`
- **Yetkiler:**
  - Başvuru işlemleri
  - Başvuru formu gönderme
  - Başvuru istatistikleri
- **Komutlar:** `/basvuruform`, `/başvurustats`

### 🟣 Mülakat Sorumlusu
- **Rol ID:** `1424076472422895746`
- **Yetkiler:**
  - Mülakat yapma
  - Mülakat istatistikleri
- **Komutlar:** `/mülakat`, `/mülakatstats`

---

## ⚙️ Ayarlar Paneli

### 🔧 Bot Ayarları (`/settings`)
- **Bot Status:** Online, Idle, DND durumu
- **Activity:** Bot aktivite ayarları
- **Embed Settings:** Renk, ikon, footer ayarları

### 🔗 Link Ayarları
- **Discord Link:** Sunucu davet linki
- **Website:** Web sitesi linki
- **Connect:** Bağlantı linki
- **Form:** Form linki

### 👥 Rol Ayarları
- **Staff Rolü:** Yönetim yetkisi
- **Supervisor Rolü:** Denetim yetkisi
- **Banhammer Rolü:** Moderasyon yetkisi
- **Başvuru Rolü:** Başvuru işlemleri
- **Mülakat Rolü:** Mülakat işlemleri
- **Owner Rolü:** ⚠️ Değiştirilemez

### 📡 Kanal Ayarları
- **Log Kanalları:** Tüm log türleri
- **Ticket Kategorisi:** Ticket kanalları
- **Whitelist Kanalları:** Başvuru ve mülakat

---

## 📝 Whitelist Sistemi

### 🎯 Amaç
Sunucuya katılmak isteyen oyuncuların başvuru sürecini yönetir.

### 📋 Süreç
1. **Başvuru:** Oyuncu `/başvuru` komutu ile başvuru yapar
2. **İnceleme:** Başvuru Sorumlusu başvuruyu inceler
3. **Mülakat:** Onaylanan başvurular mülakata alınır
4. **Sonuç:** Mülakat sonucuna göre oyuncu kabul/reddedilir

### 🔄 Roller
- **Kayıtsız:** Başvuru yapmamış oyuncular
- **Kayıtlı:** Başvuru yapmış oyuncular
- **Onaylı:** Başvurusu onaylanmış oyuncular
- **Reddedilmiş:** Başvurusu reddedilmiş oyuncular

### 📊 İstatistikler
- Başvuru sayıları
- Mülakat istatistikleri
- Top başvuru yapanlar
- IC İsim kullanım istatistikleri

---

## 🎫 Ticket Sistemi

### 🎯 Amaç
Kullanıcıların destek taleplerini organize etmek.

### 📋 Özellikler
- **Otomatik Kanal Oluşturma:** Her ticket için özel kanal
- **Yetkili Atama:** Staff otomatik atanır
- **Kapatma/Reopen:** Ticket yönetimi
- **Transfer:** Farklı staff'a devretme
- **Silme:** Gereksiz ticket'ları silme

### 👥 Yetkiler
- **Ticket Oluşturma:** Herkes
- **Ticket Yönetimi:** Staff
- **Ticket Silme:** Sadece Staff

### 📊 İstatistikler
- Açık ticket sayısı
- Top ticket açanlar
- Staff performans istatistikleri

---

## 📊 Log Sistemi

### 📋 Log Türleri
- **Join/Leave:** Katılım/ayrılış logları
- **Invite:** Davet logları
- **Autorole:** Otomatik rol logları
- **Supervision:** Denetim logları
- **Business:** İşletme logları
- **Department:** Departman logları
- **Organization:** Oluşum logları
- **Role:** Rol değişiklik logları
- **Interview:** Mülakat logları
- **Application:** Başvuru logları
- **Punishments:** Ceza logları
- **Ban/Unban:** Yasak logları
- **IC Name:** IC İsim logları
- **Error:** Hata logları

### 🔧 Kurulum
1. `/setup` komutu ile Log Ayarları'na tıklayın
2. "Log Kanalları Oluştur" butonuna basın
3. Otomatik olarak kategori ve kanallar oluşturulur

---

## 🏢 İşletme/Oluşum/Departman

### 🏢 İşletme Sistemi
- **Yetki:** İşletme Müdürü
- **Kategori:** İşletme kanalları için
- **Komut:** `/işletme`

### 🏛️ Oluşum Sistemi
- **Yetki:** Boss
- **Kategori:** Oluşum kanalları için
- **Komut:** `/olusum`

### 🏢 Departman Sistemi
- **Yetki:** High Command
- **Kategori:** Departman kanalları için
- **Komut:** `/departman`

### ⚙️ Kurulum
1. `/setup` komutu ile ilgili ayarlara gidin
2. Kategori ve rol ID'lerini ayarlayın
3. Sistem otomatik olarak çalışmaya başlar

---

## 🚨 Hata Giderme

### ❌ Yaygın Hatalar

#### "Yetki Bulunamadı" Hatası
- **Çözüm:** Rol ID'lerini kontrol edin
- **Kontrol:** `/settings` > Rol Ayarları

#### "Kanal Bulunamadı" Hatası
- **Çözüm:** Kanal ID'lerini kontrol edin
- **Kontrol:** `/setup` > Log Ayarları

#### Bot Yanıt Vermiyor
- **Çözüm:** Bot izinlerini kontrol edin
- **Kontrol:** Discord Developer Portal

### 📞 Destek
- **Discord:** [Sunucu Davet Linki]
- **Website:** [Web Sitesi]
- **Email:** [İletişim Email]

---

## 📄 Lisans
Bu proje özel kullanım içindir. Tüm hakları saklıdır.

---

## 👥 Katkıda Bulunanlar
- **Geliştirici:** [İsim]
- **Tasarım:** [İsim]
- **Test:** [İsim]

---

*Son güncelleme: 2025*
