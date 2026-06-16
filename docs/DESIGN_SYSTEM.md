# AKYA Energy Design System and Visual Standard

## 1. Creative direction

**Industrial intelligence, engineered energy.**

Site karanlık ve premium olmalı; ancak yalnız koyu zemin + üç kart kombinasyonuna indirgenmemelidir. Endüstriyel tesis geometrisi, boru hattı ritmi, enerji akışı ve mühendislik ölçüm dili soyut biçimde tasarıma taşınmalıdır.

## 2. Visual hierarchy

- Hero H1 desktop'ta yaklaşık 56–76 px aralığında, mobilde 38–48 px aralığında olabilir.
- Gövde metni maksimum 60–72 karakter satır uzunluğunda tutulmalı.
- Eyebrow küçük fakat okunaklı, tracking kontrollü olmalı.
- Bir section içinde tek baskın odak bulunmalı.
- Başlık, açıklama ve içerik arasındaki mesafe tutarlı olmalı.

## 3. Spacing system

Tercih edilen ölçek:

```text
4, 8, 12, 16, 24, 32, 48, 64, 80, 112, 144
```

- Section dikey boşluğu desktop'ta genellikle 96–144 px.
- Mobilde 64–88 px.
- Kart içi padding desktop 28–36 px, mobil 20–24 px.
- Rastgele margin değerleri yerine token tabanlı sistem kullan.

## 4. Color roles

```text
canvas:       #07111F
surface:      #0B1828
surface-high: #101D2E
text:         #F4F7FB
muted:        #AAB7C8
blue:         #1F6FEB
green:        #20C997
amber:        #F5A623
border:       rgba(255,255,255,.10)
```

- Yeşil ve amber aynı alanda eşit baskın kullanılmamalı.
- Metin kontrastı WCAG açısından okunabilir olmalı.
- Gradient dekoratif değil, hiyerarşi destekleyici olmalı.

## 5. Typography

- Başlık: Manrope, Sora veya güçlü geometrik sans.
- Gövde: Inter veya benzeri yüksek okunabilirlik.
- Font yükleme güvenilir ve performanslı olmalı.
- Her şeyi kalın yapma; 400/500/600/700 ağırlıklarla hiyerarşi kur.

## 6. Layout language

- 1180–1280 px ana container.
- Hero'da asimetrik iki kolon veya güçlü full-bleed kompozisyon.
- Hizmet kartları aynı olsa bile renk, crop ve içerik ritmiyle farklılaştırılmalı.
- Process bölümü klasik numaralı kart grid'i yerine çizgisel/teknik bir akış kullanabilir.
- AKYA Group bağlantısı ayrı bir marka köprüsü olarak hissedilmeli.

## 7. Motion

- 150–300 ms hover transitions.
- Scroll reveal varsa düşük mesafe ve düşük opacity değişimi.
- `prefers-reduced-motion` dikkate alınmalı.
- Ağır animation library kullanma.

## 8. Responsive rules

### Desktop

- Hero metni ilk viewport'ta güçlü görünmeli.
- Ana CTA ve servis keşfi görünür olmalı.

### Tablet

- 2 kolon kullanılabilir fakat metin sıkışmamalı.
- Menü ve hero breakpoint davranışı ayrıca test edilmeli.

### Mobile

- Tek kolon kompozisyon bilinçli yeniden tasarlanmalı.
- Header açık/kapalı durumları ekranı taşırmamalı.
- CTA hit area en az 44 px olmalı.
- Hero görseli metni boğmamalı.
- Tüm section'larda yatay scroll sıfır olmalı.

## 9. Visual score rubric

Her viewport için 100 puan:

- İlk bakış ve özgünlük: 20
- Marka/premium görünüm: 20
- Typography ve hierarchy: 15
- Spacing ve composition: 15
- Görsel kullanımı: 10
- Renk/kontrast: 10
- Responsive detay: 10

Final ortalama en az 82/100; hiçbir viewport 75 altına düşmemelidir.
