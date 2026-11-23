# 6. The Piggy Bank (Kumbara) — Geride bırakılan değer

## Bağlam
Netflix, öneri algoritmasının kendilerine yılda yaklaşık **1 milyar dolar** kazandırdığını tahmin ediyor. Nedeni şu:
İzlediğin her dizi Netflix'e ne sevdiğini öğretir. Bir sürü şey izledikten sonra Netflix'i iptal etmek
sıfırdan başlamak gibi gelir; ne izlemeyi sevdiğini tekrar anlatmak istemezsin.

## İlke
Bağımlılık yapan uygulamaların çoğu böyle çalışır. Her kullanımda kendinden biraz bırakırsın:
zevkini, çalma listelerini, bağlantılarını, arkadaşlarını. Kumbara gibi: her kullanımda içine bir bozuk para atarsın
ve ne kadar çok kullanırsan çekip gitmek o kadar zorlaşır.

Uygulama senden biraz emek ister: zamanını, tercihlerini, verini. Böylece daha kişisel hale gelir ve sen ona daha bağlı olursun.
**Örnek:** TikTok'a yeni bir hesapla sıfırdan başladığını düşün. Mevcut feed'in izlediğin her videodan öğrendi;
sıfırdan başlamak kendinden bir parçayı geride bırakmak gibi gelir.

## Teşhis sorusu
> **Biri uygulamanı bugün silse gerçekten bir şey kaybeder mi?**
> Cevap hayırsa kullanıcılar geri dönmez.

## Nasıl uygulanır (videodaki "How to apply" slaydı)
1. **Kullanıcının ne yaptığını takip et.** Yaptığı her arama, tıkladığı her buton, verdiği her bilgi çok değerlidir,
   çünkü uygulamaya gerçekte ne için geldiğini öğretir. Ona bundan daha fazlasını ver. Ama önce takip etmen gerekir.
2. **Üzerine inşa edebileceği bir şey ver:** ilerleme, seviyeler, giderek daha iyi tanıyan bir algoritma.
   Seçenekler neredeyse sınırsız. Önemli olan, kullanıcının her gün üzerine ekleyebileceği ve geri dönmezse
   **kaybedebileceğinin farkında olduğu** bir şey olması.

## Biriktirilebilir değer türleri
- **Kişiselleştirme:** öğrenen öneriler, kişisel plan, tercih profili
- **İlerleme:** seviye, seri (streak), tamamlanan program, istatistik geçmişi
- **İçerik:** kullanıcının oluşturduğu listeler, notlar, fotoğraflar, kayıtlar
- **Sosyal:** arkadaşlar, takipçiler, gruplar, lig sıralaması
- **Kimlik:** profil, rozet koleksiyonu, kişisel rekorlar

## Kontrol listesi
- [ ] Temel davranış olayları (arama, görüntüleme, tamamlama, atlama) analitikte takip ediliyor
- [ ] Bu veri ürüne geri besleniyor (öneriler, kişisel plan)
- [ ] Kullanıcının biriktirdiği değer görünür (ör. "42 gün, 120 antrenman, 3 kişisel rekor")
- [ ] "Silsem ne kaybederim?" sorusunun cevabı uygulama içinde net
- [ ] Veri toplama şeffaf ve izinli (ATT, gizlilik etiketi); veriyi dışa aktarma imkânı var (bkz. `ethics-guardrails.md`)
