# AKYA Energy Web Sitesi — Coder Agent Uygulama Talimatı

> Bu dosya, `akyaenergy.com` için oluşturulacak basic/statik kurumsal web sitesinin tamamını tarif eder. Coder agent bu dosyayı tek kaynak olarak kabul etmeli, ek soru sormadan siteyi uygulamalıdır.

---

## 1. Proje Özeti

AKYA Energy, AKYA Group çatısı altında konumlanan; petrokimya, doğalgaz ve yenilenebilir enerji alanlarına odaklanan yeni bir alt marka web sitesidir.

Ana hedef: `akya.net` üzerindeki AKYA Group kurumsal kimliğini bozmadan, aynı aileden geldiği hissedilen fakat enerji sektörüne özel daha farklı, daha endüstriyel ve daha güçlü bir marka havası veren sade bir web sitesi oluşturmak.

Site basic/statik olacaktır.

**Kesin kapsam dışı:**

- Yönetim paneli yok.
- CMS yok.
- Kullanıcı girişi yok.
- Dinamik blog yönetimi yok.
- Veritabanı yok.
- Backend zorunluluğu yok.
- Ürün sepeti/e-ticaret yok.
- Karmaşık dashboard yok.

Site; statik sayfalar, responsive arayüz, kurumsal içerikler, stok görseller ve iletişim alanından oluşacaktır.

---

## 2. Mevcut AKYA Group Sitesinden Alınacak Kurumsal Yön

Referans site: `akya.net`

Mevcut AKYA Group sitesinde şu karakter korunmalıdır:

- Koyu zeminli, kurumsal, teknoloji ve mühendislik hissi veren arayüz.
- Büyük hero alanı.
- Net ve güçlü başlıklar.
- Kart tabanlı çözüm/hizmet gösterimi.
- Kategorili üst menü mantığı.
- Mühendislik yaklaşımını anlatan süreç bölümü.
- Teknik, sade, güven veren metin dili.
- “Uçtan uca çözüm”, “ölçülebilir mühendislik”, “kritik altyapı”, “sürdürülebilirlik” gibi AKYA Group diline yakın ifadeler.

AKYA Energy sitesi birebir kopya olmamalıdır. Aynı aileden geldiği anlaşılmalı ancak renk, görsel dünya ve içerik dili enerji sektörüne kaydırılmalıdır.

---

## 3. Marka Konumlandırması

### Marka adı

**AKYA Energy**

### Ana marka ilişkisi

AKYA Energy, AKYA Group bünyesinde enerji, endüstriyel tesis ve sürdürülebilir altyapı projelerine odaklanan alt şirkettir.

### Marka hissi

- Kurumsal
- Güvenilir
- Mühendislik odaklı
- Endüstriyel
- Saha tecrübesi yüksek
- Sürdürülebilirlik bilinci olan
- Teknoloji ve enerji altyapısını birleştiren

### Ana mesaj

AKYA Group’un uçtan uca mühendislik ve dijital altyapı yaklaşımını enerji sektörüne taşıyan, petrokimya, doğalgaz ve yenilenebilir enerji alanlarında proje geliştirme, mühendislik, entegrasyon ve sürdürülebilir altyapı çözümleri sunan kurumsal enerji markası.

---

## 4. Tasarım Dili

### Genel yaklaşım

AKYA Group sitesinin karanlık, premium ve kurumsal çizgisi korunacak. AKYA Energy için daha sıcak, enerji odaklı ve endüstriyel renk vurguları eklenecek.

### Renk önerisi

Ana zemin:

- Çok koyu lacivert/siyaha yakın: `#07111F`
- İkinci koyu zemin: `#0B1828`
- Kart zemini: `#101D2E`

AKYA Group bağı:

- Kurumsal mavi: `#1F6FEB` veya benzeri güçlü teknik mavi

AKYA Energy farkı:

- Enerji yeşili: `#20C997`
- Sıcak enerji vurgusu: `#F5A623`
- Açık metin: `#F4F7FB`
- İkincil metin: `#AAB7C8`
- Border/çizgi: `rgba(255,255,255,0.10)`

Renk kullanımı:

- Ana görünüm koyu lacivert olmalı.
- CTA butonlarında enerji yeşili veya sıcak turuncu kullanılabilir.
- Petrokimya sayfasında turuncu/amber vurgu.
- Doğalgaz sayfasında mavi/çelik vurgu.
- Yenilenebilir enerji sayfasında yeşil vurgu.

### Tipografi

Modern, kurumsal ve okunabilir font kullanılmalı.

Öneri:

- Başlık: `Inter`, `Manrope` veya `Sora`
- Gövde: `Inter` veya sistem fontları

Başlıklar büyük, net ve kısa olmalı. Paragraflar çok uzun bloklar halinde verilmemeli.

### Görsel tarzı

- Stok fotoğraflar kullanılacak.
- Görseller endüstriyel, gerçekçi, premium ve yüksek çözünürlüklü olmalı.
- Yapay/ucuz görünen illüstrasyonlardan kaçınılmalı.
- Görseller koyu overlay ile siteye entegre edilmeli.
- Rafineri, boru hatları, enerji altyapısı, güneş paneli, rüzgar türbini, saha mühendisi, kontrol odası gibi görseller tercih edilmeli.

