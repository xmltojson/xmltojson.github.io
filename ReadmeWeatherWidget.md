# 🌤️ Weather Widget

A beautiful, animated weather widget with glass morphism design, responsive layouts, and local storage persistence.

![Weather Widget Preview](https://raw.githubusercontent.com/weatherwidget/weatherwidget.github.io/main/preview.png)

## ✨ Features

### 🎨 Visual Design
- **Glass morphism** effect with backdrop blur
- **Dynamic gradient backgrounds** based on weather conditions
- **Magnetic glow** effect that follows cursor movement
- **Floating particles** animated background
- **Smooth transitions** and micro-interactions

### 🌦️ Weather Animations
| Weather | Animation |
|---------|-----------|
| ☀️ Sunny | Rotating sun with pulsing rays and glow |
| ☁️ Cloudy | Floating clouds with depth effect |
| 🌧️ Rainy | Falling raindrops with cloud cover |
| ❄️ Snowy | Animated snowflakes drifting down |
| ⛈️ Stormy | Heavy rain with lightning flashes |

### 📱 Responsive Design
- **Vertical layout** optimized for mobile portrait
- **Horizontal layout** for desktop and landscape
- **Auto-adapting** grid for weather details
- **Touch-friendly** interactive elements
- **Orientation change** support

### 💾 Persistent State
Automatically saves to localStorage:
- Location name
- Selected weather type
- Temperature and weather data
- Layout preference

## 🚀 Quick Start

### Option 1: Direct Use
Visit the live demo: [https://weatherwidget.github.io](https://weatherwidget.github.io)

### Option 2: Clone Repository
```bash
git clone https://github.com/weatherwidget/weatherwidget.github.io.git
cd weatherwidget.github.io
```

Open `index.html` in your browser.

### Option 3: Download
Download the latest release and open `index.html`.

## 📁 Project Structure

```
weatherwidget.github.io/
├── index.html      # Main application file (HTML + CSS + JS)
├── README.md       # Documentation
├── LICENSE         # MIT License
└── preview.png     # Preview image
```

## 🎮 Usage

### Change Weather
Click any weather button to switch between conditions:
- ☀️ **Sunny** - Clear skies, warm temperatures
- ☁️ **Cloudy** - Overcast conditions
- 🌧️ **Rainy** - Precipitation with clouds
- ❄️ **Snowy** - Winter conditions
- ⛈️ **Stormy** - Thunderstorm with lightning

### Update Location
1. Enter city name in the input field
2. Press **Enter** or click **Update**

### Toggle Layout
Click the layout button (☰) in the top-right corner to switch between:
- **Vertical** - Compact, mobile-friendly
- **Horizontal** - Wide, desktop-optimized

## 📊 Technical Details

### Technologies Used
- **HTML5** - Semantic markup
- **CSS3** - Animations, Grid, Flexbox, Backdrop Filter
- **Vanilla JavaScript** - No dependencies
- **LocalStorage API** - State persistence

### Performance
- No external dependencies
- Optimized CSS animations using `transform` and `opacity`
- Efficient DOM manipulation
- Minimal repaints and reflows

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🐛 Known Issues

- Backdrop filter may not work in older browsers
- Heavy animations may affect performance on low-end devices

## 📄 License

MIT

## 🙏 Acknowledgments

- [Google Fonts](https://fonts.google.com/) - Poppins font family
- Inspired by modern glass morphism design trends

---

<p align="center">
  Made with ❤️ for beautiful weather visualization
</p>

<p align="center">
  <a href="https://github.com/weatherwidget/weatherwidget.github.io/stargazers">⭐ Star this repo</a> •
  <a href="https://github.com/weatherwidget/weatherwidget.github.io/issues">🐛 Report Bug</a> •
  <a href="https://github.com/weatherwidget/weatherwidget.github.io/issues">💡 Request Feature</a>
</p>
