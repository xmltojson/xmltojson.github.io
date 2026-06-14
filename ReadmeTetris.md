# 🎮 Tetris Clone

A modern, feature-rich implementation of the classic Tetris game built with vanilla HTML, CSS, and JavaScript. No frameworks, no dependencies — just pure web technologies wrapped in a single HTML file.

🌐 **[Play Live Demo →](https://tetrisjs.github.io)**

![Tetris](https://img.shields.io/badge/game-tetris-00d4ff)
![License](https://img.shields.io/badge/license-MIT-green)
![Languages](https://img.shields.io/badge/languages-UK%20%7C%20EN-yellow)

## ✨ Features

### 🎯 Classic Gameplay
- All 7 standard tetrominoes (I, O, T, S, Z, J, L)
- Smooth piece movement and rotation with wall kicks
- Soft drop and hard drop mechanics
- Hold piece functionality
- Next piece preview
- Ghost piece showing landing position
- Line clearing with classic scoring system
- Progressive difficulty — game speeds up every 10 lines

### 🇺🇦 Multilingual Support
- **Ukrainian (default)** and English languages
- Instant language switching from the main menu
- Full UI translation including game over screens and notifications
- Cyrillic keyboard layout support (ь for Hold, з for Pause)

### 💾 Persistent State
- Auto-saves your game progress to local storage
- Resume exactly where you left off after closing the browser
- Top 5 high scores leaderboard with date tracking
- Best score record across all sessions
- Language preference persistence

### 📱 Responsive Design
- **Horizontal layout** for desktops and landscape orientation
- **Vertical layout** automatically adapts for mobile portrait mode
- Touch controls with swipe gestures and on-screen buttons
- Adaptive canvas sizing for any screen
- Glassmorphism UI with neon accents

### 🎨 Modern Visuals
- 3D-styled blocks with gradients and lighting effects
- Animated line-clear flash effect
- Glowing neon UI elements
- Smooth gradient background
- Custom inline SVG favicon

## 🚀 Getting Started

### Quick Start

Simply open `index.html` in any modern web browser:

```bash
git clone https://github.com/tetrisjs/tetrisjs.github.io.git
cd tetrisjs.github.io
open index.html
```

## 🎮 Controls

### Keyboard

| Key | Action |
|-----|--------|
| `←` `→` | Move piece left/right |
| `↓` | Soft drop |
| `↑` | Rotate piece |
| `Space` | Hard drop |
| `C` / `ь` | Hold piece |
| `P` / `з` | Pause/Resume |

### Touch / Mobile

- **Swipe left/right** — Move piece
- **Swipe down** — Soft drop
- **Fast swipe down** — Hard drop
- **Tap on board** — Rotate piece
- **On-screen buttons** — Full control panel for all actions

## 📊 Scoring System

| Lines Cleared | Points (× Level) |
|--------------|------------------|
| Single (1 line) | 100 |
| Double (2 lines) | 300 |
| Triple (3 lines) | 500 |
| Tetris (4 lines) | 800 |
| Soft drop | 1 per row |
| Hard drop | 2 per row |

**Level progression**: Increases every 10 cleared lines. Drop speed increases with each level (capped at maximum speed).

## 🏗️ Project Structure

```
tetrisjs.github.io/
├── index.html       # Single-file application (HTML + CSS + JS)
└── README.md        # This file
```

The entire application is contained in a single HTML file with:
- Embedded CSS for styling
- Inline JavaScript for game logic
- Inline SVG favicon (no external image files)
- Complete SEO metadata and Open Graph tags

## 🛠️ Technology Stack

- **HTML5** — Semantic markup and Canvas API for rendering
- **CSS3** — Modern features including:
  - Flexbox & responsive media queries
  - Backdrop filters (glassmorphism)
  - Linear gradients and box shadows
  - Keyframe animations
- **JavaScript (ES6+)** — Pure vanilla, no frameworks:
  - Canvas 2D rendering
  - LocalStorage API for persistence
  - RequestAnimationFrame for smooth animation
  - Touch and Keyboard event APIs

## 💡 Key Implementation Details

### State Management
Game state (board, current piece, score, level, etc.) is automatically serialized to `localStorage` after every meaningful action. On page reload, the app restores the state and presents a paused game ready to resume.

### Rotation System
Implements basic wall-kick logic — when rotation would cause a collision, the piece tries small horizontal offsets (±1, ±2 cells) to find a valid position.

### Internationalization
A simple key-value translation map drives all user-facing text. Adding a new language requires only adding a new entry to the `translations` object.

### Storage Keys

| Key | Purpose |
|-----|---------|
| `tetris_state` | Current game state (board, pieces, score) |
| `tetris_highscores` | Top 5 results array |
| `tetris_best` | Best score across all sessions |
| `tetris_lang` | Selected interface language |

## 🔒 Privacy

This game runs **entirely in your browser**. No data is sent to any server. All scores, preferences, and game states are stored locally on your device using the browser's LocalStorage API. You can clear all data at any time using the **Reset** button.

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Ideas for Contributions
- Additional language translations
- Sound effects and background music
- Multiplayer mode
- Custom themes / skins
- Replay system
- T-spin detection and bonus scoring
- Customizable controls

## 📄 License

This project is open source and available under the MIT License.

---

**Enjoy the game! 🎮 Грайте з задоволенням!**
