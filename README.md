# YÖKDİL Akademi — Vercel + Gemini

## Neler var?
- Responsive koyu tema arayüz
- Sosyal bilimler, sağlık bilimleri, fen bilimleri ve genel akademik İngilizce
- Türkçe konu anlatımı, kelime kartları, çeviri, paragraf ve YÖKDİL tarzı özgün testler
- Yanıt kontrolü ve Türkçe açıklama
- Tarayıcıda çalışma geçmişi ve istatistik
- Gemini anahtarı sunucu tarafında `/api/study.js` içinde kullanılır; HTML'e gömülmez

## Vercel'e yükleme
1. ZIP'i açın.
2. Dosyaları GitHub'da yeni bir depoya yükleyin.
3. Vercel'de **Add New → Project** seçin ve depoyu içe aktarın.
4. Vercel projesinde **Settings → Environment Variables** bölümüne:
   - `GEMINI_API_KEY` = Google AI Studio'dan aldığınız Gemini API anahtarı
   - İsteğe bağlı `GEMINI_MODEL` = `gemini-2.5-flash`
5. Environment variable ekledikten sonra **Redeploy** yapın.
6. Yayınlanan Vercel adresini açın.

## Yerelde deneme
Node.js kuruluysa:
```bash
npm install -g vercel
vercel dev
```
Sonra terminalin verdiği yerel adresi açın. `index.html` dosyasını çift tıklayarak açmak API yolunu çalıştırmaz.

## Ücretsiz kullanım ve güncelleme notu
- Gemini API'nin ücretsiz kullanım durumu model, bölge ve güncel kota/koşullara bağlıdır; Google AI Studio'da güncel limitleri kontrol edin. Ücretsiz kota aşılırsa istekler hata verebilir.
- Bu sürüm her düğmeye bastığınızda Gemini'den yeni çalışma içeriği ister. Yapay zekâ modeli kendi kendine arka planda durmaksızın güncellenmez; içerik üretimi kullanıcı isteğiyle gerçekleşir.
- API anahtarını GitHub'a, HTML'e veya herkese açık koda koymayın. Sadece Vercel Environment Variables kullanın.
- Bu uygulama resmî ÖSYM/YÖK uygulaması değildir. Üretilen sorular çalışma amaçlı özgün alıştırmalardır.
