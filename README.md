# Bingo Maths! — PWA → Google Play Store Guide

## Your App Files
```
bingo-maths/
├── index.html       ← The full game
├── manifest.json    ← PWA identity & icons config
├── sw.js            ← Service worker (offline support)
├── icons/           ← All icon sizes for store & device
│   ├── icon-72.png
│   ├── icon-96.png
│   ├── icon-128.png
│   ├── icon-144.png
│   ├── icon-152.png
│   ├── icon-192.png  ← Used on home screen
│   ├── icon-384.png
│   └── icon-512.png  ← Used in Play Store listing
└── README.md
```

---

## Step 1 — Host Your App (Free options)

You need the files live on HTTPS before submitting to the Play Store.

**Option A — Netlify (Recommended, free)**
1. Go to https://netlify.com → Sign up free
2. Drag the `bingo-maths/` folder onto the Netlify dashboard
3. You get a URL like: `https://bingo-maths-abc123.netlify.app`

**Option B — GitHub Pages (Free)**
1. Create a GitHub account & new repo called `bingo-maths`
2. Upload all files to the repo root
3. Go to Settings → Pages → Deploy from main branch
4. URL: `https://yourusername.github.io/bingo-maths`

---

## Step 2 — Submit to Google Play via PWABuilder

1. Go to **https://pwabuilder.com**
2. Paste your hosted URL (e.g. `https://bingo-maths-abc123.netlify.app`)
3. Click "Start" — it will score your PWA (should be 100/100!)
4. Click "Package for Stores" → choose **Google Play**
5. Fill in:
   - Package name: `com.yourname.bingomaths`
   - App version: `1.0`
   - Signing key: Generate a new one (save the password!)
6. Download the `.aab` bundle

---

## Step 3 — Google Play Console

1. Go to **https://play.google.com/console** → Create Developer Account ($25 one-time fee)
2. Create a new app → "Bingo Maths!"
3. Upload the `.aab` file to Internal Testing first
4. Fill in the store listing:
   - **Title**: Bingo Maths! Times Tables Edition
   - **Short description**: Fun times tables bingo for kids aged 5–11
   - **Category**: Education → Brain Games
   - **Content rating**: Everyone (ESRB E) / PEGI 3
5. Upload screenshots (take them on your phone)
6. Submit for review — usually approved in 1–3 days!

---

## Tips for Approval

- ✅ Set content rating to "Everyone" / PEGI 3
- ✅ No ads, no in-app purchases = easier review
- ✅ Add a privacy policy (required — use https://privacypolicygenerator.info for a free one)
- ✅ Test on a real Android device before submitting

---

## Features in This Version

- 9 times tables (2× through 10×) + Mixed mode
- Animated sleet / rain background
- Questions read aloud via speech synthesis
- Web Audio API sound effects (correct chime, wrong buzz, BINGO fanfare)
- Score, streak & personal best tracker (saved locally)
- Full confetti celebration on BINGO
- Works 100% offline after first load
- Portrait-locked for phones
