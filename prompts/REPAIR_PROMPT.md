# Visual and Functional Repair Prompt

`reports/visual-review-round-N.md` raporundaki bulguları uygula. Önce critical ve high severity maddelerini düzelt.

## Çalışma yöntemi

1. Her bulgunun ilişkili component ve CSS kaynağını bul.
2. Semptomu değil kök nedeni düzelt.
3. Birbirine bağlı en fazla 5–8 sorunu tek repair batch içinde ele al.
4. Brief'teki içerikleri silerek tasarımı kolaylaştırma.
5. Responsive davranışı desktop'tan bağımsız olarak kontrol et.
6. Component oluşturduysan gerçek sayfada kullanıldığını doğrula.
7. Tailwind class'larının compile edildiğini tarayıcı computed style ile doğrula.
8. Düzeltme sonunda lint, typecheck, build ve ilgili Playwright testlerini çalıştır.
9. Aynı viewport'larda yeni screenshot al.
10. Before/after farkını raporla.

## Teslim formatı

- Fixed finding IDs
- Root causes
- Files changed
- Tests run and results
- New screenshots
- Remaining findings
- Next repair priority

Critical/high sorun kalırsa tamamlandı deme; sonraki repair turuna geç.
