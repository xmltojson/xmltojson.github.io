# 🎆 Fireworks Show · Nightfall

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://fireworksshowj.github.io)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

An interactive canvas-based fireworks simulation above a moonlit city. Create your own show with glowing particles, water reflections, procedural sound effects, and customizable physics.

Choose from **9 explosion shapes plus Random mode**, **10 color palettes**, and **3 interface languages**. Built with vanilla JavaScript—no frameworks, dependencies, or build tools required.

<p align="center">
  <a href="https://fireworksshowj.github.io">
    <img src="https://img.shields.io/badge/🚀%20Live%20Demo-Click%20Here-ff6b6b?style=for-the-badge" alt="Live Demo">
  </a>
</p>

---

## ✨ Features

### 🎨 Visual Effects

- **Particle Physics** — Gravity, drag, and velocity-driven motion
- **Delta-Time Animation** — Time-based updates with clamped frame steps
- **Glowing Sparks** — Cached glow sprites and additive blending
- **Light Trails** — Adjustable persistence on a separate effects canvas
- **Ambient Lighting** — Optional soft illumination around explosions
- **Drifting Smoke** — Subtle expanding clouds after each burst
- **Moonlit Skyline** — Layered buildings, illuminated windows, stars, and atmospheric haze
- **Water Reflections** — Rippling, horizontally displaced reflections of the fireworks

### 💥 Explosion Patterns

| Pattern | Description |
|---------|-------------|
| 🔵 **Sphere** | Classic burst using a projected spherical shell |
| ❤️ **Heart** | Heart-shaped outline |
| ⭐ **Star** | Five-pointed star outline |
| 💍 **Ring** | Single elliptical ring |
| 🎯 **Double Ring** | Two concentric rings with independently selected colors |
| 🌿 **Willow** | Long-lasting sparks that fall in graceful arcs |
| 🌸 **Chrysanthemum** | Layered radial spokes |
| 🌴 **Palm** | Upward-spreading fronds |
| 🌀 **Spiral** | Sparks arranged along a spiral |
| 🎲 **Random** | Selects a shape for each rocket |

### 🌈 Color Palettes

Rainbow · Red · Blue · Green · Gold · Purple · Pastel · Fire · Ice · White

### 🔊 Audio & Effects

- **Procedural Launch Sound** — Rising filtered-noise effect
- **Explosion Boom** — Low-pass noise burst with a fading envelope
- **Volume Control** — Adjustable master volume
- **Glitter Sparks** — Optional brightness modulation on selected particles
- **No Audio Downloads** — Sounds are generated locally with the Web Audio API

> Sound is off by default and must be enabled manually. It is also reset to off when the page reloads.

### 🌍 Languages & Accessibility

- **German** — Default interface language
- **Ukrainian**
- **English**
- Keyboard shortcuts and visible focus indicators
- Accessible labels and live status announcements
- Tabbed settings dialog with keyboard navigation
- Manual pause and resume controls
- Reduced-motion preference detection
- Optional **Less motion and light** mode

Reduced-motion mode disables automatic shows, volleys, finales, smoke, and ambient flashes while reducing particle count, burst size, and lifetime. Manual launches remain available.

### 📱 Responsive Design

- Desktop, tablet, and mobile layouts
- Touch-to-launch interaction
- Compact controls for small screens
- Landscape layouts for shorter displays
- Safe-area support for notched devices
- Fullscreen controls where supported

### 💾 Persistent Settings

- Saves settings and language in `localStorage`
- Restores validated values on return
- Provides a reset-to-defaults button
- Continues working if browser storage is unavailable

Sound always starts disabled. A system reduced-motion preference is respected on load.

### ⚡ Performance

- `requestAnimationFrame` animation loop
- Adaptive particle density based on observed frame timing
- Device-aware particle and rocket limits
- Particle pooling and swap-remove cleanup
- Cached glow sprites and environment layers
- Capped canvas pixel ratio
- Opaque main canvas
- Rendering pauses while the tab is hidden or settings are open

Actual frame rate depends on device capabilities, display resolution, and show intensity.

---

## 🎮 Controls

### Mouse & Touch

| Action | Result |
|--------|--------|
| **Click or tap the sky** | Launch a rocket toward that position |

Launch targets are constrained to the visible sky.

### Buttons

| Button | Function |
|--------|----------|
| ↗ **Launch** | Launch one rocket toward a random sky position |
| ⟳ **Auto** | Toggle continuous launches |
| ✧ **Volley** | Schedule five rockets in quick succession |
| ✺ **Finale** | Schedule a rapid sequence of 40 launches |
| ⚙ **Settings** | Open the settings dialog |
| × **Clear** | Remove active effects and cancel automatic or queued launches |
| Ⅱ / ▶ **Pause / Resume** | Pause or resume the show |
| ⛶ **Full screen** | Enter or exit fullscreen where available |
| **Language selector** | Switch between German, Ukrainian, and English |

Rocket and particle limits may reduce the number of effects visible during intense sequences.

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Launch one rocket |
| `A` | Toggle automatic launches |
| `M` | Launch a volley |
| `F` | Start the finale |
| `P` | Pause or resume |
| `C` | Clear the show |
| `Esc` | Close settings |

Within the settings tabs, use `←`, `→`, `Home`, and `End` to navigate.

Show shortcuts are inactive while settings are open or focus is on an interactive form control.

---

## ⚙️ Customization Options

### Physics

