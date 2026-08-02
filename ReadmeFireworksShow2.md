# 🎆 Fireworks Show

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://fireworksshowj.github.io)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

An interactive canvas-based fireworks simulation with stunning particle effects, 10 explosion patterns, immersive sound design, and fully customizable settings. Optimized for smooth performance on 120Hz displays. Click anywhere to launch beautiful fireworks into the night sky!

<p align="center">
  <a href="https://fireworksshowj.github.io">
    <img src="https://img.shields.io/badge/🚀%20Live%20Demo-Click%20Here-ff6b6b?style=for-the-badge" alt="Live Demo">
  </a>
</p>

---

## ✨ Features

### 🎨 Visual Effects
- **Realistic Physics** - Particles with gravity, friction, and velocity simulation
- **Frame-Rate Independent Motion** - Delta-time physics ensures identical speed on 60Hz, 120Hz, or any refresh rate
- **Glowing Particles** - Beautiful additive-blend glow effects with shadow blur
- **Silky Particle Trails** - Dynamic multi-point trails following each particle
- **Radial Screen Flash** - Soft, atmospheric bloom centered on each explosion
- **City Skyline** - Atmospheric silhouette with illuminated windows
- **Starry Background** - 160 organically twinkling stars with randomized pulse timing

### 💥 Explosion Patterns
| Pattern | Description |
|---------|-------------|
| 🔵 **Circle** | Classic spherical explosion |
| ❤️ **Heart** | Romantic heart-shaped burst |
| ⭐ **Star** | Five-pointed star pattern |
| 💍 **Ring** | Double concentric rings |
| 🎯 **Double** | Two-color layered explosion |
| 🌿 **Willow** | Drooping, long-hanging cascade |
| 🌸 **Chrysanthemum** | Multi-layered spherical bloom |
| 🌴 **Palm** | Rising fronds like a palm tree |
| 🌀 **Spiral** | Rotating spiral trajectory |
| 🎲 **Random** | Randomly selected pattern each launch |

### 🎨 Color Schemes
- 🌈 Rainbow (default)
- 🔴 Red
- 🔵 Blue
- 🟢 Green
- 🟡 Gold
- 🟣 Purple
- 🩷 Pastel
- 🔥 Fire
- ❄️ Ice
- ⚪ White

### 🔊 Audio & Effects
- **Launch Whistle** - Procedurally generated rising tone (Web Audio API)
- **Explosion Boom** - Filtered noise burst for each detonation
- **Screen Flash** - Toggleable radial light bloom
- **Glitter Trails** - Optional sparkling secondary particles

### 💾 Persistent State
- All settings preserved in localStorage
- Debounced saving for smooth slider interaction
- Settings restored automatically on return

### ⚡ Performance
- **120Hz optimized** with clamped delta-time stepping
- **Opaque canvas context** for faster compositing
- **Swap-remove** particle management (zero-allocation cleanup)
- **Auto-pause** rendering when the browser tab is hidden

---

## 🎮 Controls

### Mouse
| Action | Result |
|--------|--------|
| **Click anywhere** | Launch firework at cursor position |

### Buttons
| Button | Function |
|--------|----------|
| 🚀 **Launch** | Fire a single random firework |
| 🔄 **Auto Mode** | Toggle continuous firework show |
| 💥 **Multi Shot** | Launch 3-6 fireworks burst |
| 🎇 **Finale** | Trigger an intense grand finale sequence |
| ⚙️ **Settings** | Open/close the settings popup |
| 🗑️ **Clear** | Clear all particles from screen |

### Keyboard Shortcuts
| Key | Action |
|-----|--------|
| `Space` | Launch single firework |
| `M` | Multi-shot burst |
| `A` | Toggle auto mode |
| `F` | Launch grand finale |
| `Esc` | Close settings popup |

---

## ⚙️ Customization Options

| Setting | Range | Description |
|---------|-------|-------------|
| **Particle Count** | 30 - 300 | Number of particles per explosion |
| **Explosion Size** | 0.5x - 2.5x | Scale of the explosion |
| **Trail Length** | 0.03 - 0.5 | Persistence of particle trails |
| **Auto Speed** | 200ms - 3000ms | Interval between auto launches |
| **Gravity** | 0.01 - 0.15 | Particle fall speed |
| **Glitter Trails** | On / Off | Sparkling secondary particles |
| **Screen Flash** | On / Off | Radial light bloom on explosion |
| **Sound FX** | On / Off | Launch & explosion audio |