### Genel layout

- Geniş container: max-width 1180–1280 px.
- Bol boşluklu section yapısı.
- Kartlarda hafif border, hafif blur/gradient, yumuşak radius.
- Button hover efektleri olmalı.
- Mobilde sade ve okunabilir yapı korunmalı.

---

## 5. Teknik Kapsam ve Stack Talimatı

Coder agent mevcut bir repo içinde çalışıyorsa mevcut stack’i bozmadan ilerlemelidir. Sıfırdan proje oluşturulacaksa aşağıdaki yapı önerilir:

- Framework: Next.js veya React/Vite
- Styling: Tailwind CSS veya sade CSS modules
- Dil: TypeScript tercih edilir
- Site türü: Statik kurumsal site
- Deploy hedefi: Vercel, Netlify veya klasik static hosting uyumlu olmalı

Backend kurulmayacak. Contact form varsa sadece front-end validasyonlu olabilir. Gerçek mail gönderimi için ileride backend/form service bağlanacak şekilde placeholder bırakılmalıdır.

### Performans

- Görseller optimize edilmeli.
- Stok görseller mümkünse `.webp` formatına çevrilmeli.
- Lazy loading kullanılmalı.
- Gereksiz animasyon ve ağır kütüphaneler kullanılmamalı.

### SEO

Her sayfada ayrı title, description, canonical mantığı ve Open Graph bilgileri hazırlanmalıdır.

---

## 6. Site Haritası

Oluşturulacak sayfalar:

```txt
/
/hizmetler
/hizmetler/petrokimya
/hizmetler/dogalgaz
/hizmetler/yenilenebilir-enerji
/hakkimizda
/iletisim
```

Minimum bu sayfalar uygulanmalıdır. `/hizmetler` sayfası, üç hizmetin toplu gösterildiği kategori sayfası olmalıdır.

---

## 7. Üst Menü Yapısı

Header sabit veya sticky olabilir. AKYA Group sitesindeki kurumsal menü hissi korunmalı.

### Menü

- Ana Sayfa → `/`
- Hizmetler → dropdown/mega dropdown
  - Petrokimya → `/hizmetler/petrokimya`
  - Doğalgaz → `/hizmetler/dogalgaz`
  - Yenilenebilir Enerji → `/hizmetler/yenilenebilir-enerji`
- Hakkımızda → `/hakkimizda`
- İletişim → `/iletisim`

### Header detayları

Sol tarafta logo:

- Eğer resmi logo verilmemişse geçici text logo kullan:
  - `AKYA` büyük ve güçlü
  - `Energy` daha ince veya yeşil/turuncu vurgu ile
- Altında veya yakınında küçük ifade kullanılabilir:
  - `AKYA Group Company`

Sağ tarafta CTA butonu:

- `Projenizi Konuşalım` → `/iletisim`

Mobilde hamburger menü olmalı. Dropdown mobilde accordion gibi açılmalı.

---

## 8. Footer Yapısı

Footer koyu zeminde olmalı.

Footer kolonları:

1. Marka
   - AKYA Energy
   - AKYA Group bünyesinde enerji ve endüstriyel altyapı çözümleri.

2. Hizmetler
   - Petrokimya
   - Doğalgaz
   - Yenilenebilir Enerji

3. Şirket
   - Hakkımızda
   - İletişim

4. İletişim
   - Adres için AKYA Group adresi placeholder olarak kullanılabilir.
   - E-posta placeholder: `info@akyaenergy.com`
   - Telefon placeholder: `+90 ...`

Alt satır:

`© 2026 AKYA Energy. AKYA Group bünyesindedir. Tüm hakları saklıdır.`

---

## 9. Ana Sayfa İçerik Yapısı

Ana sayfa güçlü, kısa ve hizmetleri hemen anlatan yapıda olmalı.

### 9.1 Hero Section

#### Eyebrow

`AKYA GROUP BÜNYESİNDE ENERJİ ÇÖZÜMLERİ`

#### H1

`Enerji altyapılarında güvenilir mühendislik ortağınız`

#### Alt metin

`AKYA Energy; petrokimya, doğalgaz ve yenilenebilir enerji alanlarında mühendislik, proje geliştirme, saha entegrasyonu ve sürdürülebilir altyapı çözümleri sunar. AKYA Group’un uçtan uca çözüm yaklaşımını enerji sektörünün kritik ihtiyaçlarıyla birleştirir.`

#### CTA butonları

- Birincil: `Hizmetleri İncele` → `/hizmetler`
- İkincil: `İletişime Geç` → `/iletisim`

#### Hero görseli

Stok görsel: Endüstriyel enerji tesisi, boru hatları, güneş/rüzgar enerji teması veya enerji kontrol merkezi.

Arama terimleri:

- `industrial energy infrastructure engineer`
- `oil gas pipeline energy facility`
- `renewable energy engineer solar wind`
- `energy control room industrial`

