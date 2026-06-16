# Operations Guide — Ollama, OpenCode and Playwright

## 1. Model doğrulama

```bash
ollama list
ollama show qwen3-vl:30b
```

Model adı yerel Ollama kurulumunda farklı görünüyorsa `ollama list` çıktısındaki tam tag kullanılmalıdır.

## 2. Modelin ayakta olduğunu doğrulama

```bash
curl -s http://127.0.0.1:11434/api/tags | jq .
```

## 3. Context yaklaşımı

Tesla P40 24 GB üzerinde güvenli çalışma için:

- Gereksiz dev context açma.
- Repository'nin tamamını tek seferde prompt'a yükleme.
- Dosyaları tool ile ihtiyaç oldukça oku.
- Uzun logları özet dosyasına yönlendir.
- Screenshot review sırasında yalnız gerekli görselleri ve ilgili brief bölümünü gönder.
- Agent state'ini Markdown dosyalarında tut.

Başlangıç için 16K–24K efektif context mantıklıdır; runtime VRAM davranışı gözlenerek artırılmalıdır. Aynı turda çok sayıda yüksek çözünürlüklü screenshot vermek yerine 1–3 görsellik gruplar kullan.

## 4. Playwright kurulumu

Repository paket yöneticisine göre:

```bash
npm install -D @playwright/test
npx playwright install chromium
```

Ubuntu Server bağımlılıkları eksikse:

```bash
npx playwright install --with-deps chromium
```

## 5. Headless çalışma

GUI gerekli değildir. Chromium headless modda çalışır. Screenshot, trace ve video dosyaları disk üzerinde üretilir ve multimodal modele dosya olarak verilir.

## 6. Önerilen package scripts

```json
{
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "lint": "next lint",
    "typecheck": "tsc --noEmit",
    "test:e2e": "playwright test",
    "test:visual": "playwright test tests/visual.spec.ts",
    "qa": "npm run lint && npm run typecheck && npm run build && npm run test:e2e"
  }
}
```

Mevcut Next.js sürümünde `next lint` desteklenmiyorsa doğrudan ESLint script'i kullanılmalıdır.

## 7. Süreç yönetimi

Test için development server yerine mümkünse production build kullan:

```bash
npm run build
npm run start -- -p 3000
```

Playwright `webServer` özelliği ile server otomatik başlatılabilir.

## 8. Agent tur sınırı

Bir visual repair turunda:

- En fazla 5–8 ilişkili high-impact sorun düzelt.
- Sonra yeniden test ve screenshot al.
- Çok büyük tek patch yerine ölçülebilir turlar yap.

En az iki repair turu önerilir. İlk tur kompozisyon/hiyerarşi, ikinci tur responsive/polish odaklı olmalıdır.

## 9. Log ve artefact klasörleri

```text
reports/
test-results/
playwright-report/
```

Bunlar kalıcı QA kanıtlarıdır. Büyük trace/video dosyalarının git'e eklenip eklenmeyeceği `.gitignore` politikasına göre belirlenmelidir.
