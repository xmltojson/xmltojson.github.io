# Northlight — Aurora Borealis

A peaceful, interactive Northern Lights visualization above an imaginary Arctic landscape. Fine aurora curtains flow across a star-filled sky, illuminating snowy mountain ridges and reflecting in a quiet lake.

Built entirely with HTML, CSS, and vanilla JavaScript in a single file. No external images, libraries, or build tools required.

![Aurora Borealis](https://img.shields.io/badge/Aurora-Borealis-00ff88?style=for-the-badge&logo=github)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-Canvas-orange?style=for-the-badge)
![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-f7df1e?style=for-the-badge)

## 🌌 Live Demo

**[View Live Demo](https://auroraborealisj.github.io)**

## ✨ Features

### Aurora & Night Sky

- **Fine Aurora Curtains** — Hundreds of narrow light rays form layered, folding curtains with softly fading upper edges.
- **Subtle Bloom** — Restrained glow adds depth without overwhelming the night sky.
- **Eight Color Palettes** — Naturalistic greens alongside artistic violet, crimson, blue, and rose interpretations.
- **Twinkling Stars** — A seeded starfield with varied brightness, size, color, and subtle twinkle.
- **Occasional Meteors** — Brief shooting stars with fading trails, without interrupting the scene.

### Procedural Landscape

- **Snow-Covered Mountains** — Layered ridges with irregular snow lines, rock faces, and shadowed gullies.
- **Lake Reflections** — The rendered sky and mountains are mirrored in gently displaced water strips.
- **Foreground Details** — Pine silhouettes, shorelines, and low rocks frame the landscape.
- **Atmospheric Depth** — Horizon haze, faint diffuse starlight, and edge darkening create a more photographic appearance.
- **New Scene Discovery** — Generate a different landscape, aurora arrangement, and selected settings.

### Application

- **Customizable Settings** — Adjust movement, brightness, curtain layers, star density, and night exposure.
- **PNG Export** — Save the rendered scene without interface controls.
- **Pause & Fullscreen** — Stop on a favorite moment or enter fullscreen where supported.
- **Persistent Settings** — Preferences and the landscape seed are stored locally when browser storage is available.
- **Rendering Quality Options** — Automatic, High, and Low modes balance detail and rendering cost.
- **Responsive Interface** — Full-screen canvas with a scrollable settings panel.
- **Keyboard Accessibility** — Labeled controls, visible focus indicators, and focus containment in the settings dialog.
- **Reduced-Motion Support** — Animation starts paused when the system requests reduced motion.
- **Background Efficiency** — Rendering stops while the browser tab is hidden.

> This application is an artistic, procedural visualization—not a scientific aurora model, live camera, or space-weather forecast.

## 🎮 Controls

### Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `H` | Open or close scene settings |
| `Space` | Pause or resume animation when focus is outside interactive controls |
| `Escape` | Close scene settings |
| `Tab` / `Shift + Tab` | Navigate controls |

### Toolbar

| Control | Action |
|---------|--------|
| Pause / Play | Pause or resume the scene |
| Camera | Export the current scene as a PNG |
| Fullscreen | Enter or exit fullscreen where supported |
| Settings | Open the scene settings panel |

Fullscreen is hidden on small screens and disabled when unsupported.

### Scene Settings

| Setting | Range / Options | Default |
|---------|-----------------|---------|
| Movement speed | 0.1×–3.0× | 1.0× |
| Aurora brightness | 20–100% | 70% |
| Curtain layers | 2–7 | 3 |
| Star density | 50–1,000 stars | 450 |
| Night exposure | 60–140% | 100% |
| Lake reflections | On / Off | On |
| Occasional meteors | On / Off | On |
| Subtle star twinkle | On / Off | On |
| Image quality | Automatic / High / Low | Automatic |

- **Discover a scene** changes the landscape seed, palette, movement speed, brightness, curtain count, and animation position.
- **Reset defaults** restores the original scene settings and landscape.

### Color Palettes

| Palette | Appearance |
|---------|------------|
| **Oxygen green** | Naturalistic green with a faint violet upper fringe |
| **Violet** | Violet curtains with a rose-colored upper glow |
| **Crimson** | Artistic amber and crimson, inspired by rare red auroras |
| **Ice blue** | Pale cyan ribbons with a cool blue glow |
| **Iridescent** | Layered green, blue, and violet |
| **Rose** | Muted rose fading into indigo |
| **Teal** | Turquoise light with ocean-colored tones |
| **Pale green** | A softer, less saturated green aurora |

## 🚀 Quick Start

1. Clone the repository:

   ```bash
   git clone https://github.com/auroraborealisj/auroraborealisj.github.io.git
   ```

2. Enter the project directory:

   ```bash
   cd auroraborealisj.github.io
   ```

3. Open `index.html` in a modern browser.

**No installation, dependencies, or build process required.**

## 🛠️ Technologies

- **HTML5 Canvas 2D** — Aurora, stars, terrain, reflections, and image export.
- **Vanilla JavaScript** — Procedural generation, animation, settings, and interface behavior.
- **CSS3** — Responsive layout, translucent panels, transitions, and focus styling.
- **`requestAnimationFrame`** — Frame scheduling with elapsed-time-based motion.
- **LocalStorage API** — Local settings persistence.
- **Page Visibility API** — Suspension of rendering in hidden tabs.
- **Fullscreen API** — Optional immersive viewing.
- **`prefers-reduced-motion`** — Respect for system motion preferences.

## 🎨 How Rendering Works

1. **Build static layers**  
   Seeded generation creates the background sky, mountain ridges, snow, shorelines, and trees.

2. **Animate the aurora**  
   Layered wave functions and smooth noise control fine light rays, producing coherent folds and varying brightness.

3. **Composite the sky**  
   Stars, aurora emission, bloom, meteors, haze, and mountains are combined into an offscreen canvas.

4. **Reflect the scene**  
   Narrow mirrored strips of the rendered scene are displaced to suggest rippled water.

5. **Add finishing details**  
   Water shading, foreground silhouettes, a vignette, and exposure adjustments complete the image.

The landscape seed is saved, but animation progress and meteor events are not. Reloading preserves scene settings rather than an exact frame.

## ⚡ Performance & Browser Support

Use a current browser with JavaScript and Canvas 2D support.

- **Automatic** provides balanced rendering resolution.
- **High** increases resolution and aurora detail.
- **Low** reduces rendering cost and skips the bloom pass.
- Device pixel ratio and pixel-budget limits help control canvas memory usage.
- Static landscape layers are cached instead of regenerated every frame.
- Actual performance depends on screen size, browser, and hardware.

If the animation feels slow, select **Low**, reduce **Curtain layers** or **Star density**, or disable **Lake reflections**.

Fullscreen, image downloads, local storage, and some visual effects may vary by browser or embedded environment.

## 🔒 Privacy & Storage

- Scene generation and rendering happen locally in your browser.
- No account, backend, analytics, or external rendering service is required.
- Settings are saved in your browser when local storage is available.
- If storage is blocked, the application continues to work, but preferences may not persist.
- PNG export creates an image locally; the application does not upload it.

## 📁 Project Structure

```text
├── index.html    # Complete application: markup, styles, and rendering code
└── README.md     # Documentation
```

## 📄 License

This project is licensed under the MIT License.

---

<p align="center">Made with ✨ and JavaScript · A quiet moment beneath the sky</p>