| Setting | Range | Default | Description |
|---------|-------|---------|-------------|
| **Sparks** | 40–300 | 150 | Requested particles per explosion; adapts to performance |
| **Burst size** | 0.5×–2.5× | 1× | Initial burst velocity scale |
| **Light trails** | 0.1–1 | 0.5 | Persistence of the light layer |
| **Launch interval** | 300–3000 ms | 1200 ms | Time between automatic launches |
| **Gravity** | 15–100 | 45 | Particle gravity strength |

### Appearance

| Setting | Options | Default |
|---------|---------|---------|
| **Color palette** | 10 palettes | Multicolor |
| **Burst pattern** | 9 shapes + Random | Random |
| **Glitter sparks** | On / Off | On |
| **Soft ambient light** | On / Off | On* |
| **Smoke** | On / Off | On* |
| **Water reflections** | On / Off | On |

### General

| Setting | Options | Default |
|---------|---------|---------|
| **Sound effects** | On / Off | Off |
| **Volume** | 0–100% | 35% |
| **Less motion and light** | On / Off | Follows system preference on first use |
| **Reset settings** | Button | Restores defaults |

\* Ambient lighting is disabled and smoke is not rendered in reduced-motion mode.

---

## 🚀 Quick Start

### Option 1: Visit the Live Demo

Open **[https://fireworksshowj.github.io](https://fireworksshowj.github.io)**.

### Option 2: Run Locally

1. **Clone the repository**

   ```bash
   git clone https://github.com/fireworksshowj/fireworksshowj.github.io.git
   ```

2. **Navigate to the project**

   ```bash
   cd fireworksshowj.github.io
   ```

3. **Open `index.html` in your browser**

   ```bash
   open index.html        # macOS
   start index.html       # Windows Command Prompt
   xdg-open index.html    # Linux
   ```

No installation or build step is required.

> Audio requires explicit activation through the interface. Fullscreen availability depends on the browser and device.

---

## 📁 Project Structure

```text
fireworksshowj.github.io/
├── index.html          # Complete application: HTML, CSS, and JavaScript
├── favicon.ico         # Browser icon referenced by index.html
├── README.md           # Project documentation
└── LICENSE             # MIT License
```

The application generates its scenery, particle effects, and audio locally. No external JavaScript libraries, fonts, or audio files are required.

---

## 🛠️ Technologies

| Technology | Purpose |
|------------|---------|
| **HTML5 Canvas 2D** | Fireworks, skyline, moon, stars, smoke, and reflections |
| **CSS3** | Responsive layouts, glass-style controls, and visual states |
| **Vanilla JavaScript** | Physics, scheduling, localization, and interface logic |
| **Web Audio API** | Procedural launch and explosion sounds |
| **localStorage** | Persistent settings and language |
| **HTML `<dialog>`** | Modal settings interface |
| **ResizeObserver** | Canvas resizing when the app dimensions change |
| **Fullscreen API** | Optional fullscreen presentation |
| **Page Visibility API** | Background-tab rendering suspension |
| **`prefers-reduced-motion`** | System motion-preference detection |

---

## 📊 Browser Support

Designed for current versions of:

- Chrome
- Edge
- Firefox
- Safari
- Opera

A modern browser with Canvas 2D, native `<dialog>`, and `ResizeObserver` support is required.

- Fullscreen behavior varies across browsers, especially on mobile.
- Audio requires Web Audio API support and user activation.
- Older browsers may not display backdrop blur.
- Internet Explorer 11 is not supported.

---

## 🤝 Contributing

Contributions are welcome!

1. **Fork the repository** using GitHub’s **Fork** button.

2. **Clone your fork**

   ```bash
   git clone https://github.com/YOUR-USERNAME/fireworksshowj.github.io.git
   cd fireworksshowj.github.io
   ```

3. **Create a feature branch**

   ```bash
   git checkout -b feature/amazing-feature
   ```

4. **Commit your changes**

   ```bash
   git add .
   git commit -m "Add amazing feature"
   ```

5. **Push your branch**

   ```bash
   git push origin feature/amazing-feature
   ```

6. **Open a pull request** against the original repository.

### Before Submitting

Please check:

- Desktop and mobile layouts
- Portrait and landscape orientations
- All three interface languages
- Keyboard navigation and focus visibility
- Reduced-motion behavior
- Pause, clear, and hidden-tab handling
- Sound activation and settings persistence

### Ideas for Contributions

- [ ] Text-shaped explosions
- [ ] Custom drawable burst patterns
- [ ] Additional color palettes
- [ ] Firework presets and themed shows
- [ ] Screenshot or video export
- [ ] Additional interface languages
- [ ] Synchronized show scripting
- [ ] Automated accessibility and browser tests

---

## 📜 License

Licensed under the [MIT License](LICENSE).

---

## 🙏 Acknowledgments

- Inspired by real fireworks displays and nighttime waterfronts
- Built with open web technologies
- Thanks to the open-source community

---

## 📧 Contact

- **Repository:** [github.com/fireworksshowj/fireworksshowj.github.io](https://github.com/fireworksshowj/fireworksshowj.github.io)
- **Live Demo:** [fireworksshowj.github.io](https://fireworksshowj.github.io)
- **Issues:** [Report a bug or request a feature](https://github.com/fireworksshowj/fireworksshowj.github.io/issues)

---

<p align="center">
  Made with ❤️ and ✨
  <br><br>
  <a href="https://fireworksshowj.github.io">
    <img src="https://img.shields.io/badge/🎆%20Launch%20Fireworks-NOW-ff6b6b?style=for-the-badge" alt="Launch Fireworks">
  </a>
</p>

⭐ **Star this repository if you enjoyed the show!**
