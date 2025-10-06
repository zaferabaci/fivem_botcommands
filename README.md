## Genel Bakış

FiveM Bot, Discord sunucularında otomatik moderasyon, whitelist yönetimi, ticket sistemi ve kapsamlı log takibi sağlayan profesyonel bir bot sistemidir. Bu dokümantasyon, bot'un kurulumundan günlük kullanımına kadar tüm süreçleri kapsar.

## Yetki Sistemi

### Owner (En Yüksek Yetki)
**Rol ID:** `1222303283385729044` (Değiştirilemez)

**Yetkiler:**
- Tüm bot ayarlarını değiştirme
- Sistem yönetimi ve bakım
- Diğer tüm rollere sahip olma

**Komutlar:**
- `/setup` - Bot kurulum paneli
- `/settings` - Bot ayarları paneli
- `/system` - Sistem bilgileri
- `/topreset` - İstatistikleri sıfırlama

### Staff (Yönetim)
**Rol ID:** `1222303180088676412`

**Yetkiler:**
- Ceza verme ve kaldırma
- Rol yönetimi
- Ticket yönetimi
- Tüm istatistik komutları
- Liderlik tablolarını görüntüleme

**Komutlar:**
- `/ceza` - Ceza verme
- `/cezakaldir` - Ceza kaldırma
- `/rolver` - Rol verme
- `/rolal` - Rol alma
- `/rolkontrol` - Rol kontrolü
- `/destekstats` - Destek istatistikleri
- `/destektop` - Destek liderlik tablosu
- `/başvurutop` - Başvuru liderlik tablosu
- `/mülakattop` - Mülakat liderlik tablosu
- `/icisimtop` - IC İsim liderlik tablosu

### Supervisor (Denetim)
**Rol ID:** `1222303138124533821`

**Yetkiler:**
- Staff işlemlerini denetleme
- Rapor görüntüleme
- Tüm Staff yetkilerine sahip

### Banhammer (Moderasyon)
**Rol ID:** `1222599530315251773`

**Yetkiler:**
- Ban ve unban işlemleri
- Yasak bilgisi sorgulama

**Komutlar:**
- `/ban` - Kullanıcı yasaklama
- `/unban` - Yasak kaldırma
- `/baninfo` - Yasak bilgisi

### Başvuru Sorumlusu
**Rol ID:** `1424076465909137429`

**Yetkiler:**
- Başvuru işlemleri
- Başvuru formu gönderme
- Başvuru istatistikleri

**Komutlar:**
- `/basvuruform` - Başvuru formu gönderme
- `/başvurustats` - Başvuru istatistikleri

### Mülakat Sorumlusu
**Rol ID:** `1424076472422895746`

**Yetkiler:**
- Mülakat yapma
- Mülakat istatistikleri

**Komutlar:**
- `/mülakat` - Mülakat yapma
- `/mülakatstats` - Mülakat istatistikleri

### IC İsim Rolü
**Rol ID:** Whitelist ayarlarından belirlenir

**Yetkiler:**
- IC İsim onaylama/reddetme
- IC İsim istatistikleri

**Komutlar:**
- `/icisimstats` - IC İsim istatistikleri

## Temel Kurulum Komutları

### /setup Komutu
Bot'un temel kurulumunu yapmak için kullanılır. Owner yetkisi gereklidir.

**Kullanım:**
1. `/setup` komutunu çalıştırın
2. Açılan panelde gerekli ayarları seçin:
   - Log Ayarları
   - Ticket Ayarları
   - Whitelist Ayarları
   - İşletme Ayarları
   - Oluşum Ayarları
   - Departman Ayarları

**Önemli Notlar:**
- Log kanalları otomatik olarak oluşturulur
- Her ayar kategorisi için ayrı butonlar bulunur
- Ayarlar config dosyasına otomatik kaydedilir

### /settings Komutu
Detaylı bot ayarlarını görüntülemek ve düzenlemek için kullanılır. Owner yetkisi gereklidir.

**Kullanım:**
1. `/settings` komutunu çalıştırın
2. Açılan panelde ayar kategorilerini seçin:
   - Bot Ayarları
   - Link Ayarları
   - Embed Ayarları
   - Sunucu Ayarları
   - Rol Ayarları
   - Kanal Ayarları

## Sistem Yönetimi

### /system Komutu
Bot durumu ve sistem bilgilerini gösterir. Owner yetkisi gereklidir.

**Görüntülenen Bilgiler:**
- Bot durumu (Online/Offline)
- Veritabanı bağlantı durumu
- Sistem performans bilgileri
- Aktif kullanıcı sayısı

### /topreset Komutu
Tüm istatistikleri sıfırlar. Owner yetkisi gereklidir.

**Uyarı:** Bu işlem geri alınamaz ve tüm istatistik verilerini siler.

## Ticket Sistemi

