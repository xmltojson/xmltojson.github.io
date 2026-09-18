# ❄️ The Snow Globe — A Little Winter

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/Demo-Live-brightgreen)](https://snowglobej.github.io)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](#)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](#)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](#)

A little winter, held in glass. An interactive snow globe featuring a detailed miniature cabin, drifting snow, and four atmospheric modes.

Built with **pure HTML, CSS, and JavaScript** — no frameworks, dependencies, or build tools.

## 🌐 [Try the Live Demo →](https://snowglobej.github.io)

---

## ✨ Features

- 🔮 **Realistic Glass Effects** — Layered reflections, illuminated rims, optical shading, and a wooden base with a brass-style plaque.
- 🏠 **Detailed Winter Miniature** — A dimensional cabin, glowing windows, snow-covered evergreens, distant mountains, a snowman, and drifting chimney smoke.
- 🌤️ **Four Atmospheres** — Daylight, Midnight, Aurora, and Blizzard, each with its own lighting, colors, and snowfall behavior.
- ❄️ **Animated Snow Physics** — Depth-aware particles with wind, swirling motion, glass-boundary collisions, and settling.
- 🎚️ **Adjustable Snowfall** — Set intensity from 10% to 100% using the slider.
- 🎮 **Multiple Ways to Interact** — Tap, drag, use the Shake button, press keyboard shortcuts, or enable device shake where supported.
- ⏯️ **Pause and Play** — Stop the animation whenever you want a still winter scene.
- 📊 **Live Statistics** — Track globe shakes and the current number of snow particles.
- 💾 **Saved Preferences** — Atmosphere, snowfall intensity, shake count, and pause state are stored locally.
- 🖥️ **Native 100% Zoom Layout** — Compact desktop controls and viewport-aware globe sizing, with a stacked layout on smaller screens.
- ♿ **Accessibility Features** — Keyboard controls, visible focus indicators, descriptive labels, status announcements, and reduced-motion support.

---

## 🌌 Atmospheres

| Mode | Experience |
|------|------------|
| ☀️ **Daylight** | Pale winter sunshine, soft blue shadows, and gently drifting snow. |
| 🌙 **Midnight** | A moonlit landscape, star-filled sky, and warm cabin windows. |
| 🌌 **Aurora** | Animated northern lights above a peaceful, starlit forest. |
| 🌨️ **Blizzard** | Stronger gusts, wind-driven snow, and atmospheric winter haze. |

---

## 🚀 Quick Start

### Option 1: Open the Live Demo

Visit **[https://snowglobej.github.io](https://snowglobej.github.io)**.

### Option 2: Run Locally

Clone the repository:

```bash
git clone https://github.com/snowglobej/snowglobej.github.io.git
cd snowglobej.github.io
```

Open `index.html` in a modern browser. No installation or build step is required.

> Device motion requires browser support and a secure context, typically HTTPS. For device shake, use the live demo in a supported mobile browser.

---

## 🎮 How to Use

| Action | Method |
|--------|--------|
| **Shake the globe** | Tap or click the glass, drag and release, or click **Shake the globe**. |
| **Stir the snow** | Drag across the globe while the animation is playing. |
| **Adjust snowfall** | Move the **Snowfall intensity** slider. |
| **Change atmosphere** | Select **Daylight**, **Midnight**, **Aurora**, or **Blizzard**. |
| **Pause / play** | Click the pause or play button. |
| **Enable device shake** | Click **Enable device shake** and grant permission if requested. |
| **Reset statistics** | Click **Reset count** to clear the shake counter without changing your scene settings. |

### ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Shake the globe |
| `P` | Pause or resume animation |
| `1` | Daylight |
| `2` | Midnight |
| `3` | Aurora |
| `4` | Blizzard |
| `Enter` or `Space` on the focused globe | Shake the globe |

Global shortcuts do not override standard interactions while a form control or link is focused.

### 📱 Device Shake

Device shake is optional and must be enabled manually.

- Availability depends on your browser, device sensors, and security settings.
- Some browsers require explicit motion permission.
- Device shake does not trigger while the animation is paused or the page is hidden.
- Move your device gently and keep a secure grip.

Tap, drag, keyboard, and button controls remain available without motion access.

---

## ♿ Accessibility & Motion

The globe respects your system’s **reduced-motion preference** by starting with animation paused and disabling the decorative shake animation.

You can explicitly press **Play** to animate the scene. Controls include accessible labels, keyboard focus styles, and screen-reader status messages.

---

## 💾 Saved Preferences

The application saves these values locally in your browser:

- Selected atmosphere
- Snowfall intensity
- Shake count
- Pause state

Compatible preferences from the previous version are migrated automatically.

If local storage is unavailable, the globe remains usable, but preferences may not persist between visits.

---

## 🛠️ Built With

- **HTML5 Canvas** — Miniature scenery, snowfall, smoke, aurora, and storm effects.
- **CSS** — Responsive layout, glass shading, wooden base, and interface styling.
- **SVG** — Glass reflections and control icons.
- **JavaScript** — Particle simulation, interaction handling, and local state.
- **Browser APIs** — `requestAnimationFrame`, `ResizeObserver`, localStorage, and optional device motion.

Static scenery is cached in offscreen canvases, and the animation loop stops while the page is hidden.

---

## 📁 Repository Structure

```text
snowglobej.github.io/
├── index.html      # Complete application: markup, styles, and JavaScript
├── README.md       # Project documentation
└── LICENSE         # MIT License
```

---

## 🤝 Contributing

Contributions, bug reports, and suggestions are welcome!

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/new-feature
   ```
3. Make your changes and check desktop and mobile layouts.
4. Test keyboard controls and reduced-motion behavior.
5. Commit and push:
   ```bash
   git commit -m "Add new feature"
   git push origin feature/new-feature
   ```
6. Open a pull request.

Please keep the application dependency-free and preserve its accessibility features.

---

## 📄 License

Released under the [MIT License](LICENSE).

Copyright (c) 2025 Yuliya Kolesnikova  
[ORCID: 0009-0000-6151-7415](https://orcid.org/0009-0000-6151-7415)

---

<p align="center">
  Made with ❄️ and ☕ · A moment of calm.<br>
  <a href="https://snowglobej.github.io"><strong>Shake a little winter →</strong></a>
</p>