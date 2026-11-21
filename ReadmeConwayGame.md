# Conway's Game of Life

An interactive simulation of Conway's Game of Life, a classic cellular automaton. Draw on the grid, place famous patterns, control the speed, and watch the colours change as cells age. The interface is in Ukrainian by default, with English available.

## Demo

**Live Demo:** [https://conwaygame.github.io](https://conwaygame.github.io)

## Features

### Visual Effects
- **Age-based coloring** - Cells shift from cyan to violet to magenta as they survive generations
- **Newborn glow** - Freshly born cells glow softly and have a bright core
- **Cell trails** - Dying cells leave fading violet traces that show movement and history
- **Adaptive grid lines** - A subtle grid with stronger lines every 10 cells; it hides automatically at small cell sizes
- **Stamp preview** - A ghost outline shows where a pattern will be placed before you click
- **High DPI support** - Crisp, pixel-perfect rendering on retina displays

### Simulation
- **Classic rules (B3/S23)** - A live cell with 2–3 neighbours survives; a dead cell with exactly 3 neighbours is born
- **Toroidal wrapping** - Optional wrap-around edges, so the field behaves like a torus
- **Double-buffered engine** - Fast typed-array computation
- **Accurate timing** - Speed stays steady regardless of frame rate
- **Auto-pause** - The simulation stops automatically when all cells die
- **Generation & population counters** - Live statistics

### Controls
| Control | Description |
|---------|-------------|
| Start / Pause | Run or stop the simulation |
| Step | Advance exactly one generation |
| Random | Fill the grid randomly (~28% density) |
| Clear | Remove all cells and reset the generation counter |
| Speed | 1–60 generations per second |
| Tool | Draw, Erase, or Stamp a pattern |
| Presets | Choose a pattern to stamp or insert |
| To center | Clear the grid and place the selected pattern in the center |
| Rotate | Rotate the selected pattern 90° |
| Grid size | Small (40×30), Medium (64×48), Large (96×72), Huge (144×108), Square (64×64) |
| Wrap edges | Turn toroidal wrapping on or off |
| Show grid | Show or hide grid lines |
| Cell trails | Show or hide fading trails |

### Keyboard Shortcuts
| Key | Action |
|-----|--------|
| `Space` | Start / Pause |
| `N` / `→` | Step |
| `R` | Random |
| `C` | Clear |
| `Q` | Rotate pattern |
| `1` `2` `3` | Draw / Erase / Stamp tool |

### Pattern Presets
- ✈️ **Glider** - The smallest spaceship, which travels diagonally
- 🚀 **Lightweight spaceship (LWSS)** - Moves horizontally
- 🔫 **Gosper glider gun** - Fires an endless stream of gliders
- 💠 **Pulsar** - A large oscillator with period 3
- 🔟 **Pentadecathlon** - An oscillator with period 15
- 🌌 **Kok's galaxy** - A rotating, galaxy-like oscillator
- ➖ **Blinker** - The simplest oscillator, with period 2
- 🐸 **Toad** - An oscillator with period 2
- 🚨 **Beacon** - An oscillator with period 2
- 🌱 **R-pentomino** - A methuselah that evolves for 1103 generations
- 🌰 **Acorn** - A methuselah that evolves for 5206 generations
- 💀 **Diehard** - Vanishes completely after 130 generations
- ♾️ **Infinite growth** - A single-line pattern that grows without limit

### Language Support
- 🇺🇦 **Ukrainian** - Default language
- 🇬🇧 **English** - One-click switch
- Page title, meta description, labels and number formatting update instantly

### Responsive Design
- **Landscape** - The field and side control panel sit side by side
- **Portrait** - The field is on top, with a scrollable control panel below
- **Tablets in portrait** - A two-column control panel
- **Compact phone layouts** - Icon-only secondary buttons on small screens and short landscape screens
- **Auto-orienting grid** - The grid rotates to fit the screen; Life's rules are symmetric, so the simulation continues correctly
- **Touch, mouse and pen** - Supported through Pointer Events, with smooth line drawing
- **Safe-area support** - Works correctly on notched devices

### Persistence
Everything is saved automatically to Local Storage and restored on page reload:
- Grid cells, cell ages (colors) and trails
- Generation counter and running/paused state
- Speed, tool, selected pattern and its rotation
- Grid size, wrap, grid lines and trails settings
- Language and control panel scroll position

## Installation

### Option 1: Direct Use
Open `index.html` in any modern web browser. It has no dependencies and needs no build step.

### Option 2: GitHub Pages
Fork the [repository](https://github.com/conwaygame/conwaygame.github.io/) and enable GitHub Pages in your repository settings.

### Option 3: Clone
```bash
git clone https://github.com/conwaygame/conwaygame.github.io.git
cd conwaygame.github.io
# open index.html in your browser
```

## Usage

1. **Draw cells** - Click or drag on the grid with the Draw tool. If you start a stroke on a live cell, it erases instead.
2. **Erase** - Switch to the Erase tool to remove cells.
3. **Place patterns** - Pick a preset; the Stamp tool activates automatically. Click the grid to place the pattern, and use **Rotate** to turn it.
4. **Insert to center** - Click **To center** to clear the field and place the selected pattern in the middle.
5. **Run** - Press **Start** (or `Space`) and adjust the **Speed** slider.
6. **Step through** - Use **Step** (or `N`) to advance one generation at a time.
7. **Experiment** - Try **Random**, change the grid size, or turn off edge wrapping.
8. **Switch language** - Use the **УКР / ENG** toggle in the header.

## Technologies

- HTML5 Canvas
- CSS3 (Grid, Flexbox, Media Queries)
- Vanilla JavaScript (ES6+)
- Typed Arrays
- Pointer Events API
- ResizeObserver API
- Local Storage API

## File Structure

```
conwaygame.github.io/
├── index.html
└── README.md
```

## License

MIT

## Links

- **Live Demo:** [https://conwaygame.github.io](https://conwaygame.github.io)
- **About the Game of Life:** [Wikipedia – Conway's Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life)
- **Pattern encyclopedia:** [LifeWiki](https://conwaylife.com/wiki/)
