# 🍅 Pomodoro Timer

A beautiful, feature-rich Pomodoro Timer application to boost your productivity. Built with pure HTML, CSS, and JavaScript.

![Pomodoro Timer](https://img.shields.io/badge/Pomodoro-Timer-e94560?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## ✨ Features

- **🎯 Focus Sessions** - Customizable work intervals (default 25 minutes)
- **☕ Break Intervals** - Short breaks (5 min) and long breaks (15 min)
- **🔔 Sound Notifications** - Pleasant audio alerts when sessions complete
- **📱 Browser Notifications** - Get notified even when the tab is in the background
- **💾 Persistent Timer** - Timer continues running even after page reload
- **🌓 Theme Toggle** - Switch between dark and light modes
- **🌍 Bilingual Support** - Ukrainian (default) and English languages
- **ℹ️ Info Section** - Learn about Pomodoro Technique right in the app
- **📊 Statistics** - Track completed pomodoros and total focus time
- **⚙️ Customizable Settings** - Adjust durations and preferences
- **⌨️ Keyboard Shortcuts** - Quick controls for power users
- **📱 Responsive Design** - Works on desktop and mobile devices
- **🎨 Beautiful UI** - Modern design with smooth animations

## 🚀 Demo

Visit the live application: [https://pomodorotimerj.github.io](https://pomodorotimerj.github.io)

## 🎮 Usage

### Basic Controls

| Action | Button | Keyboard Shortcut |
|--------|--------|-------------------|
| Start/Pause | ▶/⏸ | `Space` |
| Reset | ↺ | `R` |
| Skip Session | ⏭ | `S` |
| Show Info | ℹ️ | `I` |

### Timer Modes

- **Focus** - Work session (default: 25 minutes)
- **Short Break** - Quick rest (default: 5 minutes)
- **Long Break** - Extended rest after 4 pomodoros (default: 15 minutes)

### Settings

Click the ⚙️ Settings button to customize:

- Focus duration (1-60 minutes)
- Short break duration (1-30 minutes)
- Long break duration (1-60 minutes)
- Sessions until long break (2-10)
- Sound notifications toggle
- Auto-start breaks
- Auto-start pomodoros

### Language

Click the language button (🇺🇦/🇬🇧) in the header to switch between:

- 🇺🇦 Українська (Ukrainian) - Default
- 🇬🇧 English

### Theme

Click the theme button (☀️/🌙) to toggle between:

- 🌙 Dark mode
- ☀️ Light mode

## 📦 Installation

### Option 1: Direct Use
Simply open `index.html` in your web browser.

### Option 2: Clone Repository
```bash
git clone https://github.com/pomodorotimerj/pomodorotimerj.github.io.git
cd pomodorotimerj.github.io
```

Then open `index.html` in your browser.

### Option 3: GitHub Pages
Fork this repository and enable GitHub Pages in your repository settings.

## 🛠️ Technical Details

### Technologies Used

- **HTML5** - Structure and semantics
- **CSS3** - Styling, animations, and responsive design
- **Vanilla JavaScript** - Application logic and state management
- **Web Audio API** - Sound notifications
- **Local Storage API** - Persistent data storage
- **Notifications API** - Browser notifications

### Key Technical Features

- **Persistent Timer** - Timer state is saved to localStorage and continues accurately even after page reload
- **Visibility API** - Timer stays accurate when tab is in background
- **Custom Modal System** - Beautiful popup dialogs instead of browser confirms
- **CSS Variables** - Easy theming with CSS custom properties
- **i18n Support** - Built-in internationalization system for multiple languages

## 📁 Project Structure

```
PomodoroTimerj.github.io/
├── index.html      # Main application file (HTML + CSS + JS)
├── README.md       # Documentation
└── LICENSE         # MIT License
```

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Ideas for Contributions

- [ ] Add more languages
- [ ] Add task list integration
- [ ] Add daily/weekly statistics
- [ ] Add export/import settings
- [ ] Add PWA support for offline use
- [ ] Add custom sound options

## 📝 What is the Pomodoro Technique?

The Pomodoro Technique is a time management method developed by Francesco Cirillo in the late 1980s. The name comes from the tomato-shaped kitchen timer (Italian: "pomodoro") that Cirillo used while studying at university.

### The Basic Steps:

1. 🎯 Choose a task to work on
2. ⏱️ Set the timer for 25 minutes (one "pomodoro")
3. 💪 Work on the task until the timer rings
4. ☕ Take a short 5-minute break
5. 🔄 After 4 pomodoros, take a longer 15-30 minute break

### Benefits:

- ✅ Improves concentration and focus
- ✅ Reduces mental fatigue
- ✅ Increases productivity
- ✅ Helps fight procrastination
- ✅ Improves planning and time estimation

## 📄 License

This project is licensed under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- Inspired by the Pomodoro Technique® by Francesco Cirillo
- Icons and emojis from Unicode Standard
- Built with ❤️ for the productivity community

---

<p align="center">
  Made with ❤️ for productivity enthusiasts
</p>

<p align="center">
  <a href="https://github.com/pomodorotimerj/pomodorotimerj.github.io">⭐ Star this repository if you found it helpful!</a>
</p>
