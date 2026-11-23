# 5. The Bottomless Pit (Dipsiz Kuyu) — Durma işaretlerini kaldır

## Bağlam
Değişken ödüller ancak her zaman bir sonrakinin geleceği varsa işe yarar. Sonsuz kaydırmayı icat eden tasarımcı
**Aza Raskin**, kendi tahminine göre her gün kaydırmaya harcanan zamanın toplamda yaklaşık 100.000 insan ömrüne eşit olduğunu söylüyor.
Sayfanın sonunu kaldırmanın gücü bu.

## Psikoloji — Durma işaretleri (stopping cues)
Hayattaki çoğu şeyin bir durma işareti vardır: günün sonu, bir videonun bitişi, sayfanın dibi.
Bunlar beynin "Devam mı edeyim, durma zamanı mı?" diye sorduğu anlardır.
Bu işaretlerin hepsini kaldırırsan ayrılma kararını kullanıcının kendisi vermek zorunda kalır.
Paved Path'te gördüğümüz gibi insanlar genellikle kendi kararlarını vermez, işaretler kalkınca da kalırlar.

## Ortalama uygulamanın hatası
Çoğu uygulama farkında olmadan kullanıcıyı durduracak şekilde tasarlanmıştır.
Her boş arama ekranı, her çıkmaz sokak, kullanıcıyı başka bir yere götürmediğin her yer,
beynin "artık bıraksam mı?" demesi için bir fırsattır.

## Örnekler
- **Duolingo:** Ders bitince ekrandaki en büyük buton bir sonrakini başlatır.
- **TikTok:** Feed'in sonu yok.
- **Tinder:** Kart destesinin sonu yok.
- **Netflix:** Sen izleyip izlemeyeceğine karar vermeden sıradaki bölüm başlar.

Dipsiz kuyu: Kullanıcıya her zaman sıradakini (sıradaki aksiyon, sıradaki bölüm) vermek ve ona asla bir çıkış yolu göstermemek.

## Nasıl uygulanır
1. **Tüm çıkmaz sokakları listele:** liste sonları, boş arama sonuçları, hata durumundaki ekranlar...
   Kullanıcıyı başka bir yere götürmeyen her şeyi yaz.
2. **Her birini bir yere bağla:**
   - Boş arama sonucu → aradığı şey olabilecek bir şey göster.
   - Liste sonu → ilgisini çekebilecek başka bir şey göster.
   - Bölüm/ders sonu → sıradakini göster, ama "bitti" deme.

## Çıkmaz sokak envanteri şablonu
| Ekran / durum | Şu an ne gösteriyor | Bağlanacağı yer | Öncelik |
|---------------|--------------------|-----------------|---------|
| Boş arama | "Sonuç bulunamadı" | Popüler/benzer öğeler | Yüksek |
| Liste sonu | Hiçbir şey | "Bunları da beğenebilirsin" | Orta |
| Tamamlama ekranı | "Tebrikler!" + Kapat | Büyük "Sıradaki" butonu | Yüksek |
| Hata ekranı | Hata mesajı | Yeniden dene + çevrimdışı içerik | Orta |
| Boş durum (ilk kullanım) | Boş ekran | Başlangıç önerisi / örnek içerik | Yüksek |

## Kontrol listesi
- [ ] Tüm çıkmaz sokaklar envanteri çıkarıldı
- [ ] Hiçbir tamamlama ekranının birincil butonu "Kapat" değil
- [ ] Boş durumlar ve boş aramalar öneri gösteriyor
- [ ] Hata ekranları kullanıcıyı bir sonraki faydalı şeye yönlendiriyor
- [ ] Hedefe ulaşma anında sağlıklı bir "bugünlük bu kadar" seçeneği bilinçli olarak tasarlandı mı? (bkz. `ethics-guardrails.md`)
