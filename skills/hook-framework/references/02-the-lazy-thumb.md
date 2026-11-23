# 2. The Lazy Thumb (Tembel Başparmak) — Çekirdek aksiyonu tek adıma indir

## Problem
Itch kullanıcıya uygulamayı açtırır. Sonrasında olanlar, kullanıcının uygulamayı gerçekten kullanmaya başlayıp başlamayacağını belirler.

## Psikoloji — BJ Fogg (Stanford Behavior Design Lab)
Bir şeyi yapma motivasyonun gün içinde iner çıkar ve onu gerçekten kontrol edemezsin.
Kontrol edebildiğin şey **aksiyonu almanın ne kadar kolay olduğu.**
Kullanıcının çok motive olmasını bekleme. Ona o kadar kolay bir şey ver ki motivasyonu düşükken bile yapabilsin.

## Örnekler
- **Yazio ve Cal AI karşılaştırması (kalori takibi):** Yazio'da ana ekrandan bir iki dokunuşla yemek giremiyorsun.
  Kaydırıyorsun, bir menüye giriyorsun, yazıyorsun. Videodaki görselde Yazio'nun kalabalık bir liste ekranı var,
  Cal AI'ın ise ortada tek bir kamera butonu. Cal AI'da tabağın fotoğrafını çekiyorsun ve iş bitiyor; ürünün tamamı bu.
  İkisi aynı işi yapıyor ama biri çok adımda, diğeri tek fotoğrafla. **Kolay olan 2 yılda 15 milyondan fazla indirme aldı.**
- En bağımlılık yapan uygulamalarda çekirdek aksiyon son derece basit: **TikTok** tek kaydırma, **Tinder** tek kaydırma,
  **Duolingo** ise ekranın altında yeni oturum başlatan dev bir buton.
- **Duolingo:** Önceden seriyi (streak) yalnızca tam günlük hedef tamamlanınca sayıyordu. Tek bir dersi yeterli saymaya başlayınca
  **retention %3,3 arttı.**

## Nasıl uygulanır (videodaki "How to apply" slaydı)
1. **Uygulamanın çekirdek aksiyonunu yaz.**
2. **Adımlarını say ve tek adıma indir.** Acımasız ol.
   Aksiyonu yapan butonu ekranın **en büyük** öğesi yap ve mümkünse **alta, başparmağın olduğu yere** koy,
   çünkü kullanıcıların yaklaşık yarısı telefonu tek elle kullanıyor.
3. **"Bitti" sayılan çıtayı düşür** (Duolingo'nun "tek ders = seri" kararı).

## Kontrol listesi
- [ ] Çekirdek aksiyon tek cümleyle tanımlı
- [ ] Uygulamanın açılışından aksiyonun tamamlanmasına kadar dokunuş sayısı ölçüldü → hedef: 1
- [ ] Birincil CTA ekrandaki en büyük öğe
- [ ] Birincil CTA başparmak bölgesinde (ekranın alt üçte biri)
- [ ] Yazmak yerine fotoğraf, ses, tek dokunuş ya da öneri seçimi gibi girdiler düşünüldü
- [ ] "Bugünlük tamam" eşiği mümkün olan en küçük anlamlı birime indirildi
- [ ] Motivasyonun düşük olduğu senaryo ("yorgunum, 10 saniyem var") için bir yol var

## iOS notları
- `safeAreaInset(edge: .bottom)` ile alta sabitlenmiş büyük birincil buton.
- App Intents ve Kısayollar, Kontrol Merkezi kontrolleri ve etkileşimli widget'lar çekirdek aksiyonu uygulamayı açmadan "sıfır adım"a indirebilir.
- Kamera veya ses girdisi bir yazı formunun yerini alıyorsa daima onu tercih et.
