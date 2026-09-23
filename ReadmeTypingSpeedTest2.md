# ⌨️ Typing Speed Test

A modern, multilingual typing speed test with live feedback, personal statistics, and achievements. A calm workspace-inspired design helps you focus on building faster, more accurate typing habits.

![Typing Speed Test](https://img.shields.io/badge/HTML-CSS-JavaScript-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## 🌐 Demo

[https://typingspeedtestj.github.io](https://typingspeedtestj.github.io)

## ✨ Features

- **4 Languages** — English, Ukrainian, Russian, and German.
- **32 Original Passages** — Eight passages per language, shuffled for each test.
- **3 Time Modes** — Practice for 30, 60, or 120 seconds.
- **First-Keystroke Timer** — Prepare at your own pace; timing begins when you type.
- **Live Statistics** — Track CPM, WPM, accuracy, and typing errors.
- **Character Feedback** — See correct characters, mistakes, and your current position.
- **Progress Tracking** — View practice days, monthly summaries, and daily results.
- **Personal Statistics** — Review your best speed, recent averages, and speed trend.
- **Test History** — Store up to 100 recent results and display the latest 20.
- **CSV Export** — Download saved results for your own analysis.
- **12 Achievements** — Celebrate milestones in speed, accuracy, and consistency.
- **Daily Rewards** — Earn visit-streak bonuses, stars, and points.
- **Visual Keyboard** — A desktop US-layout guide highlights physical keys as you type.
- **Responsive Design** — Layouts adapt to desktop, tablet, and mobile screens.
- **Accessibility Features** — Keyboard navigation, labeled controls, native dialogs, live announcements, and reduced-motion support.
- **Local Progress Storage** — No account or backend required.

## 🚀 Quick Start

1. Clone the repository:

   ```bash
   git clone https://github.com/typingspeedtestj/typingspeedtestj.github.io.git
   ```

2. Enter the project folder:

   ```bash
   cd typingspeedtestj.github.io
   ```

3. Open `index.html` in a modern browser.

No build step or package installation is required.

## 🎯 How to Use

1. Choose your practice language.
2. Select a duration: **30**, **60**, or **120 seconds**.
3. Click **Start test**.
4. Type the displayed passage. Your first character starts the timer.
5. Match capitalization, spaces, and punctuation.
6. Use Backspace to correct mistakes when needed.
7. Review your results and try again.

### Test Behavior

- Each full-length passage advances automatically, even if it contains mistakes.
- A test ends when time runs out or all eight passages are completed.
- Language, duration, application navigation, and help are locked during a test.
- **Reset** discards the current attempt without saving a result.
- The timer continues when you switch browser tabs.
- Pasting and dropping text into the typing field are disabled.
- **Tab** moves between controls normally.

## ⌨️ Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `Enter` | Start from the typing-test section when not editing or focused on a button/link |
| `Esc` | Reset the current test or close an open dialog |
| `Ctrl + Enter` / `⌘ + Enter` | Try again while the results dialog is open |
| `Tab` / `Shift + Tab` | Move between interactive controls |
| `F1` | Open help outside an active test |
| `1`–`4` | Switch between Typing Test, Calendar, Statistics, and Achievements |
| `Alt + 1`–`4` | Select English, Ukrainian, Russian, or German |

> Section and language shortcuts are inactive while typing, during an active test, or while a dialog is open. Some browser or operating-system shortcuts may take precedence.

## 📊 Understanding Your Results

### Characters per Minute — CPM

CPM measures the correct characters remaining in your typed text, including completed passages, per minute:

```text
CPM = correct characters ÷ elapsed minutes
```

Spaces and punctuation count. The live speed display remains at zero during the first second to avoid misleading initial spikes.

### Words per Minute — WPM

WPM uses the standard five-character word convention:

```text
WPM = CPM ÷ 5
```

### Accuracy

Accuracy measures correct character-entry attempts:

```text
Accuracy = correct character-entry attempts ÷ total character-entry attempts × 100
```

- Each newly entered incorrect character adds an error.
- Correcting a mistake does not erase the original incorrect attempt.
- Deletions do not add errors.
- CPM reflects correct text retained, while accuracy reflects your entry attempts.

### Statistics and History

- **Average CPM and accuracy:** Based on up to 100 recent saved tests.
- **Best CPM and total tests:** Tracked across all completed tests.
- **Recent history:** Displays the latest 20 results.
- **Speed trend:** Plots up to 20 recent results.
- **CSV export:** Includes all currently retained history entries, up to 100.

## ⭐ Scoring

| Stars | Requirements |
|-------|-------------|
| ⭐⭐⭐ | At least 95% accuracy and 200 CPM |
| ⭐⭐ | At least 85% accuracy and 150 CPM |
| ⭐ | Finish a test with at least one correct character |

Points are calculated as:

```text
Points = round(
    CPM × (accuracy ÷ 100)
    + stars × 50
    + completed passages × 20
)
```

A test with no correct characters earns **zero test points and stars**.

### Daily Visit Rewards

Each new daily visit earns:

- **1 bonus star**
- **Visit streak × 10 bonus points**

Consecutive daily visits extend your streak. Missing a day resets the current visit streak to one on your next visit.

> A **visit streak** counts consecutive visits. A **practice day** requires at least one completed test. Calendar summaries count practice days, not visits alone.

## 🏆 Achievements

Unlocked achievements remain saved.

| Achievement | Requirement |
|-------------|-------------|
| 🎯 First Steps | Complete your first test |
| ⚡ Speed Demon | Reach 300 CPM |
| 💯 Perfectionist | Finish with no typing errors and at least one correct character |
| 📈 Consistent | Complete 10 tests |
| 🔥 Dedicated | Build a 7-day visit streak |
| 🌍 Polyglot | Complete tests in all four languages |
| 🏃 Marathon | Complete 50 tests |
| ⚡ Lightning | Reach 400 CPM |
| 🗓️ Week Warrior | Practice on seven different days |
| 👑 Master | Complete 100 tests |
| 🔥 Streak Master | Build a 30-day visit streak |
| 🎯 Accuracy King | Reach at least 95% average accuracy after completing a test |

### External Resources and Offline Use

The application uses:

- **Google Fonts** for typography
- **Unsplash** for the workspace photograph

These services receive normal browser requests when their resources are loaded.

The typing logic does not require a backend. If external assets are unavailable, fallback fonts and a built-in CSS desk illustration are used.

> Local storage is not an offline cache. This application does not include a service worker or guaranteed offline loading of the hosted page. A downloaded copy can run locally without the external fonts or photograph.

## 📁 Project Structure

```text
├── index.html    # Complete application: HTML, CSS, and JavaScript
├── favicon.ico   # Browser icon referenced by the HTML
└── README.md     # Project documentation
```

## 🛠️ Technologies

- **HTML5** — Semantic layout and native dialogs
- **CSS3** — Responsive layouts, visual keyboard, and fallback illustration
- **Vanilla JavaScript** — Test logic, scoring, and interface behavior
- **LocalStorage API** — Local progress persistence
- **SVG** — Speed-trend chart
- **Blob and URL APIs** — CSV downloads
- **Performance API** — Elapsed-time measurement

No JavaScript frameworks or build tools are required.

## 🌍 Deployment

The application can be hosted on any static hosting service.

For GitHub Pages:

1. Place `index.html`, `favicon.ico`, and `README.md` in the repository.
2. Open **Settings → Pages**.
3. Select **Deploy from a branch**.
4. Choose the appropriate branch and root folder.
5. Save and wait for deployment.

## 🤝 Contributing

Contributions are welcome.

1. Fork the repository.
2. Create a branch:

   ```bash
   git checkout -b feature/improvement
   ```

3. Make and test your changes.
4. Commit:

   ```bash
   git commit -m "Add feature"
   ```

5. Push:

   ```bash
   git push origin feature/improvement
   ```

6. Open a pull request.

### Contribution Guidelines

- Preserve the **eight original passages per language**.
- Keep the favicon link in the HTML.
- Maintain keyboard accessibility and responsive layouts.
- Respect reduced-motion preferences.
- Avoid introducing unnecessary dependencies.
- Test scoring, corrections, passage transitions, and timer behavior.
- Verify that the application remains usable when local storage or external resources are unavailable.

## 📄 License

Released under the **MIT License**.