Görsel koyu overlay ile kullanılmalı.

#### Hero metrikleri

Kartlar halinde:

- `3` — Odak enerji alanı
- `Uçtan uca` — Mühendislik yaklaşımı
- `Saha odaklı` — Proje ve entegrasyon deneyimi
- `Sürdürülebilir` — Verimli enerji altyapısı

---

### 9.2 Hizmetler Özeti

Başlık:

`Enerji sektörünün kritik alanları için çözüm başlıkları`

Alt metin:

`AKYA Energy, endüstriyel tesislerin enerji ihtiyaçlarını yalnızca ekipman veya uygulama seviyesinde değil; analiz, tasarım, entegrasyon, izleme ve sürdürülebilir operasyon perspektifiyle ele alır.`

Üç kart:

#### Kart 1 — Petrokimya

Kısa metin:

`Petrokimya tesislerinde enerji altyapısı, proses destek sistemleri, saha mühendisliği ve güvenilir operasyon için teknik çözümler.`

Buton: `Detayları Gör`

Link: `/hizmetler/petrokimya`

#### Kart 2 — Doğalgaz

Kısa metin:

`Doğalgaz altyapılarında güvenli, izlenebilir ve mevzuata uyumlu mühendislik, entegrasyon ve saha destek çözümleri.`

Buton: `Detayları Gör`

Link: `/hizmetler/dogalgaz`

#### Kart 3 — Yenilenebilir Enerji

Kısa metin:

`Güneş, rüzgar ve hibrit enerji projelerinde fizibiliteden saha uygulamasına kadar sürdürülebilir enerji çözümleri.`

Buton: `Detayları Gör`

Link: `/hizmetler/yenilenebilir-enerji`

---

### 9.3 AKYA Group Bağlantısı

Başlık:

`AKYA Group’un mühendislik yaklaşımı enerji sektöründe`

Metin:

`AKYA Energy, AKYA Group’un kritik tesisler, dijital altyapılar, otomasyon, izleme ve sürdürülebilirlik alanlarındaki mühendislik yaklaşımını enerji projelerine taşır. Böylece enerji yatırımlarında yalnızca kurulum değil; ölçülebilir performans, izlenebilir operasyon ve uzun vadeli sürdürülebilirlik hedeflenir.`

Yan kartlar:

- `Analiz ve fizibilite`
- `Mühendislik tasarımı`
- `Saha uygulaması`
- `Test ve devreye alma`
- `İzleme ve optimizasyon`

---

### 9.4 Çalışma Yaklaşımı

Başlık:

`Analizden devreye almaya ölçülebilir enerji mühendisliği`

Adımlar:

1. **Analiz**  
   `Mevcut altyapı, tesis koşulları, enerji tüketimi, operasyonel gereksinimler ve teknik riskler değerlendirilir.`

2. **Tasarım**  
   `Proje ihtiyacına göre enerji altyapısı, ekipman seçimi, saha yerleşimi, izleme noktaları ve entegrasyon yapısı planlanır.`

3. **Projelendirme**  
   `Teknik dokümanlar, uygulama detayları, tek hat şemaları, saha planları ve iş paketleri hazırlanır.`

4. **Uygulama ve Entegrasyon**  
   `Saha ekipleri, tedarikçiler ve teknik paydaşlarla koordineli şekilde uygulama ve sistem entegrasyonu gerçekleştirilir.`

5. **Test ve Optimizasyon**  
   `Devreye alma, performans kontrolü, ölçüm, raporlama ve iyileştirme çalışmaları ile sistemin sürdürülebilirliği desteklenir.`

---

### 9.5 Sektörel Kullanım Alanları

Başlık:

`Endüstriyel enerji yatırımları için uygulanabilir çözümler`

Kartlar:

- Endüstriyel tesisler
- Üretim tesisleri
- Kritik altyapılar
- Enerji santralleri
- Rafineri ve petrokimya tesisleri
- Doğalgaz altyapıları
- GES ve hibrit enerji sahaları

---

### 9.6 CTA Section

Başlık:

`Enerji projenizi birlikte değerlendirelim`

Metin:

`Petrokimya, doğalgaz veya yenilenebilir enerji alanındaki projeniz için ihtiyaç analizi, teknik kapsam ve uygulanabilir yol haritası oluşturalım.`

Buton:

`İletişime Geç` → `/iletisim`

---

## 10. Hizmetler Genel Sayfası — `/hizmetler`

### H1

`Enerji çözümlerimiz`

### Açıklama

`AKYA Energy, enerji sektörünün üç kritik alanında mühendislik ve uygulama odaklı çözümler sunar: petrokimya, doğalgaz ve yenilenebilir enerji. Her hizmet alanında amaç; güvenli, sürdürülebilir, izlenebilir ve ölçeklenebilir enerji altyapıları oluşturmaktır.`

### Hizmet kartları

Üç büyük kart yer almalı:

1. Petrokimya
2. Doğalgaz
3. Yenilenebilir Enerji

Her kartta:

- Stok görsel
- Kategori etiketi
- Başlık
- 2–3 cümle açıklama
- 4 maddelik mini liste
- `Detayları Gör` butonu

