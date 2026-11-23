---
name: retention-audit
description: Mevcut bir mobil uygulamayı (ekran görüntüleri, kaynak kod, akış açıklaması veya App Store sayfası) 6 adımlı Hook çerçevesine göre puanlar ve önceliklendirilmiş bir iyileştirme raporu çıkarır. Use when asked to audit, review or score an app's retention, engagement, onboarding, day-1 drop-off, or "why don't users come back".
---

# Retention Audit — 6 adımlı Hook denetimi

Bu skill mevcut bir uygulamayı `hook-framework` skill'indeki 6 adıma göre denetler.
Adımların detayları için `../hook-framework/references/` altındaki dosyaları kullan. Bu skill yüklü değilse
aşağıdaki özet kriterler yeterli.

## Girdi türleri ve nasıl incelenir
- **Ekran görüntüleri / ekran kaydı:** Her ekranda birincil CTA'yı, boyutunu ve konumunu, seçenek sayısını ve çıkmaz sokakları not et.
- **Kaynak kod (SwiftUI/UIKit/React Native/Flutter):**
  - Bildirim metinleri: `UNMutableNotificationContent`, `Localizable.strings`/`.xcstrings`, push payload şablonları.
  - Açılış ekranı: `@main` App → ilk `View`/root view controller.
  - Boş durumlar: `isEmpty`, `ContentUnavailableView`, "no results"/"empty" araması.
  - Tamamlama ekranları: "completed", "success", "congrats", `dismiss()` çağrıları.
  - Analitik olayları: `track(`, `logEvent(`, `Analytics.`.
- **Yalnızca açıklama / App Store sayfası:** Kullanıcıdan eksik bilgiyi iste veya varsayımlarını açıkça belirt.

## Puanlama
Her adıma **0–3** puan ver:
- **0:** Hiç yok veya ters çalışıyor (ör. "Seni özledik" bildirimi, 5 adımlı çekirdek aksiyon)
- **1:** Kısmen var, belirgin eksikler
- **2:** İyi, küçük iyileştirmeler mümkün
- **3:** Örnek uygulamalar (Duolingo/TikTok/Tinder) seviyesinde

| Adım | 0 puan belirtisi | 3 puan belirtisi |
|------|------------------|------------------|
| 1. Itch | Genel "geri dön" bildirimleri, duygu tanımsız | Duyguya konuşan, doğru zamanda gelen tetikleyiciler |
| 2. Lazy Thumb | Çekirdek aksiyon 3+ adım, küçük buton, ekranın üstünde | 1 adım, en büyük öğe, başparmak bölgesinde, düşük "bitti" çıtası |
| 3. Paved Path | Açılışta menü veya dashboard, varsayılansız seçimler | Açılışta tek önemli aksiyon, her kararda varsayılan |
| 4. Slot Machine | Tahmin edilebilir rozet merdiveni veya hiç ödül yok | Sık ama öngörülemez zamanlı ve büyüklükte ödüller |
| 5. Bottomless Pit | "Kapat" ile biten tamamlama ekranları, boş "sonuç yok" ekranları | Her son bir sonrakine bağlı |
| 6. Piggy Bank | Silince hiçbir şey kaybedilmiyor | Kişiselleşme, ilerleme veya sosyal bağ birikiyor ve görünür |

Toplam: /18. **0–6** zayıf, **7–12** orta, **13–18** güçlü.

## İş akışı
1. Girdiyi incele, her adım için **kanıt** topla (ekran adı, dosya:satır, metin alıntısı).
2. Her adımı puanla ve kanıtı yaz. Kanıt yoksa "bilinmiyor" de, uydurma.
3. Her adım için en fazla 3 somut öneri yaz (ekran/metin/kod seviyesinde).
4. `../hook-framework/references/ethics-guardrails.md` kontrolünden geçir. Mevcut uygulamada karanlık desen varsa onu da raporla.
5. Önerileri **etki × efor** ile sırala, ilk 5'i "Bu sprint" olarak işaretle.
6. Raporu `templates/audit-report.md` formatında yaz.

## İpuçları
- En hızlı kazanımlar genellikle şunlar: tamamlama ekranına "Sıradaki" butonu (Pit), boş arama önerisi (Pit),
  bildirim metinlerini duyguya çevirmek (Itch), "bitti" çıtasını düşürmek (Lazy Thumb).
- En büyük kaldıraç genelde çekirdek aksiyonu tek adıma indirmektir (Yazio ile Cal AI farkı), ama efor da yüksektir.
- Ölçüm öner: her öneriyle ilişkili metrik (D1/D7 retention, oturum başına aksiyon, bildirim açılma oranı, tamamlanma oranı).
