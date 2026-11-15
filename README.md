# 🃏 Flip 7 Scorekeeper (PWA)

A fast, mobile-first Progressive Web App (PWA) for tracking scores in the **Flip 7** card game—designed to replace pen-and-paper math at the game table.

## ✨ Features
- **Tap-to-Build Hand Calculator:** Tap the number cards (`0–12`) and modifiers (`+2`, `+4`, `+6`, `+8`, `+10`, `×2`) each player holds at the end of a round.
- **Official Flip 7 Math:** Automatically applies the `×2` multiplier *only* to number cards (leaving flat modifiers untouched) and awards the **+15 Flip 7 bonus** when a player collects 7 unique number cards.
- **Fast Table Flow:** One-tap **Bust (`0`)** button, **Save & Next** player cycling, automatic dealer rotation, and **Undo Last Round** support.
- **Live Standings & Endgame Alerts:** Tracks progress bars toward **200 points**, highlights players in the **170+ endgame zone**, and crowns the winner automatically.
- **Offline & Installable (PWA):** Includes a Web App Manifest and Service Worker so you can install it directly onto an iOS or Android home screen and play offline.
- **Auto-Save:** Automatically saves your ongoing game state to `localStorage` so accidental refreshes never lose your scores.

## 📁 Project Structure
```text
├── index.html      # Complete single-file app UI, styling, and scoring logic
├── manifest.json   # PWA metadata, standalone display config, and app icons
├── sw.js           # Service worker for offline caching
├── icon-192.png    # Home screen icon (192x192)
├── icon-512.png    # Splash/high-res icon (512x512)
└── README.md       # Project documentation
```

## 🚀 Running & Installing on Mobile
1. **Local Testing:** Open `index.html` with a local dev server (such as the **Live Server** extension in VS Code).
2. **Hosting:** Deploy the folder to any static HTTPS host (**GitHub Pages**, **Netlify**, or **Vercel**).
3. **Install on Phone:**
   - **iOS (Safari):** Open the hosted URL → tap **Share** → **Add to Home Screen**.
   - **Android (Chrome):** Open the hosted URL → tap the **⋮ menu** → **Install app**.

## 🎲 Scoring Formula Reference
$$\text{Round Score} = (\text{Sum of Unique Number Cards} \times 2\text{ if }\times 2) + \text{Flat Modifiers} + 15\text{ (if 7 unique numbers)}$$