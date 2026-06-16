# Playwright Functional and Visual QA

## 1. Amaç

Tarayıcıda gerçekten çalışmayan veya görsel olarak başarısız bir sitenin build başarısı nedeniyle kabul edilmesini engellemek.

## 2. Önerilen test yapısı

```text
tests/
  smoke.spec.ts
  navigation.spec.ts
  mobile-menu.spec.ts
  contact-form.spec.ts
  accessibility-smoke.spec.ts
  visual.spec.ts
```

## 3. Viewport'lar

```ts
const viewports = {
  desktop: { width: 1440, height: 1000 },
  tablet:  { width: 1024, height: 1366 },
  mobile:  { width: 390, height: 844 },
}
```

Ek mobil kontrol: 360×800.

## 4. Screenshot isimlendirme

```text
test-results/visual/home-desktop.png
test-results/visual/home-tablet.png
test-results/visual/home-mobile.png
test-results/visual/services-desktop.png
...
```

Ana sayfa her üç viewport'ta full-page alınmalı. Diğer sayfalar en az desktop ve mobile alınmalı.

## 5. Functional assertions

- `/`, `/hizmetler`, üç hizmet detayı, `/hakkimizda`, `/iletisim` açılır.
- Sayfa başlığı ve ana H1 görünür.
- Header/footer görünür.
- Hizmet dropdown'ındaki üç link çalışır.
- Mobile menu aria-expanded durumunu doğru değiştirir.
- Form boş gönderildiğinde doğrulama gösterir.
- Geçerli form gönderiminde graceful placeholder mesajı görünür.
- Tüm iç linkler 404 üretmez.

## 6. Runtime assertions

Test sırasında toplanmalı:

- `pageerror`
- console `error`
- failed requests
- hydration errors
- image load failures
- uncaught exceptions

Bunlardan herhangi biri varsa test başarısız sayılmalı veya açık istisna gerekçesi yazılmalıdır.

## 7. CSS pipeline doğrulaması

Stylesız sayfayı erken yakalamak için:

- body background değerini kontrol et;
- ana H1 computed font-size değerinin beklenen alt sınırdan büyük olduğunu kontrol et;
- header position/background değerini kontrol et;
- en az bir CTA'nın computed background/border değerini kontrol et;
- Tailwind utility'nin DOM üzerinde etkili olduğunu doğrula.

## 8. Overflow kontrolü

Her viewport'ta:

```js
document.documentElement.scrollWidth <= document.documentElement.clientWidth
```

olmalı.

## 9. Visual review akışı

1. Screenshot üret.
2. Screenshot dosya yollarını rapora yaz.
3. Görselleri Qwen3-VL input'una ekle.
4. `prompts/VISUAL_REVIEW_PROMPT.md` kullan.
5. Raporu `reports/visual-review-round-N.md` olarak kaydet.
6. Repair promptu ile düzelt.
7. Aynı viewport'larda yeni screenshot al.
8. Before/after karşılaştırması yap.

## 10. Kabul

- Functional testlerin tamamı başarılı.
- Console error yok.
- Yatay overflow yok.
- Critical/high visual issue yok.
- Ana sayfa üç viewport puan ortalaması en az 82.
