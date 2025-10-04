# 🎮 FivemBOT Komut Rehberi

## 📋 İçindekiler
- [🏢 İşletme Komutları](#-işletme-komutları)
- [🏛️ Departman Komutları](#️-departman-komutları)
- [🏭 Organizasyon Komutları](#-organizasyon-komutları)
- [👥 Personel Komutları](#-personel-komutları)
- [🎫 Ticket Sistemi](#-ticket-sistemi)
- [📝 Beyaz Liste Komutları](#-beyaz-liste-komutları)
- [⚙️ Panel Komutları](#️-panel-komutları)
- [📊 İstatistik Komutları](#-istatistik-komutları)

---

## 🏢 İşletme Komutları

### `/işletmeolustur`
**Açıklama:** Yeni bir işletme oluşturur ve gerekli roller ile kanalları ayarlar.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:**
- `isletmeadi` (zorunlu) - İşletme adı
- `yönetici` (zorunlu) - İşletme yöneticisi kullanıcısı
- `renk` (zorunlu) - Rol rengi (hex kod: FF0000)

**Kullanım Örneği:**
```
/işletmeolustur isletmeadi:Burger Palace yönetici:@kullanici renk:FF5733
```

**Ne Yapar:**
- İşletme adında yeni rol oluşturur
- Yöneticiye işletme rolü verir
- İşletme için özel kanal oluşturur
- Veritabanına kayıt yapar
- İşlem loglarını tutar

---

### `/işletmeüyeekle`
**Açıklama:** Mevcut bir işletmeye üye ekler.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:**
- `kullanıcı` (zorunlu) - Eklenecek kullanıcı
- `işletme` (zorunlu) - İşletme adı (otomatik tamamlama)

**Kullanım Örneği:**
```
/işletmeüyeekle kullanıcı:@yeniüye işletme:Burger Palace
```

**Ne Yapar:**
- Kullanıcıya işletme rolü verir
- Veritabanında üye listesini günceller
- İşlem loglarını tutar

---

### `/işletmeüyeçıkar`
**Açıklama:** İşletmeden üye çıkarır.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:**
- `kullanıcı` (zorunlu) - Çıkarılacak kullanıcı
- `işletme` (zorunlu) - İşletme adı (otomatik tamamlama)

**Kullanım Örneği:**
```
/işletmeüyeçıkar kullanıcı:@eskiüye işletme:Burger Palace
```

**Ne Yapar:**
- Kullanıcıdan işletme rolünü alır
- Veritabanında üye listesini günceller
- İşlem loglarını tutar

---

### `/işletmesil`
**Açıklama:** İşletmeleri listeler ve silme seçeneği sunar.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:** Yok

**Kullanım Örneği:**
```
/işletmesil
```

**Ne Yapar:**
- Mevcut işletmeleri dropdown menüde listeler
- Seçilen işletmeyi tamamen siler
- İşletme rolünü ve kanalını kaldırır
- Tüm üyelerden işletme rollerini alır

---

## 🏛️ Departman Komutları

### `/departmanolustur`
**Açıklama:** Yeni bir departman oluşturur.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:**
- `departmanadi` (zorunlu) - Departman adı
- `yönetici` (zorunlu) - Departman yöneticisi
- `renk` (zorunlu) - Rol rengi (hex kod)

**Kullanım Örneği:**
```
/departmanolustur departmanadi:Polis Departmanı yönetici:@komiser renk:0000FF
```

**Ne Yapar:**
- Departman rolü ve kanalı oluşturur
- Yöneticiye departman rolü verir
- Veritabanına kayıt yapar

---

### `/departmanüyeekle`
**Açıklama:** Departmana üye ekler.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:**
- `kullanıcı` (zorunlu) - Eklenecek kullanıcı
- `departman` (zorunlu) - Departman adı

**Kullanım Örneği:**
```
/departmanüyeekle kullanıcı:@polis departman:Polis Departmanı
```

---

### `/departmanüyeçıkar`
**Açıklama:** Departmandan üye çıkarır.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:**
- `kullanıcı` (zorunlu) - Çıkarılacak kullanıcı
- `departman` (zorunlu) - Departman adı

**Kullanım Örneği:**
```
/departmanüyeçıkar kullanıcı:@polisi departman:Polis Departmanı
```

---

### `/departmansil`
**Açıklama:** Departmanları listeler ve silme seçeneği sunar.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:** Yok

**Kullanım Örneği:**
```
/departmansil
```

---

## 🏭 Organizasyon Komutları

### `/olusumolustur`
**Açıklama:** Yeni bir organizasyon oluşturur.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:**
- `olusumadi` (zorunlu) - Organizasyon adı
- `yönetici` (zorunlu) - Organizasyon yöneticisi
- `renk` (zorunlu) - Rol rengi (hex kod)

**Kullanım Örneği:**
```
/olusumolustur olusumadi:Mafya Ailesi yönetici:@don renk:800080
```

**Ne Yapar:**
- Organizasyon rolü ve kanalı oluşturur
- Yöneticiye organizasyon rolü verir
- Veritabanına kayıt yapar

---

### `/olusumüyeekle`
**Açıklama:** Organizasyona üye ekler.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:**
- `kullanıcı` (zorunlu) - Eklenecek kullanıcı
- `olusum` (zorunlu) - Organizasyon adı

**Kullanım Örneği:**
```
/olusumüyeekle kullanıcı:@mafyaüyesi olusum:Mafya Ailesi
```

---

### `/olusumüyeçıkar`
**Açıklama:** Organizasyondan üye çıkarır.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:**
- `kullanıcı` (zorunlu) - Çıkarılacak kullanıcı
- `olusum` (zorunlu) - Organizasyon adı

**Kullanım Örneği:**
```
/olusumüyeçıkar kullanıcı:@mafyaüyesi olusum:Mafya Ailesi
```

---

### `/olusumsil`
**Açıklama:** Organizasyonları listeler ve silme seçeneği sunar.

**Yetki:** `Supervisor` rolü gerekli

**Parametreler:** Yok

**Kullanım Örneği:**
```
/olusumsil
```

---

## 👥 Personel Komutları

### `/rolver`
**Açıklama:** Kullanıcıya rol verir.

**Yetki:** `Staff` rolü gerekli

**Parametreler:**
- `kullanici` (zorunlu) - Rol verilecek kullanıcı
- `rol` (zorunlu) - Verilecek rol

**Kullanım Örneği:**
```
/rolver kullanici:@yeniüye rol:@Vatandaş
```

**Ne Yapar:**
- Kullanıcıya belirtilen rolü verir
- İşlem loglarını tutar
- Hata kontrolü yapar

---

### `/rolal`
**Açıklama:** Kullanıcıdan rol alır.

**Yetki:** `Staff` rolü gerekli

**Parametreler:**
- `kullanici` (zorunlu) - Rolü alınacak kullanıcı
- `rol` (zorunlu) - Alınacak rol

**Kullanım Örneği:**
```
/rolal kullanici:@kullanici rol:@Vatandaş
```

**Ne Yapar:**
- Kullanıcıdan belirtilen rolü alır
- İşlem loglarını tutar
- Hata kontrolü yapar

---

## 🎫 Ticket Sistemi

### `/ticketsetup`
**Açıklama:** Ticket sistemi kurulum panelini oluşturur.

**Yetki:** `Owner` rolü gerekli

**Parametreler:**
- `kanal` (zorunlu) - Ticket embedinin gönderileceği kanal

**Kullanım Örneği:**
```
/ticketsetup kanal:#destek
```

**Ne Yapar:**
- Belirtilen kanala ticket sistemi embedini gönderir
- "Destek Talebi Oluştur" butonu ekler
- "Sıkça Sorulan Sorular" butonu ekler
- "Sunucuya Bağlan" link butonu ekler

---

### `/destekstats`
**Açıklama:** Bir kullanıcının destek istatistiklerini gösterir.

**Yetki:** `Support` rolü gerekli

**Parametreler:**
- `kullanıcı` (zorunlu) - İstatistikleri görüntülenecek kullanıcı

**Kullanım Örneği:**
```
/destekstats kullanıcı:@destekçi
```

**Ne Yapar:**
- Toplam devraldığı talep sayısını gösterir
- Toplam kapattığı talep sayısını gösterir
- Ortalama yanıt süresini gösterir

---

### `/destektop`
**Açıklama:** En iyi destek performansını gösterir.

**Yetki:** `Support` rolü gerekli

**Parametreler:** Yok

**Kullanım Örneği:**
```
/destektop
```

**Ne Yapar:**
- En çok talep alan destekçileri listeler
- En hızlı yanıt veren destekçileri gösterir

---

## 📝 Beyaz Liste Komutları

### `/başvuru`
**Açıklama:** Bir kullanıcının başvuru sonucunu bildirir.

**Yetki:** `Application` rolü gerekli

**Parametreler:**
- `kullanıcı` (zorunlu) - İşlem yapılacak kullanıcı
- `işlem` (zorunlu) - Başvuru sonucu (Onayla/Reddet)
- `sebep` (opsiyonel) - Red sebebi (reddet seçildiyse zorunlu)

**Kullanım Örneği:**
```
/başvuru kullanıcı:@başvurucu işlem:Onayla
/başvuru kullanıcı:@başvurucu işlem:Reddet sebep:Eksik bilgi
```

**Ne Yapar:**
- Başvuru onaylandığında: Mülakat rolü verir
- Başvuru reddedildiğinde: Red rolü verir ve sebep loglar
- İstatistik kayıtlarını günceller
- Kullanıcıya DM gönderir

---

### `/mülakat`
**Açıklama:** Bir kullanıcının mülakat sonucunu bildirir.

**Yetki:** `Interviewer` rolü gerekli

**Parametreler:**
- `kullanıcı` (zorunlu) - İşlem yapılacak kullanıcı
- `işlem` (zorunlu) - Mülakat sonucu (Onayla/Reddet)
- `sebep` (opsiyonel) - Red sebebi (reddet seçildiyse zorunlu)

**Kullanım Örneği:**
```
/mülakat kullanıcı:@aday işlem:Onayla
/mülakat kullanıcı:@aday işlem:Reddet sebep:Roleplay yetersiz
```

**Ne Yapar:**
- Mülakat onaylandığında: Kayıtlı rol + Onay rolü verir
- Mülakat reddedildiğinde: Red rolü verir
- Kayıtsız rolünü kaldırır
- İstatistik kayıtlarını günceller

---

### `/basvuruform`
**Açıklama:** Başvuru panelini görüntüler.

**Yetki:** Herkes kullanabilir

**Parametreler:** Yok

**Kullanım Örneği:**
```
/basvuruform
```

**Ne Yapar:**
- Başvuru formu embedini gönderir
- "Başvuru Formunu Aç" butonu ekler
- Başvuru kurallarını açıklar

---

### `/başvurustats`
**Açıklama:** Bir kullanıcının başvuru istatistiklerini gösterir.

**Yetki:** `Staff` rolü gerekli

**Parametreler:**
- `kullanıcı` (zorunlu) - İstatistikleri görüntülenecek kullanıcı

**Kullanım Örneği:**
```
/başvurustats kullanıcı:@başvuruçi
```

**Ne Yapar:**
- Onaylanan başvuru sayısını gösterir
- Reddedilen başvuru sayısını gösterir
- Toplam başvuru sayısını gösterir

---

### `/başvurutop`
**Açıklama:** En iyi başvuru performansını gösterir.

**Yetki:** `Staff` rolü gerekli

**Parametreler:** Yok

**Kullanım Örneği:**
```
/başvurutop
```

---

### `/mulakatstats`
**Açıklama:** Bir kullanıcının mülakat istatistiklerini gösterir.

**Yetki:** `Staff` rolü gerekli

**Parametreler:**
- `kullanıcı` (zorunlu) - İstatistikleri görüntülenecek kullanıcı

**Kullanım Örneği:**
```
/mulakatstats kullanıcı:@mülakatçi
```

---

### `/mulakattop`
**Açıklama:** En iyi mülakat performansını gösterir.

**Yetki:** `Staff` rolü gerekli

**Parametreler:** Yok

**Kullanım Örneği:**
```
/mulakattop
```

---

## ⚙️ Panel Komutları

### `/system`
**Açıklama:** Sistem yönetim paneli.

**Yetki:** `Owner` rolü gerekli

**Parametreler:** Yok

**Kullanım Örneği:**
```
/system
```

**Ne Yapar:**
- Sistem yönetim panelini açar
- Otorol ayarları butonu ekler
- Diğer sistem ayarları için butonlar sunar

---

### `/topreset`
**Açıklama:** İstatistik sıfırlama paneli.

**Yetki:** `Owner` rolü gerekli

**Parametreler:** Yok

**Kullanım Örneği:**
```
/topreset
```

**Ne Yapar:**
- İstatistik sıfırlama butonları sunar
- Mülakat istatistiklerini sıfırlama
- Başvuru istatistiklerini sıfırlama
- Destek istatistiklerini sıfırlama

---

## 📊 İstatistik Komutları

### Genel İstatistik Bilgileri

Tüm istatistik komutları MongoDB veritabanından veri çeker ve aşağıdaki bilgileri gösterir:

**Başvuru İstatistikleri:**
- Onaylanan başvuru sayısı
- Reddedilen başvuru sayısı
- Toplam başvuru sayısı

**Mülakat İstatistikleri:**
- Onaylanan mülakat sayısı
- Reddedilen mülakat sayısı
- Toplam mülakat sayısı

**Destek İstatistikleri:**
- Toplam devralınan talep sayısı
- Toplam kapatılan talep sayısı
- Ortalama yanıt süresi

---

## 🔧 Teknik Detaylar

### Yetki Sistemi
- **Owner:** En yüksek yetki, tüm sistem ayarlarına erişim
- **Supervisor:** İşletme, departman, organizasyon yönetimi
- **Staff:** Rol verme/alma, istatistik görüntüleme
- **Application:** Başvuru değerlendirme
- **Interviewer:** Mülakat değerlendirme
- **Support:** Ticket sistemi yönetimi

### Veritabanı Yapısı
- **MongoDB:** İstatistik verileri için
- **Collections:** `basvuruStats`, `mulakatStats`, `supportStats`
- **İşletme/Departman/Organizasyon:** Ayrı koleksiyonlarda saklanır

### Log Sistemi
- Tüm işlemler ilgili log kanallarına kaydedilir
- Embed formatında detaylı log bilgileri
- Kullanıcı ID, tarih, işlem detayları dahil

### Hata Yönetimi
- Kapsamlı hata kontrolü
- Kullanıcı dostu hata mesajları
- Console logları ile debug bilgileri

---

## 🚀 Kullanım İpuçları

1. **Rol Renkleri:** Hex kodları kullanın (örn: FF0000 = kırmızı)
2. **Otomatik Tamamlama:** İşletme/departman adları otomatik tamamlanır
3. **Ephemeral Mesajlar:** Çoğu komut gizli yanıt verir (flags: 64)
4. **Log Kanalları:** Tüm işlemler otomatik loglanır
5. **Veritabanı:** MongoDB bağlantısı gerekli

---

## 📝 Notlar

- Tüm komutlar slash command formatında çalışır
- Embed mesajları tutarlı tasarım kullanır
- Türkçe karakter desteği tam
- Responsive tasarım ve hata yönetimi
- Detaylı log sistemi ile şeffaflık

---

*Bu rehber FivemBOT'un tüm komutlarını kapsar. Komutları kullanmadan önce gerekli yetkilere sahip olduğunuzdan emin olun.*
