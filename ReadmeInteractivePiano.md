# 🎹 Interactive Piano

A feature-rich, browser-based virtual piano application with recording capabilities, multiple instruments, and a library of classical compositions.

**Live Demo:** [https://interactivepiano.github.io](https://interactivepiano.github.io)

![Interactive Piano](https://img.shields.io/badge/Piano-Interactive-e94560?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-ffd700?style=for-the-badge)

## ✨ Features

### 🎵 Play Piano
- **14 playable keys** spanning 2 octaves
- **4 instrument sounds**: Piano, Electric Piano, Organ, and Synth
- **Touch support** for mobile devices
- **Keyboard support** for desktop users
- **Adjustable octave range** (octaves 2-6)
- **Volume control**

### ⏺️ Recording
- **Record your performances** in real-time
- **Auto-save** recordings to "My Songs" library
- **Rename** your recordings
- **Download** recordings as JSON files
- **Upload** previously saved recordings

### 📚 Music Library
- **30+ pre-installed classical compositions** including:
  - Für Elise - Beethoven
  - Moonlight Sonata - Beethoven
  - Canon in D - Pachelbel
  - Turkish March - Mozart
  - Nocturne Op.9 No.2 - Chopin
  - And many more!
- **Play All** mode for continuous playback
- **Visual playback** with highlighted keys

### 🎨 Visual Features
- **Real-time audio visualizer**
- **Progress bar** during playback
- **Recording indicator**
- **Responsive design** for all screen sizes
- **Dark theme** with elegant gradients

## ⌨️ Keyboard Shortcuts

| Key | Note | | Key | Note |
|-----|------|-|-----|------|
| A | C | | F | F |
| W | C# | | T | F# |
| S | D | | G | G |
| E | D# | | Y | G# |
| D | E | | H | A |
| | | | U | A# |
| | | | J | B |

### Additional Controls

| Key | Action |
|-----|--------|
| Z | Octave Down |
| X | Octave Up |
| Space | Toggle Play All |

## 🚀 Getting Started

### Option 1: Visit Live Site
Simply go to [https://interactivepiano.github.io](https://interactivepiano.github.io)

### Option 2: Run Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/interactivepiano/interactivepiano.github.io.git
   ```
2. Open `index.html` in your web browser

No build process or dependencies required!

## 📱 Mobile Support

- Fully responsive design
- Touch-optimized piano keys
- Gesture support for playing multiple notes
- Mobile-friendly controls

## 💾 Data Storage

- Recordings are saved locally in your browser using `localStorage`
- Export recordings as JSON files for backup
- Import previously exported recordings

## 🛠️ Technologies

- **HTML5** - Structure
- **CSS3** - Styling with CSS Variables, Flexbox, Grid
- **JavaScript (ES6+)** - Application logic
- **Web Audio API** - Sound synthesis
- **LocalStorage API** - Data persistence

## 📁 Project Structure

```
interactivepiano.github.io/
├── index.html      # Main application file (single-file app)
└── README.md       # Documentation
```

## 🎼 How Recording Works

1. Click the **Record** button (⏺️)
2. Play notes on the piano using mouse, touch, or keyboard
3. Click **Record** again to stop
4. Your recording is automatically saved to "My Songs"
5. Rename, play, download, or delete your recordings anytime

## 🎹 Sound Synthesis

The application uses the Web Audio API to synthesize instrument sounds:

- **Piano**: Multi-harmonic synthesis with natural decay
- **Electric Piano**: Dual oscillator with sine and triangle waves
- **Organ**: Drawbar-style additive synthesis with sustained tones
- **Synth**: Sawtooth and square waves with filter envelope

## 🌐 Browser Compatibility

Works on all modern browsers:
- Chrome / Chromium
- Firefox
- Safari
- Edge
- Opera

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest features
- Submit pull requests

## 📄 License

MIT

## 🔗 Links

- **Repository:** [https://github.com/interactivepiano/interactivepiano.github.io](https://github.com/interactivepiano/interactivepiano.github.io)
- **Live Demo:** [https://interactivepiano.github.io](https://interactivepiano.github.io)

---

<p align="center">
  Made with ❤️ and 🎵
</p>