---

## 11. Petrokimya Sayfası — `/hizmetler/petrokimya`

### SEO

Title:

`Petrokimya Enerji Çözümleri | AKYA Energy`

Description:

`AKYA Energy, petrokimya tesisleri için enerji altyapısı, saha mühendisliği, entegrasyon, izleme ve sürdürülebilir operasyon çözümleri sunar.`

### Hero

Eyebrow:

`HİZMETLER / PETROKİMYA`

H1:

`Petrokimya tesisleri için güvenilir enerji ve altyapı mühendisliği`

Alt metin:

`Petrokimya tesislerinde süreklilik, güvenlik ve proses kararlılığı kritik öneme sahiptir. AKYA Energy, enerji altyapısı, saha mühendisliği, teknik entegrasyon ve performans izleme yaklaşımlarıyla petrokimya operasyonlarının güvenilirliğini destekler.`

CTA:

`Projenizi Değerlendirelim` → `/iletisim`

Hero görsel arama terimleri:

- `petrochemical plant pipes refinery night`
- `industrial refinery pipeline engineer`
- `chemical plant energy infrastructure`

### Sayfa bölümleri

#### Bölüm 1 — Genel Yaklaşım

Başlık:

`Proses sürekliliğini destekleyen mühendislik yaklaşımı`

Metin:

`Petrokimya tesislerinde enerji altyapısı, yalnızca elektrik veya mekanik sistemlerden ibaret değildir. Proses güvenliği, yardımcı tesisler, izleme noktaları, saha erişimi, bakım sürekliliği ve operasyonel riskler birlikte değerlendirilmelidir. AKYA Energy, bu bütüncül bakışla tesislerin enerji ve altyapı ihtiyaçlarını analiz eder, uygulanabilir teknik çözümler geliştirir.`

#### Bölüm 2 — Çözüm Kapsamı

Kart/madde yapısı:

1. **Enerji altyapısı değerlendirmesi**  
   `Mevcut enerji dağıtımı, saha yükleri, kritik hatlar ve operasyonel süreklilik ihtiyaçları analiz edilir.`

2. **Proses destek sistemleri**  
   `Yardımcı enerji sistemleri, otomasyon bağlantıları, izleme noktaları ve saha ekipmanları proje kapsamına göre ele alınır.`

3. **Saha mühendisliği ve uygulama koordinasyonu**  
   `Saha koşulları, iş güvenliği, uygulama planı ve teknik paydaş koordinasyonu dikkate alınarak proje yürütülür.`

4. **İzleme ve performans takibi**  
   `Enerji tüketimi, proses destek altyapısı ve kritik operasyon parametreleri izlenebilir hale getirilecek şekilde kurgulanır.`

5. **Sürdürülebilirlik ve verimlilik**  
   `Tesisin enerji kullanımı, kayıp noktaları ve iyileştirme potansiyelleri analiz edilerek sürdürülebilir operasyon hedeflenir.`

#### Bölüm 3 — Öne Çıkan Değerler

- Operasyon sürekliliği
- Teknik risklerin görünür hale getirilmesi
- Güvenli saha uygulaması
- Enerji verimliliği
- İzlenebilir altyapı
- Uzun vadeli bakım ve performans yaklaşımı

#### Bölüm 4 — CTA

Başlık:

`Petrokimya tesisiniz için teknik kapsam oluşturalım`

Metin:

`Mevcut tesisinizin enerji altyapısını, saha koşullarını veya yeni yatırım planınızı birlikte değerlendirelim.`

Buton:

`İletişime Geç`

---

## 12. Doğalgaz Sayfası — `/hizmetler/dogalgaz`

### SEO

Title:

`Doğalgaz Altyapı Çözümleri | AKYA Energy`

Description:

`AKYA Energy, doğalgaz altyapıları için güvenli, izlenebilir ve saha odaklı mühendislik, entegrasyon ve teknik danışmanlık çözümleri sunar.`

### Hero

Eyebrow:

`HİZMETLER / DOĞALGAZ`

H1:

`Doğalgaz altyapıları için güvenli ve izlenebilir çözümler`

Alt metin:

`Doğalgaz projelerinde güvenlik, süreklilik, ölçüm, izleme ve mevzuata uyum temel kriterlerdir. AKYA Energy, doğalgaz altyapılarında mühendislik, saha entegrasyonu ve operasyonel güvenilirlik odaklı çözümler geliştirir.`

CTA:

`Doğalgaz Projenizi Konuşalım` → `/iletisim`

Hero görsel arama terimleri:

- `natural gas pipeline valve station`
- `gas distribution station engineer`
- `industrial gas pipeline infrastructure`
- `natural gas pressure regulating station`

### Sayfa bölümleri

#### Bölüm 1 — Genel Yaklaşım

Başlık:

`Güvenlik ve süreklilik odağında doğalgaz mühendisliği`

Metin:

