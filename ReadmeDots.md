# 🔴🔵 Dots / Точки

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/Demo-Live-brightgreen)](https://dotsjs.github.io)

A beautiful, interactive Dots (Точки) game — the classic abstract strategy game where you capture enemy dots by surrounding them with a continuous chain of your own. Features an unbeatable AI, a mesmerizing AI vs AI showcase mode, and full Ukrainian language support. Fully responsive for all devices and orientations!

## 🌐 Live Demo

**[https://dotsjs.github.io](https://dotsjs.github.io)**

## ✨ Features

- 🔴🔵 Classic Dots gameplay on clean squared-paper grid
- 🤖 Unbeatable AI opponent (capture-aware evaluation with threat detection)
- 🎬 AI vs AI mode (default) with auto-restart every 5 seconds
- ⏸️ Stop / Resume control for AI vs AI matches
- 👥 Local 2-player mode
- 🎯 Four modes: AI vs AI, 2 Players, Easy, and Unbeatable
- 📐 Six board sizes: 9×9, 11×11, 13×13, 15×15, 17×17, 19×19
- 🏆 Smart winner calculation with grounding rule & at-risk tie-breaker
- 🎨 Captured territories shaded & outlined in the owner's color
- 🇺🇦 Ukrainian language by default (English also available)
- 💾 Auto-saves game state, scores & settings to Local Storage
- 📱 Responsive layout — vertical, horizontal & small screens
- 🖥️ Scroll-free desktop layout (board + panel side-by-side)
- ↩️ Undo move & live scoreboard

## 🚀 Quick Start

```bash
# Clone repository
git clone https://github.com/dotsjs/dotsjs.github.io.git

# Open in browser
open index.html
```

Or just visit the [live demo](https://dotsjs.github.io)!

## 🎮 How to Play

Place a dot of your color on an empty grid intersection. If you complete a **closed chain** of your dots (connected horizontally, vertically, or diagonally) that **encloses at least one enemy dot**, all dots and empty points inside are **captured** — they're removed from play and added to your score. Whoever captures the **most enemy dots** wins!

| Mode | Description |
|------|-------------|
| 🎬 **AI vs AI** | Watch two AIs battle, auto-restarts after each game |
| 👥 **2 Players** | Play locally against a friend |
| 🟢 **AI (Easy)** | Beatable AI for casual play |
| 🔴 **AI (Unbeatable)** | Challenge the smart AI |

**Key rules:**
- 🔗 Chains connect dots in all 8 directions (including diagonals)
- 🚫 You cannot surround an empty area — it must contain enemy dots
- 🌍 **Grounding rule**: groups of dots touching the board border cannot be captured
- 🏁 Click **Finish** to end the game and score, or the game ends automatically when no moves remain

## 🛠️ Tech Stack

- HTML5
- CSS3 (Animations & Responsive Design)
- Vanilla JavaScript (Canvas API, Flood-Fill Capture Engine, Local Storage)

## 📁 Structure

```
├── index.html    # Main application
├── README.md     # Documentation
└── LICENSE       # MIT License
```

## 🎨 Customization

Change the default board size in `index.html`:
```javascript
size: 11,   // 9, 11, 13, 15, 17 or 19
```

Adjust AI vs AI auto-restart delay (milliseconds):
```javascript
const AUTO_RESTART_MS = 5000;
```

Modify board & dot colors in CSS:
```css
--board-bg: #f4f1e8;
--board-line: #cfd8e0;
--red: #e94560;
--blue: #0f9d9d;
```

Set default language:
```javascript
lang: 'uk',  // 'uk' or 'en'
```

## 🧠 About the AI

The AI uses a **capture-aware evaluation engine** built on top of a **flood-fill enclosure detector**. For every candidate move it:

- 💥 Simulates the move and computes any **immediate captures** using flood-fill (regions that don't reach the border and contain live enemy dots)
- 🛡️ Scans the opponent's **best capture response** one ply ahead to avoid giving dots away
- 📍 Rewards central play, adjacency to friendly dots, and proximity to enemy dots

The winner calculation applies the classic **grounding rule** — dots connected to the border are safe — and uses the count of **at-risk (ungrounded) dots** as a tie-breaker when captured scores are equal. Controlled randomness among near-best moves ensures every AI vs AI match plays out differently.

## 📱 Browser Support

Chrome, Firefox, Safari, Edge, iOS Safari, Android Chrome ✅

## 📝 License

[MIT](LICENSE)

---

<div align="center">

**🔴🔵 Surround enemy dots to capture them! / Оточуй точки суперника, щоб захопити їх! 🔴🔵**

⭐ Star this repo if you like it!

</div>