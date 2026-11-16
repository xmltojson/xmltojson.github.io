# 🌟 Starry Night Sky

An interactive night sky experience with twinkling stars, shooting stars, discoverable constellations, and atmospheric effects. Create your own celestial scene with a responsive observatory interface available in **German, Ukrainian, and English**.

![HTML5](https://img.shields.io/badge/HTML5-Canvas-orange.svg)
![Languages](https://img.shields.io/badge/languages-DE%20%7C%20UK%20%7C%20EN-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)

> An artistic sky for exploration and relaxation—not a live astronomical star map.

## ✨ Features

### Visual Elements
- **Twinkling Stars** — Canvas-rendered stars with varied sizes, colors, and subtle glow
- **Adjustable Star Density** — Display between 50 and 800 background stars
- **Shooting Stars** — Random meteors with luminous trails
- **Interactive Constellations** — Discover six familiar celestial patterns:
  - Ursa Major (The Great Bear, containing the Big Dipper)
  - Cassiopeia (The Queen)
  - Orion (The Hunter)
  - Leo (The Lion)
  - Cygnus (The Swan)
  - Scorpius (The Scorpion)
- **Moonlight** — An illuminated moon with crater details
- **Northern Lights** — Animated aurora effects
- **Atmospheric Scenery** — Soft celestial gradients and layered mountain silhouettes

### Interactive Controls
- Toggle background stars, automatic meteors, constellations, moonlight, and aurora
- Adjust star density with a slider
- Send a shooting star with **Make a wish**
- Pause or resume sky animations
- Enter fullscreen where supported
- Reset sky settings while keeping the selected language

### 🌐 Languages
Switch instantly using the **DE | UK | EN** control:

| Switch | Language |
|--------|----------|
| **DE** | Deutsch — German, default |
| **UK** | Українська — Ukrainian |
| **EN** | English |

- Translated interface, constellation descriptions, tooltips, and notifications
- Localized accessibility labels, page title, and metadata
- Language selection remembered across visits
- Switching languages preserves the current sky, selected constellation, and statistics

### State Persistence
- Sky visibility settings, star density, and language saved to `localStorage`
- Saved preferences restored after refresh
- Session-only operation when browser storage is unavailable
- Meteor counts tracked **for the current session**, not across page reloads

### Responsive Design & Accessibility
- Viewport-fitting desktop layout that avoids vertical scrolling at typical desktop sizes
- Three-column arrangement for short desktop windows
- Naturally scrolling tablet and mobile layouts
- Touch-friendly controls and visible keyboard focus indicators
- Keyboard-operable constellation and language controls
- Support for the system’s reduced-motion preference
- Animation suspended while the browser tab is hidden

## 🚀 Demo

Visit the live demo: [https://starrynightskyj.github.io](https://starrynightskyj.github.io)

## 📦 Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/starrynightskyj/starrynightskyj.github.io.git
   ```

2. Navigate to the project directory:

   ```bash
   cd starrynightskyj.github.io
   ```

3. Open `index.html` in your preferred web browser.

No package installation, build step, or backend is required.

### Optional: Run a Local Server

For a consistent local origin and browser storage behavior:

```bash
python -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000).

## 🎮 Usage

### Controls

The names below use the English interface. German is selected by default on the first visit.

| Control | Function |
|---------|----------|
| **DE \| UK \| EN** | Switch the interface language |
| ⭐ Starlight | Toggle background stars |
| ☄️ Shooting stars | Toggle automatically generated meteors |
| 🌟 Constellations | Toggle constellation patterns |
| 🌙 Moonlight | Toggle the moon |
| 🌌 Northern lights | Toggle the aurora |
| Star density | Set the background star count from 50 to 800 |
| ☄️ Make a wish | Send a shooting star manually |
| ⏸️ / ▶️ Pause / Resume | Pause or resume animation |
| ⛶ Fullscreen | Enter or exit fullscreen, where supported |
| 🔄 Reset | Restore default sky settings and clear the meteor count |

### Interactions
- **Select a constellation** to highlight its pattern and read its story.
- **Use the six navigation markers** in the information card to select a constellation. This also enables constellation visibility if it was off.
- **Click an empty area of the sky**, press **Escape**, or use the information card’s close button to clear the selection.
- **Make a wish** sends a meteor even when automatic shooting stars are disabled.
- **Settings save automatically** when browser storage is available.

### Keyboard Navigation
- Use **Tab** to move between controls.
- Use **Enter** or **Space** to activate buttons.
- With a language button focused, use **Left/Right Arrow**, **Home**, or **End** to select a language.
- Use the focused density slider’s arrow keys to adjust the star count.
- Press **Escape** to clear a constellation selection.

### Motion Preferences
When the operating system requests reduced motion:
- The sky is rendered without continuous animation.
- Aurora movement is disabled.
- Animation and manual meteor controls are disabled.

Manually pausing animation also disables **Make a wish** until animation resumes.

### Default Settings

| Setting | Default |
|---------|---------|
| Language | German (`de`), unless a saved choice exists |
| Background stars | On |
| Star density | 350 |
| Automatic shooting stars | On |
| Constellations | On |
| Moonlight | Off |
| Northern lights | Off |
| Animation | Running, unless reduced motion is requested |

**Reset** restores the sky defaults, clears the current selection and meteor count, and preserves the chosen language.

## 📁 Project Structure

```text
starrynightskyj.github.io/
│
├── index.html      # Complete application: HTML, CSS, JavaScript, translations
├── favicon.ico     # Browser icon referenced by index.html
└── README.md       # Project documentation
```

The application uses inline SVG icons and has no external runtime libraries or font dependencies.

## 🛠️ Technologies Used

- **HTML5** — Semantic interface and Canvas
- **CSS3** — Grid, Flexbox, gradients, animations, and responsive layouts
- **Vanilla JavaScript (ES6+)** — Rendering, interactions, and localization
- **Canvas 2D API** — Background stars and meteor trails
- **`requestAnimationFrame`** — Animation timing
- **`localStorage` API** — Preference persistence
- **`Intl.NumberFormat`** — Localized number formatting
- **Fullscreen API** — Optional fullscreen viewing
- **Page Visibility API** — Background-tab animation suspension
- **ResizeObserver** — Canvas resizing
- **`prefers-reduced-motion`** — Motion accessibility

### Storage Keys

| Key | Contents |
|-----|----------|
| `starryNightState` | Layer visibility settings and star density |
| `starryNightLanguage` | Selected language: `de`, `uk`, or `en` |

Preferences stay in the browser; no backend is required to store them.

## 📊 Statistics Tracked

- **Background stars** — Current enabled background star count; constellation stars are counted separately
- **Meteors seen** — Automatically generated and manually triggered meteors during the current session
- **Constellations** — Six when enabled, zero when hidden

The meteor counter resets on page reload or when **Reset** is selected.

## 📱 Responsive Breakpoints

| Breakpoint | Description |
|------------|-------------|
| Width > 900px | Viewport-sized desktop layout with a sky area and stacked side panels |
| Width ≥ 1600px | Larger spacing and wider side panels |
| Width ≤ 1200px | Compact sky controls and simplified decorative labels |
| Width > 900px, height ≤ 760px | Reduced desktop spacing |
| Width > 900px, height ≤ 660px | Three-column layout with separate settings and information panels |
| Width ≤ 900px | Naturally scrolling layout with the sky above the side panels |
| Width ≤ 600px | Single-column mobile layout and a dedicated controls row |
| Width > 900px, height ≤ 420px | Scrolling fallback to keep controls accessible |

## 🔗 Links

- **Repository:** [https://github.com/starrynightskyj/starrynightskyj.github.io](https://github.com/starrynightskyj/starrynightskyj.github.io)
- **Live Demo:** [https://starrynightskyj.github.io](https://starrynightskyj.github.io)

## 📄 License

MIT

---

<div align="center">

🌌 *Look up and make a wish upon a shooting star.* ✨

**DE:** Wünsch dir etwas. · **UK:** Загадай бажання. · **EN:** Make a wish.

⭐ **Star this repo if you enjoyed the night sky!** ⭐

</div>
