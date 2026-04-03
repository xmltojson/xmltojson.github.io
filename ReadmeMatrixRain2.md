# Matrix Rain

**Free your mind and watch the code rain fall.**

A mesmerizing interactive Matrix digital rain simulation inspired by the iconic Matrix trilogy. Built with pure HTML, CSS, and JavaScript — no dependencies required.

**[▶ Live Demo](https://matrixrainj.github.io)**

## Features

### 🟢 Visual Effects
- Smooth cascading character rain at 120 FPS
- Dynamic glow effects on leading characters
- Adjustable trail length for fade control
- Rainbow mode with multi-color shifting streams
- Sub-pixel smooth animation

### 🎨 Customization
- **Color Themes** — Classic Green, Cyan, Magenta, Yellow, Orange, Red, and custom color picker
- **Character Sets** — Katakana, Binary, Hexadecimal, Kanji, Symbols, and Custom Messages
- **Rain Speed** — Adjustable from slow drift to rapid downpour
- **Column Density** — Control the number of rain columns
- **Font Size** — Scale characters from 10px to 30px
- **Trail Length** — 5 levels from long ghostly trails to sharp short fades

### ⚙️ Controls
- Real-time settings panel with glassmorphism UI
- Pause / Resume animation
- Screenshot capture as PNG
- Reset to default settings
- Settings persist via LocalStorage

### ⌨️ Keyboard Shortcuts
| Key | Action |
|-------|----------------|
| `Space` | Pause / Resume |
| `H` | Toggle control panel |

## Getting Started

### Run Locally

1. Clone the repository:

```bash
git clone https://github.com/matrixrainj/matrixrainj.github.io.git
```

2. Open `index.html` in your browser.

No build tools, no dependencies, no setup required.

### Deploy

This project works as a static site. Deploy it to any static hosting:

- **GitHub Pages** — Push to `main` branch and enable Pages
- **Netlify / Vercel** — Connect the repository and deploy
- **Any web server** — Just serve the `index.html` file

## Project Structure

```
matrixrainj.github.io/
├── index.html      # Complete application (HTML + CSS + JS)
├── favicon.ico     # Site icon
├── LICENSE         # MIT License
└── README.md       # Documentation
```

## Technical Details

- **Rendering** — HTML5 Canvas with `alpha: false` optimization
- **Animation** — Fixed timestep at 120 FPS with accumulator-based physics
- **Movement** — Sub-pixel positioning for buttery smooth scrolling
- **Persistence** — All settings saved to LocalStorage automatically
- **Responsive** — Adapts to any screen size, mobile and desktop
- **Performance** — Delta time capping to prevent spiral of death
- **Zero Dependencies** — Pure vanilla HTML, CSS, and JavaScript

## License

MIT
