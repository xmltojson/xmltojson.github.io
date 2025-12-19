# 💕 Valentine Hearts

A beautiful Valentine's Day themed web application featuring floating hearts animation with love messages and shareable configurations.

![Valentine Hearts](https://img.shields.io/badge/Valentine-Hearts-ff6b9d?style=for-the-badge&logo=heart&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## ✨ Features

### 🎨 Visual Effects
- Continuously animated floating hearts rising from the bottom
- Heart burst effect creating 20 hearts simultaneously
- Click anywhere to create mini heart explosions
- Twinkling starry background
- Smooth CSS animations with transforms and filters
- Toast notifications for user feedback

### 💬 Love Messages
- 15 pre-loaded romantic messages
- Add your own personalized messages
- Automatic message rotation every 5 seconds
- Click any floating heart to reveal its message

### ⚙️ Settings Popup
All customization options in a clean modal interface:
- **Heart Speed** - Control float duration (5-20 seconds)
- **Heart Frequency** - Adjust spawn rate (0.5-3 seconds)
- **Heart Size** - Change dimensions (20-80px)
- **Auto Messages** - Toggle automatic message rotation
- **Sound Effects** - Enable/disable click sounds

### 🔗 Shareable URL System
Create and share unique configurations:
- Generate URL with all settings encoded
- Copy URL to clipboard with one click
- Open configuration in new tab
- Share via WhatsApp, Telegram, or Email
- Recipients see exactly what you created

### 🔧 Reset Options
- **Restore Defaults** - Reset settings while keeping custom messages
- **Clear All Data** - Complete reset including messages and stats

### 💾 Persistent State
All data saved to localStorage:
- Custom settings
- Personalized messages
- Statistics (hearts created, clicked, messages shown)

### 📱 Responsive Design
- Mobile-first approach
- Portrait mode with stacked layout
- Landscape mode with side-by-side layout
- Touch-friendly controls

## 🚀 Demo

Visit the live demo: [https://valentinehearts.github.io](https://valentinehearts.github.io)

### Example Configurations

| Description | Link |
|-------------|------|
| Fast & Small Hearts | `?speed=5&freq=500&size=25&auto=1` |
| Slow & Large Hearts | `?speed=18&freq=2500&size=70&auto=1` |
| Silent Mode | `?speed=10&freq=1500&size=40&auto=0&sound=0` |

## 📦 Installation

### Option 1: Direct Download
1. Clone the repository:
   ```bash
   git clone https://github.com/valentinehearts/valentinehearts.github.io.git
   ```
2. Open `index.html` in your browser

### Option 2: GitHub Pages
Fork the repository and enable GitHub Pages in your repository settings.

## 🎮 Usage

### Main Controls

| Button | Action |
|--------|--------|
| 💝 **New Message** | Shows random love message |
| 💖 **Heart Burst** | Creates 20 hearts at once |
| ⏸️ **Pause/Play** | Toggles heart animation |
| ⚙️ **Settings** | Opens settings popup |
| 🔗 **Share** | Opens share popup |

### Interactions

| Action | Result |
|--------|--------|
| Click floating heart | Reveals love message |
| Click anywhere | Creates mini heart explosion |
| Press Escape | Closes any open popup |

## 🔗 URL Parameters

Create custom configurations using URL parameters:

| Parameter | Description | Values | Default |
|-----------|-------------|--------|---------|
| `speed` | Heart float duration | 5-20 | 10 |
| `freq` | Spawn frequency (ms) | 500-3000 | 1500 |
| `size` | Heart size (px) | 20-80 | 40 |
| `auto` | Auto messages | 0, 1 | 1 |
| `sound` | Sound effects | 0, 1 | 0 |
| `msgs` | Custom messages | JSON array | - |

### URL Examples

**Basic configuration:**
```
https://valentinehearts.github.io/?speed=8&freq=1000&size=50
```

**With custom message:**
```
https://valentinehearts.github.io/?speed=10&msgs=%5B%22I%20love%20you%22%5D
```

**Full configuration:**
```
https://valentinehearts.github.io/?speed=12&freq=2000&size=45&auto=1&sound=0&msgs=%5B%22Forever%20yours%22%2C%22My%20heart%22%5D
```

## 📁 Project Structure

```
valentinehearts.github.io/
│
├── index.html      # Main application (HTML + CSS + JS)
├── README.md       # Documentation
└── LICENSE         # MIT License
```

## 🛠️ Technologies

- **HTML5** - Structure and semantics
- **CSS3** - Styling, animations, and responsive design
- **Vanilla JavaScript** - Application logic and state management
- **LocalStorage API** - Data persistence
- **Web Audio API** - Sound effects
- **URL Search Params API** - Shareable configurations

## 📊 Statistics Tracked

| Stat | Description |
|------|-------------|
| Hearts Created | Total floating hearts generated |
| Hearts Clicked | Number of hearts clicked by user |
| Messages Shown | Total messages displayed |

## 🎨 Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Primary Pink | `#ff6b9d` | Main accent color |
| Deep Pink | `#c44569` | Gradients and shadows |
| Light Pink | `#ffb8d0` | Text highlights |
| Red | `#e74c3c` | Secondary buttons |
| Gold | `#f39c12` | Special buttons |
| Purple | `#9b59b6` | Settings button |
| Blue | `#3498db` | Share button |

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Escape` | Close open popup |

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

MIT

## 💖 Acknowledgments

- Inspired by the spirit of Valentine's Day
- Created with love for spreading joy

---

<p align="center">
  Made with 💕 for Valentine's Day
</p>

<p align="center">
  <a href="https://github.com/valentinehearts/valentinehearts.github.io">⭐ Star this repo if you like it!</a>
</p>
