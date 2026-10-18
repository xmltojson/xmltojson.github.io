# 🎲 3D Dice Roller

A beautiful, animated 3D dice roller with realistic rolling effects, customizable dice counts, Ukrainian-first language support, responsive layouts, and local storage persistence.

**[🎲 Open Dice Roller](https://3ddiceroller.github.io)**

<!-- Add preview.png to the repository, then uncomment:
![3D Dice Roller Preview](https://raw.githubusercontent.com/3ddiceroller/3ddiceroller.github.io/main/preview.png)
-->

## ✨ Features

### 🎨 Visual Design
- **CSS 3D dice** with six individually rendered faces
- **Ivory surfaces and inset pips** for a realistic appearance
- **Rolling and bouncing animations** with staggered landing times
- **Dark gradient interface** with a textured dice tray
- **Soft shadows and lavender accents**
- **Smooth transitions** and button micro-interactions

### 🎲 Dice Rolling
| Feature | Description |
|---------|-------------|
| 🎲 Custom dice count | Roll between 1 and 8 six-sided dice |
| 🔄 Animated rolls | Watch dice rotate, bounce, and settle |
| ➕ Instant totals | View individual values and their combined sum |
| 🕘 Roll history | Keep the latest 8 rolls |
| 🔊 Optional sound | Enable locally synthesized dice impacts |
| ⌨️ Keyboard shortcut | Press **Space** when not focused on an interactive control |

### 🌍 Language Support
- **Ukrainian** is the default language on first launch
- **English** is available through the compact **УК / EN** switcher
- Interface labels and screen-reader announcements follow the selected language
- Language preference is saved automatically

### 📱 Responsive Design
- **Viewport-height desktop layout** minimizes page scrolling
- **Side-by-side result and roll controls** on wider screens
- **Scrollable history panel** keeps desktop content compact
- **Stacked mobile layout** with touch-friendly controls
- **Portrait and landscape support**
- Natural page scrolling remains available on narrow or very short screens

### ♿ Accessibility
- Semantic markup and labeled controls
- Visible keyboard focus indicators
- Screen-reader announcements for roll results
- Support for **`prefers-reduced-motion`**
- Keyboard-accessible controls and history panel

### 💾 Persistent State
Automatically saves to `localStorage`:
- Selected language
- Number of dice
- Sound preference
- Current dice values
- Latest 8 rolls

If browser storage is unavailable, the application continues working for the current page session and displays a notice.

## 🚀 Quick Start

### Option 1: Direct Use
Visit the GitHub Pages application:

**[https://3ddiceroller.github.io](https://3ddiceroller.github.io)**

### Option 2: Clone Repository
```bash
git clone https://github.com/3ddiceroller/3ddiceroller.github.io.git
cd 3ddiceroller.github.io
```

Open `index.html` in a modern browser. No installation or build step is required.

### Option 3: Download
1. Open the [repository](https://github.com/3ddiceroller/3ddiceroller.github.io).
2. Select **Code → Download ZIP**.
3. Extract the archive.
4. Open `index.html`.

## 📁 Project Structure

```text
3ddiceroller.github.io/
├── index.html      # Complete application: HTML, CSS, and JavaScript
└── README.md       # Documentation
```

Optional repository additions:
- `preview.png` — Screenshot for this README
- `LICENSE` — Project license and distribution terms

## 🎮 Usage

### Choose the Number of Dice
Use the **− / +** buttons or the slider to select between **1 and 8 dice**.

Changing the count updates the displayed dice without recording a new roll.

### Roll the Dice
Click **Кинути кубики / Roll the dice**, or press **Space** when focus is outside an interactive control.

After the animation finishes:
- Each die displays its result
- The total updates
- The roll is added to history
- The application saves its state

Dice-count controls are temporarily disabled during a roll.

### Switch Language
Use the compact switcher in the top-right corner:
- **УК** — Ukrainian
- **EN** — English

Your selection is remembered for your next visit.

### Toggle Sound
Enable **Звук кубиків / Dice sounds** to hear dice impacts.

Sound is generated through the Web Audio API; no audio files are downloaded.

### Review or Clear History
The history panel shows the latest **8 rolls**, newest first.

Click **Очистити / Clear** to remove history. This does not reset your settings or current dice values.

### Change Layout
No manual layout switch is necessary. The interface adapts automatically to the available screen width, height, and orientation.

## 📊 Technical Details

### Technologies Used
- **HTML5** — Semantic application structure
- **CSS3** — 3D transforms, gradients, Grid, Flexbox, and responsive layouts
- **Vanilla JavaScript** — Application logic without frameworks
- **Web Animations API** — Dice rotation and bounce sequences
- **Web Audio API** — Synthesized impact sounds
- **Web Crypto API** — Random dice values when available
- **LocalStorage API** — Persistent settings and history

### Randomness
Dice results use `crypto.getRandomValues()` when available. Rejection sampling avoids modulo bias when converting random integers into values from **1 to 6**.

If Web Crypto is unavailable, the application falls back to `Math.random()`.

The rolling animation visualizes the selected results; it is not a physical dice simulation.

### Storage
Application state is stored under:

```text
dice-studio-v1
```

Saved values are validated before use. Settings and history stay in the browser; the application does not send them to a backend.

### Performance
- No external libraries, fonts, images, or audio files are required
- No build tooling or package installation
- Transform-based rolling animations
- History is limited to 8 entries
- Reduced-motion mode skips the rolling animation

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add amazing feature"
   ```
4. Push the branch:
   ```bash
   git push origin feature/amazing-feature
   ```
5. Open a Pull Request.

Before submitting, check:
- Ukrainian and English interfaces
- Dice counts from 1 through 8
- Desktop, mobile portrait, and landscape layouts
- Keyboard navigation and reduced-motion behavior
- State restoration after refreshing the page

## 🐛 Known Issues & Limitations

- Older browsers may not fully support CSS 3D transforms or the Web Animations API.
- Sound depends on browser Web Audio support and autoplay restrictions.
- Storage may be unavailable in restricted browsing environments.
- Persistence for pages opened through `file://` varies by browser; use a local server if needed.
- Very short windows and enlarged browser zoom may require page scrolling to keep controls accessible.
- Multiple 3D dice animations may be less smooth on low-end devices.

Found a problem? [Open an issue](https://github.com/3ddiceroller/3ddiceroller.github.io/issues).

## 📄 License

MIT

## 🙏 Acknowledgments

- Built with native web platform APIs
- Inspired by tabletop games and physical dice
- Designed with Ukrainian-first localization and accessible interaction in mind

---

<p align="center">
  Made with ❤️ for board games, big decisions, and little adventures
</p>

<p align="center">
  <a href="https://github.com/3ddiceroller/3ddiceroller.github.io/stargazers">⭐ Star this repo</a> •
  <a href="https://github.com/3ddiceroller/3ddiceroller.github.io/issues">🐛 Report Bug</a> •
  <a href="https://github.com/3ddiceroller/3ddiceroller.github.io/issues">💡 Request Feature</a>
</p>
