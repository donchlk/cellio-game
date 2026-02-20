# Cell.io - Enhanced Professional Edition

Cell.io is a lightweight single-file browser game inspired by Agar.io. This version is the **Professional Edition**, featuring advanced physics, competitive mechanics, and smart bot AI.

---

## 🚀 Demo / Quick Start

1. Clone this repository.
2. Open `cellio_game.html` directly in your browser.
3. Enter your nickname and press **Play**.
4. Use your mouse to steer, **Space** to split, and **W** to eject mass.

---

## ✨ Key Features

- **Advanced Physics**: Deterministic `dt`-based simulation ensures smooth movement regardless of frame rate.
- **Split Mechanic (Space)**: Divide your mass into pieces to catch smaller prey or escape.
- **Mass Ejection (W)**: Shoot out mass to feed others or distract bots.
- **Micro Growth Boost**: Consuming food or cells gives a temporary visual and speed boost.
- **Aggregated Leaderboard**: Real-time ranking of all players and bots based on total mass across all pieces.
- **Smart Bot AI**: Bots roam for food, chase smaller cells, and avoid viruses.
- **Dynamic Camera**: Smooth zoom that scales with your total mass.

---

## 🧮 Physics & Formulas

The game uses real-world competitive balancing formulas:

### 1. Speed Formula
Movement speed is inversely proportional to mass to ensure large cells are slower:
`Speed = BASE_SPEED / (sqrt(mass) + 0.002 * mass)`

### 2. Merge Timer
Splitting creates pieces that must wait to merge back. The wait time increases with mass:
`Time = 8 + (mass ^ 0.35) * 1.3` (seconds)

### 3. Growth Boost Effect
When eating, cells temporarily grow slightly larger and faster using an exponential decay model:
`BoostFactor(t) = 1 + 0.08 * e^(-4 * (1 - intensity))`

### 4. Deterministic Simulation
All movement and logic are calculated using a `dt` (delta time) factor:
`Position = Position + Velocity * dt`

---

## 🕹️ Controls

| Key | Action |
|---|---|
| **Mouse** | Steer your cell |
| **Space** | Split into two |
| **W** | Eject mass |

---

## 🧱 Tech Stack

- **Language**: Vanilla JavaScript (ES6+), HTML5, CSS3.
- **Rendering**: HTML5 Canvas 2D API.
- **Optimization**: Zero external dependencies, single-file architecture.

---

## 📜 License

This project is licensed under the MIT License. Feel free to fork and improve!
