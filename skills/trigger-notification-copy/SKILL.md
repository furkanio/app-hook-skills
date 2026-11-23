---
name: trigger-notification-copy
description: Bir uygulamanın karşıladığı duyguyu (iç tetikleyici) belirleyip o duyguya konuşan push bildirimi, widget, rozet ve e-posta metinleri yazar ve ne zaman gönderileceğini planlar. Use when writing push notifications, re-engagement messages, reminder copy, notification strategy or timing for a mobile app, in Turkish or English.
---

# Trigger Notification Copy — "The Itch" için metin ve zamanlama

Hook çerçevesinin 1. adımı (bkz. `hook-framework`). Amaç, uygulamanın zamanla bir **duyguyla eşleşmesi**.
Bildirim bu eşleşmeyi kuran dış tetikleyicidir. İdeal sonuçta kullanıcı bildirimsiz açar, çünkü
"can sıkıntısı bildirimin kendisi" olur.

## Altın kural
> Flört uygulamaları "Biri seni beğendi" der, "Uygulamamızı kullanmaya devam et" demez. O kurumsal dil kimsenin umurunda değil.

Bildirim ya **kullanıcının hissettiği bir duyguya** ya da **onu gerçekten ilgilendiren somut bir olaya** dayanmalı.

## İş akışı

### 1. Duygu haritası çıkar
Kullanıcıdan veya uygulamadan şunları öğren:
- Uygulama hangi duyguya cevap veriyor? (sıkılma, merak, heyecan, stres, yalnızlık, geride kalma, suçluluk, gurur, FOMO)
- Kullanıcı bu duyguyu **ne zaman** ve **nerede** hissediyor? (işe gidiş, öğle arası, yatmadan önce, pazartesi sabahı)
- Uygulamada o duyguya cevap veren **somut olaylar** neler? (yeni içerik, biri etkileşime geçti, seri tehlikede, hedefe yaklaşıldı, kişisel rekor)

Tablo olarak yaz:
| Duygu | Ne zaman | Uygulamadaki cevap | Olay tetikleyici |
|-------|----------|--------------------|------------------|

### 2. Metin yaz
Her duygu ya da olay için **3 varyant** yaz:
- **Olay odaklı:** Somut bir şey oldu. ("Aylin antrenmanını tamamladı, sıra sende 💪")
- **Duygu odaklı:** Hissettiği şeye isim ver. ("Kafan mı dolu? 3 dakikalık nefes egzersizi hazır.")
- **Merak odaklı:** Açınca öğrenebileceği bir şey. ("Bu haftaki ilerlemen seni şaşırtabilir 👀")

Kurallar:
- Başlık ≤ 30, gövde ≤ 90 karakter (kilit ekranında kesilmesin).
- Kullanıcının adını veya verisini kullan (kişisel > genel).
- Tek bir net aksiyon ima et; deep link ile o aksiyona götür (Lazy Thumb).
- Yasak ifadeler: "Seni özledik", "Uzun zamandır görüşmedik", "Uygulamamızı kullanmayı unutma", "Geri dön".
- Sahte aciliyet, sahte sosyal kanıt, utandırma yok (bkz. `hook-framework/references/ethics-guardrails.md`).
- Türkçe metinlerde samimi "sen" dili; marka sesine uygun emoji (en fazla 1).

### 3. Zamanlama planı
| Tetikleyici | Tür | Zamanlama kuralı | Frekans sınırı |
|-------------|-----|------------------|----------------|
| Seri tehlikede | Olay | Kullanıcının olağan açılış saatinden 2 saat sonra hâlâ açılmadıysa | Günde 1 |
| Biri etkileşti | Olay | Anında (sessiz saatler hariç) | Gruplanmış |
| Duygu anı | Duygu | Duygunun ortaya çıktığı saat dilimi (ör. 08:15 işe gidiş) | Haftada 2–3 |

Genel sınırlar: sessiz saatlere (ör. 22:30–08:00) saygı, günde en fazla 1–2 pazarlama bildirimi,
3 bildirim üst üste açılmadıysa frekansı düşür.

### 4. Bildirim dışı tetikleyiciler
- **Widget:** Duyguyla ilgili durumu ana ekranda göster (seri, günün sorusu, bugünkü hedef).
- **Live Activity / Dynamic Island:** Devam eden oturumlar için.
- **Rozet sayısı:** Yalnızca gerçek, okunmamış ve anlamlı olaylar için. Rozeti yapay şekilde şişirme.

## Çıktı formatı
```markdown
## Duygu haritası
<tablo>

## Bildirim kütüphanesi
### <Duygu/olay>
| Varyant | Başlık | Gövde | Deep link |
|---------|--------|-------|-----------|

## Zamanlama planı
<tablo>

## A/B test önerisi
- Hipotez: ... · Metrik: açılma oranı, D7 retention
```

## Örnek (fitness uygulaması)
| Varyant | Başlık | Gövde |
|---------|--------|-------|
| Olay | 🔥 12 günlük serin | Bugün 7 dakikalık hızlı antrenman bile sayılır. |
| Duygu | Uzun bir gün müydü? | 10 dakikalık esneme seni bekliyor, sonra kendini daha iyi hissedeceksin. |
| Merak | Yeni kişisel rekor yakın 👀 | Geçen haftaki şınav sayına sadece 3 kaldı. |
