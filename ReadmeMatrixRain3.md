# Matrix Rain

**Free your mind and watch the code rain fall.**

A cinematic, interactive digital rain simulation inspired by the Matrix films. Layered character streams, phosphor glow, and subtle film effects create an atmospheric display.

Built with pure HTML, CSS, and JavaScript — no dependencies, build tools, or installation required.

**[▶ Live Demo](https://matrixrainj.github.io)**

## Features

### 🟢 Cinematic Visuals

- **Layered depth** — Three layers with different character sizes, speeds, brightness, and coverage
- **Grid-based rain** — Illuminated stream heads advance through character rows while glyphs change independently
- **Phosphor glow** — Bright leading characters with adjustable optical bloom
- **Variable trails** — Five trail-length levels with gradual brightness falloff
- **Film texture** — Optional grain and scanlines
- **Lens vignette** — Subtle edge darkening for a cinematic appearance
- **Spectrum colors** — Multicolored streams
- **Natural variation** — Randomized stream lengths, spacing, intensity, and character mutations

### 🎨 Customization

| Setting | Options |
|---------|---------|
| Rain speed | 10–120 |
| Stream density | 10–40; higher values create denser rain |
| Character size | 10–30 px base size, scaled by depth layer |
| Trail length | 1–5; higher values create longer trails |
| Brightness | 40–150% |
| Bloom intensity | 0–100%, available when phosphor glow is enabled |
| Phosphor color | Six presets and a custom color picker |
| Character set | Katakana + numerals, Binary, Hexadecimal, Kanji, Symbols, or Custom |
| Visual effects | Toggle depth, glow, film texture, vignette, and spectrum colors |

**Color presets:** Phosphor Green, Classic Green, Ice Blue, Ultraviolet, Amber, and Crimson.

**Custom characters:** Enter up to 50 characters and select **Set**. The text becomes a pool of glyphs used in the rain; it is not displayed as a complete message.

### 🌌 Scene Presets

- **Cinematic** — Layered green rain with bloom, film texture, and vignette
- **Classic** — Faster, denser green rain with a single depth layer
- **Deep focus** — Slower, dimmer ice-blue rain with reduced visual texture

Applying a preset keeps the selected render quality.

### ⚙️ Controls and Saved State

- Glass-style, responsive settings panel
- **Settings collapsed by default** on the first visit
- Panel open/closed state restored after reloading
- Visual settings saved automatically to LocalStorage
- Pause/play state restored after reloading
- Fullscreen toggle where supported
- PNG screenshots without interface controls
- Restore default visual settings without changing panel or playback state

If LocalStorage is unavailable, the application still works, but preferences may not persist.

### ♿ Motion and Accessibility

- Pauses on initial load when the system requests reduced motion
- Pauses when reduced motion is enabled while the application is running
- Allows playback to be started manually
- Labeled controls, visible keyboard focus, and accessible status announcements
- Collapsed settings are removed from keyboard interaction
- Animation stops while the browser tab is hidden

### ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Pause / Play |
| `H` | Show / Hide settings |
| `Esc` | Close settings |
| `F` | Toggle fullscreen |
| `S` | Save a PNG screenshot |

Shortcuts other than `Esc` are ignored while an input, select, button, or editable element has focus, preserving normal keyboard interaction.

## Getting Started

### Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/matrixrainj/matrixrainj.github.io.git
   ```

2. Open `index.html` in your browser.

No build step or dependencies are required.

### Use the Application

1. Select the settings icon in the upper-right corner, or press `H`.
2. Choose a scene preset or customize the individual controls.
3. Hide the panel to enjoy an unobstructed view.
4. Select **Save image**, or press `S`, to export the current frame.
5. Reload the page to restore your saved preferences and panel state.

### Deploy

Deploy the application to any static hosting service:

- **GitHub Pages** — Select the repository branch and directory under **Settings → Pages**
- **Netlify / Vercel** — Deploy as a static site; no build command is required
- **Any web server** — Serve `index.html`

## Project Structure

```text
matrixrainj.github.io/
├── index.html      # Complete application: HTML, CSS, and JavaScript
├── favicon.ico     # Optional site icon
├── LICENSE         # MIT License
└── README.md       # Documentation
```

## Render Quality

| Mode | Target frame rate | Maximum pixel ratio |
|------|-------------------|---------------------|
| Balanced | Up to 60 FPS | 1.5× |
| High definition | Up to 60 FPS | 2× |
| Low power | Up to 30 FPS | 1× |

Actual frame rate depends on the browser, device, viewport size, and scene settings. A pixel-budget cap can reduce rendering resolution on large displays.

For lower resource usage, choose **Low power**, reduce stream density, or disable layered depth and glow.

## Technical Details

- **Rendering** — HTML5 Canvas 2D with an opaque output canvas
- **Animation** — `requestAnimationFrame` with elapsed-time movement and frame-rate limiting
- **Timing protection** — Update delta capped at 100 ms to avoid large jumps after interruptions
- **Glyph rendering** — Cached character atlases reduce repeated text-rendering work
- **Bloom** — Downsampled offscreen canvases create glow without per-character shadow blur
- **High-DPI support** — Device pixel ratio is capped according to quality and pixel budget
- **Film grain** — Reusable noise texture shifts at a low rate and freezes when paused
- **Persistence** — Settings are validated when loaded and saved immediately after changes
- **Lifecycle handling** — Rendering stops in hidden tabs and resumes appropriately on return
- **Responsive interface** — Supports desktop and mobile layouts
- **Zero dependencies** — No external libraries, fonts, or services required

## License

MIT — see [LICENSE](LICENSE)
