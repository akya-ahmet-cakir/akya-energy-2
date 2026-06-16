# Autonomous Local UI Agent Architecture

## 1. Amaç

Tek bir yerel multimodal modelin repository üzerinde kod yazması, Playwright ile gerçek tarayıcı testi yapması, screenshot'ları incelemesi ve görsel onarım turu yürütmesi.

## 2. Bileşenler

```text
OpenCode
├── Ollama provider
│   └── qwen3-vl:30b
├── Repository tools
│   ├── read / write / patch
│   ├── shell
│   └── git
├── Web research tools
│   ├── search
│   └── fetch
└── Browser QA
    ├── Playwright
    ├── Chromium headless
    ├── screenshots
    ├── traces
    └── console/network capture
```

## 3. Tek-model neden yeterli

Bu proje karmaşık backend veya algoritma gerektirmez. Aynı model şu rolleri sırayla üstlenebilir:

- brief analyst
- visual designer
- frontend implementer
- browser test debugger
- screenshot reviewer
- repair agent

Ayrı modeller yerine rol geçişleri prompt ve artefact'larla yönetilir. Böylece VRAM'de model değişimi, unload/reload ve farklı modeller arasında context aktarımı ortadan kalkar.

## 4. Agent state

Kalıcı state konuşma context'ine bırakılmaz. Şu dosyalarda tutulur:

- `ACTIVE_TASK.md`: operasyonel durum
- `DECISION_LOG.md`: karar hafızası
- `CHANGELOG_AI.md`: değişiklik özeti
- `playwright-report/`: test kanıtları
- `test-results/`: screenshot, trace ve hata artefact'ları
- `reports/`: visual review ve final audit raporları

## 5. Döngü

### Phase A — Discovery

- source tree
- package scripts
- styling pipeline
- route map
- baseline render
- console/network errors

### Phase B — Design plan

- brand concept
- page composition
- design tokens
- typography scale
- reusable components
- responsive rules

### Phase C — Implementation

- foundation
- global navigation
- homepage
- service pages
- about/contact
- SEO/accessibility

### Phase D — Functional QA

- build/lint/typecheck
- route checks
- interactions
- form
- console
- overflow

### Phase E — Visual QA

- desktop 1440×1000
- tablet 1024×1366
- mobile 390×844
- full-page screenshot
- above-the-fold screenshot when needed

### Phase F — Repair

- critical/high issues first
- one coherent repair batch
- rerun tests
- rescreenshot
- compare before/after

### Phase G — Final audit

- brief checklist
- visual score
- test evidence
- remaining known limitations

## 6. Güvenlik ve sınırlar

- Shell komutları repository ve gerekli build araçlarıyla sınırlıdır.
- Sistem dosyalarını veya başka projeleri değiştirme.
- Secrets üretme veya commit etme.
- Lisanssız/filigranlı görsel indirme.
- `curl | sh` gibi doğrulanmamış kurulum yollarından kaçın.
- Destructive git komutlarını kullanma.
