# Genel SaaS - Teknik Döküman Oluşturma

## Açıklama
Çeşitli SaaS uygulamaları için teknik döküman hazırlamakta kullabileceğim promptları içermektedir. Bu konuda en başarılı LLM Claude 3.7 Sonnet (31 Mart 2025) olarak görünüyor.

## Çerçeve Belirleyici
Bu teknik dökümanı yazmak için oluşturulacak prompt’un çerçevesini belirler, teknik dökümanda yer alması veya olmaması istenen alanlara göre aşağıdaki prompt düzenlenebilir.

```markdown
**Görev:** [SaaS uygulamanızın adı] için [döküman türü] oluştur.

# Bağlam
- Uygulama: [SaaS uygulamanızın kısa açıklaması]
- Hedef kitle: [Geliştiriciler/Son kullanıcılar/Yöneticiler]
- Amaç: [Dökümanın amacı]

# Teknik Detaylar
- [Temel teknik özellikler]
- [Mimarinin özeti]
- [Teknoloji stack'i]

# Format
- Başlık ve alt başlıklar kullan
- Kod örnekleri ekle
- Teknik terminolojiyi açıkla
- Varsa api referansları ekle
- Adım adım talimatlar ver
- Tüm diyagramları d2 (https://d2lang.com/) kodu/formatı olarak ekle

# Ekstra Gereksinimler
- [Özel istekler: Diyagramlar, tablolar vb.]
```

## Teknik Dökümanı Üretecek Prompt'u Üretmek
Yukarıdaki çerçeveyle birlikte bu prompt’a projenin detaylarını içeren PDF dosyasının da eklenmesi de daha isabetli bir sonuç ortaya koyacaktır.

```markdown
Yukarıdaki çerçeveyi kullanarak ve eklediğim projenin özetini barındıran PDF doyasını da okuyarak örnek bir prompt hazırlayabilir misin?
```

## Teknik Dökümanı Üretecek Prompt'un Örnek Çıktısı
```
**Görev:** DentaTrack mobil uygulaması için kapsamlı teknik doküman oluştur.

# Bağlam
- Uygulama: DentaTrack, kullanıcıların diş tedavilerini ve kontrol randevularını takip edebilecekleri, günlük tutabilecekleri ve diş hekimi ziyaretleri için hatırlatıcılar ayarlayabilecekleri bir mobil uygulama.
- Hedef kitle: Uygulama geliştiricileri ve teknik ekip üyeleri
- Amaç: Uygulama mimarisini, API'lerini, veri modelini ve temel işlevselliğini detaylandırmak

# Teknik Detaylar
- Frontend: React Native kullanılarak iOS ve Android için hibrit uygulama
- Backend: Node.js ile Express API
- Veritabanı: MongoDB (kullanıcı profilleri ve günlük kayıtları için), PostgreSQL (randevu yönetimi için)
- Kimlik doğrulama: JWT tabanlı OAuth2 entegrasyonu
- Bildirim sistemi: Firebase Cloud Messaging
- API entegrasyonları: Google Takvim API, yerel sağlık hizmeti sağlayıcılarının API'leri
- Performans optimizasyonu

# Format
- Başlık ve alt başlıklar kullan
- İlgili her bölüm için kod örnekleri ekle
- RESTful API endpoints'lerinin tam referansını sağla
- Veri modeli şemalarını açıkla
- Bildirim konfigürasyonlarını detaylandır
- Uygulama state yönetimi açıklaması

# Ekstra Gereksinimler
- Mimari diyagram ekle
- Veritabanı ilişkiler şeması 
- Güvenlik önlemleri ve veri saklama politikaları belgesi
- Periyodik hatırlatıcı sisteminin teknik işleyişi
- Offline modu ve veri senkronizasyon mekanizması açıklaması

Teknik dökümanı her bölüm için ayrı md dosyaları olacak şekilde Markdown formatında root klasöründe oluştur.
Döküman dilini Türkçe yap.
Giriş(içindekiler) dosyasında diğer dosyalara link vermeyi unutma.
```


