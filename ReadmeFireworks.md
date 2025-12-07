# 🎆 Fireworks Show

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://fireworksshow.github.io)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

An interactive canvas-based fireworks simulation with stunning particle effects, multiple explosion patterns, and fully customizable settings. Click anywhere to launch beautiful fireworks into the night sky!

<p align="center">
  <a href="https://fireworksshow.github.io">
    <img src="https://img.shields.io/badge/🚀%20Live%20Demo-Click%20Here-ff6b6b?style=for-the-badge" alt="Live Demo">
  </a>
</p>

---

## ✨ Features

### 🎨 Visual Effects
- **Realistic Physics** - Particles with gravity, friction, and velocity simulation
- **Glowing Particles** - Beautiful glow effects with shadow blur
- **Particle Trails** - Dynamic trails following each particle
- **City Skyline** - Atmospheric silhouette with illuminated windows
- **Starry Background** - Twinkling stars for immersive night sky

### 💥 Explosion Patterns
| Pattern | Description |
|---------|-------------|
| 🔵 **Circle** | Classic spherical explosion |
| ❤️ **Heart** | Romantic heart-shaped burst |
| ⭐ **Star** | Five-pointed star pattern |
| 💍 **Ring** | Double concentric rings |
| 🎯 **Double** | Two-color layered explosion |
| 🎲 **Random** | Randomly selected pattern |

### 🎨 Color Schemes
- 🌈 Rainbow (default)
- 🔴 Red
- 🔵 Blue
- 🟢 Green
- 🟡 Gold
- 🟣 Purple
- ⚪ White

### 💾 Persistent State
- Launch counter saved across sessions
- All settings preserved in localStorage
- Session time tracking

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
| ⚙️ **Settings** | Open/close settings panel |
| 🗑️ **Clear** | Clear all particles from screen |

### Keyboard Shortcuts
| Key | Action |
|-----|--------|
| `Space` | Launch single firework |
| `M` | Multi-shot burst |
| `A` | Toggle auto mode |

---

## ⚙️ Customization Options

| Setting | Range | Description |
|---------|-------|-------------|
| **Particle Count** | 30 - 200 | Number of particles per explosion |
| **Explosion Size** | 0.5x - 2.0x | Scale of the explosion |
| **Trail Length** | 0.05 - 0.5 | Length of particle trails |
| **Auto Speed** | 200ms - 3000ms | Interval between auto launches |
| **Gravity** | 0.01 - 0.15 | Particle fall speed |

---

## 🚀 Quick Start

### Option 1: Visit Live Demo
Simply go to **[https://fireworksshow.github.io](https://fireworksshow.github.io)**

### Option 2: Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/fireworksshow/fireworksshow.github.io.git
   ```

2. **Navigate to directory**
   ```bash
   cd fireworksshow.github.io
   ```

3. **Open in browser**
   ```bash
   # Simply open index.html in your preferred browser
   open index.html        # macOS
   start index.html       # Windows
   xdg-open index.html    # Linux
   ```

   Or use a local server:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Node.js (npx)
   npx serve
   
   # PHP
   php -S localhost:8000
   ```

---

## 📁 Project Structure

```
fireworksshow.github.io/
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
| **localStorage API** | Persistent settings and statistics |
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
   git fork https://github.com/fireworksshow/fireworksshow.github.io.git
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
- [ ] Add sound effects
- [ ] New explosion patterns (spiral, text, custom shapes)
- [ ] More color gradients
- [ ] Mobile touch gestures
- [ ] Firework presets/themes
- [ ] Screenshot/recording feature
- [ ] Background music integration
- [ ] Multi-language support

---

## 📝 Changelog

### v1.0.0 (2024)
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

```
MIT License

Copyright (c) 2024 Fireworks Show

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 Acknowledgments

- Inspired by real fireworks displays
- Built with modern web technologies
- Thanks to the open-source community

---

## 📧 Contact

- **Repository**: [github.com/fireworksshow/fireworksshow.github.io](https://github.com/fireworksshow/fireworksshow.github.io)
- **Live Demo**: [fireworksshow.github.io](https://fireworksshow.github.io)
- **Issues**: [Report a bug](https://github.com/fireworksshow/fireworksshow.github.io/issues)

---

<p align="center">
  Made with ❤️ and ✨
  <br><br>
  <a href="https://fireworksshow.github.io">
    <img src="https://img.shields.io/badge/🎆%20Launch%20Fireworks-NOW-ff6b6b?style=for-the-badge" alt="Launch">
  </a>
</p>

---

⭐ **Star this repo if you enjoyed the show!** ⭐
```

---

## 📄 LICENSE File

Create a separate `LICENSE` file:

```
MIT License

Copyright (c) 2024 Fireworks Show

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📄 .gitignore File

```gitignore
# OS generated files
.DS_Store
.DS_Store?
._*
.Spotlight-V100
.Trashes
ehthumbs.db
Thumbs.db

# IDE files
.idea/
.vscode/
*.swp
*.swo
*~

# Logs
*.log
npm-debug.log*

# Dependencies
node_modules/

# Build outputs
dist/
build/

# Environment files
.env
.env.local

# Temporary files
*.tmp
*.temp
```

---

## 📁 Final Repository Structure

```
fireworksshow.github.io/
├── index.html      # Main application
├── README.md       # Documentation  
├── LICENSE         # MIT License
└── .gitignore      # Git ignore rules
```

Your GitHub Pages site will automatically be live at **https://fireworksshow.github.io** once you push these files! 🎆
