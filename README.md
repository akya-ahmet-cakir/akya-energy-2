# AKYA Energy — Qwen3-VL Local Agent Pack

Bu paket, AKYA Energy kurumsal sitesini **tek yerel model (`qwen3-vl:30b`)** ile üretmek, Playwright üzerinden test etmek, masaüstü/tablet/mobil ekran görüntülerini modele inceletmek ve görsel onarım turları yürütmek için hazırlanmıştır.

## Hedef mimari

```text
PROJECT_BRIEF.md
        ↓
OpenCode / qwen3-vl:30b
        ↓
Next.js + TypeScript + Tailwind uygulaması
        ↓
Build + lint + typecheck + Playwright
        ↓
Desktop / tablet / mobile screenshot
        ↓
Qwen3-VL visual review
        ↓
Önceliklendirilmiş repair turu
        ↓
Kalite kapıları ve final kabul
```

## Dosyalar

- `AGENTS.md`: OpenCode için ana davranış ve çalışma kuralları.
- `PROJECT_BRIEF.md`: Ürünün içerik, sayfa, tasarım ve kabul şartları.
- `ACTIVE_TASK.md`: Agent'ın o anda yürüttüğü işi takip eder.
- `DECISION_LOG.md`: Mimari ve tasarım kararlarının gerekçeli kaydı.
- `CHANGELOG_AI.md`: Agent'ın yaptığı değişikliklerin özeti.
- `HANDOFF_PROTOCOL.md`: Kesinti, context kaybı ve yeniden başlatma protokolü.
- `docs/ARCHITECTURE.md`: Tek-model agent mimarisi.
- `docs/DESIGN_SYSTEM.md`: Görsel sistem ve UI kalite standardı.
- `docs/PLAYWRIGHT_VISUAL_QA.md`: Test, screenshot ve görsel inceleme döngüsü.
- `docs/QUALITY_GATES.md`: Tamamlanma ve kalite kapıları.
- `docs/OPERATIONS.md`: Sunucu çalıştırma, model ve agent işletimi.
- `prompts/MASTER_IMPLEMENTATION_PROMPT.md`: İlk uygulama turunun ana promptu.
- `prompts/VISUAL_REVIEW_PROMPT.md`: Screenshot inceleme promptu.
- `prompts/REPAIR_PROMPT.md`: Görsel/işlevsel onarım promptu.
- `prompts/FINAL_AUDIT_PROMPT.md`: Teslim öncesi son denetim promptu.
- `templates/VISUAL_REVIEW_REPORT.md`: Görsel inceleme rapor şablonu.
- `templates/TEST_REPORT.md`: Test raporu şablonu.

## Kullanım

1. Paketi proje repository kök dizinine çıkar.
2. `PROJECT_BRIEF.md`, `AGENTS.md` ve diğer kontrol dosyalarını repository içinde tut.
3. OpenCode provider/model ayarında Ollama üzerindeki `qwen3-vl:30b` modelini seç.
4. İlk görev olarak `prompts/MASTER_IMPLEMENTATION_PROMPT.md` içeriğini ver.
5. Her görsel turda `prompts/VISUAL_REVIEW_PROMPT.md`, ardından `prompts/REPAIR_PROMPT.md` kullan.
6. Teslimden önce `prompts/FINAL_AUDIT_PROMPT.md` çalıştır.

## Temel ilke

Build başarısı teslim anlamına gelmez. Agent, gerçek sayfayı Chromium'da açmadan, etkileşimleri çalıştırmadan ve üç viewport screenshot'ını görsel olarak değerlendirmeden işi tamamlanmış sayamaz.
"# akya-energy-2" 