`Doğalgaz altyapılarında sistem güvenliği, ölçüm doğruluğu, saha ekipmanlarının erişilebilirliği ve operasyon sürekliliği birlikte değerlendirilmelidir. AKYA Energy; proje gereksinimlerini, saha koşullarını, ilgili mevzuat ve yetkili kurum beklentilerini dikkate alarak uygulanabilir teknik çözümler oluşturur.`

#### Bölüm 2 — Çözüm Kapsamı

1. **Altyapı analizi ve teknik değerlendirme**  
   `Mevcut veya planlanan doğalgaz altyapısının kapasite, güvenlik, ölçüm ve izleme ihtiyaçları değerlendirilir.`

2. **Saha entegrasyonu**  
   `Saha ekipmanları, kontrol noktaları, enerji beslemeleri, haberleşme altyapısı ve yardımcı sistemler proje bütünlüğü içinde ele alınır.`

3. **Ölçüm ve izleme altyapısı**  
   `Basınç, debi, tüketim ve operasyon verilerinin izlenebilir olması için teknik altyapı kurgulanır.`

4. **Güvenlik ve operasyon sürekliliği**  
   `Risk noktaları, acil durum senaryoları, bakım erişilebilirliği ve işletme sürekliliği dikkate alınır.`

5. **Teknik dokümantasyon ve raporlama**  
   `Proje kapsamı, saha bulguları, teknik çizimler ve uygulama notları düzenli raporlanır.`

#### Bölüm 3 — Öne Çıkan Değerler

- Güvenli altyapı yaklaşımı
- Mevzuat ve kurum şartlarına uyum bilinci
- İzlenebilir saha operasyonu
- Ölçüm ve raporlama kabiliyeti
- Bakım erişilebilirliği
- Teknik risk yönetimi

#### Bölüm 4 — CTA

Başlık:

`Doğalgaz altyapınız için güvenli bir yol haritası oluşturalım`

Metin:

`Planlanan veya mevcut doğalgaz altyapınız için teknik kapsam, saha gereksinimleri ve izleme yaklaşımını birlikte değerlendirelim.`

Buton:

`İletişime Geç`

---

## 13. Yenilenebilir Enerji Sayfası — `/hizmetler/yenilenebilir-enerji`

### SEO

Title:

`Yenilenebilir Enerji Çözümleri | AKYA Energy`

Description:

`AKYA Energy, güneş, rüzgar ve hibrit yenilenebilir enerji projeleri için fizibilite, mühendislik, saha uygulaması, izleme ve performans çözümleri sunar.`

### Hero

Eyebrow:

`HİZMETLER / YENİLENEBİLİR ENERJİ`

H1:

`Sürdürülebilir enerji yatırımları için uçtan uca mühendislik`

Alt metin:

`Yenilenebilir enerji projelerinde doğru fizibilite, doğru mühendislik ve doğru saha uygulaması yatırım performansını doğrudan etkiler. AKYA Energy, güneş, rüzgar ve hibrit enerji projelerinde sürdürülebilir, izlenebilir ve ölçeklenebilir çözümler sunar.`

CTA:

`Yenilenebilir Enerji Projenizi Başlatalım` → `/iletisim`

Hero görsel arama terimleri:

- `solar panels engineer renewable energy`
- `wind turbines solar farm engineer`
- `renewable energy infrastructure field`
- `solar power plant drone view`

### Sayfa bölümleri

#### Bölüm 1 — Genel Yaklaşım

Başlık:

`Fizibiliteden performans optimizasyonuna sürdürülebilir enerji yaklaşımı`

Metin:

`Yenilenebilir enerji yatırımlarında yalnızca kurulu güç değil; saha koşulları, üretim potansiyeli, bağlantı altyapısı, ekipman seçimi, işletme modeli ve performans izleme kabiliyeti birlikte ele alınmalıdır. AKYA Energy, projelerin teknik ve operasyonel sürdürülebilirliğini destekleyen bütüncül bir mühendislik yaklaşımı sunar.`

#### Bölüm 2 — Çözüm Kapsamı

1. **Fizibilite ve saha değerlendirmesi**  
   `Saha koşulları, enerji üretim potansiyeli, altyapı uygunluğu ve yatırım hedefleri analiz edilir.`

2. **GES ve hibrit enerji mühendisliği**  
   `Güneş enerjisi, rüzgar destekli çözümler ve hibrit sistem ihtiyaçları proje bazında değerlendirilir.`

3. **Elektrik altyapısı ve bağlantı yaklaşımı**  
   `Enerji üretim tesisi bağlantıları, dağıtım yapısı, koruma yaklaşımı ve izleme altyapısı planlanır.`

4. **Saha uygulaması ve devreye alma desteği**  
   `Uygulama planı, saha koordinasyonu, test süreçleri ve devreye alma adımları teknik olarak desteklenir.`

5. **Performans izleme ve verimlilik**  
   `Üretim verileri, kayıp analizleri, performans oranı ve operasyonel iyileştirme alanları izlenebilir hale getirilir.`

#### Bölüm 3 — Öne Çıkan Değerler

- Sürdürülebilir yatırım yaklaşımı
- Doğru fizibilite ve saha analizi
- GES ve hibrit sistem bilgisi
- Ölçülebilir performans
- Enerji verimliliği
- Uzun vadeli operasyon desteği

