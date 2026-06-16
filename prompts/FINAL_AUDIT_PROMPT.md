# Final Audit Prompt

Repository'yi teslim öncesi bağımsız denetçi gibi incele. Yeni özellik ekleme; yalnız eksik veya hatalı olanı düzelt.

## Zorunlu kontroller

- `PROJECT_BRIEF.md` içindeki her kabul kriterini tek tek kontrol et.
- Tüm route'ları production build üzerinde aç.
- Header, dropdown, mobile menu, accordion, CTA ve formu test et.
- Console error, pageerror, failed request ve hydration problemi olmadığını doğrula.
- Tailwind/global CSS'in gerçek render'a uygulandığını doğrula.
- Desktop/tablet/mobile screenshot'ları son kez incele.
- Alt text, labels, keyboard focus ve temel contrast kontrolü yap.
- SEO metadata ve title/description kontrolü yap.
- Placeholder, lorem ipsum, broken image, dead button veya kullanılmayan kritik component bırakma.
- `QUALITY_GATES.md` dosyasını kanıtlarla doldur.

## Final karar

Yalnız şu koşullarda PASS ver:

- tüm functional testler başarılı;
- build/lint/typecheck başarılı;
- hiçbir critical/high visual issue yok;
- ana sayfa visual ortalaması en az 82/100;
- tüm brief kriterleri tamamlanmış;
- rapor ve state dosyaları güncel.

Çıktı:

1. FINAL_STATUS
2. BRIEF_COMPLIANCE_TABLE
3. TEST_EVIDENCE
4. VISUAL_SCORE
5. REMAINING_LOW_RISK_ISSUES
6. DELIVERY_NOTES
