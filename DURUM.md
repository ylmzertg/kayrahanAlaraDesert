# DURUM — Devam Notu (Kayrahan's Dessert Shop)

> Başka bilgisayarda devam ederken: bu repoyu klonla, bu dosyayı ve `youtubeOrnekOyunlar.md`'yi oku, kaldığın yerden devam et. (Claude sohbet geçmişi cihazlar arası senkronize OLMAZ; kod ve bu notlar repoda.)

## Oyun nedir
Çocuklar için **tatlı süsleme** oyunu (YouTube Playables uyumlu). Referans: **"Dessert DIY"** (≈63M oynanma) — mekanik taklit, görsel/karakter **özgün**.
Akış: **Karakter seç → müşteri sipariş verir → krema sık → sos çek → süsle → servis → para → kilit aç.**

## Repolar (AYRI iki oyun)
| Oyun | Repo | Durum |
|------|------|------|
| Tatlı Dükkânı (bu repo) | `github.com/ylmzertg/kayrahanAlaraDesert` | private — public yapılınca `https://ylmzertg.github.io/kayrahanAlaraDesert/` |
| Platform oyunu (Mario tarzı) | `github.com/ylmzertg/youtubeKayrahanMario` | public, Pages canlı |

Bu repo **kendi kökünde** çalışır: `index.html · style.css · game.js · assets/{hero.png, alara.png}`.

## Karakterler
Açılışta **Kayrahan** (`assets/hero.png`) veya **Alara** (`assets/alara.png`) seçilir; seçilen şef olur.

## ✅ Tamamlananlar
- Karakter seçim ekranı (Kayrahan / Alara)
- Müşteri + sipariş (istediği tatlı+süs; eşleşince bonus para — "Perfect/Yummy")
- Krema sıkma (parmakla sürükleme, mesafe-bazlı) — süs eklemeden önce krema gerekir
- Şurup/sos çizme (seçili renkte, sürükleyerek)
- 8 süs: çilek, çikolata, gökkuşağı şeker, kalp, muz (ücretsiz) + kiraz(15), yaban mersini(20), yıldız(30) kilitli
- 3 tatlı çeşidi: kek 🧁 / dondurma 🍦 / kurabiye 🍪 (sağdan seçilir)
- 8 krema rengi (pembe/çikolata/vanilya/nane/mavi/mor/kırmızı/beyaz); servis → para; parayla kilit açma
- 5 tatlı çeşidi: kek/dondurma/kurabiye/donut/pasta dilimi
- Ses efektleri + titreşim + ikisi için aç/kapa; `sendScore`; İngilizce arayüz
- Kalıcılık: `saveData` SDK **+ localStorage çift-yazma**
- Dükkân meta'sı: 🛍️ My Shop ekranı (parayla bayrak/bitki/pencere/tezgah)
- **İlk deneyim:** 3 adımlı mini tutorial (👇 krema→süs→servis) + kademeli açılım (ilk servise kadar sade: 5 süs; sos/kilitli süs/Shop gizli)

## ⏳ Kalan yol haritası (sırayla)
- ~~Faz 3.1 sos · 3.2 yeni süsler · 3.3 yeni çeşitler · 3.4 ek renkler~~ ✅ TAMAM
- ~~Faz 4 — Dükkân meta'sı (My Shop ekranı)~~ ✅ TAMAM
- ~~Faz 5 — Cila: müşteri tepkisi + yıldız puanı (5.1) · arka plan müziği (5.2)~~ ✅ TAMAM
- ~~İlk deneyim: mini tutorial + kademeli açılım~~ ✅ TAMAM

**🎉 Yol haritası tamamlandı.** Sıradaki fikirler (opsiyonel): daha çok süs/çeşit, günlük ödül, daha çok müşteri çeşidi, animasyonlu servis. Asıl öneri: repo'yu public yapıp gerçek bir çocukla test.
(Detaylı analiz + karar: `youtubeOrnekOyunlar.md`)

## Yerel çalıştırma / önizleme
```bash
npx http-server . -p 4322 -c-1      # http://127.0.0.1:4322
```

## Önemli teknik notlar
- **Kalıcılık:** `ytgame` SDK YouTube dışında da tanımlı oluyor → saveData hem SDK hem `localStorage`'a yazılmalı (kod öyle). Yoksa standalone linkte ilerleme kaybolur.
- **Görsel ekleme:** ham görseli (beyaz arka plan) `assets/`'e koy; arka planı şeffaflaştırıp kırpmak için jimp flood-fill script'i kullanıldı (eşik ~228). Sohbete yapıştırılan görseller diske düşmez — dosya olarak kaydedip ver.
- **Canlı link için:** repo **public** olmalı (Settings → Danger Zone → Make public) → sonra Pages kök dizinden açılır.

## Son commit
`2585405` — Alara karakter görseli eklendi.