---

## 🚀 Quick Start

### Option 1: Visit Live Demo
Simply go to **[https://fireworksshowj.github.io](https://fireworksshowj.github.io)**

### Option 2: Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/fireworksshowj/fireworksshowj.github.io.git
   ```

2. **Navigate to directory**
   ```bash
   cd fireworksshowj.github.io
   ```

3. **Open in browser**
   ```bash
   # Simply open index.html in your preferred browser
   open index.html        # macOS
   start index.html       # Windows
   xdg-open index.html    # Linux
   ```

> **Note:** Sound effects require a user interaction (click or key press) to initialize due to browser autoplay policies.

---

## 📁 Project Structure

```
fireworksshowj.github.io/
│
├── index.html          # Main application (all-in-one HTML/CSS/JS)
├── README.md           # Documentation
├── LICENSE             # MIT License
└── .gitignore          # Git ignore file
```

---

## 🛠️ Technologies

| Technology | Purpose |
|------------|---------|
| **HTML5 Canvas** | Rendering fireworks and particles |
| **CSS3** | Styling, animations, glassmorphism effects |
| **Vanilla JavaScript** | Game logic, physics, state management |
| **Web Audio API** | Procedural launch and explosion sound effects |
| **localStorage API** | Persistent settings |
| **SVG** | City skyline silhouette |

---

## 📊 Browser Support

| Browser | Support |
|---------|---------|
| Chrome | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| Edge | ✅ Full |
| Opera | ✅ Full |
| IE11 | ❌ Not supported |

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork the repository**
   ```bash
   git fork https://github.com/fireworksshowj/fireworksshowj.github.io.git
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```

3. **Commit your changes**
   ```bash
   git commit -m "Add amazing feature"
   ```

4. **Push to the branch**
   ```bash
   git push origin feature/amazing-feature
   ```

5. **Open a Pull Request**

### Ideas for Contributions
- [ ] Text/message-shaped explosions
- [ ] Custom drawable shape patterns
- [ ] More color gradients & themes
- [ ] Mobile touch gestures (pinch, swipe)
- [ ] Firework presets/themes
- [ ] Screenshot/GIF recording feature
- [ ] Background music integration
- [ ] Multi-language support
- [ ] Synchronized "show" scripting

---

## 📝 Changelog

### v2.0
- ⚡ **120Hz optimization** with frame-rate-independent delta-time physics
- 🔊 Added procedural **sound effects** (Web Audio API)
- 🎇 New **Finale** mode for grand sequences
- 🌿 Added **Willow, Chrysanthemum, Palm & Spiral** patterns (now 10 total)
- 🩷 Added **Pastel, Fire & Ice** color schemes (now 10 total)
- 🪟 Redesigned **settings popup** — centered, topmost modal with backdrop blur
- 💫 Softer **radial screen flash** and silkier trails
- 🚀 Performance: opaque canvas, swap-remove cleanup, debounced saves, tab-hidden auto-pause
- 🧹 Removed statistics panel and moon for a cleaner scene

### v1.0
- ✨ Initial release
- 🎆 6 explosion patterns
- 🎨 7 color schemes
- ⚙️ Customizable physics settings
- 💾 LocalStorage state persistence
- 🏙️ City skyline background
- ⭐ Animated star field
- 📱 Responsive design

---

## 📜 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Inspired by real fireworks displays
- Built with modern web technologies
- Thanks to the open-source community

---

## 📧 Contact

- **Repository**: [github.com/fireworksshowj/fireworksshowj.github.io](https://github.com/fireworksshowj/fireworksshowj.github.io)
- **Live Demo**: [fireworksshowj.github.io](https://fireworksshowj.github.io)
- **Issues**: [Report a bug](https://github.com/fireworksshowj/fireworksshowj.github.io/issues)

---

<p align="center">
  Made with ❤️ and ✨
  <br><br>
  <a href="https://fireworksshowj.github.io">
    <img src="https://img.shields.io/badge/🎆%20Launch%20Fireworks-NOW-ff6b6b?style=for-the-badge" alt="Launch">
  </a>
</p>

---

⭐ **Star this repo if you enjoyed the show!** ⭐
