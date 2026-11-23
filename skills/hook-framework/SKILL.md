---
name: hook-framework
description: Mobil uygulama, özellik veya onboarding tasarlarken kullanıcıların her gün geri dönmesini sağlayan 6 adımlı alışkanlık çerçevesini (Itch, Lazy Thumb, Paved Path, Slot Machine, Bottomless Pit, Piggy Bank) uygular. Use when designing app retention, habit loops, engagement, daily active use, streaks, core action, onboarding or "why do users leave on day one".
---

# Hook Framework — 6 adımda alışkanlık yaratan uygulama tasarımı

Kaynak: App Breakdown, "How to design an app SO addictive people can't stop using it"
(https://www.youtube.com/watch?v=NHIq3HnokOI).

Temel tez: Uygulama ne kadar iyi görünürse görünsün, kullanıcı ilk gün bırakıyorsa emek boşa gider.
Duolingo, TikTok ve Tinder aynı 6 adımı kullanır. Bu adımlar kullanıcı uygulamayı açmadan önce başlar
ve her gün geri dönmesine kadar uzanır.

```
İÇERİ ALMA (Getting you in)              TUTMA (Keeping you)
1. The Itch        → açtırır             4. The Slot Machine    → değişken ödül
2. The Lazy Thumb  → ilk aksiyon kolay   5. The Bottomless Pit  → çıkış yok, hep "sıradaki"
3. The Paved Path  → yol önceden seçili  6. The Piggy Bank      → bıraktıkça kaybedecek bir şey birikir
```

## Ne zaman hangi referansı oku

| Konu | Dosya |
|------|-------|
| Kullanıcı uygulamayı açmıyor / bildirimler işe yaramıyor | `references/01-the-itch.md` |
| Açıyor ama çekirdek aksiyonu yapmıyor | `references/02-the-lazy-thumb.md` |
| Çok seçenek, menü, kararsızlık | `references/03-the-paved-path.md` |
| Ödüller / rozetler / gamification sıkıcı | `references/04-the-slot-machine.md` |
| Oturumlar kısa, kullanıcı bir yerde takılıp çıkıyor | `references/05-the-bottomless-pit.md` |
| Gün 7 / gün 30 retention düşük, silip gidiyorlar | `references/06-the-piggy-bank.md` |
| Sorumlu kullanım, mağaza kuralları, karanlık desenler | `references/ethics-guardrails.md` |

Yalnızca ilgili referansları oku. Genel bir tasarım isteğinde altısını da sırayla uygula.

## İş akışı

1. **Bağlamı topla:** Uygulama ne yapıyor, kullanıcı kim, çekirdek aksiyon ne, şu anki metrikler (D1/D7/D30, oturum süresi) varsa ne?
2. **Adım adım ilerle:** Her adım için referanstaki "Nasıl uygulanır" maddelerini bu uygulamaya özel somut önerilere çevir. Genel tavsiye verme; ekran, buton, metin, bildirim düzeyinde konuş.
3. **Etik kontrolü:** Her öneriyi `references/ethics-guardrails.md` ile kontrol et. Kullanıcının kendi hedefine hizmet etmeyen öneriyi işaretle veya değiştir.
4. **Çıktı:** Aşağıdaki formatı kullan.

## Çıktı formatı

```markdown
# <Uygulama> — Hook Framework Planı

**Çekirdek duygu (Itch):** ...
**Çekirdek aksiyon (Lazy Thumb):** ... (şu an X adım → hedef 1 adım)

## 1. The Itch
- Mevcut durum: ...
- Öneriler: ... (somut bildirim metinleri, zamanlama)
## 2. The Lazy Thumb
...
## 6. The Piggy Bank
...

## Öncelik sırası
| # | Değişiklik | Adım | Etki | Efor |
|---|-----------|------|------|------|

## Ölçülecek metrikler
- ...
```

## Hızlı hatırlatma kartı

- **Itch:** Uygulamanın cevap verdiği duyguyu yaz → o duyguya konuşan bildirimler yaz → duygunun ortaya çıktığı anda hatırlat.
- **Lazy Thumb:** Çekirdek aksiyonu yaz → tek adıma indir (acımasız ol) → "bitti" çıtasını düşür. Buton ekranın en büyük öğesi olsun ve başparmağın eriştiği altta dursun.
- **Paved Path:** Uygulama açılınca menü değil tek önemli seçenek görünsün → her karar noktasını listele → her birine varsayılan koy.
- **Slot Machine:** Gerçek ödülü belirle → ne zaman ve ne büyüklükte geleceğini öngörülemez yap → ama sık ver.
- **Bottomless Pit:** Tüm çıkmaz sokakları listele (liste sonu, boş arama, hata ekranı) → her birini bir sonraki şeye bağla → "bitti" deme.
- **Piggy Bank:** Kullanıcının yaptığı her şeyi takip et → üzerine inşa edebileceği bir şey ver (ilerleme, seviye, öğrenen algoritma) → silerse kaybedeceğini bilsin.