#### Bölüm 4 — CTA

Başlık:

`Yenilenebilir enerji yatırımınızı teknik olarak değerlendirelim`

Metin:

`Saha, kapasite, bağlantı ve performans hedeflerinize göre uygulanabilir bir enerji yol haritası oluşturalım.`

Buton:

`İletişime Geç`

---

## 14. Hakkımızda Sayfası — `/hakkimizda`

### SEO

Title:

`Hakkımızda | AKYA Energy`

Description:

`AKYA Energy, AKYA Group bünyesinde petrokimya, doğalgaz ve yenilenebilir enerji alanlarında mühendislik ve sürdürülebilir altyapı çözümleri sunar.`

### H1

`AKYA Group’un enerji sektöründeki mühendislik markası`

### Ana metin

`AKYA Energy, AKYA Group çatısı altında enerji ve endüstriyel altyapı alanlarına odaklanan kurumsal bir mühendislik markasıdır. Petrokimya, doğalgaz ve yenilenebilir enerji başlıklarında proje geliştirme, teknik analiz, saha entegrasyonu, izleme ve sürdürülebilir operasyon çözümleri sunar.`

`AKYA Group’un kritik tesisler, dijital altyapılar, otomasyon, test, analiz ve sürdürülebilirlik alanlarındaki yaklaşımı; AKYA Energy ile enerji sektörünün ihtiyaçlarına özel hale getirilir. Amaç, enerji projelerinde güvenilir, ölçülebilir ve uzun vadeli değer üreten altyapılar oluşturmaktır.`

### Değerler

- Güvenilir mühendislik
- Saha gerçeklerine uygun çözüm
- Ölçülebilir performans
- Sürdürülebilir enerji yaklaşımı
- AKYA Group kurumsal gücü
- Teknik şeffaflık ve raporlama

### CTA

Başlık:

`Enerji projelerinde AKYA yaklaşımıyla ilerleyin`

Buton:

`İletişime Geç`

---

## 15. İletişim Sayfası — `/iletisim`

### SEO

Title:

`İletişim | AKYA Energy`

Description:

`Petrokimya, doğalgaz ve yenilenebilir enerji projeleriniz için AKYA Energy ile iletişime geçin.`

### H1

`Enerji projenizi birlikte değerlendirelim`

### Açıklama

`Petrokimya, doğalgaz veya yenilenebilir enerji alanındaki proje, yatırım veya teknik ihtiyaçlarınız için AKYA Energy ekibiyle iletişime geçebilirsiniz.`

### İletişim bilgileri

- E-posta: `info@akyaenergy.com`
- Telefon: `+90 ...`
- Adres: `1552. Sokak, Çiğdem Mahallesi, No:1, Kat:4, Çankaya, Ankara, Türkiye`

Adres, AKYA Group adresi olarak placeholder kullanılabilir. Daha sonra kesin bilgi ile güncellenecek şekilde kolay değiştirilebilir olmalıdır.

### Form alanları

Form backend’e bağlanmayacaksa bile arayüz olarak yer alabilir.

Alanlar:

- Ad Soyad
- Şirket
- E-posta
- Telefon
- Hizmet Alanı
  - Petrokimya
  - Doğalgaz
  - Yenilenebilir Enerji
  - Genel Bilgi
- Mesaj

Buton:

`Mesaj Gönder`

Form gönderiminde backend yoksa:

- Sayfa çökmesin.
- Kullanıcıya şu mesaj gösterilsin:
  - `Teşekkürler. Mesaj gönderim altyapısı aktif edildiğinde bu form çalışacaktır. Şimdilik info@akyaenergy.com üzerinden iletişime geçebilirsiniz.`

Alternatif olarak `mailto:` linki kullanılabilir.

---

## 16. Stok Görsel Talimatları

Coder agent, stok görselleri lisans problemi olmayan kaynaklardan seçmelidir.

Önerilen kaynaklar:

- Unsplash
- Pexels
- Pixabay

Kesin kurallar:

- Watermark içeren görsel kullanılmayacak.
- Logo/marka içeren görsel kullanılmayacak.
- Kalitesiz, bulanık, aşırı yapay görsel kullanılmayacak.
- İnsanlı görsel kullanılacaksa profesyonel saha mühendisi/operatör hissi vermeli.
- Görseller mümkünse `.webp` formatına çevrilmeli.
- Tüm görseller için `alt` metni yazılmalı.
- Görseller `/public/images/` altında tutulmalı.

### Görsel dosya planı

```txt
/public/images/hero-energy-infrastructure.webp
/public/images/service-petrochemical.webp
/public/images/service-natural-gas.webp
/public/images/service-renewable-energy.webp
/public/images/akya-group-energy-bridge.webp
/public/images/cta-energy-project.webp
```

### Görsel eşleşmeleri

#### Ana sayfa hero

Dosya: `hero-energy-infrastructure.webp`

Arama:

- `industrial energy infrastructure engineer`
- `energy plant pipeline control room`

