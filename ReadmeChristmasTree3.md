# 🎄 Interactive Christmas Tree

<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5"> <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript"> <img src="https://img.shields.io/badge/Canvas-FF6384?style=flat-square&logo=html5&logoColor=white" alt="Canvas"> <img src="https://img.shields.io/badge/Web_Audio_API-8DD6F9?style=flat-square&logo=javascript&logoColor=black" alt="Web Audio API"> <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="License">

<div align="center">

**A festive, interactive web application featuring a detailed canvas Christmas tree, gently falling snow, and browser-generated Christmas melodies! 🎅✨**

[Live Demo](https://christmastreej.github.io) • [Report Bug](https://github.com/ChristmasTreej/ChristmasTreej.github.io/issues) • [Request Feature](https://github.com/ChristmasTreej/ChristmasTreej.github.io/issues)

</div>

---

## ✨ Features

- 🎄 **Detailed Canvas Tree** — Procedurally drawn pine branches, fine needles, a textured trunk, and snow resting on the boughs.
- 🌙 **Winter Scenery** — A moonlit forest, starry sky, snowy ground, and wrapped presents.
- ❄️ **Falling Snow** — Toggle gently drifting snowfall.
- 💡 **Fairy Lights** — 125 lights arranged in a spiral with warm glows and subtle shimmer.
- 🎨 **Glossy Ornaments** — 38 initial decorations with reflective highlights, shadows, and five color palettes.
- 🎁 **Personalize Your Tree** — Add up to 60 extra ornaments or restore the original decorations.
- ⭐ **Golden Star** — A faceted star topper illuminated when the lights are enabled.
- 🎵 **Christmas Melodies** — Five recognizable carol melodies synthesized locally with soft bell-like tones.
- 🔁 **Playlist or Repeat** — Play all melodies in sequence or repeat the selected song.
- 📊 **Audio Visualizer** — Frequency-driven bars displayed in the music settings when animation is enabled.
- ⚙️ **Settings Popup** — Scene controls, language selection, and music preferences in one modal.
- 🌍 **Three Languages** — German by default, followed by Ukrainian and English.
- 💾 **Persistent Settings** — Restore your decorations, preferences, selected song, and playback position after reloading.
- 📱 **Responsive Layout** — Adapts to desktop, tablet, and mobile screens.
- ♿ **Accessibility Features** — Keyboard-operable controls, accessible labels, status announcements, and reduced-motion support.

---

## 🚀 Quick Start

### Option 1: Visit Online

👉 **[ChristmasTreej.github.io](https://christmastreej.github.io)**

### Option 2: Run Locally

```bash
# Clone the repository
git clone https://github.com/ChristmasTreej/ChristmasTreej.github.io.git

# Enter the project directory
cd ChristmasTreej.github.io

No build step, package installation, or API keys are required.

---

## 🎮 Usage

Click **Settings / Einstellungen / Налаштування** in the top-right corner to open the settings popup.

Close it using the **×** button, the **Escape** key, or a click outside the popup.

### Scene Controls

| Control | Action |
|---|---|
| ❄ Snowfall | Enable or disable falling snow |
| ✦ Fairy lights | Enable or disable the lights and star illumination |
| 🎁 Add an ornament | Place another randomly positioned ornament on the tree |
| Reset decorations | Restore the original 38 ornaments |
| Gentle animation | Enable or disable snow movement, light shimmer, and visualizer animation |

Resetting decorations does not reset your language or music preferences.

### Language Selection

Available languages appear in this order:

1. **Deutsch** — Default for first-time visitors
2. **Українська**
3. **English**

Your selected language is remembered after reloading.

### Music Controls

- **Play music / Resume music** — Start the selected melody or continue from the saved position.
- **Stop music** — Stop playback while retaining the current position.
- **Volume** — Adjust the output level.
- **Play all melodies** — Enable sequential playlist playback.

### Song Selection

- 🔔 Jingle Bells
- 🌲 O Christmas Tree
- 🌙 Silent Night
- ❄ Deck the Halls
- 🎄 We Wish You a Merry Christmas

Selecting a different song starts that song from the beginning if playback is active. Otherwise, it becomes the saved selection.

> 🔁 With **Play all melodies** enabled, the playlist advances automatically and wraps back to the first song. When disabled, the selected melody repeats. Manually selecting a song does not change this setting.

---

## 💾 Saved Settings & Playback Restoration

The application stores its state in **`localStorage`** under:

```text
winter-tree-state-v1
```

Saved data includes:

- Selected language
- Snowfall and fairy-light settings
- Explicit animation preference
- Volume
- Playlist setting
- Selected song
- Whether music should be playing
- Playback note index, position within the note, and remaining inter-song pause
- Ornament positions, sizes, and colors

Settings are saved when changed. During playback, the application also saves a checkpoint approximately once per second and saves again when the page becomes hidden or is left.

### Resuming Music After Reload

If music was playing before a reload, the application restores the selected song and saved musical position, then attempts to resume.

**Browsers may block automatic sound after reloading.** If that happens:

- Click **Resume music**, or
- Click elsewhere on the page or press a supported key.

The saved playback position remains available while the application waits for permission.

Because audio is synthesized rather than loaded from a recording, restoration reconstructs playback from the saved note position; it does not preserve an already-ringing audio waveform.

### Background Tabs

Music and animation pause when the page becomes hidden. The playback position and intention to continue are retained, allowing music to resume when you return, subject to browser audio restrictions.

### Storage Notes

- Settings remain in the current browser and origin; they do not sync between devices.
- Private browsing, browser cleanup, or blocked storage can prevent persistence.
- If storage is unavailable, the application continues working and displays a warning in Settings.
- Previously saved language and volume preferences from the earlier application version are migrated when no current state exists.

---

## 🎼 How the Music Works

The application uses the **Web Audio API** to synthesize melodies entirely in the browser. No audio files or streaming services are required.

Each carol is represented as a sequence of notes and beat lengths.

### Audio Pipeline

1. **Bell-like synthesis** — Three sine-wave partials create each note.
2. **Amplitude envelopes** — A short attack and exponential decay produce a softly struck sound.
3. **Master gain** — Applies the selected volume.
4. **Dynamics compression** — Controls the combined output level.
5. **Frequency analysis** — Supplies data to the visualizer.

A short look-ahead scheduler queues upcoming notes without scheduling the entire song at once. The playback tracker distinguishes the currently heard note from notes already scheduled ahead, allowing more accurate restoration.

> 🎵 These are synthesized melody arrangements, not recorded performances or multi-track orchestral arrangements.

---

## 🛠️ Built With

- **HTML5** — Page structure and native `<dialog>` settings popup
- **CSS3** — Responsive layout, styling, and focus indicators
- **Vanilla JavaScript** — Scene generation, controls, persistence, and playback
- **Canvas 2D API** — Tree, scenery, ornaments, lights, and snowfall
- **Web Audio API** — Procedural music synthesis and visualization
- **Web Storage API** — Local preference and playback persistence
- **Page Visibility API** — Background-tab pause and restoration
- **`requestAnimationFrame`** — Animation updates, throttled to approximately 30 FPS
- **`ResizeObserver`** — Canvas resizing
- **`prefers-reduced-motion`** — Initial animation preference

### Rendering Approach

The static background and decorations are cached on offscreen canvases. Animation frames reuse these layers and draw changing elements, such as snow and light shimmer, on top.

The artwork uses deterministic random generation so branches and scenery do not change between frames.

**No frameworks, external JavaScript libraries, fonts, image assets, or audio downloads are required by the application.**

---

## ♿ Accessibility & Browser Support

The application includes:

- Native modal focus containment and Escape-key dismissal
- Visible keyboard focus indicators
- Localized accessible control labels
- Pressed states for toggle buttons
- Live status messages for music and decoration changes
- A text description of the canvas scene
- Reduced-motion detection and a manual animation setting

The system motion preference is followed until you explicitly choose an animation setting, which is then saved.

Use a current version of **Chrome, Edge, Firefox, or Safari** with Canvas, Web Audio, and native `<dialog>` support.

---

## 🌐 Live Demo

👉 **[ChristmasTreej.github.io](https://christmastreej.github.io)**

The application can also be hosted on any static web server. No backend is needed.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the project.
2. Create your feature branch:

   ```bash
   git checkout -b feature/AmazingFeature
   ```

3. Commit your changes:

   ```bash
   git commit -m "Add AmazingFeature"
   ```

4. Push the branch:

   ```bash
   git push origin feature/AmazingFeature
   ```

5. Open a pull request.

Please test changes across all three languages, mobile layouts, reduced-motion settings, and reload/playback restoration.

---

## 📝 License

MIT

---

<div align="center">

### 🎄 Frohe Weihnachten! • Веселого Різдва! • Merry Christmas! 🎄

**Made with ❤️ and holiday spirit**

If you enjoyed this project, please ⭐ star the repository!

</div>
