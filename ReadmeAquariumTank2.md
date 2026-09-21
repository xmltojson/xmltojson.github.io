# 🐠 Aquarium Tank

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/demo-live-brightgreen)](https://aquariumtank.github.io)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](#-tech-stack)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](#-tech-stack)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](#-tech-stack)

**A small world. A little peace.**

A relaxing, interactive virtual aquarium built with pure HTML, CSS, and JavaScript. Watch fish explore a planted underwater landscape, feed them, and shape your own aquascape.

Everything in the aquarium is drawn procedurally using HTML5 Canvas—no external libraries, image assets, or build tools required.

## 🌐 Live Demo

**[Open Aquarium Tank](https://aquariumtank.github.io/)**

---

## ✨ Features

### 🐟 Fish

- Five selectable species:
  - Neon tetra
  - Angelfish
  - Golden gourami
  - Silver barb
  - Clownfish
- Species-specific colors, markings, fins, and swimming speeds
- Animated tails, fins, and smooth changes of direction
- Depth-based scaling and shading
- Gentle schooling and separation behavior
- Fish seek out and eat nearby food
- Click a fish to see its name, species, time in the aquarium, and bites eaten
- Up to **40 fish** per aquarium

### 🌿 Plants & Coral

- Six planting options:
  - Ribbon grass
  - Amazon sword
  - Stem plant
  - Red ludwigia
  - Sea fan
  - Anemone
- Swaying vegetation influenced by the water-current setting
- Foreground and background planting for visual depth
- Optional foreground grass
- Up to **55 plants and coral additions**

### 🪨 Hardscape

- Natural river stones with textured surfaces
- Weathered driftwood
- Optional stone shelter
- Toggleable moss on rocks
- Four substrate styles:
  - Natural river sand
  - Pale limestone
  - Dark aquasoil
  - River gravel

### 💨 Bubbles & Feeding

- Add up to **8 air stones**
- Rising bubbles with varied sizes and gentle wobble
- Surface ripples from feeding and some surfacing bubbles
- Drop food using the toolbar or by clicking the water
- Fish accelerate toward nearby food
- Feeding limit prevents excessive food accumulation

### 🎨 Lighting & Environment

- Three water palettes:
  - Emerald shallows
  - Blue lagoon
  - Forest stream
- Switch between daylight and moonlight
- Adjustable light intensity and water current
- Optional sunbeams and shimmering substrate caustics
- Animated water surface and floating particles
- Glass reflections, shadows, and edge shading

### 🖥️ Interface & Performance

- Responsive layout designed for desktop at **100% browser zoom**
- Mobile-friendly controls
- Fullscreen aquarium mode where supported
- Pause and resume controls
- High-detail and battery-friendly rendering modes
- Animation pauses while the browser tab is hidden
- Starts paused when the device requests reduced motion
- Keyboard controls and labeled interface elements

### 💾 Local Persistence

- Saves fish, plants, air stones, environment settings, and feeding statistics
- Saves shortly after changes and every **30 seconds** while the aquarium is active
- Attempts to save when the tab is hidden or the page is left
- Restores saved aquarium data on reload
- Falls back to session-only use when browser storage is unavailable
- One-click restoration of the original aquascape

> Active food particles, bubbles, ripples, and pause state are not persisted. Saves are local to the current browser and site; there is no cloud synchronization.

---

## 🚀 Getting Started

1. Download the project.
2. Extract the files.
3. Open `index.html` in a modern browser.

No installation, server, or dependencies are required.

> Storage availability for directly opened `file://` pages varies by browser.

---

## 🎮 Controls

### Main Toolbar

| Control | Action |
|---------|--------|
| **Species selector** | Choose the species for the next fish |
| **+ Add fish** | Add a fish of the selected species |
| **Feed** | Drop food at a random horizontal position |
| **Bubbles +** | Add an air stone |
| **Plant +** | Add a random ribbon, broad-leaf, stem, or red plant |
| **Moonlight** | Toggle night lighting |
| **Pause / Play** | Pause or resume the simulation |
| **Fullscreen** | Expand the aquarium where supported |
| **Settings** | Open environment, planting, and hardscape controls |

### Aquarium Interactions

- **Click a fish** → Open its information card.
- **Click the water** → Drop food from the surface at that horizontal position.
- **Press `Space` while the aquarium canvas is focused** → Pause or resume.
- **Press `F` while the aquarium canvas is focused** → Feed at the center.

You can focus the aquarium canvas using `Tab`.

> Food can be added while paused. Resume the aquarium to watch it sink and the fish respond.

### Settings

Use **Settings** to:

- Change the water palette and substrate.
- Adjust lighting and water current.
- Select rendering quality.
- Add a specific plant or coral type.
- Toggle stones, driftwood, shelter, grass, moss, and lighting effects.
- Clear fish, plants, or air stones.
- Reset to the original aquascape.

Clearing fish, clearing plants, and resetting the aquarium require confirmation. Foreground grass is controlled separately from added plants.

### Statistics

The panel beneath the tank displays:

- Total fish
- Total plants and coral additions
- Total air stones
- Total feeding actions
- Local save status

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| **HTML5** | Application structure, controls, and settings dialog |
| **HTML5 Canvas 2D** | Procedural aquarium rendering |
| **CSS3** | Responsive layout, interface styling, and glass overlays |
| **Vanilla JavaScript** | Animation, fish behavior, feeding, and interactions |
| **Local Storage** | Browser-local aquarium persistence |
| **requestAnimationFrame** | Animation scheduling |
| **ResizeObserver** | Canvas resizing |
| **Fullscreen API** | Optional fullscreen viewing |

### Rendering Approach

- Backgrounds and hardscape are cached in offscreen canvases.
- Fish sprites are generated once per species and reused.
- Plants, fins, bubbles, particles, and lighting effects animate independently.
- Canvas resolution adapts to device pixel ratio and rendering quality.
- Scene scale responds to both tank width and height.

### Browser Support

Designed for current versions of Chrome, Firefox, Safari, Edge, and other modern browsers with Canvas 2D support.

Fullscreen availability and local-storage behavior depend on the browser, device, and hosting context.

---

## 📁 Project Structure

```text
aqariumtank.github.io/
├── index.html    # Complete application: HTML, CSS, and JavaScript
├── README.md     # Documentation
└── LICENSE       # MIT License
```

---

## 📝 Notes

- This is a **decorative simulation**, not an aquarium-care guide.
- Freshwater fish, marine fish, plants, and coral can coexist here for visual variety; this does not imply real-world compatibility.
- Fish age represents elapsed time since the fish was created, including time while the page was closed.
- The aquarium does not simulate swimming or feeding while the page is closed.
- Clearing browser storage removes the saved aquarium.
- The application itself requires no external assets. The badges in this README are hosted externally.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature/NewFeature
   ```

3. Commit your changes:

   ```bash
   git commit -m "Add NewFeature"
   ```

4. Push the branch:

   ```bash
   git push origin feature/NewFeature
   ```

5. Open a pull request.

### Contribution Ideas

- Additional fish species and plant varieties
- Optional ambient sound with mute controls
- Automatic day/night transitions
- Aquarium save import and export
- More hardscape options
- Improved keyboard access to individual fish
- Further performance optimizations for mobile devices

Please preserve the dependency-free design and test changes on desktop, mobile, and with reduced motion enabled.

---

## 📄 License

MIT License — see [LICENSE](LICENSE).

---

## 🔗 Links

- **Live demo:** [aquariumtank.github.io](https://aquariumtank.github.io)
- **Author ORCID:** [0009-0000-6151-7415](https://orcid.org/0009-0000-6151-7415)

---

<p align="center">A small world. A little peace. 🐟</p>