Alt text:

`Endüstriyel enerji altyapısını temsil eden tesis ve mühendislik görseli`

#### Petrokimya

Dosya: `service-petrochemical.webp`

Arama:

- `petrochemical plant pipes refinery`
- `industrial refinery at night`

Alt text:

`Petrokimya tesisi ve proses boru hatlarını temsil eden endüstriyel görsel`

#### Doğalgaz

Dosya: `service-natural-gas.webp`

Arama:

- `natural gas pipeline valve station`
- `gas pressure regulating station`

Alt text:

`Doğalgaz boru hattı ve vana istasyonunu temsil eden altyapı görseli`

#### Yenilenebilir Enerji

Dosya: `service-renewable-energy.webp`

Arama:

- `solar panels wind turbines engineer`
- `renewable energy solar farm`

Alt text:

`Yenilenebilir enerji sahası, güneş panelleri ve rüzgar türbinlerini temsil eden görsel`

---

## 17. Component Planı

Uygulama component tabanlı yapılmalıdır.

Önerilen componentler:

```txt
components/
  Header.tsx
  Footer.tsx
  Container.tsx
  Button.tsx
  SectionHeader.tsx
  ServiceCard.tsx
  ProcessSteps.tsx
  CTASection.tsx
  Hero.tsx
  Breadcrumb.tsx
  ContactForm.tsx
  StatCard.tsx
```

### Header

- Logo
- Desktop menü
- Hizmetler dropdown
- Mobil hamburger
- CTA butonu

### ServiceCard

Props:

- title
- category
- description
- image
- href
- accent

### ProcessSteps

Props:

- steps array
- step number
- title
- description

### CTASection

Props:

- title
- description
- buttonText
- buttonHref

### ContactForm

- Front-end validasyon
- Backend yoksa graceful message
- Submit sonrası kullanıcı bilgilendirme

---

## 18. Veri Dosyası Önerisi

İçerikler tek bir data dosyasında tutulabilir.

Örnek:

```txt
data/services.ts
```

İçerik yapısı:

```ts
export const services = [
  {
    slug: 'petrokimya',
    title: 'Petrokimya',
    href: '/hizmetler/petrokimya',
    accent: 'amber',
    image: '/images/service-petrochemical.webp',
    shortDescription: 'Petrokimya tesislerinde enerji altyapısı, proses destek sistemleri ve saha mühendisliği çözümleri.',
  },
  {
    slug: 'dogalgaz',
    title: 'Doğalgaz',
    href: '/hizmetler/dogalgaz',
    accent: 'blue',
    image: '/images/service-natural-gas.webp',
    shortDescription: 'Doğalgaz altyapılarında güvenli, izlenebilir ve mevzuata uyumlu mühendislik çözümleri.',
  },
  {
    slug: 'yenilenebilir-enerji',
    title: 'Yenilenebilir Enerji',
    href: '/hizmetler/yenilenebilir-enerji',
    accent: 'green',
    image: '/images/service-renewable-energy.webp',
    shortDescription: 'Güneş, rüzgar ve hibrit enerji projelerinde sürdürülebilir enerji mühendisliği çözümleri.',
  },
]
```

---

## 19. Sayfa Tasarım Şablonu

Hizmet detay sayfaları aynı template’i kullanmalıdır.

```txt
[Header]
[Hero / Breadcrumb + H1 + açıklama + CTA + görsel]
[Genel Yaklaşım]
[Çözüm Kapsamı kartları]
[Öne Çıkan Değerler]
[İlgili Hizmetler veya diğer hizmet kartları]
[CTA]
[Footer]
```

Her hizmet sayfasında diğer iki hizmete link veren küçük bir “Diğer Hizmetler” bölümü yer alabilir.

---

## 20. Responsive Davranış

### Desktop

- Header yatay menü.
- Hizmetler dropdown hover/click ile açılabilir.
- Hero iki kolon: sol metin, sağ görsel.
- Hizmet kartları üç kolon.
- Process step yatay veya grid.

### Tablet

- Kartlar iki kolon olabilir.
- Hero görsel/metin dengeli olmalı.

### Mobil

- Header hamburger.
- Hero tek kolon.
- Kartlar tek kolon.
- Font boyutları küçülmeli ama premium hissi bozulmamalı.
- CTA butonları alt alta gelebilir.
- Dropdown mobilde accordion olmalı.

---

## 21. Animasyon ve Etkileşim

Aşırı animasyon kullanılmamalı. Kurumsal ve ciddi kalmalı.

Kabul edilebilir efektler:

- Hover’da kart border/parlaklık değişimi.
- Buton hover.
- Header scroll sonrası hafif blur veya koyulaşma.
- Section girişlerinde çok hafif fade-up kullanılabilir.

Kullanılmaması gerekenler:

- Aşırı hareketli background.
- Ucuz particle efektleri.
- Gereksiz slider/carousel.
- Sayfa performansını düşüren ağır animasyonlar.

---

## 22. SEO İçerikleri

### Genel site title

`AKYA Energy | Petrokimya, Doğalgaz ve Yenilenebilir Enerji Çözümleri`

