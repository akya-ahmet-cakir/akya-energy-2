# Visual Review Prompt

Aşağıdaki screenshot'lar AKYA Energy sitesinin gerçek Chromium render çıktılarıdır. Bunları bir kıdemli art director, UI/UX designer ve frontend QA uzmanı gibi incele.

Önce `PROJECT_BRIEF.md` ve `docs/DESIGN_SYSTEM.md` içindeki hedefleri dikkate al. Kod yazma; bu tur yalnız teşhis ve önceliklendirme turudur.

## İncelenecek alanlar

1. İlk bakış etkisi ve özgünlük
2. Premium kurumsal görünüm
3. AKYA Group ile marka akrabalığı
4. Enerji/endüstri karakteri
5. Hero kompozisyonu
6. Typography ve visual hierarchy
7. Spacing ve section ritmi
8. Renk dengesi ve kontrast
9. Görsellerin crop/overlay kalitesi
10. CTA görünürlüğü ve kullanıcı akışı
11. Kart monotonluğu veya template hissi
12. Header/footer kalitesi
13. Desktop/tablet/mobile responsive davranış
14. Taşma, clipping, okunmaz metin veya boş alan
15. Brief'te istenen bölümlerin görsel karşılığı

## Sert kurallar

- Nazik veya genel yorum yapma.
- “Güzel görünüyor” gibi kanıtsız ifadeler kullanma.
- Her sorunu screenshot üzerindeki bölgeyi tarif ederek yaz.
- Semptom ile çözümü ayır.
- Önce critical/high sorunları belirle.
- Kodu görmeden çözüm uydurma; gerektiğinde hangi dosya/component'in incelenmesi gerektiğini yaz.

## Çıktı formatı

### Overall verdict

- Skor: X/100
- Karar: PASS / REPAIR_REQUIRED
- En büyük üç problem:

### Viewport scores

| Viewport | Score | Main issue |
|---|---:|---|

### Findings

Her bulgu:

- ID
- Severity: critical/high/medium/low
- Viewport
- Region
- Problem
- Why it hurts the design
- Concrete repair direction
- Verification after repair

### Repair order

En fazla 8 maddelik, etki sırasına göre uygulanabilir onarım listesi.
