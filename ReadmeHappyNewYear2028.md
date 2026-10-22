# 🎆 Happy New Year 2028

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub Pages](https://img.shields.io/badge/Demo-Live-brightgreen)](https://happynewyearj.github.io)

An interactive New Year celebration web app featuring realistic fireworks, golden confetti, and a moonlit waterfront. Built with plain HTML, CSS, and JavaScript, with responsive layouts for desktop, mobile, and landscape viewing.

## 🌐 Live Demo

**[https://happynewyearj.github.io](https://happynewyearj.github.io)**

## ✨ Features

- 🎆 **Realistic fireworks** — spherical particle bursts, glowing trails, subtle smoke, and water reflections.
- 🎊 **Celebration confetti** — falling, rotating confetti triggered by the celebrate button.
- 🌙 **Moonlit scenery** — procedurally drawn stars, a textured moon, distant hills, and an illuminated waterfront skyline.
- ⏳ **Live countdown** — counts down to January 1, 2028, at midnight in the visitor’s local time zone.
- 🕐 **Localized clock** — displays the current local date and time.
- 🎯 **Interactive celebration** — launches a fireworks sequence with the original four-note sound effect.
- 💛 **Eight selectable wishes** — health, prosperity, love, happiness, success, peace, strength, and luck, each with its own message.
- 🌍 **Three languages** — German by default, followed by Ukrainian and English.
- 💾 **Saved preferences** — remembers language and sound settings when browser storage is available.
- 🔊 **Sound control** — enable or mute the celebration sound.
- ⏸️ **Animation control** — pause or resume visual effects.
- ♿ **Accessibility features** — keyboard-friendly controls, visible focus indicators, screen-reader status messages, and reduced-motion support.
- 📱 **Responsive layouts** — compact portrait and two-column landscape layouts, with safe-area support.
- ⚡ **Efficient rendering** — bounded particle counts, time-based animation, and animation suspension while the page is hidden.
- 📦 **No dependencies** — no frameworks, external fonts, images, or audio downloads required for the application.

> Standard layouts are designed to fit the viewport without page scrolling. Exceptionally small or heavily zoomed viewports allow the main content to scroll so controls remain accessible.

## 🚀 Quick Start

```bash
# Clone repository
git clone https://github.com/happynewyearj/happynewyearj.github.io.git

# Enter project directory
cd happynewyearj.github.io

# Open in browser on macOS
open index.html
```

On Windows or Linux, open `index.html` directly in your browser.

No build step or package installation is required.

Or just visit the [live demo](https://happynewyearj.github.io)!

## 🎮 How to Use

1. Choose **Deutsch**, **Українська**, or **English** from the language menu.
2. Select a wish to display its message and launch a firework when animation is enabled.
3. Press the **celebrate button** for fireworks, confetti, and the four-note sound.
4. Use the **speaker button** to toggle sound.
5. Use the **pause/play button** to control animation.

Sound plays only after a user interaction. Reduced-motion preferences disable animation initially; it can be enabled manually.

## 🛠️ Tech Stack

- **HTML5** — semantic structure and accessible controls.
- **CSS3** — responsive grids, metallic text gradients, glass-style panels, and safe-area spacing.
- **Vanilla JavaScript** — application logic and interactions.
- **Canvas API** — procedural scenery, fireworks, reflections, and confetti.
- **Web Audio API** — synthesized celebration sound.
- **Intl.DateTimeFormat** — localized date and time.
- **Local Storage** — language and sound preferences.

## 📁 Structure

```text
├── index.html    # Complete application: HTML, CSS, and JavaScript
├── favicon.ico   # Browser tab icon
├── README.md     # Documentation
└── LICENSE       # MIT License
```

The favicon is referenced in the HTML:

```html
<link rel="icon" type="image/x-icon" href="favicon.ico"/>
```

## 🌍 Languages

| Order | Language | Code | Default |
|---|---|---|---|
| 1 | Deutsch | `de` | ✅ |
| 2 | Українська | `uk` | |
| 3 | English | `en` | |

Translations include greetings, countdown labels, wishes, control labels, status messages, page titles, and descriptions.

German is used on the first visit. A saved language preference takes precedence on subsequent visits.

## 📝 License

[MIT](LICENSE) © 2025–2028 Yuliya Kolesnikova  
[ORCID: 0009-0000-6151-7415](https://orcid.org/0009-0000-6151-7415)

---

<div align="center">

**🎆 Frohes neues Jahr 2028! 🎆**  
**З Новим 2028 роком!**  
**Happy New Year 2028!**

⭐ Star this repo if you like it!

</div>
