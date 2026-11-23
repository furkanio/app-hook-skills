# 1. The Itch (Kaşıntı) — Uygulamayı açtıran duygu

## Problem
Ortalama bir kişinin telefonunda 93 uygulama var ama herhangi bir ayda bunların yalnızca yaklaşık yarısını açıyor.
En son TikTok'u açtığında büyük ihtimalle bir bildirim yüzünden değildi. Canın sıkılmıştı, dürtüyü hissettin
ve düşünmeden başparmağın ikonun üstündeydi. Bu dürtüye **itch** deniyor.

## Psikoloji — Nir Eyal, *Hooked*
Uygulama açma nedenleri ikiye ayrılır:
- **Dış tetikleyiciler:** bildirimler, ikon üzerindeki kırmızı rozetler.
- **İç tetikleyiciler:** duygular. Sıkılmak, merak, "İspanyolcamda geride kaldım" hissi.

Uygulamaların çoğu zaman iç tetikleyicilerle açılır.

**Karşı örnek:** Ocak'ta meditasyon uygulaması indirdin, ilk gün 10 dakika meditasyon yaptın, iyi hissettin.
Üçüncü gün uygulamanın varlığını unuttun. Stres hissi gitmedi. Uygulama kendini o duyguyla
**eşleştirmeyi başaramadı.**

> En iyi uygulamalar dış tetikleyicilerle başlar ve zamanla kendilerini bir duyguyla eşleştirir.
> TikTok'u açmak için bildirime ihtiyacın yok, çünkü **can sıkıntısı bildirimin kendisi.**

## Teşhis sorusu
Uygulamandaki metinlere ve gönderdiğin bildirimlere bak:
"Seni özledik" gibi genel şeyler mi, yoksa kullanıcının **duygusuna** mı konuşuyorlar?

## Nasıl uygulanır (videodaki "How to apply" slaydı)
1. **Uygulamanın cevap verdiği duyguyu yaz:** sıkılma, merak, heyecan, stres, yalnızlık, geride kalma kaygısı...
2. **O duyguya konuşan bildirimler yaz.** Flört uygulamaları "Biri seni beğendi" der, "Uygulamamızı kullanmaya devam et" demez. O kurumsal dil kimsenin umurunda değil.
3. **Kullanıcının o duyguyu ne zaman hissettiğini bil** ve tam o anda uygulamanın var olduğunu hatırlat.
   Uygulaman can sıkıntısıyla ilgiliyse ve kullanıcının işe gidiş yolunda canı sıkılıyorsa, hatırlatmayı yolculuk sırasında gönder.

## Kontrol listesi
- [ ] Tek cümlelik "duygu → uygulama" eşleşmesi yazılı mı? ("Canım sıkıldığında → X'i açarım")
- [ ] Bildirimlerin hiçbiri "Seni özledik / Geri dön" türünde genel bir metin değil
- [ ] Her bildirim ya bir duyguya ya da kullanıcıyı ilgilendiren somut bir olaya ("biri seni beğendi", "serin 3 günde") dayanıyor
- [ ] Bildirim zamanlaması duygunun ortaya çıktığı ana göre ayarlanmış (sabit "her gün 10:00" değil)
- [ ] Kullanıcının kendi davranış saatleri öğreniliyor (ör. en çok açtığı saat dilimi)

## iOS notları
- Zamanlamayı kullanıcının geçmiş açılış saatlerine göre yerel `UNCalendarNotificationTrigger` ile kişiselleştir.
- Widget'lar (WidgetKit) ve Live Activities "dış tetikleyiciyi" bildirimsiz sağlar; ana ekranda sürekli görünür olmak duyguyla eşleşmeyi hızlandırır.
- Detaylı metin üretimi için `trigger-notification-copy` skill'ini kullan.
