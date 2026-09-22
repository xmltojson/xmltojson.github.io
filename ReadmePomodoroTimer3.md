# 🍅 Pomodoro Timer / Forest

A calm, nature-inspired Pomodoro timer for focused work and intentional breaks. Built with pure HTML, CSS, and JavaScript—no frameworks, dependencies, or build tools.

![Pomodoro Timer](https://img.shields.io/badge/Pomodoro-Forest-41603d?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## 🚀 Demo

Visit the live application: **[pomodorotimerj.github.io](https://pomodorotimerj.github.io)**

## ✨ Features

- **🎯 Customizable focus sessions** — Work in focused intervals, starting at 25 minutes.
- **☕ Short and long breaks** — Rest for 5 minutes between sessions and 15 minutes after a completed cycle by default.
- **🌲 Forest-inspired interface** — Landscape photography, translucent panels, and a circular timer with dial markings.
- **🖥️ Compact desktop layout** — Designed for comfortable use at 100% browser zoom, with height-aware sizing for laptop screens.
- **📱 Responsive design** — A stacked layout and larger touch controls on smaller screens.
- **📝 Current task** — Write down one meaningful task and keep it visible while you focus.
- **📊 Progress tracking** — View completed pomodoros, total completed focus time, and progress through the current cycle.
- **💾 Local persistence** — Save timer state, preferences, task text, and statistics on your device.
- **🔔 Completion alerts** — A gentle audio chime, in-app messages, and optional desktop notifications.
- **⏩ Optional automatic transitions** — Independently enable auto-start for breaks and focus sessions.
- **🌓 Dark and light themes** — Dark mode by default.
- **🌍 Ukrainian and English** — Switch languages without resetting the timer.
- **⌨️ Keyboard shortcuts** — Start, pause, reset, skip, or open the technique guide.
- **🛡️ Confirmation dialogs** — Confirm before discarding session progress or skipping a session.
- **♿ Accessibility features** — Semantic controls, accessible labels, visible keyboard focus, native dialogs, and reduced-motion support.

## 🎮 Usage

### Basic Workflow

1. Enter a task in **“What are you focusing on?”**
2. Choose **Focus**, **Short break**, or **Long break**.
3. Press the start button or `Space`.
4. Work until the session finishes.
5. Start the next session manually, or enable automatic starts in Settings.

### Controls

| Action | Button | Keyboard Shortcut |
|--------|--------|-------------------|
| Start / Pause / Resume | ▶ / ⏸ | `Space` |
| Reset current session | ↺ | `R` |
| Skip current session | ⏭ | `S` |
| Open the technique guide | ℹ | `I` |

Shortcuts are inactive while a dialog is open or focus is inside an input, button, link, or another editable control.

### Timer Modes

| Mode | Default Duration | Purpose |
|------|------------------|---------|
| Focus | 25 minutes | Work on one task |
| Short break | 5 minutes | Rest between focus sessions |
| Long break | 15 minutes | Rest after a completed focus cycle |

A cycle contains **4 completed focus sessions** by default.

### Session and Statistics Rules

- Completing a focus session adds **one pomodoro** and its full duration to your statistics.
- Paused, reset, or skipped sessions do not add focus time.
- Skipping a focus session does not advance the completed-session count.
- Completing enough focus sessions selects a long break.
- Finishing or skipping a long break resets the cycle.
- You can also select any timer mode manually.

Statistics are cumulative on the current device; they are not daily or weekly reports.

### Settings

Open **Settings** in the header to customize:

| Setting | Default | Allowed Range |
|---------|---------|---------------|
| Focus duration | 25 minutes | 1–120 minutes |
| Short break duration | 5 minutes | 1–60 minutes |
| Long break duration | 15 minutes | 1–120 minutes |
| Sessions per cycle | 4 | 2–10 |
| Completion sound | On | On / Off |
| Auto-start breaks | Off | On / Off |
| Auto-start focus | Off | On / Off |

Duration changes apply to the next session without changing a running or partially completed session. If the current timer has not started, its duration updates immediately.

Desktop notifications can also be enabled from Settings.

### Language and Theme

- Click **UA / EN** to switch between Ukrainian and English. Ukrainian is the default.
- Click **☀ / ☾** to switch between light and dark themes. Dark is the default.

Both preferences are saved locally.

## 💾 Persistence and Timer Behavior

The application stores the following in your browser’s `localStorage`:

- Timer mode, duration, remaining time, and running deadline
- Completed pomodoros and completed focus time
- Current cycle progress
- Current task
- Duration and auto-start settings
- Sound preference
- Language and theme

A running timer uses a wall-clock deadline rather than counting interval callbacks. This helps it recover the correct remaining time after a reload or background-tab throttling.

**When reopening an expired timer:**

- Only the session that was running is counted as completed.
- The next mode is selected but is not automatically started during restoration.
- The app does not invent completed sessions for time spent away.

> Closing the page stops its JavaScript. The app restores timer state when reopened, but it cannot play sounds or deliver scheduled completion alerts while the page is closed.

If browser storage is unavailable, the timer remains usable, but progress may be lost when the page closes.

## 🔔 Notifications and Sound

### Completion Sound

The completion chime is generated with the **Web Audio API**—no audio files are required.

Browsers generally require a user interaction before allowing audio. Starting a session normally provides that interaction.

### Desktop Notifications

To enable desktop notifications:

1. Open **Settings**.
2. Select **Enable desktop notifications**.
3. Allow notifications in the browser permission prompt.

Notifications depend on browser support, site permissions, and operating-system settings. Use **HTTPS** or **localhost** for a secure context.

Some mobile browsers require a service worker for notifications; this application does not currently include one. In-app completion messages remain available.

Background tabs may be throttled or suspended, so completion alerts are not guaranteed to arrive at the exact deadline.

## 📦 Installation

### Option 1: Open Directly

Download the project and open `index.html` in a modern browser.

The timer requires no installation or build step. Browser storage and notification behavior may vary when opened through a `file://` URL.

### Option 2: Deploy with GitHub Pages

1. Fork or copy this repository.
2. Open **Settings → Pages**.
3. Choose **Deploy from a branch**.
4. Select the branch containing `index.html` and the repository root.
5. Save and open the published Pages URL.

No build command or environment variables are needed.

## 🛠️ Technical Details

### Technologies Used

| Technology | Purpose |
|------------|---------|
| HTML5 | Page structure, semantic controls, native `<dialog>` elements |
| CSS3 | Themes, responsive layouts, translucent surfaces, dial styling |
| Vanilla JavaScript | Timer logic, settings, translations, state management |
| Inline SVG | Interface icons, progress ring, and dial markings |
| Web Audio API | Generated completion chime |
| Local Storage API | Device-local persistence |
| Notifications API | Optional desktop notifications |
| Page Visibility API | Timer refresh when returning to the tab |

### Implementation Highlights

- **Single-file application** — HTML, CSS, and JavaScript live in `index.html`.
- **Deadline-based timing** — Uses `Date.now()` to calculate remaining time.
- **250 ms refresh interval** — Checks the deadline and refreshes the visible timer when needed.
- **Validated saved state** — Restored durations and counters are checked and constrained.
- **Native modal dialogs** — Settings, help, and confirmation dialogs use `<dialog>`.
- **CSS custom properties** — Shared color tokens and layout variables simplify customization.
- **Height-aware desktop styling** — Compact layouts adapt to shorter laptop windows without CSS zoom or transform scaling.
- **Built-in translations** — Ukrainian and English strings are stored in a JavaScript dictionary.
- **Reduced-motion support** — Transitions are disabled when requested by the operating system.

### Browser Support

Use a current version of Chrome, Edge, Firefox, or Safari.

The interface uses modern features including native dialogs, CSS Grid, `aspect-ratio`, and CSS custom properties. Some visual effects and notification capabilities vary by browser.

## 🔒 Privacy and External Resources

- No account is required.
- There is no application backend or built-in analytics.
- Tasks, preferences, and statistics are stored locally rather than sent to an application server.
- Progress is not synchronized across devices or browsers.
- Clearing site data removes saved progress.

The forest background is loaded from **Unsplash**, so displaying it makes a request to an external service. A gradient fallback is provided if the image cannot load.

The application has no external JavaScript, stylesheet, font, or audio dependencies.

> This is not currently an installable PWA and does not include a service worker or guaranteed offline caching.

## 📁 Project Structure

```text
pomodorotimerj.github.io/
├── index.html      # Complete application: HTML, CSS, and JavaScript
├── README.md       # Project documentation
└── LICENSE         # MIT License
```

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature/amazing-feature
   ```

3. Make and test your changes.
4. Commit your work:

   ```bash
   git commit -m "Add amazing feature"
   ```

5. Push the branch:

   ```bash
   git push origin feature/amazing-feature
   ```

6. Open a pull request.

### Suggested Checks

Before submitting changes, verify:

- Desktop layouts at **100% browser zoom**, including shorter laptop windows
- Mobile layouts and touch controls
- Both themes and languages
- Start, pause, resume, reset, and skip behavior
- Cycle progression and completed-session statistics
- Reloading an active or expired timer
- Settings validation and local persistence
- Keyboard navigation and dialog behavior
- Behavior when notifications or storage are unavailable

### Ideas for Contributions

- [ ] Additional languages
- [ ] Multiple tasks and task history
- [ ] Daily and weekly statistics
- [ ] Settings and statistics export/import
- [ ] PWA installation and offline support
- [ ] Additional completion sounds
- [ ] Cross-tab state synchronization
- [ ] Automated tests for timer and cycle logic

## 📝 What Is the Pomodoro Technique?

The Pomodoro Technique is a time-management method developed by **Francesco Cirillo**. Its name comes from the tomato-shaped kitchen timer he used—*pomodoro* means “tomato” in Italian.

### The Basic Steps

1. 🎯 Choose one task.
2. ⏱️ Set a timer for 25 minutes.
3. 💪 Focus until the timer ends.
4. ☕ Take a 5-minute break.
5. 🔄 After 4 completed sessions, take a longer 15–30 minute break.

Adjust the durations to suit your needs. The goal is a sustainable rhythm of focused work and meaningful rest.

## 📄 License

Licensed under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- Francesco Cirillo for the Pomodoro Technique
- Unsplash for the forest background photograph
- Everyone contributing ideas, improvements, and feedback

---

<p align="center">
  Small steps. Meaningful progress. 🌿
</p>

<p align="center">
  <a href="https://github.com/pomodorotimerj/pomodorotimerj.github.io">⭐ Star this repository if you find it helpful!</a>
</p>
