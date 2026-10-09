# Zemberek Web

[zemberek.app](https://zemberek.app) — Zemberek iOS uygulamasının resmi web sitesi. GitHub Pages ile yayınlanır; özel alan adı `CNAME` dosyasındadır, `.nojekyll` Jekyll işlemesini kapatır (sayfalar olduğu gibi servis edilir).

## Sayfalar

| Sayfa | Türkçe | English |
|---|---|---|
| Ana sayfa | [zemberek.app](https://zemberek.app/) | — |
| Gizlilik Politikası | [privacy-policy](https://zemberek.app/privacy-policy.html) | [privacy-policy-en](https://zemberek.app/privacy-policy-en.html) |
| Kullanım Koşulları | [terms-of-service](https://zemberek.app/terms-of-service.html) | [terms-of-service-en](https://zemberek.app/terms-of-service-en.html) |
| Topluluk Kuralları | [community-rules](https://zemberek.app/community-rules.html) | [community-rules-en](https://zemberek.app/community-rules-en.html) |
| KVKK Aydınlatma Metni | [kvkk-aydinlatma](https://zemberek.app/kvkk-aydinlatma.html) | [kvkk-notice-en](https://zemberek.app/kvkk-notice-en.html) |

Destek: destek@zemberek.app

## Yasal sayfaları güncelleme

Gizlilik, koşullar, topluluk kuralları ve KVKK sayfaları **elle düzenlenmez**: uygulama içindeki metinle birebir aynı kalması için tek kaynaktan üretilir.

1. Uygulama deposunda `scripts/legal_content.py` içindeki metni ve `UPDATED` tarihini düzenle.
2. `python3 scripts/generate_legal.py` çalıştır. Betik hem uygulamadaki `ChronoVault/Models/LegalDocuments.swift`'i hem bu sitenin 8 sayfasını yeniden üretir (varsayılan yol `~/Desktop/zemberek-site`; farklıysa yolu ilk argüman olarak ver).
3. Bu depoda değişiklikleri commit'le ve `main`'e pushla; GitHub Pages bir dakika içinde yayınlar.

`index.html` yasal metin içermez, elle düzenlenir.

## Yayın öncesi kontrol

- Yerel önizleme: `python3 -m http.server 8000` ve http://localhost:8000
- Sayfalardaki bağlantıların var olan dosyalara gittiğinden emin ol.
