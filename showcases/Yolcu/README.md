<p align="center"><img src="assets/icon.svg" width="96" alt="Yolcu uygulama ikonu"></p>
<h1 align="center">Yolcu</h1>
<p align="center"><strong>Sen yol alırken, küçük bir hayal de ilerlesin.</strong></p>
<p align="center">Mobil web · Dijital karakter dünyası · Kapalı pilot prototipi</p>
<p align="center"><a href="https://yolcu-blond.vercel.app/demo">Örnek yolculuğu dene</a> · <a href="README.en.md">English</a> · <a href="https://github.com/Mahmutakin99/project-portfolio/issues/new/choose">Geri bildirim</a></p>

![Yolcu'nun gerçek public demo giriş ekranı](assets/screenshots/landing.png)

Yolcu, zaten yapacağın şehirler arası yolculuğa küçük bir karakter hikâyesi ekler. Bir rota seç, bir Yolcu'yu emanet al ve onun bir sonraki şehre ulaşmasına yardımcı ol. Şehir damgaları ve küçük katkılar, yolculuğun sonunda bir pasaporta dönüşür.

Bu depo ürünün herkese açık tanıtımıdır; uygulama kaynakları private tutulur. Yolcu şimdilik çalışma adıdır.

## Küçük bir ortak hikâye

| Adım | Deneyim |
| --- | --- |
| Rotanı seç | Başlangıç, varış ve yaklaşık günü belirt. |
| Birini emanet al | Rotana uygun bir karakterle yolculuğa başla. |
| İz bırak | Varışta şehir damgası ve isteğe bağlı küçük katkıyla pasaportu zenginleştir. |
| Devret | Tanıdıklar arasında çift onaylı QR veya dijital istasyon akışını kullan. |
| Hatırayı aç | Tamamlanan hikâyeyi pasaport sayfalarında incele. |

Canlı kişi takibi ve serbest sohbet ürün akışına dahil değildir. Karakterin sahibi taşıyıcının kesin konumunu, kimliğini veya gelecek rotasını görmez. Bakım etkileşimleri isteğe bağlıdır; seri kaybı veya karakter ölümü baskısı yaratılmaz.

## Mobil ekranlar

<table>
<tr><td width="50%" align="center"><strong>Rota planlama</strong></td><td width="50%" align="center"><strong>Örnek pasaport</strong></td></tr>
<tr><td align="center"><img src="assets/screenshots/route.png" width="280" alt="Yolcu mobil rota planlama ekranı, sentetik Afyon-Ankara örneği"></td><td align="center"><img src="assets/screenshots/passport.png" width="280" alt="Uygulamadaki Lumi adlı örnek karakterin sentetik tamamlanmış pasaportu"></td></tr>
</table>

Gerçek tarayıcı yakalamaları; rota ve pasaport sentetik demo verisi kullanır. Masaüstü giriş görseli mevcut public demo sürümünden, mobil görseller yerel geliştirme sürümünden alınmıştır. [Görsel kaydı](PROVENANCE.md).

## Demoyu dene

[Hesapsız örnek yolculuk](https://yolcu-blond.vercel.app/demo) tarayıcıda açılır. Gerçek GPS ve saha devri bu demo içinde simüle edilir. Kapalı pilot 18+ katılımcılar için tasarlanmıştır; demo, gerçek kullanıcılarla pilot doğrulamasının yerine geçmez.

## Geliştirme yaklaşımı

React ve TypeScript ile mobil öncelikli PWA; isteğe bağlı native özellikler için Capacitor. Prototip, yerel sentetik durum ile gerçek kapalı beta entegrasyonlarını ayırır. Supabase tabanlı saha akışlarının kabulü ve gerçek katılımcı çalışmaları ayrı geliştirme adımlarıdır.

## Geri bildirim

[Öneri veya sorun paylaş](https://github.com/Mahmutakin99/project-portfolio/issues/new/choose). Gerçek rota, e-posta, kişi bilgisi veya kesin konum yayınlama; demo adımlarını belirtmen yeterli.

[Mahmut Akın](https://github.com/Mahmutakin99) · [Portföy](https://github.com/Mahmutakin99/project-portfolio) · [Haklar](NOTICE.md)
