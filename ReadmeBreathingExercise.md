# 🌬️ Дихальна вправа / Breathing Exercise

A beautiful, calming breathing exercise web application with guided inhale/exhale animations for meditation and relaxation. Track your progress, build daily habits, and earn achievements — all in a single HTML file.

## 🌐 Live Application

**[https://breathingexercise.github.io](https://breathingexercise.github.io)**

---

## ✨ Features

### 🧘 Guided Breathing
- Smooth animated breathing circle that expands (inhale) and contracts (exhale) with precise timing for each phase
- Live phase labels (Inhale / Hold / Exhale / Hold) and a countdown timer
- Animated gradient background with floating particles for a soothing atmosphere
- Configurable number of cycles per session

### 🌊 8 Breathing Techniques
| Technique | Pattern | Purpose |
|-----------|---------|---------|
| **4-7-8** | 4-7-8 | Relaxation before sleep |
| **Box** | 4-4-4-4 | Focus & calm |
| **Calm** | 4-6 | Gentle calming |
| **Deep** | 5-5 | Even breathing |
| **Energy** | 2-2 | Alertness / wake up |
| **Coherent** | 5.5-5.5 | Heart balance |
| **Triangle** | 4-4-4 | Three-phase breathing |
| **Anti-stress** | 4-7-8-4 | Long exhale relaxation |

### 📊 Statistics & Calendar
- Stat cards: active days, total sessions, total cycles, current day streak, and awards earned
- Interactive monthly calendar highlighting completed days (with session counts) and today
- Navigate freely between months

### 🏆 Achievement System
Unlock 12 awards for your dedication:
- 🌱 **First breath** — complete your first session
- 🔥 **Three in a row** / ⭐ **Week of calm** / 🧘 **Zen master** — daily streaks (3 / 7 / 30 days)
- 💨 **50 cycles** / 🌊 **200 cycles** / 🏔️ **500 cycles** — total cycle milestones
- 📅 **Consistency** / 💎 **Devotion** — completed session milestones (10 / 50)
- 🧭 **Explorer** — try all techniques
- 🌅 **Early bird** / 🌙 **Night owl** — time-based awards

An animated toast notification celebrates each new achievement.

### 🌍 Multilingual
- **Ukrainian** (default) and **English** support
- Instant switching with full UI translation

### 💾 State Persistence
Everything is saved to `localStorage` and restored on reload:
- Selected language, technique, and cycle count
- Full session history, statistics, and earned awards
- **Last-viewed tab** is remembered
- **Paused exercise** is restored on reload (resumes exactly where you left off, in a paused state)

### 📱 Responsive Design
- Optimized layouts for phones, tablets, and desktops
- Full support for both **portrait** and **landscape** orientations

---

## 🚀 Getting Started

No build tools, dependencies, or installation required. The entire app is contained in a single HTML file.

1. Clone or download the repository:
   ```bash
   git clone https://github.com/breathingexercise/breathingexercise.github.io.git
   ```
2. Open `index.html` in any modern web browser.

That's it! 🎉

You can also host it on any static hosting service (GitHub Pages, Netlify, etc.).

---

## 🎯 How to Use

1. **Choose a technique** from the program cards on the *Exercise* tab.
2. Set the desired number of **cycles**.
3. Press **Start** and follow the breathing circle — inhale as it grows, exhale as it shrinks.
4. Use **Pause / Resume** anytime, or **Reset** to start over.
5. Check the **Statistics** tab to review your calendar and progress.
6. Visit the **Awards** tab to see unlocked and upcoming achievements.

---

## 🛠️ Technology

Built with pure **HTML**, **CSS**, and **vanilla JavaScript** — no frameworks, no external libraries. The favicon is an inline SVG, so the app works fully offline as a single file.

---

## 📄 License

MIT

---

## 🔗 Repository

[https://github.com/breathingexercise/breathingexercise.github.io](https://github.com/breathingexercise/breathingexercise.github.io)

---

<p align="center">Breathe in. Breathe out. Find your calm. 🌿</p>
