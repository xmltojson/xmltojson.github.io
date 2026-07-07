# 🎄 Interactive Christmas Tree

<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5">
<img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3">
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript">
<img src="https://img.shields.io/badge/Canvas-FF6384?style=flat-square&logo=html5&logoColor=white" alt="Canvas">
<img src="https://img.shields.io/badge/Web_Audio_API-8DD6F9?style=flat-square&logo=javascript&logoColor=black" alt="Web Audio API">
<img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="License">

<div align="center">

**A festive, interactive web application featuring a hand-drawn canvas Christmas tree and a full multi-track music synthesizer! 🎅✨**

[Live Demo](https://christmastreej.github.io) • [Report Bug](https://github.com/ChristmasTreej/ChristmasTreej.github.io/issues) • [Request Feature](https://github.com/ChristmasTreej/ChristmasTreej.github.io/issues)

</div>

---

## ✨ Features

- 🎄 **Canvas-Rendered Tree** - A detailed, layered Christmas tree drawn in real time with a textured trunk, jagged pine layers, procedural branches, and snow-capped edges
- ❄️ **Falling Snow** - Toggle a continuously generated, realistic snowfall animation
- 💡 **Twinkling Lights** - 50 spiraling, color-cycling lights with a glowing flicker effect
- 🎨 **Animated Ornaments** - Glossy, pulsing ornaments with highlights, shadows, and a glow halo across 8 colors
- 🎁 **Add Ornament** - Place new decorations dynamically anywhere on the tree with a floating note burst
- ⭐ **Animated Star** - Glowing, pulsing golden star topper
- 🎵 **Advanced Music System** - A built-in synthesizer that plays **5 full Christmas carols** with layered melody, harmony, and bass tracks
- 🎼 **Song Selector** - Choose from Jingle Bells, O Christmas Tree, Silent Night, Deck the Halls, and We Wish You a Merry Christmas
- 🔁 **Auto-Rotate Playlist** - Songs automatically advance to the next carol until you pick one manually
- 📊 **Music Visualizer** - An animated equalizer bar display synced to playback
- 🎁 **Gift Boxes** - Bouncing wrapped presents with golden bows at the tree base
- 📱 **Responsive Design** - Canvas and layout adapt fluidly to any screen size

---

## 🚀 Quick Start

### Option 1: Visit Online
👉 **[ChristmasTreej.github.io](https://christmastreej.github.io)**

### Option 2: Run Locally
```bash
# Clone the repository
git clone https://github.com/ChristmasTreej/ChristmasTreej.github.io.git

# Open index.html in your browser
cd ChristmasTreej.github.io
open index.html
```

### Option 3: Download
Download the ZIP file and open `index.html` in any modern browser.

---

## 🎮 Usage

**Interactive Controls:**
- `❄️ Toggle Snow` - Turn the snowfall animation on/off
- `💡 Toggle Lights` - Turn the twinkling Christmas lights on/off
- `🎵 Play Music` - Start/stop the music player (button switches to `⏹️ Stop Music`)
- `🎁 Add Ornament` - Add a new colorful ornament to the tree

**Song Selection:**
- 🔔 Jingle Bells
- 🌲 O Christmas Tree
- 🌙 Silent Night
- ⛄ Deck the Halls
- 🎅 We Wish You a Merry Christmas

> 💡 While music plays, songs auto-rotate through the playlist. Selecting a song manually stops auto-rotation and plays your choice on repeat.

---

## 🎼 How the Music Works

The app uses the **Web Audio API** to synthesize music entirely in the browser — no audio files required. Each song is defined as note data (melody, harmony, and bass) and rendered through custom instrument synthesis:

- **Bell Tone** - Additive harmonic synthesis for the lead melody
- **Glockenspiel** - Bright overtones on sustained notes
- **Pad** - Detuned sawtooth voices with a lowpass filter for warm harmony
- **Bass** - Triangle + sine layered tone with a lowpass filter
- **Sleigh Bells** - Filtered noise bursts for a festive percussive rhythm
- **Reverb & Compression** - A convolution reverb and dynamics compressor for a polished, spacious mix

---

## 🛠️ Built With

- Pure HTML5, CSS3, and Vanilla JavaScript
- No frameworks or dependencies
- **HTML5 Canvas** for real-time tree, lights, and ornament rendering
- **Web Audio API** for procedural multi-track music synthesis
- CSS3 animations for snow, star glow, presents, and floating notes

---

## 🌐 Live Demo

👉 **[ChristmasTreej.github.io](https://ChristmasTreej.github.io)**

---

## 🤝 Contributing

Contributions are welcome! 

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

MIT License

---

<div align="center">

### 🎄 Merry Christmas! 🎄

**Made with ❤️ and holiday spirit**

If you enjoyed this project, please ⭐ star the repository!

</div>
