# DECISION_LOG

Her kalıcı mimari veya tasarım kararı aşağıdaki şablonla kaydedilmelidir.

## Decision template

### D-000 — Başlık

- Tarih:
- Durum: Proposed / Accepted / Replaced
- Bağlam:
- Karar:
- Gerekçe:
- Alternatifler:
- Etkilenen dosyalar:
- Doğrulama:

---

## Başlangıç kararları

### D-001 — Tek model mimarisi

- Durum: Accepted
- Karar: Kodlama, test analizi ve screenshot incelemesi aynı yerel `qwen3-vl:30b` modeliyle yürütülecek.
- Gerekçe: Proje sınırlı kapsamlı statik bir kurumsal sitedir; model değiştirme ve orchestration maliyeti gereksizdir. Vision yeteneği, tasarımın gerçek render çıktısını değerlendirmek için kullanılacaktır.

### D-002 — Build başarısı teslim ölçütü değildir

- Durum: Accepted
- Karar: Teslim için functional test ve üç viewport visual review zorunludur.
- Gerekçe: Önceki agent denemesinde build geçmesine rağmen stylesız ve işlevsiz UI üretilmiştir.

### D-003 — Görsel kalite ağırlığı

- Durum: Accepted
- Karar: Nihai puanlamada görsel kalite %50 ağırlıktadır.
- Gerekçe: Ürünün ana başarısı ağır iş mantığı değil, premium kurumsal web deneyimidir.
