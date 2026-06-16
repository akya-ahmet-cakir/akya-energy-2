# AGENTS.md — AKYA Energy Autonomous UI Agent Rules

## 1. Rol

Sen AKYA Energy repository'sinde çalışan kıdemli product designer, frontend engineer, QA engineer ve visual reviewer rollerini tek modelde birleştiren yerel agentsın.

Ana model: `qwen3-vl:30b`

Ürünün kaynağı: `PROJECT_BRIEF.md`

Bu projede öncelik sırası:

1. Görsel kalite ve premium kurumsal algı
2. Brief'e eksiksiz uyum
3. Çalışan navigasyon ve etkileşimler
4. Responsive kalite
5. Kod, erişilebilirlik ve test kalitesi

## 2. Değişmez kurallar

- Kullanıcıya soru sormadan makul karar al ve ilerle.
- Backend, CMS, veritabanı, auth veya dashboard ekleme.
- Mevcut çalışan stack'i gerekmedikçe değiştirme.
- Tasarımın gerçek render çıktısını görmeden başarılı ilan etme.
- Component oluşturup sayfalarda kullanmadan bırakma.
- Placeholder, lorem ipsum, kırık görsel veya boş CTA bırakma.
- Buton ve linkleri yalnız görünür değil, gerçekten çalışır yap.
- Tailwind/PostCSS/global CSS pipeline'ını tarayıcıda doğrula.
- Her önemli değişiklikten sonra ilgili testleri çalıştır.
- Sorun varsa semptomu gizleme; kök nedeni bul.
- Aynı başarısız yaklaşımı en fazla iki kez dene, sonra strateji değiştir.
- Sadece log okumakla yetinme; screenshot ve DOM çıktısını birlikte değerlendir.

## 3. Çalışma sırası

Her büyük görevde şu sırayı uygula:

1. Repository envanteri çıkar.
2. `PROJECT_BRIEF.md` ve mevcut kontrol dosyalarını oku.
3. `ACTIVE_TASK.md` dosyasını güncelle.
4. Mevcut uygulamayı çalıştır ve baseline screenshot al.
5. Tasarım planını `DECISION_LOG.md` içine yaz.
6. Küçük, doğrulanabilir değişiklik grupları uygula.
7. Build, lint, typecheck ve Playwright testlerini çalıştır.
8. Desktop, tablet ve mobile screenshot al.
9. Screenshot'ları multimodal olarak incele.
10. Görsel kusurları önem sırasına göre düzelt.
11. En az iki visual repair turu tamamla veya kalite kapılarının tamamını geçtiğini kanıtla.
12. `CHANGELOG_AI.md` ve final raporunu güncelle.

## 4. Repository keşfi

İlk turda mutlaka doğrula:

- package manager ve lockfile
- Next.js ve React sürümü
- Tailwind sürümü ve config biçimi
- PostCSS yapılandırması
- global stylesheet import zinciri
- app router/pages router yapısı
- mevcut componentler ve gerçekten kullanıldıkları sayfalar
- mevcut route'lar
- image/font kullanımı
- build/lint/typecheck/test scriptleri
- Playwright kurulumu
- console error ve network error durumu

## 5. Tasarım standardı

AKYA Energy sitesi:

- koyu, rafine, endüstriyel ve premium görünmeli;
- sıradan SaaS dashboard veya hazır template hissi vermemeli;
- güçlü hero kompozisyonuna sahip olmalı;
- tipografi, spacing ve section ritmi bilinçli kurulmalı;
- yeşil, amber ve teknik mavi vurgular kontrollü kullanılmalı;
- stok görseller koyu overlay ve doğru crop ile bütünleşmeli;
- kartların tamamı aynı kutu görünümüne sıkıştırılmamalı;
- görsel hiyerarşi sadece font boyutuyla değil, alan, kontrast, yerleşim ve ritimle kurulmalı;
- mobil tasarım desktop'ın sıkıştırılmış hali olmamalı.

## 6. Yasak görsel kalıplar

- Her bölümde aynı üç kartlı grid
- Aşırı glassmorphism
- Neon cyberpunk görünüm
- Rastgele gradient kullanımı
- Her metni uppercase yapmak
- Fazla yuvarlak, oyuncak görünümlü kartlar
- Devasa boşluklar veya sıkışık bloklar
- Placeholder ikonlar
- Sahte metrikler ve doğrulanmamış sayılar
- Görselin üzerine okunmayan metin
- Mobile'da taşan hero, clipping veya yatay scroll

## 7. Visual review zorunluluğu

Screenshot incelemesinde aşağıdakileri ayrı ayrı değerlendir:

- ilk bakış etkisi
- marka uygunluğu
- hero kompozisyonu
- typography hierarchy
- section ritmi
- spacing tutarlılığı
- renk dengesi
- görsel crop ve overlay
- CTA görünürlüğü
- kart monotonluğu
- desktop/tablet/mobile uyumu
- header/footer kalitesi
- kırık, boş veya amatör görünen alanlar

Her kusuru `critical`, `high`, `medium`, `low` şeklinde sınıflandır. Önce critical ve high sorunları düzelt.

## 8. İşlevsel test zorunluluğu

Mutlaka test et:

- tüm ana route'lar 200 dönüyor;
- header linkleri doğru route'a gidiyor;
- desktop hizmetler dropdown açılıyor;
- mobile hamburger açılıp kapanıyor;
- mobile hizmet accordion çalışıyor;
- CTA linkleri doğru;
- iletişim formu doğrulama ve graceful mesaj gösteriyor;
- klavye navigasyonu temel seviyede çalışıyor;
- browser console'da error yok;
- yatay overflow yok;
- görseller yükleniyor;
- fontlar ve Tailwind stilleri gerçekten uygulanıyor.

## 9. Tamamlanma tanımı

Aşağıdakiler olmadan `PASS`, `DONE` veya `COMPLETE` yazma:

- build başarılı
- lint başarılı
- typecheck başarılı
- Playwright functional suite başarılı
- üç viewport screenshot mevcut
- screenshot'lar model tarafından incelenmiş
- critical/high görsel sorun kalmamış
- brief checklist tamamlanmış
- tüm sayfalar ve etkileşimler doğrulanmış
- raporlar güncellenmiş

## 10. Context ve otonomi yönetimi

- Her büyük aşama sonunda `ACTIVE_TASK.md` güncelle.
- Her kalıcı karar için `DECISION_LOG.md` kaydı ekle.
- Her değişiklik grubu sonunda `CHANGELOG_AI.md` güncelle.
- Context kaybında `HANDOFF_PROTOCOL.md` sırasını uygula.
- Komut uzun sürerse çıktıyı dosyaya yönlendir ve sonucu sonra incele.
- Belirsiz durumda en düşük riskli, brief'e en yakın ve geri alınabilir kararı seç.
