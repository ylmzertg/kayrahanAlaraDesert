# Kayrahan'ın Tatlı Dükkânı 🧁

Çocuklar için basit, rahatlatıcı **tatlı süsleme** oyunu (YouTube Playables uyumlu).
"Dessert DIY" tarzı: krema rengi seç, keke dokunarak süs ekle, servis et, para kazan,
yeni süsleri aç.

## Nasıl oynanır
- 🎨 Alttaki renklerden **krema rengi** seç
- 🍓 Bir **süs** seç (çilek, çikolata, gökkuşağı şeker, kalp; kilitli: kiraz, yıldız)
- 🧁 **Keke dokun** (veya sürükle) → süs eklenir
- 🍽️ **Servis Et** → konfeti + para
- 🔒 Kazanılan parayla yeni süsleri aç · 🧽 temizle

## Özellikler
- Dikey (portrait) HTML5 canvas, tamamen dokunmayla
- YouTube Playables SDK (firstFrameReady/gameReady, onPause/onResume, saveData/loadData, sendScore)
- İlerleme kalıcı (SDK bulut + localStorage çift-yazma)
- Ses + titreşim ve ikisi için aç/kapa
- Özgün çizim; tek harici görsel: `assets/hero.png` (Kayrahan şef)

## Dosyalar
```
index.html · style.css · game.js · assets/hero.png
```

## Yerel test
```bash
npx http-server . -p 4322 -c-1   # http://127.0.0.1:4322
```
