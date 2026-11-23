# 3. The Paved Path (Döşenmiş Yol) — Seçimi kullanıcı yerine sen yap

## Problem
Bazen tek dokunuş bile fazladır, çünkü neye dokunacağına karar vermek zordur.
İnsanların kendileri seçmek istediğini düşünürsün ama çoğu zaman onlar için önceden seçilmiş olanla devam ederler.

## Psikoloji — Varsayılan etkisi (default effect)
En ünlü örnek Avrupa'da organ bağışı üzerine yapılan 2003 çalışması:
- Bağışçı olmayı **seçmen gereken** ülkelerde (opt-in) bağış oranı ~**%23**.
- Bağışçı olmamayı **seçmen gereken** ülkelerde (opt-out) oran ~**%86**.

Karar aynı ama fark devasa, çünkü bir ülkede bir yol, diğerinde öteki yol "döşenmiş". Döşenmiş yoldan çıkmak efor ister
ve insanlar bu eforu harcamaz. İnsanlar organ bağışı kadar önemli bir konuda bile varsayılanla gidiyorsa,
bir uygulamada hangi butona basacaklarına hiç efor harcamazlar.

## Örnekler
- **TikTok** ne izlemek istediğini asla sormaz; video zaten oynuyordur.
- **Duolingo** sayısız seçenek sunmaz; sıradaki dersi gösterir ve onu parlatır.
- **Tinder** sırada kimi görmek istediğini sormaz; birini gösterir.

Döşenmiş yol: Kullanıcı için bir sonraki seçeneği belirlemek ve onu düşündürmemek.

## Nasıl uygulanır
1. **Lazy Thumb'da yazdığın aksiyonu, uygulama açılınca görülen ilk şey yap.**
   Kullanıcı uygulamayı açınca bir menü ya da bir sürü seçenek değil, önemli olan tek seçeneği görmeli.
2. **Uygulamayı gez ve kullanıcıya karar verdirdiğin her yeri listele.**
3. **Her karar için bir varsayılan koy.** Varsayılan hem senin hem kullanıcının yararına olanı seçmeli.
   Kullanıcıların çoğu zaman varsayılanı seçtiğini göreceksin.

## Kontrol listesi
- [ ] Açılış ekranı (cold start ve geri dönüş) tek bir birincil aksiyon gösteriyor
- [ ] Uygulamadaki tüm karar noktaları listelendi (onboarding soruları, ayarlar, içerik seçimi, plan seçimi...)
- [ ] Her karar noktasının bir varsayılanı var
- [ ] Varsayılanlar **kullanıcının hedefi** açısından da savunulabilir (bkz. `ethics-guardrails.md`)
- [ ] "Ne yapmak istersin?" türü boş/açık uçlu ekranlar kaldırıldı veya önerilerle dolduruldu
- [ ] Onboarding'deki seçimler mümkünse akıllı varsayılanlarla önceden dolduruldu

## İlk 3 adımın özeti
Bu üç adım bağımlılık yapan uygulamaların **seni içeri alma** yöntemi:
uygulamayı açtıran bir *itch*, bir şey yaptıran çok kolay bir ilk aksiyon ve senin için önceden belirlenmiş bir yol.
Ama içeri almak savaşın yarısı. Sonraki üç adım kullanıcıyı **tutar**.
