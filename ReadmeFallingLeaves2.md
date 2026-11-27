# Falling Leaves

A beautiful, interactive autumn woodland with detailed falling leaves, natural wind effects, golden sunlight, and responsive controls. Built with HTML, CSS, and JavaScript—no external libraries or image assets required for the scene.

## Demo

[Live Demo](https://fallingleavesj.github.io)

## Features

### Visual Effects
- Multiple leaf shapes with shaded surfaces, branching veins, and natural colors
- Falling leaves with tumbling, fluttering, and depth-based sizing
- Smooth wind effects with optional natural gusts
- Golden sunlight, atmospheric haze, and soft light rays
- Soft background clouds
- Procedurally drawn autumn trees with detailed branches and foliage
- Winding woodland path with textured ground, dry grass, and fallen leaves
- Ground shadows and settling leaves that gradually fade
- Subtle floating dust and seed motes

### Customizable Settings
- **Falling Leaves** — Adjust the number of falling leaves (10–200)
- **Breeze** — Control wind intensity (0–10)
- **Fall Speed** — Set how fast leaves fall (0.5–5)
- **Tumble** — Adjust leaf rotation and flutter (0–10)
- **Leaf Size** — Change leaf size (15–60)
- **Woodland** — Show or hide trees
- **Soft Clouds** — Show or hide background clouds
- **Natural Gusts** — Enable or disable varying wind intensity

### State Persistence
- Scene settings automatically saved to `localStorage`
- Settings restored on page reload
- Settings panel minimized by default on the first visit
- Collapsed or expanded panel preference saved and restored
- Reset button restores scene defaults without changing the panel preference
- Application remains usable when browser storage is unavailable

### Responsive Design and Accessibility
- Responsive layout for desktop, tablet, and mobile devices
- Support for portrait and landscape orientations
- Collapsible, scrollable settings panel
- Mouse and touch interactions
- Labeled controls, keyboard-accessible buttons, and visible focus indicators
- Motion starts paused when the system requests reduced motion
- Pause and resume controls

### Interactive Elements
- Click or tap the woodland to scatter leaves
- **Scatter some leaves** button adds a larger burst
- **Pause / Resume** button controls animation
- Wind indicator describes the breeze as **Still**, **Gentle**, **Steady**, or **Gusty**

### Performance
- Landscape rendered separately from animated leaves
- Reusable leaf sprites
- Frame-rate-independent movement
- Animation suspended while the browser tab is hidden
- Bounded temporary leaf counts and canvas resolution

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/fallingleavesj/fallingleavesj.github.io.git
   ```

2. Open `index.html` in a modern browser.

No build step or package installation is required.

> Settings persistence depends on browser storage permissions and may vary when opening the HTML file directly.

## Usage

- **Open Settings:** Click the arrow button in the minimized panel.
- **Adjust Settings:** Use the sliders and switches to customize the scene.
- **Create Leaves:** Click or tap anywhere in the woodland outside the controls.
- **Scatter Leaves:** Click **Scatter some leaves** for a larger burst.
- **Pause Animation:** Click **Pause**, then **Resume** to continue.
- **Toggle Panel:** Click the arrow button to collapse or expand settings. Your preference is saved automatically.
- **Reset:** Click **Reset settings** to restore scene defaults while keeping your panel preference.

> When animation is paused, newly scattered leaves remain still until you resume.

## Technologies

- HTML5
- CSS3 — Responsive layouts, gradients, Flexbox, Grid, and backdrop blur
- JavaScript (ES6+)
- Canvas API and Path2D
- requestAnimationFrame
- LocalStorage API
- Page Visibility API
- matchMedia for reduced-motion support

## License

MIT
