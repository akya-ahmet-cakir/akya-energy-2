# Same-Repository Model Benchmark Protocol

Bu dosya ileride `qwen3-vl:30b` ile alternatif modelleri adil biçimde karşılaştırmak için kullanılır.

## Sabit koşullar

- aynı başlangıç commit'i
- aynı `PROJECT_BRIEF.md`
- aynı agent dosyaları
- aynı context limiti
- aynı maksimum çalışma süresi
- aynı tool izinleri
- aynı internet erişimi
- aynı Playwright testleri
- aynı viewport'lar
- aynı repair turu sayısı
- temiz model session'ı

## Her model için ayrı branch

```text
benchmark/qwen3-vl-30b
benchmark/model-b
benchmark/model-c
```

## Değerlendirme

| Kategori | Ağırlık |
|---|---:|
| Görsel kalite | 50% |
| Brief uyumu | 20% |
| Çalışan linkler ve etkileşimler | 10% |
| Responsive kalite | 10% |
| Kod kalitesi ve test başarısı | 10% |

## Görsel değerlendirme yöntemi

- Screenshot'lar model adı gizlenerek insan değerlendiriciye sunulmalı.
- Desktop, tablet ve mobile ayrı puanlanmalı.
- İlk tur sonucu ile repair sonrası sonuç ayrı tutulmalı.
- Yalnız son ekran görüntüsüne değil, kaç turda ulaşıldığına ve regresyon sayısına da bakılmalı.

## Operasyonel metrikler

- toplam süre
- toplam model turu
- başarısız tool çağrısı
- test tekrar sayısı
- context taşması
- model restart sayısı
- build kırma sayısı
- final unresolved issue sayısı
