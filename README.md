# 🌱 Mind Garden

**A meditative digital garden where your thoughts become living, breathing procedural plants.**

[**→ Visit the Live Garden**](#) <!-- Replace # with your GitHub Pages URL -->

![Mind Garden](https://img.shields.io/badge/Mind-Garden-4ecdc4?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0naHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmcnIHZpZXdCb3g9JzAgMCAxMDAgMTAwJz48dGV4dCB5PScuOWVtJyBmb250LXNpemU9JzkwJz7wn4yxPC90ZXh0Pjwvc3ZnPg==)
![No Dependencies](https://img.shields.io/badge/Dependencies-Zero-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

---

## What is this?

Mind Garden is a **single-file web application** — part journaling tool, part generative art, part digital zen garden. Type a thought, and it grows into a procedurally generated plant whose shape, color, and behavior are uniquely derived from your words.

- **Positive thoughts** grow green, teal, and lush
- **Reflective thoughts** bloom in purples and blues  
- **Difficult feelings** take on warm reds and pinks — still beautiful, still part of the garden

Every plant is deterministic: the same words always create the same plant. Your garden is yours alone, stored locally in your browser.

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🌿 **Procedural Plants** | Four plant types (trees, flowers, ferns, succulents) generated from text DNA |
| 🎨 **Sentiment-Driven Colors** | Simple NLP maps emotional tone to hue and luminosity |
| 🌙 **Real-Time Day/Night Cycle** | The garden reflects your actual time of day — stars, moon, dawn, dusk |
| ✨ **Fireflies** | Ambient bioluminescent particles that emerge at night |
| 🌬️ **Wind Simulation** | Plants sway organically with procedural wind |
| 💾 **Persistent Garden** | Everything saved to localStorage — your garden grows over days and weeks |
| 📖 **Thought Journal** | Side panel to review, revisit, and manage past thoughts |
| 🔥 **Streak Tracking** | Tracks consecutive days of journaling |
| 🖱️ **Click-to-Place** | Choose exactly where in the garden your thought grows |
| 📱 **Responsive** | Works on desktop and mobile |

## 🚀 Deploy to GitHub Pages

### Option 1: Direct Deploy (Simplest)

1. Fork or clone this repository
2. Go to **Settings → Pages**
3. Under "Source", select **Deploy from a branch**
4. Choose `main` (or `master`) branch and `/ (root)` folder
5. Click **Save**
6. Your garden will be live at `https://yourusername.github.io/mind-garden/`

### Option 2: GitHub Actions (Included)

This repo includes a `.github/workflows/deploy.yml` that automatically deploys on push. Just enable Pages with "GitHub Actions" as the source.

## 🏗️ Architecture

```
index.html          ← The entire application (single file, zero dependencies)
README.md           ← You are here
LICENSE             ← MIT License
.github/
  workflows/
    deploy.yml      ← GitHub Actions workflow for Pages deployment
.nojekyll           ← Tells GitHub Pages to skip Jekyll processing
```

### How Plant DNA Works

```
User Input: "I feel grateful for the sunshine today"
                ↓
        Hash Function (text → seed)
                ↓
        Seeded Random Generator
                ↓
    ┌─────────────────────────────┐
    │  Plant DNA                  │
    │  ─────────                  │
    │  type: "flower"             │
    │  height: 82px               │
    │  hue: 142° (green/teal)     │
    │  branches: 4                │
    │  bloomSize: 6.2             │
    │  swaySpeed: 1.3             │
    │  glowIntensity: 0.45        │
    │  sentiment: +0.67           │
    └─────────────────────────────┘
                ↓
        Procedural Rendering
        (Canvas 2D API)
```

Every property of the plant — its height, curvature, leaf count, color — is derived deterministically from the input text. Same text = same plant, every time.

### Sentiment Analysis

A lightweight keyword-based sentiment analyzer maps words to emotional valence:

- **Positive words** (love, hope, dream, bloom...) → greens, teals, warm light
- **Negative words** (sad, lost, fear, grief...) → reds, pinks, cooler tones  
- **Neutral** → purples, blues

No external API. No data leaves your browser. Ever.

## 🎮 Controls

| Control | Action |
|---------|--------|
| Type + Enter | Plant a thought at a random position |
| Click garden + type | Plant at clicked position |
| 📖 | Open/close the thought journal |
| 🌬️ | Toggle wind simulation |
| ✨ | Toggle fireflies |
| 🌙 | Toggle real-time day/night cycle |
| 🗑️ | Clear entire garden |
| Hover plant | View the thought that created it |

## 🔒 Privacy

- **Zero tracking.** No analytics, no cookies, no external requests.
- **100% local.** All data stored in `localStorage`.
- **No dependencies.** A single HTML file with vanilla JS.
- **Your thoughts stay yours.**

## 💡 Philosophy

This project asks: *what if journaling was less about reading your thoughts back, and more about watching them grow?*

Each entry becomes part of a landscape that evolves over time. Bad days don't ruin the garden — they add contrast, texture, depth. The garden is a mirror: it shows not what you think, but the shape of your thinking.

## 🛠️ Technical Details

- **Rendering:** HTML5 Canvas 2D (no WebGL, no libraries)
- **Animation:** `requestAnimationFrame` at native refresh rate
- **Plant generation:** Seeded PRNG from text hash → deterministic procedural geometry
- **Performance:** Efficient rendering with depth sorting, particle pooling
- **Storage:** `localStorage` with JSON serialization
- **Compatibility:** All modern browsers (Chrome, Firefox, Safari, Edge)

## 📄 License

MIT — do whatever you want with it. Plant something beautiful.

---

<p align="center">
  <em>Made with 🌱 by a mind that wanted to show what it could grow.</em>
</p>