### Kurulum
1. `/setup` > Ticket Ayarları
2. Kategori ID ve Staff rolü ayarlayın
3. `/ticketsetup` komutu ile ticket kanalına mesaj gönderin

### Kullanım
- Kullanıcılar ticket butonuna tıklayarak destek talebi oluşturur
- Otomatik olarak özel kanal oluşturulur
- Staff üyeleri ticket'ları yönetebilir

## Whitelist Sistemi

### Başvuru Süreci
1. Kullanıcı `/başvuru` komutu ile başvuru yapar
2. Başvuru Sorumlusu başvuruyu inceler
3. Onaylanan başvurular mülakata alınır
4. Mülakat Sorumlusu mülakat yapar
5. Sonuç kullanıcıya bildirilir

### Roller
- Kayıtsız: Başvuru yapmamış kullanıcılar
- Kayıtlı: Başvuru yapmış kullanıcılar
- Onaylı: Başvurusu onaylanmış kullanıcılar
- Reddedilmiş: Başvurusu reddedilmiş kullanıcılar

## Log Sistemi

### Log Türleri
- Join/Leave: Katılım ve ayrılış logları
- Invite: Davet logları
- Autorole: Otomatik rol logları
- Supervision: Denetim logları
- Business: İşletme logları
- Department: Departman logları
- Organization: Oluşum logları
- Role: Rol değişiklik logları
- Interview: Mülakat logları
- Application: Başvuru logları
- Punishments: Ceza logları
- Ban/Unban: Yasak logları
- IC Name: IC İsim logları
- Error: Hata logları

### Kurulum
1. `/setup` > Log Ayarları
2. "Log Kanalları Oluştur" butonuna tıklayın
3. Otomatik olarak kategori ve kanallar oluşturulur

## Organizasyon Yönetimi

### İşletme Sistemi
- **Yetki:** Supervisor
- **Komut:** `/işletme`
- **Amaç:** İşletme organizasyonlarını yönetme
- **Alt Komutlar:** `oluştur`, `sil`, `üyeekle`, `üyeçıkar`

### Oluşum Sistemi
- **Yetki:** Supervisor
- **Komut:** `/olusum`
- **Amaç:** Oluşum organizasyonlarını yönetme
- **Alt Komutlar:** `oluştur`, `sil`, `üyeekle`, `üyeçıkar`

### Departman Sistemi
- **Yetki:** Supervisor
- **Komut:** `/departman`
- **Amaç:** Departman organizasyonlarını yönetme
- **Alt Komutlar:** `oluştur`, `sil`, `üyeekle`, `üyeçıkar`

## İstatistik Sistemi

### Kişisel İstatistikler
- **Destek İstatistikleri:** `/destekstats` (Staff)
- **Başvuru İstatistikleri:** `/başvurustats` (Başvuru Sorumlusu)
- **Mülakat İstatistikleri:** `/mülakatstats` (Mülakat Sorumlusu)
- **IC İsim İstatistikleri:** `/icisimstats` (IC İsim Rolü)

### Liderlik Tabloları
- **Destek Liderliği:** `/destektop` (Staff)
- **Başvuru Liderliği:** `/başvurutop` (Staff)
- **Mülakat Liderliği:** `/mülakattop` (Staff)
- **IC İsim Liderliği:** `/icisimtop` (Staff)

## Moderasyon Komutları

### Ceza Sistemi
- `/ceza @kullanıcı sebep` - Ceza verme (Staff)
- `/cezakaldir @kullanıcı` - Ceza kaldırma (Staff)

### Rol Yönetimi
- `/rolver @kullanıcı @rol` - Rol verme (Staff)
- `/rolal @kullanıcı @rol` - Rol alma (Staff)
- `/rolkontrol @kullanıcı` - Rol kontrolü (Staff)

### Yasak Sistemi
- `/ban @kullanıcı sebep` - Yasaklama (Banhammer)
- `/unban kullanıcı_id` - Yasak kaldırma (Banhammer)
- `/baninfo kullanıcı_id` - Yasak bilgisi (Banhammer)

## Hata Giderme

### Yaygın Sorunlar

#### "Yetki Bulunamadı" Hatası
- Rol ID'lerini kontrol edin
- `/settings` > Rol Ayarları'ndan doğruluğunu onaylayın

#### "Kanal Bulunamadı" Hatası
- Kanal ID'lerini kontrol edin
- `/setup` > Log Ayarları'ndan yeniden oluşturun

## Lisans

Bu proje özel kullanım içindir. Tüm hakları saklıdır.

## Sürüm Geçmişi

- v1.0.0 - İlk sürüm
- v1.1.0 - Whitelist sistemi eklendi
- v1.2.0 - Organizasyon yönetimi eklendi
- v1.3.0 - İstatistik sistemi geliştirildi

---

*Son güncelleme: 2025*
*Dokümantasyon versiyonu: 1.0*