### Genel description

`AKYA Energy, AKYA Group bünyesinde petrokimya, doğalgaz ve yenilenebilir enerji alanlarında mühendislik, saha entegrasyonu ve sürdürülebilir altyapı çözümleri sunar.`

### Anahtar kelime yönü

Metinlerde doğal şekilde şu kavramlar geçebilir:

- enerji mühendisliği
- petrokimya enerji çözümleri
- doğalgaz altyapısı
- yenilenebilir enerji çözümleri
- güneş enerjisi projeleri
- endüstriyel enerji altyapısı
- saha mühendisliği
- sürdürülebilir enerji
- enerji izleme ve optimizasyon

Keyword stuffing yapılmamalı.

---

## 23. Erişilebilirlik

- Tüm görsellerde açıklayıcı alt text olmalı.
- Butonlar klavye ile kullanılabilir olmalı.
- Renk kontrastı yeterli olmalı.
- Header menüsü klavye erişimine uygun olmalı.
- Form label’ları gerçek label olarak yazılmalı.

---

## 24. Dosya ve Klasör Yapısı Önerisi

Next.js tercih edilirse:

```txt
app/
  layout.tsx
  page.tsx
  hizmetler/
    page.tsx
    petrokimya/
      page.tsx
    dogalgaz/
      page.tsx
    yenilenebilir-enerji/
      page.tsx
  hakkimizda/
    page.tsx
  iletisim/
    page.tsx
components/
  Header.tsx
  Footer.tsx
  Container.tsx
  Button.tsx
  Hero.tsx
  ServiceCard.tsx
  SectionHeader.tsx
  ProcessSteps.tsx
  CTASection.tsx
  ContactForm.tsx
data/
  services.ts
  navigation.ts
public/
  images/
    hero-energy-infrastructure.webp
    service-petrochemical.webp
    service-natural-gas.webp
    service-renewable-energy.webp
styles/
  globals.css
```

React/Vite tercih edilirse aynı mantık `src/pages`, `src/components`, `src/data` şeklinde uygulanabilir.

---

## 25. İçerik Tonu

Metin dili Türkçe olmalı.

Ton:

- Kurumsal
- Teknik ama anlaşılır
- İddialı fakat abartısız
- Sahaya ve mühendisliğe yakın
- AKYA Group çizgisine uygun

Kaçınılması gerekenler:

- “Dünyanın en iyisi” gibi abartılı iddialar
- Belgesi olmayan sertifika/akreditasyon iddiaları
- Tamamlanmış proje sayısı gibi doğrulanmamış sayılar
- Lisans/yetki belgesi iddiası
- Fazla reklam kokan metin

---

## 26. Kabul Kriterleri

Site tamamlandığında aşağıdakiler sağlanmış olmalı:

- Ana sayfa mevcut.
- Hizmetler genel sayfası mevcut.
- Petrokimya hizmet sayfası mevcut.
- Doğalgaz hizmet sayfası mevcut.
- Yenilenebilir enerji hizmet sayfası mevcut.
- Hakkımızda sayfası mevcut.
- İletişim sayfası mevcut.
- Üst menüde Hizmetler dropdown içinde üç hizmet başlığı mevcut.
- Mobil menü çalışıyor.
- Tüm linkler doğru route’a gidiyor.
- Site basic/statik çalışıyor.
- Yönetim paneli yok.
- Backend yok.
- Stok görseller yerleştirilmiş.
- Görsellerde watermark yok.
- Tüm görsellerde alt text var.
- Footer düzenli.
- SEO title ve description alanları doldurulmuş.
- Site AKYA Group kurumsal kimliğine yakın ama AKYA Energy olarak farklılaşıyor.
- Tasarım koyu, kurumsal, mühendislik odaklı ve enerji sektörüne uygun.

---

## 27. Coder Agent İçin Uygulama Sırası

1. Mevcut repo varsa incele, yoksa statik kurumsal site için proje oluştur.
2. Global theme, renkler, font ve layout container yapısını hazırla.
3. Header, footer ve temel componentleri oluştur.
4. Ana sayfayı oluştur.
5. Hizmetler genel sayfasını oluştur.
6. Üç hizmet detay sayfasını aynı template mantığıyla oluştur.
7. Hakkımızda ve iletişim sayfalarını oluştur.
8. Stok görselleri seç, optimize et ve `/public/images/` altına koy.
9. SEO metadata alanlarını ekle.
10. Responsive kontrolleri yap.
11. Linkleri ve mobil menüyü test et.
12. Final polish: spacing, hover, contrast, görsel overlay, typography.
13. Build al ve hata varsa düzelt.

---

## 28. Son Not

Bu web sitesi, AKYA Group’un mevcut kurumsal duruşunu enerji sektörüne taşıyan sade ve güçlü bir alt marka sitesi olmalıdır. Tasarım akya.net ile akraba görünmeli; ancak AKYA Energy’nin petrokimya, doğalgaz ve yenilenebilir enerji odaklı ayrı bir uzmanlık markası olduğu ilk bakışta anlaşılmalıdır.
