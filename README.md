# App Hook Skills

Kullanıcıların her gün geri döndüğü mobil uygulamalar tasarlamak için Claude skill seti.

Kaynak: **App Breakdown — "How to design an app SO addictive people can't stop using it"**
(https://www.youtube.com/watch?v=NHIq3HnokOI, 15 dk). Video; Duolingo, TikTok, Tinder, Netflix gibi uygulamaların
ortak kullandığı **6 adımlı bir çerçeveyi** anlatıyor.

---

## Videonun özeti

Ana fikir: Uygulama ne kadar güzel görünürse görünsün, kullanıcı ilk gün bırakıyorsa emek boşa gider.
En "bağımlılık yapan" uygulamalar, kullanıcı uygulamayı açmadan önce başlayıp her gün geri dönmesine kadar uzanan
aynı 6 adımı kullanır. İlk 3 adım kullanıcıyı **içeri alır**, son 3 adım onu **tutar**.

### İçeri alma (Getting you in)

| # | Adım | Psikoloji | Özü |
|---|------|-----------|-----|
| 1 | **The Itch (Kaşıntı)** | Nir Eyal, *Hooked* — dış vs. iç tetikleyiciler | Uygulama bir *duyguyla* (sıkılma, merak, "İspanyolcamda geride kaldım") eşleşmeli. TikTok'u açmak için bildirime gerek yok: **can sıkıntısı bildirimin kendisi.** Bildirimler "Seni özledik" değil, duyguya hitap etmeli ("Biri seni beğendi"). |
| 2 | **The Lazy Thumb (Tembel Başparmak)** | BJ Fogg (Stanford) — motivasyon iner çıkar, kolaylığı sen kontrol edersin | Çekirdek aksiyon tek adım olmalı. TikTok/Tinder: tek kaydırma; Duolingo: tek büyük buton. Cal AI (fotoğraf çek, bitti) vs. çok adımlı kalori uygulaması → Cal AI 2 yılda 15M+ indirme. Duolingo, seriyi tam günlük hedef yerine tek ders ile saymaya başlayınca retention %3,3 arttı. |
| 3 | **The Paved Path (Döşenmiş Yol)** | Varsayılan etkisi — 2003 organ bağışı çalışması (opt-in ~%23, opt-out ~%86) | Kullanıcıya seçim yaptırma, seçimi sen yap. TikTok ne izlemek istediğini sormaz, oynatır. Duolingo bir sonraki dersi parlatır. Her karar noktasında bir varsayılan olmalı. |

### Tutma (Keeping you)

| # | Adım | Psikoloji | Özü |
|---|------|-----------|-----|
| 4 | **The Slot Machine (Kumar Makinesi)** | B.F. Skinner'ın güvercinleri — değişken ödül | Her seferinde gelen ödül sıkıcılaşır (10. rozet = umursamazsın). Ödülün **ne zaman** ve **ne büyüklükte** geldiğini öngörülemez yap ama sık ver. TikTok'un sızan iç belgelerine göre "habit moment" ~260 videodan sonra geliyor. |
| 5 | **The Bottomless Pit (Dipsiz Kuyu)** | Durma işaretleri (stopping cues) — Aza Raskin, sonsuz kaydırma | Sayfa sonu, liste sonu, boş arama sonucu = "bırakmalı mıyım?" anı. Her çıkmaz sokağı bir sonraki şeye bağla. Netflix bir sonraki bölümü sen karar vermeden başlatır; Duolingo'da ders bitince en büyük buton "bir sonraki ders". |
| 6 | **The Piggy Bank (Kumbara)** | Yatırım / kişiselleştirme — Netflix önerilerinin yılda ~1 milyar $ tasarruf sağladığı tahmini | Kullanıcı her kullanımda kendinden bir şey bırakır (zevk, liste, arkadaş, ilerleme). Test sorusu: **"Kullanıcı bugün uygulamayı silse bir şey kaybeder mi?"** Hayırsa geri dönmez. Davranışı takip et, ilerleme/seviye/öğrenen algoritma ver. |

---

## Skill'ler

| Skill | Ne zaman kullanılır |
|-------|---------------------|
| [`hook-framework`](skills/hook-framework/SKILL.md) | Yeni bir uygulama, özellik ya da onboarding akışı tasarlarken 6 adımı uygulamak için. Her adım için detaylı referans dosyası içerir. |
| [`retention-audit`](skills/retention-audit/SKILL.md) | Mevcut bir uygulamayı (ekran görüntüleri, kod, akış açıklaması) 6 adıma göre puanlayıp önceliklendirilmiş bir aksiyon listesi çıkarmak için. |
| [`trigger-notification-copy`](skills/trigger-notification-copy/SKILL.md) | "Itch" adımına özel: uygulamanın karşıladığı duyguyu bulup ona hitap eden push bildirimi, widget ve badge metinleri yazmak, zamanlamasını planlamak için. |

## Kurulum

**Claude Code:**
```bash
git clone <bu-repo>
cp -r skills/* ~/.claude/skills/
```

**Claude.ai / Desktop:** Her `skills/<isim>` klasörünü zip'leyip *Settings → Capabilities → Skills* üzerinden yükleyin.

## Etik not

Bu teknikler güçlü. Skill'ler bunları kullanıcının **gerçek bir hedefine** (dil öğrenmek, spor yapmak, sağlıklı beslenmek)
ulaşmasına yardım edecek şekilde uygulamayı önerir ve App Store / Play Store kurallarına, çocuk kullanıcılara ve
zorlayıcı karanlık desenlere (dark patterns) karşı kontrol maddeleri içerir.
