# 🎵 Music Visualizer

A beautiful, responsive audio visualizer that turns your music into immersive, real-time scenes. Built with vanilla HTML, CSS, and JavaScript—no frameworks, dependencies, or build tools required.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen)](https://musicvisualizer.github.io)

![Music Visualizer Screenshot](Screenshot.png)

## 🌐 Live Demo

**[https://musicvisualizer.github.io](https://musicvisualizer.github.io)**

## ✨ Features

### 🎨 Visualization Modes

| Mode | Scene | Description |
|------|-------|-------------|
| **Galaxy** | Deep Space | Detailed spiral galaxy with glowing stars, dust lanes, and audio-reactive lighting |
| **Landscape** | Alpine Afterglow | Layered mountains, a glowing sun, and shimmering lake reflections |
| **Bars** | Prismatic Sound | Gradient frequency bars with reflections and peak indicators |
| **Wave** | Liquid Frequencies | Layered waveform with flowing motion and adjustable bloom |
| **Circular** | Orbital Resonance | Radial frequency bars surrounding a shaded sphere with an orbiting light |
| **Particles** | Stardust | Depth-based particles responding to audio frequencies |
| **Spectrum** | Frequency Mirror | Mirrored frequency bars with colorful gradients |

Galaxy and camera movement provide an ambient preview even before playback. Frequency meters respond only to playing audio.

### 🎛️ Customization

- **10 Color Palettes** — Glacier, Aurora, Ember, Violet, Pearl, Rose, Ocean, Forest, Sunset, and Rainbow
- **Audio Sensitivity** — Adjust responsiveness from 10% to 200%
- **Frequency Smoothing** — Control frequency transitions from 0% to 95%
- **Spectrum Detail** — Choose 16–128 bars for Bars and Spectrum modes
- **Bloom Intensity** — Adjust glow effects
- **Background Modes** — Deep black, atmospheric gradient, or audio-reactive lighting
- **Rendering Quality** — Balanced, High, or Battery Saver
- **Motion Toggle** — Enable or disable gentle galaxy and camera movement
- **Reset Settings** — Restore default visual settings

### 📁 Music Library

- Choose one or multiple audio files
- Drag and drop files onto the upload area or application
- Import starts automatically—no separate upload confirmation
- Add more files while an import is running
- View import progress and file-specific errors
- Search tracks by filename
- Download original audio files from the library
- Remove tracks through a **custom confirmation popup**
- Store up to **200 MiB of audio**, displayed as 200 MB in the interface
- Keep files between visits using **IndexedDB**
- Fall back to temporary session storage if IndexedDB is unavailable

Common formats include **MP3, WAV, OGG, FLAC, M4A, AAC, and Opus**. Additional audio formats may work depending on your browser and operating system.

> Files stay on your device. Importing music does not send it to a server, and removing a library entry does not delete your original file.

### 🎮 Player Controls

- Play / Pause / Previous / Next
- Seekable progress bar with elapsed time and duration
- Volume control and mute toggle
- Shuffle playback
- Repeat the current track
- Fullscreen support where available
- Save the current visualization as a **PNG**
- Built-in **Stellar Drift** ambient demo, generated locally

### 📱 Responsive Design & Accessibility

- Desktop, tablet, and mobile layouts
- Portrait and landscape support
- Collapsible mobile music library
- Touch-friendly controls
- Keyboard-accessible dialogs and buttons
- Visible focus indicators and accessible control labels
- Import status announcements
- System reduced-motion preferences respected

### 💾 State Persistence

The application automatically saves and restores:

- Volume level
- Visualization mode
- Color palette
- Sensitivity and frequency smoothing
- Spectrum detail and bloom intensity
- Background mode and rendering quality
- Motion preference
- Shuffle and repeat states
- Last selected track, when still available

**Playback position is not saved.** Restoring a track does not automatically start playback.

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Space` | Play / Pause |
| `←` | Seek backward 5 seconds |
| `→` | Seek forward 5 seconds |
| `↑` | Increase volume by 5% |
| `↓` | Decrease volume by 5% |
| `M` | Mute / Unmute |
| `F` | Toggle fullscreen |
| `Esc` | Close a dialog or the mobile library |

Global playback shortcuts are inactive while a dialog is open or focus is on an interactive control, allowing normal keyboard interaction.

## 🚀 Getting Started

### Option 1: Use Online

Visit **[https://musicvisualizer.github.io](https://musicvisualizer.github.io)**.

### Option 2: Run Locally

1. **Clone the repository**

   ```bash
   git clone https://github.com/musicvisualizer/musicvisualizer.github.io.git
   ```

2. **Navigate to the directory**

   ```bash
   cd musicvisualizer.github.io
   ```

3. **Start a local web server**

   With Python installed:

   ```bash
   python -m http.server 8000
   ```

4. **Open the application**

   Visit **http://localhost:8000**.

You can also open `index.html` directly, but a local server is recommended for more predictable browser storage behavior.

### Add Your First Track

1. Click **Add music**.
2. Choose audio files or drag and drop them into the upload area.
3. Files are added automatically.
4. Select a track from your library to play it.
5. Choose a scene and open **Customize** to adjust its appearance.

No music files handy? Click **Try ambient demo** in the Add music popup.

## 🛠️ Technical Details

### Technologies Used

- **HTML5** — Application structure, audio playback, and native dialogs
- **Canvas 2D API** — Real-time scene rendering
- **CSS3** — Responsive layouts, gradients, and interface styling
- **Vanilla JavaScript** — Application logic without external dependencies
- **Web Audio API** — Frequency and waveform analysis
- **IndexedDB** — Local audio file storage
- **LocalStorage** — Settings and last selected track
- **File API & Blob URLs** — Local imports, playback, and downloads
- **Fullscreen API** — Optional fullscreen viewing

### Architecture

```text
┌──────────────────────────────────────────────────┐
│                  UI & Event Handlers             │
├──────────────────────────────────────────────────┤
│ Settings State │ AudioStore       │ Visualizer   │
│ LocalStorage   │ IndexedDB        │ Canvas 2D    │
│                │ Memory fallback │              │
├──────────────────────────────────────────────────┤
│ File Selection → Import Queue → Local Library    │
├──────────────────────────────────────────────────┤
│                   Web Audio API                  │
│                                                  │
│ Audio Element → AnalyserNode → Audio Destination │
│                       │                          │
│              Frequency & Waveform Data           │
│                       ↓                          │
│                  Visualizer                      │
└──────────────────────────────────────────────────┘
```

### Rendering & Performance

- Uses `requestAnimationFrame` for rendering
- Pauses rendering while the page is hidden
- Caches detailed galaxy artwork instead of rebuilding it every frame
- Uses logarithmically spaced frequency bands for audio analysis
- Adapts canvas resolution to the selected quality level

| Quality | Maximum Pixel Ratio | Target Frame Rate |
|---------|---------------------|-------------------|
| **Balanced** | 1.5× | 60 FPS |
| **High** | 2× | 60 FPS |
| **Battery Saver** | 1× | 30 FPS |

Actual frame rate depends on the device and browser. Reduced-motion preferences disable gentle scene movement and limit rendering to a 30 FPS target.

### File Structure

```text
musicvisualizer.github.io/
├── index.html      # Complete application: HTML, CSS, and JavaScript
├── README.md       # Documentation
├── LICENSE         # MIT License
├── favicon.ico     # Browser tab icon
└── Screenshot.png  # Preview image
```

### Browser Support

Use a current version of Chrome, Edge, Firefox, or Safari.

Audio decoding, persistent storage, and fullscreen availability vary by browser and platform. Some browsers require an explicit click on **Play** before audio can start.

## 📊 Storage

| Storage | Purpose | Capacity / Behavior |
|---------|---------|---------------------|
| **IndexedDB** | Audio files and metadata | Application limit: 200 MiB; browser quota may be lower |
| **LocalStorage** | Settings and last selected track | Small JSON record; browser-managed quota |
| **In-memory fallback** | Temporary audio library | Used if IndexedDB cannot open; lost when the page closes or reloads |

### Storage Identifiers

- **Database:** `MusicVisualizerDB`
- **Object store:** `audioFiles`
- **Settings key:** `musicVisualizerV2`

### Important Notes

- Libraries belong to the browser profile and site origin where files were imported.
- Files do not automatically sync between devices, browsers, or local and hosted copies.
- Clearing site data removes stored music and settings.
- Private browsing or browser storage eviction may prevent long-term retention.
- Keep backups of your original audio files.

## 🤝 Contributing

Contributions are welcome!

1. **Fork** the repository.
2. **Create** a feature branch:

   ```bash
   git checkout -b feature/amazing-feature
   ```

3. **Commit** your changes:

   ```bash
   git commit -m "Add amazing feature"
   ```

4. **Push** to your branch:

   ```bash
   git push origin feature/amazing-feature
   ```

5. **Open** a Pull Request.

When testing changes, check desktop and mobile layouts, keyboard navigation, file imports, playback, and storage behavior.

### Ideas for Contributions

- [ ] Add more visualization modes
- [ ] Implement an equalizer or other audio effects
- [ ] Add playlists and track reordering
- [ ] Support custom palette presets
- [ ] Add microphone input
- [ ] Implement dedicated beat detection
- [ ] Add video recording or visualization export
- [ ] Add installable PWA support and offline caching
- [ ] Improve automated testing and accessibility

## 📝 Changelog

### Current Version

- Seven visualization modes, including Galaxy and Landscape
- Ten color palettes with adjustable bloom and rendering quality
- Simplified file import with automatic processing
- Multi-file selection and drag-and-drop support
- Import queue, progress tracking, and file-specific errors
- Custom track-removal confirmation popup
- 200 MiB local audio library limit
- Temporary storage fallback
- Built-in locally generated ambient demo
- PNG visualization snapshots
- Responsive layouts and keyboard controls
- Reduced-motion support and saved visual preferences

## ❓ FAQ

**Q: Why can't I hear audio?**

> Select a track and click Play. Check the application volume, browser tab mute state, and system volume. Your browser may require a direct playback gesture or may not support the file’s audio codec.

**Q: Why does a scene move before I play music?**

> Some scenes include ambient movement. Audio-reactive effects and the bass, mid, and air meters respond only when music is playing. You can disable gentle scene movement in Customize.

**Q: Why was my file saved but not played?**

> Storage and audio decoding are separate operations. A file can be imported successfully even if your browser cannot decode its format. Try a supported MP3 or WAV file.

**Q: Do I need to confirm uploads?**

> No. Choose or drop your files and importing begins automatically. You can add more files while an import is running.

**Q: Does removing a track delete it from my computer?**

> No. The custom removal popup deletes only the copy stored in the application’s library. Your original file remains unchanged.

**Q: Why did my library disappear?**

> You may be using a different browser, profile, or site address. Clearing site data also removes the library. If persistent storage was unavailable, the application used temporary storage that does not survive a reload.

**Q: How do I clear all stored files?**

> Remove tracks individually, or use your browser’s developer tools to delete the `MusicVisualizerDB` IndexedDB database. Reload afterward. To reset saved settings as well, remove the `musicVisualizerV2` LocalStorage entry.

**Q: Can I use the application offline?**

> A downloaded copy can run locally without an internet connection. An already-loaded page also performs playback and visualization locally. The hosted application does not include a service worker, so reopening or refreshing it offline is not guaranteed.

**Q: Can I save a video of the visualization?**

> The application currently exports PNG snapshots only. Video recording and export are not implemented.

## 📄 License

Released under the **MIT License**. See [LICENSE](LICENSE) for details.

Copyright © 2025–2026 Yuliya Kolesnikova.

## 🙏 Acknowledgments

- Inspired by music visualization and immersive generative art
- Built with the Web Audio API and Canvas 2D
- Interface icons created with inline SVG

---

<p align="center">
  <a href="https://musicvisualizer.github.io">🎵 Try Music Visualizer Now</a>
  <br><br>
  <strong>Made with ❤️ for music lovers</strong>
</p>
