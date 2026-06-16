# HANDOFF_PROTOCOL

Bu protokol context kaybı, agent restart, model timeout veya süreç kesintisinde uygulanır.

## Yeniden başlama sırası

1. `AGENTS.md` oku.
2. `PROJECT_BRIEF.md` oku.
3. `ACTIVE_TASK.md` oku.
4. `DECISION_LOG.md` oku.
5. `CHANGELOG_AI.md` oku.
6. `git status`, son commit ve diff'i incele.
7. Uygulamayı çalıştır; mevcut health durumunu doğrula.
8. Son test ve screenshot artefact'larını incele.
9. `Next exact action` maddesinden devam et.

## Kesinti öncesi zorunlu kayıt

Uzun görev veya riskli değişiklik öncesinde:

- mevcut fazı yaz;
- değiştirilmekte olan dosyaları yaz;
- tamamlanan testleri yaz;
- bilinen hataları yaz;
- bir sonraki kesin komutu yaz.

## BLOCKED kullanımı

Yalnız aşağıdaki hallerde `BLOCKED` işaretle:

- gerekli sistem aracı kurulamaz;
- repository bozuk veya erişilemez;
- model/tool katmanı screenshot görselini aktaramaz;
- harici kaynak erişimi kalıcı olarak başarısızdır.

Kod veya tasarım zorluğu `BLOCKED` gerekçesi değildir. Alternatif yaklaşım geliştir.
