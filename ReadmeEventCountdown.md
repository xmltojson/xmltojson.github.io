# ⏱ Event Countdown

Beautiful animated flip clock countdown timer for your special events. Create customizable countdowns with stunning visuals, multiple color themes, and real-time flip number animations.

![Event Countdown](https://img.shields.io/badge/Event-Countdown-7c4dff?style=for-the-badge&logo=clockify&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-ff6ec7?style=for-the-badge)
![HTML](https://img.shields.io/badge/HTML-CSS-JS-00e5ff?style=for-the-badge)

## 🌐 Live Demo

**[https://eventcountdown.github.io](https://eventcountdown.github.io)**

## ✨ Features

### Animated Flip Clock
- Realistic 3D card-flip animation on every digit change
- Smooth transitions between numbers with top/bottom split effect
- Pulsing separator dots between time units

### Customizable Events
- Create unlimited countdown timers
- Edit existing countdowns at any time
- Name your events with custom titles
- Set precise date and time targets

### Color Themes
- 8 beautiful gradient color themes to choose from
- Purple Pink, Cyan Blue, Orange Red, Green Teal, Gold, Rose, Ice, and Lime
- Each theme applies to digits, progress bars, accents, and glow effects

### Progress Tracking
- Visual progress bar showing elapsed time since creation
- Percentage indicator updated in real time
- Expired events marked with a celebration badge

### Persistent State
- All events saved to Local Storage automatically
- Full state restoration on page reload
- No account or backend required

### Responsive Design
- Adaptive grid layout for any screen size
- Portrait orientation — single column on mobile
- Landscape orientation — compact multi-column layout
- Flip card sizes adjust dynamically to viewport
- Touch-friendly controls for mobile devices

### Visual Effects
- Floating animated background particles
- Gradient-shifting animated header
- Card hover glow effects matching theme color
- Smooth card entrance animations
- Glassmorphism modal with backdrop blur

## 📸 Screenshots

### Desktop View
Multiple countdown cards displayed in a responsive grid with flip clock animations and progress bars.

### Mobile View
Single column layout with touch-optimized controls and adaptive flip digit sizing.

## 🚀 Getting Started

### Option 1: Visit the Live Site
Open **[https://eventcountdown.github.io](https://eventcountdown.github.io)** in any modern browser.

### Option 2: Run Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/eventcountdown/eventcountdown.github.io.git
   ```

2. Navigate to the project folder:
   ```bash
   cd eventcountdown.github.io
   ```

3. Open `index.html` in your browser:
   ```bash
   open index.html
   ```

No build tools, dependencies, or server required.

## 🎯 Usage

### Creating a Countdown
1. Click the **+ New Countdown** button
2. Enter an event name (e.g., "New Year 2026")
3. Select the target date and time
4. Choose a color theme
5. Click **Save**

### Editing a Countdown
1. Hover over an event card
2. Click the ✏️ edit button
3. Modify the name, date, or color
4. Click **Save**

### Deleting a Countdown
1. Hover over an event card
2. Click the ✕ delete button

### Keyboard Shortcuts
| Key | Action |
|-----|--------|
| `Enter` | Save event (when modal is open) |
| `Escape` | Close modal |

## 🏗 Project Structure

```
eventcountdown.github.io/
└── index.html    # Single-file application (HTML + CSS + JS)
```

The entire application is contained in a single `index.html` file with no external dependencies beyond Google Fonts.

## 🛠 Technology

- **HTML5** — Semantic markup and structure
- **CSS3** — Animations, gradients, flexbox, grid, media queries, custom properties
- **Vanilla JavaScript** — DOM manipulation, Local Storage API, timer management
- **Google Fonts** — Poppins and Orbitron typefaces

## 📄 License

MIT
