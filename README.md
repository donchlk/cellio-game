# Cell.io – Minimal Agar-like Browser Game

Cell.io is a lightweight single-file browser game inspired by Agar.io. [web:22]
You control a cell, eat food pellets and smaller bots to grow, and try not to get eaten by larger enemies. [web:22]

> This is the **first prototype** version focused on core movement, AI bots, and basic game feel.

---

## 🚀 Demo / Quick Start

1. Clone this repository.
2. Open `cellio_game.html` directly in your browser (Chrome / Edge / Firefox).
3. Move your mouse to steer your cell.

No build steps, no dependencies – it is a single self-contained HTML file.

---

## 🕹️ Gameplay

- You start as a small cell in a 3000×3000 world.
- Move the mouse to steer your cell towards food and smaller bots.
- Eating food pellets slowly increases your mass.
- When you are significantly larger than another cell and get close enough, you absorb it and gain its mass.
- Larger cells move more slowly, so positioning matters. [web:22]
- If an enemy absorbs you, you die and can respawn via the in-game button.

This prototype is **single-player** only and simulates enemy bots locally in the browser.

---

## ✨ Features (v1 Prototype)

- Single-file implementation: pure HTML, CSS, and vanilla JavaScript.
- HTML5 canvas rendering with a zoomable camera and grid background.
- 600 colorful food pellets that respawn over time.
- 12 autonomous AI bots that:
  - Roam the map.
  - Chase smaller cells.
  - Flee from larger cells.
  - Eat food and grow over time.
- Dynamic movement speed based on cell size (larger = slower). [web:22]
- Smooth camera following and zoom based on player radius.
- Mass decay mechanic: large cells slowly lose mass over time. [web:22]
- Simple HUD:
  - Live mass display.
  - Top‑5 leaderboard with your cell highlighted.
- Death screen with final mass and one-click respawn.
- Soft glow effects on cells and pellets for a more modern look.

---

## 🧱 Tech Stack

- **Language:** HTML5, CSS3, JavaScript (ES6+).
- **Rendering:** HTML5 `<canvas>` 2D context.
- **Runtime:** Client-side only, no backend.
- **Dependencies:** None – no frameworks, no build tools.

---

## 📁 Project Structure

```text
.
├── cellio_game.html   # Main and only file containing markup, styles, and game logic
└── README.md          # Project documentation
