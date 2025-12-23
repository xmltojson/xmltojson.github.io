# Birthday Card

An interactive, animated birthday card web application with cake, candles, confetti, and celebration effects.

## Demo

🎂 **Live Demo:** [https://birthdaycardj.github.io](https://birthdaycardj.github.io)

## Features

### 🎂 Visual Elements
- 3-layer animated birthday cake with frosting and cherries
- Dynamic candles with realistic flickering flames (1-5 based on age)
- Floating balloons with smooth animations
- Confetti explosion with multiple shapes and colors
- Star burst effects during celebration
- Smoke effect when candles are blown out

### 🎮 Interactive Features
- **Blow Candles** - Click button or swipe up on mobile
- **Celebrate** - Triggers full celebration with confetti and stars
- **Age Selector** - Increase/decrease age (affects candle count)
- **Name Input** - Personalize the birthday card
- **Reset** - Start fresh with default settings

### 💾 State Persistence
All settings are saved to LocalStorage:
- Recipient's name
- Age setting
- Candles blown status
- Total wishes count
- Theme preference
- Sound settings

### 🎨 Themes & Settings
- Light/Dark theme toggle
- Sound effects toggle
- Procedural audio for blow sound and celebration melody

### 📱 Responsive Design
- Portrait and landscape orientation support
- Mobile touch support (swipe up to blow candles)
- Optimized layouts for all screen sizes

### ⌨️ Keyboard Shortcuts
| Key | Action |
|-----|--------|
| `Space` or `B` | Blow candles |
| `C` | Celebrate |
| `R` | Reset |
| `↑` | Increase age |
| `↓` | Decrease age |

## Installation

1. Clone the repository:
```bash
git clone https://github.com/birthdaycardj/birthdaycardj.github.io.git
```

2. Open `index.html` in your browser

No build process or dependencies required.

## Usage

1. Enter the birthday person's name
2. Set their age using the +/- buttons
3. Click "Blow Candles" or swipe up on mobile
4. Watch the celebration!
5. Click "Celebrate" anytime for more confetti

## Technologies

- HTML5
- CSS3 (Animations, Gradients, Flexbox)
- Vanilla JavaScript (ES6+)
- Web Audio API
- LocalStorage API

## License

MIT
