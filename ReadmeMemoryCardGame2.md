# 🍃 Memory Card Game

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

A relaxing photographic memory game. Explore beautiful places, find matching pairs, and improve your personal best.

*Wander. Remember. Repeat.*

[🎮 Play Now](https://memorycardgame.github.io) · [🐛 Report Bug](https://github.com/memorycardgame/memorycardgame.github.io/issues) · [✨ Request Feature](https://github.com/memorycardgame/memorycardgame.github.io/issues)

</div>

---

## ✨ Features

- **3 Difficulty Levels** — Easy (8 pairs), Medium (12 pairs), Hard (18 pairs)
- **3 Card Color Themes** — Forest, Ocean, Plum
- **Real Photography** — Beautiful nature photographs via [Unsplash](https://unsplash.com)
- **Score Tracking** — Moves, time, and points with efficiency & time bonuses
- **Personal Bests** — Top scores saved per difficulty on your device
- **Auto-Save** — Game progress and settings persist across visits
- **Hint System** — 3 hints per game (reveals a pair, costs up to 50 points)
- **Pause & Resume** — Take a breather anytime; the timer freezes with you
- **Custom Dialogs** — Elegant win and confirmation modals (no native popups)
- **3D Flip Animations** — Smooth, tactile card interactions
- **Fully Responsive** — Optimized for desktop, tablet, and mobile
- **Accessible** — Keyboard navigation, ARIA live regions, and screen reader support
- **Graceful Degradation** — Named cards remain playable if images fail to load
- **Reduced Motion** — Respects `prefers-reduced-motion` settings

---

## 🚀 Getting Started

### Play Online
Visit **[memorycardgame.github.io](https://memorycardgame.github.io)**

### Run Locally

```bash
git clone https://github.com/memorycardgame/memorycardgame.github.io.git
cd memorycardgame.github.io
open index.html
```

> **Note:** An internet connection is recommended so card photographs can load from Unsplash. If images are unavailable, cards fall back to named placeholders and remain fully playable.

---

## 🎯 How to Play

1. **Flip a photograph** — Click or tap any card to reveal its image
2. **Find the pair** — Turn over a second card to find its matching photograph
3. **Keep the pair** — Identical images stay revealed; mismatches flip back
4. **Complete the collection** — Match every pair to finish your journey
5. **Aim high** — Fewer moves and faster times earn more points
6. **Use hints wisely** — Each hint reveals a pair briefly but deducts up to 50 points

---

## 🎮 Controls

| Action | Control |
|--------|---------|
| Flip Card | Click / Tap |
| Navigate Cards | Arrow Keys / Home / End |
| New Game | 🔄 New game button |
| Pause / Resume | ⏸️ / ▶️ button |
| Hint | 💡 Hint button |
| Change Card Color | 🎨 Theme dropdown |

---

## 🏆 Scoring

Your score rewards both efficiency and speed:

- **Base points** — 100 per matched pair
- **Efficiency bonus** — Up to `(pairs × 2 − moves) × 5` extra points
- **Time bonus** — Up to `(90 − seconds elapsed)` extra points
- **Difficulty multiplier** — ×1 (Easy), ×1.5 (Medium), ×2 (Hard)
- **Hint cost** — −50 points per hint (score never drops below zero)

The top 3 personal bests per difficulty appear in the sidebar, with up to 10 retained per level.

---

## 🛠️ Technologies

- **HTML5** — Semantic markup with `<dialog>` for modals
- **CSS3** — Custom properties, grid layout, 3D transforms, backdrop filters
- **JavaScript (ES6+)** — Vanilla JS, no dependencies
- **Local Storage API** — Persistent game state, high scores, and theme
- **Unsplash** — Source photography

---

## 📁 Project Structure

```
memorycardgame.github.io/
├── index.html
├── favicon.ico
├── README.md
└── LICENSE
```

---

## ♿ Accessibility

Field Notes is built with inclusivity in mind:

- Full keyboard navigation across the board (arrow keys, Home, End)
- ARIA live region announcements for game events
- Focus management for dialogs and pause overlay
- Descriptive labels on all interactive elements
- Honors `prefers-reduced-motion` to disable animations

---

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/NewFeature`)
3. Commit changes (`git commit -m 'Add NewFeature'`)
4. Push to branch (`git push origin feature/NewFeature`)
5. Open a Pull Request

---

## 📄 License

MIT License

---

## 🔗 Links

- **Live Demo**: [memorycardgame.github.io](https://memorycardgame.github.io)
- **Photography**: [Unsplash](https://unsplash.com)

---

<div align="center">

*Less scrolling. More noticing.*

⭐ Star this repo if you enjoy it!

</div>
