# 💕 Valentine Hearts

A Valentine's Day themed web application featuring floating hearts, personalized love notes, and shareable configurations. Built as a single HTML file with no dependencies or build tools.

![Valentine Hearts](https://img.shields.io/badge/Valentine-Hearts-ce466e?style=for-the-badge&logo=heart&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## ✨ Features

### 🎨 Visual Effects
- Floating hearts drifting upward through an interactive heart garden
- Large animated heart with soft gradients and shadows
- Heart burst effect with scattered particles and nine additional floating hearts
- Particle effects when catching floating hearts
- Soft pink background with decorative sparkles
- Toast notifications for user feedback
- Embedded SVG heart favicon

### 💬 Love Messages
- 10 pre-loaded romantic notes
- Add up to 20 personal notes, with 160 characters per note
- Personalize the recipient and sender names
- Automatic message rotation every 8 seconds
- Catch a floating heart or tap the large heart to reveal a note
- Personal notes appear first when opening a personalized Valentine
- Remove individual default or personal notes
- Adaptive message sizing to fit the available letter area

### ⚙️ Settings Popup

All customization options are available in a modal interface:

- **To / From** — Personalize the greeting and signature, up to 50 characters each
- **Your Love Notes** — Add and remove messages
- **Float Duration** — Set the base drift duration from 5–20 seconds
- **A New Heart Every** — Adjust the spawn interval from 0.5–3 seconds
- **Heart Size** — Adjust the size setting from 20–80px
- **Automatic Notes** — Enable or disable message rotation
- **Soft Chimes** — Enable or disable sounds when interacting with hearts

> Floating hearts have slight randomized variations in duration and size. Their clickable area is at least 44px.

### 🔗 Shareable URL System
- Generate a link containing names, notes, and atmosphere settings
- Copy the link to the clipboard
- Preview the configuration in a new tab
- Share via WhatsApp, Telegram, or Email
- Use the device’s native share sheet when supported
- Keep activity counts private: statistics are not included in shared links

> Shared notes are encoded in the URL, not encrypted. Anyone with the link can read them.

### 🔧 Reset Options
- **Restore Atmosphere** — Reset animation and sound settings while preserving names, notes, and statistics
- **Reset Everything** — Restore default names, notes, settings, and activity counts after confirmation

### 💾 Persistent State

Changes are automatically saved to `localStorage`:

- Recipient and sender names
- Personal notes and the remaining default notes
- Animation, message rotation, and sound settings
- Activity statistics

If device storage is unavailable, the application remains usable for the current visit.

### 📱 Responsive Design
- Viewport-fitting main layout without page-level vertical scrolling
- Stacked card layout on portrait phones
- Side-by-side card layout on larger screens and short landscape windows
- Compact layouts for limited screen heights
- Dynamic viewport sizing and safe-area support
- Scrollable dialog contents when needed to keep settings accessible

### ♿ Accessibility
- Labeled buttons and form controls
- Visible keyboard focus indicators
- Screen-reader announcements for notes and notifications
- Native modal dialogs with Escape-to-close behavior
- Floating hearts stop moving while keyboard-focused
- Respects `prefers-reduced-motion`
- Automatically pauses animations and note rotation while a dialog is open or the page is hidden

## 🚀 Demo

Visit the live demo: [https://valentinehearts.github.io](https://valentinehearts.github.io)

### Example Configurations

| Description | Query String |
|-------------|--------------|
| Fast & Small Hearts | `?speed=5&freq=500&size=25&auto=1` |
| Slow & Large Hearts | `?speed=18&freq=2500&size=70&auto=1` |
| Manual Notes & No Sound | `?speed=10&freq=1500&size=40&auto=0&sound=0` |
| Personalized Greeting | `?to=Alex&from=Sam` |

## 📦 Installation

### Option 1: Direct Download

1. Clone the repository:

   ```bash
   git clone https://github.com/valentinehearts/valentinehearts.github.io.git
   ```

2. Open `index.html` in your browser.

No package installation or build step is required.

> Local file links do not work across devices. Publish the application on a website before sharing personalized links.

### Option 2: GitHub Pages

1. Fork the repository.
2. Open **Settings → Pages**.
3. Select **Deploy from a branch**.
4. Choose the branch containing `index.html` and the `/ (root)` folder.
5. Save and open the published URL once deployment completes.

## 🎮 Usage

### Main Controls

| Control | Action |
|---------|--------|
| **Another Little Note** | Displays another love note |
| **Large Heart** | Sends a heart, reveals a note, and triggers particles |
| **Heart Burst** | Triggers the large-heart action and adds nine floating hearts |
| **Pause / Play** | Pauses or resumes animations and automatic notes |
| **Make It Yours / Settings** | Opens the customization dialog |
| **Share This Valentine / Share** | Opens the sharing dialog |

### Interactions

| Action | Result |
|--------|--------|
| Catch a floating heart | Reveals its note, creates particles, and increments hearts caught |
| Tap the large heart | Reveals a note and increments hearts sent |
| Enable soft chimes | Plays a gentle chime and enables sounds for heart interactions |
| Press Escape | Closes the active dialog |
| Open a dialog or switch tabs | Temporarily pauses animations and automatic notes |

When reduced motion is enabled, drifting hearts and particle bursts are disabled. The large heart and note controls remain functional.

## 🔗 URL Parameters

Create custom configurations using URL parameters:

| Parameter | Description | Values | Default |
|-----------|-------------|--------|---------|
| `v` | Configuration version marker | Generated links use `2` | — |
| `speed` | Base float duration in seconds | 5–20 | 10 |
| `freq` | Heart spawn interval in milliseconds | 500–3000 | 1500 |
| `size` | Heart size setting in pixels | 20–80 | 40 |
| `auto` | Automatic note rotation | `0`, `1` | `1` |
| `sound` | Soft chimes | `0`, `1` | `0` |
| `to` | Recipient name | Up to 50 characters | Empty |
| `from` | Sender name | Up to 50 characters | Empty |
| `msgs` | Personal notes | URL-encoded JSON array; up to 20 notes | `[]` |
| `notes` | Included default-note collection | URL-encoded JSON array; up to 30 notes | 10 built-in notes |

Each note is limited to 160 characters.

Opening a URL containing recognized configuration parameters loads that configuration over a fresh set of defaults rather than merging it with previously saved settings. The resulting state is then saved locally.

### URL Examples

**Basic configuration:**

```text
https://valentinehearts.github.io/?speed=8&freq=1000&size=50
```

**With a personal note:**

```text
https://valentinehearts.github.io/?speed=10&msgs=%5B%22I%20love%20you%22%5D
```

**With names and personal notes:**

```text
https://valentinehearts.github.io/?v=2&to=Alex&from=Sam&speed=12&freq=2000&size=45&auto=1&sound=0&msgs=%5B%22Forever%20yours%22%2C%22My%20heart%22%5D
```

Use the application’s **Share** button to generate a link containing the complete current configuration, including changes to the default-note collection.

## 📁 Project Structure

```text
valentinehearts.github.io/
│
├── index.html      # Complete application: HTML, CSS, JavaScript, and SVG favicon
├── README.md       # Documentation
└── LICENSE         # MIT License
```

## 🛠️ Technologies

- **HTML5** — Semantic structure and native dialogs
- **CSS3** — Responsive grids, animations, gradients, and container units
- **Vanilla JavaScript** — Interactions and state management
- **Inline SVG** — Icons, heart artwork, and favicon
- **LocalStorage API** — Device-local persistence
- **Web Audio API** — Synthesized chimes without audio files
- **URL / URLSearchParams APIs** — Shareable configurations
- **Clipboard API** — Link copying with a fallback
- **Web Share API** — Native sharing where supported
- **ResizeObserver** — Adaptive note sizing
- **Page Visibility API** — Background playback management

## 📊 Statistics Tracked

| Display Label | Stored Key | Description |
|---------------|------------|-------------|
| Hearts Sent | `heartsCreated` | Floating hearts generated plus large-heart send actions |
| Hearts Caught | `heartsClicked` | Floating hearts caught by the user |
| Notes Discovered | `messagesShown` | Notes shown through automatic rotation and interactions |

The initial note is not counted. Counts represent display and interaction events, not unique notes or actual deliveries to another person.

Statistics are saved on the device and are not included in shared URLs.

## 🎨 Color Palette

| Color | Hex | Usage |
|-------|-----|-------|
| Warm Background | `#fbf5f3` | Page background |
| Paper | `#fffdfb` | Letter, buttons, and dialogs |
| Deep Plum | `#432934` | Main text |
| Muted Mauve | `#80666e` | Secondary text |
| Rose Pink | `#ce466e` | Primary accent and buttons |
| Deep Rose | `#ad3156` | Accent text and hover states |
| Soft Pink | `#f9e4e9` | Highlight backgrounds |
| Rose Border | `#eadbde` | Dividers and outlines |

## ⌨️ Keyboard Controls

| Key | Action |
|-----|--------|
| `Tab` / `Shift + Tab` | Move between interactive controls |
| `Enter` / `Space` | Activate focused buttons |
| `Enter` in the note field | Submit a personal note |
| Arrow keys on a slider | Adjust its value |
| `Escape` | Close the active dialog |

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature/amazing-feature
   ```

3. Commit your changes:

   ```bash
   git commit -m "Add amazing feature"
   ```

4. Push the branch:

   ```bash
   git push origin feature/amazing-feature
   ```

5. Open a pull request.

Before submitting, test portrait and landscape layouts, short viewports, keyboard navigation, reduced-motion behavior, and personalized share links.

## 📝 License

[MIT](LICENSE)

## 💖 Acknowledgments

- Inspired by the spirit of Valentine's Day
- Created with love for spreading joy
- Built with native web technologies to stay lightweight and easy to share

---

<p align="center">
  Made with 💕 for Valentine's Day
</p>

<p align="center">
  <a href="https://github.com/valentinehearts/valentinehearts.github.io">⭐ Star this repo if you like it!</a>
</p>
