# ✅ Application Verifier

A modern, browser-based **BDD scenario testing tool** for web applications. Write, organize, and execute Gherkin-style test scenarios with a Selenium-inspired API — all directly in your browser. No installation, no server, no dependencies beyond a single HTML file.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## ✨ Features

- 🎯 **BDD-Style Testing** — Write scenarios using Given/When/Then/And syntax
- 🇺🇦 **Bilingual Step Support** — Native Ukrainian & English keywords in every step
- 📋 **Scenario Groups** — Organize tests into collapsible, reorderable groups
- ▶️ **Flexible Execution** — Run all, run selected, run group, or run single step
- 🔀 **Enable/Disable Toggles** — Skip steps or entire groups without deleting them
- 📥 **Multi-Format Import** — JSON, YAML, and Gherkin `.feature` files
- 📤 **Multi-Format Export** — Export scenarios in JSON, YAML, or Gherkin
- 📎 **File Upload Testing** — Built-in file manager for `<input type="file">` steps
- 🖼️ **Live Preview** — Embedded iframe shows the target app during test execution
- 📊 **Real-Time Reports** — Stats, progress bar, and detailed test reports
- 📝 **Execution Log** — Timestamped log with color-coded status
- ⏱️ **Configurable Timeouts** — Per-step timeout with abort control
- 🎨 **Modern Dark UI** — Beautiful gradient design with smooth animations
- 💾 **State Persistence** — Scenarios, files, and settings saved in localStorage
- 🔒 **Privacy First** — Everything runs locally, nothing is sent anywhere
- 🚀 **No Backend Required** — Works as a single self-contained HTML file
- 📱 **Responsive Design** — Works on desktop, tablet, and mobile devices

---

## 🚀 Getting Started

### Quick Start

Simply open `index.html` in your web browser. No build process or server required.

### Local Development

Clone the repository:

```bash
git clone https://github.com/applicationverifier/applicationverifier.github.io.git
cd applicationverifier.github.io
```

Open the file in a browser:

```bash
# macOS
open index.html

# Linux
xdg-open index.html

# Windows
start index.html
```

---

## 📖 Usage

1. **Load target app** — Enter your web application URL in the preview panel and click "Load"
2. **Create a scenario group** — Click "➕ New Group" and give it a descriptive name
3. **Add steps** — Add Given/When/Then/And steps using natural language (see [Step Patterns](#-step-patterns))
4. **Attach files (optional)** — Use the "📎 Files" manager to upload files for upload-testing steps
5. **Run tests** — Click ▶ next to individual steps, groups, or use "Run All" / "Run Selected"
6. **View results** — Watch live in the preview, check the logs, or view the detailed report

---

## 📝 Step Patterns

The app supports natural-language BDD steps in both **English** and **Ukrainian**. Click **❓ Help** in the app to see the full list with examples.

### 🌐 Navigation
```gherkin
Given I open https://example.com
Given Відкрити https://example.com
```

### 🖱️ Interactions
```gherkin
When I click on "#submit"
When I type "hello@world.com" into "#email"
When I choose "Ukraine" from "#country"
When натиснути "button.primary"
When ввести "текст" в "#input"
```

### 📎 File Upload
```gherkin
When upload file "photo.jpg" to "#fileInput"
When завантажити file "document.pdf" в "input[name=upload]"
```

### 👁️ Visibility Assertions
```gherkin
Then element "#modal" is visible
Then element ".error" is hidden
Then element "#hidden-field" exists
Then element "#hero" is in viewport
Then елемент "#modal" видимий
```

### ⏳ Waiting
```gherkin
When wait for "#login" to be visible
When wait for ".spinner" to be hidden
When wait 1000
When чекати на "#login" видимим
```

### ✍️ Text & Field Assertions
```gherkin
Then I see "Welcome"
Then I see "Hello" in "#comment"
Then field "#email" has value "test@test.com"
Then бачу "Ласкаво просимо"
```

### 🔽 Select Verification
```gherkin
Then "Ukraine" is selected in "#country"
Then select "#country" has value "UA"
Then select "#country" has text "Ukraine"
Then selected option in "#country" is "Ukraine"
Then "Україна" вибрано в "#country"
```

### 🔗 URL
```gherkin
Then URL contains "/dashboard"
Then URL містить "/dashboard"
```

---

## 🛠️ How It Works

The application uses native browser APIs to execute BDD scenarios against a target web app loaded in an iframe:

| Component | Technology |
|-----------|------------|
| Target App Rendering | HTML5 `<iframe>` with sandbox |
| Element Detection | `querySelector` + `checkVisibility` API |
| Click Simulation | Native `.click()` + hit-testing via `elementFromPoint` |
| Text Input | React/Vue-compatible native setters via `Object.getOwnPropertyDescriptor` |
| File Upload | `DataTransfer` API + `FileReader` for base64 storage |
| Persistence | `localStorage` for state and files |
| YAML Parsing | [js-yaml](https://github.com/nodeca/js-yaml) via CDN |

### Execution Flow

1. **Parse** each step against a library of regex patterns (English + Ukrainian)
2. **Dispatch** matching action to the `TestDriver` class
3. **Wait** for elements with configurable timeout + abort control
4. **Verify** DOM state (visibility, text, values, viewport, etc.)
5. **Report** step status: ✅ passed, ❌ failed, ⏱ timeout, ⏭ skipped

> ⚠️ **CORS Note:** Due to browser security, the iframe can only access same-origin URLs or pages that permit iframe embedding. For cross-origin testing, host the app on the same origin or use a local proxy.

---

## ⚙️ Configuration

### Timeout Settings

- **Per-step timeout** — configurable in the preview toolbar (1–300 seconds)
- **Default:** 15 seconds
- Applies to element-waiting patterns and step execution as a whole

### Import Options

| Option | Description |
|--------|-------------|
| **Auto-run after import** | Immediately execute imported scenarios |
| **Replace existing** | Clear current scenarios before import |

### Supported File Formats

| Format | Extension | Use Case |
|--------|-----------|----------|
| **JSON** | `.json` | Programmatic generation, structured data |
| **YAML** | `.yaml`, `.yml` | Human-readable configs |
| **Gherkin** | `.feature` | Standard BDD tooling compatibility |

### File Upload Limits

- **Max file size:** 10 MB per file
- **Storage:** Files stored as base64 in localStorage (subject to browser quota)

---

## 🌐 Languages

The application interface supports:

- 🇺🇦 **Ukrainian** (Українська)
- 🇬🇧 **English**

Language preference is automatically saved and restored. Step patterns work in **both languages simultaneously** — mix and match freely.

---

## 🐛 Troubleshooting

### "Cannot access iframe content (CORS or not loaded)"

The target page must either:
- Be served from the same origin as the app, or
- Allow embedding via appropriate CORS/`X-Frame-Options` headers

For testing external sites, host both the verifier and the app on the same domain or use a local dev proxy.

### Steps run but nothing happens visually

- Ensure the target URL was loaded (green iframe visible)
- Check the **Logs** tab for detailed step-by-step output
- Verify your selector syntax matches the target DOM

### Import fails with "Expected array of groups"

- **JSON/YAML:** Root must be an array of `{ name, steps: [...] }` objects
- **Gherkin:** File must contain at least one `Feature:` and `Scenario:` block

### File upload step says "File not found in file store"

Upload the file via the **📎 Files** manager first. The file name in the step must match exactly (case-sensitive).

### localStorage quota exceeded

Files stored as base64 consume ~33% more space than raw size. Remove unused files via the Files manager, or reduce the number/size of test files.

---

## 📁 Project Structure

```
applicationverifier.github.io/
├── index.html          # Main application file (all-in-one)
├── README.md           # This file
└── LICENSE             # MIT License
```

---

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-step-pattern`)
3. Commit your changes (`git commit -m 'Add amazing step pattern'`)
4. Push to the branch (`git push origin feature/amazing-step-pattern`)
5. Open a Pull Request

---

## 📝 License

[MIT](LICENSE)

---

## 🔗 Links

- **Repository:** [github.com/applicationverifier/applicationverifier.github.io](https://github.com/applicationverifier/applicationverifier.github.io)
- **Live Demo:** [applicationverifier.github.io](https://applicationverifier.github.io)
- **Issues:** [Report a bug](https://github.com/applicationverifier/applicationverifier.github.io/issues)

---

## 💡 Acknowledgments

Built with native web technologies:

- [MediaQuery API](https://developer.mozilla.org/en-US/docs/Web/API/Window/matchMedia) for responsive design
- [checkVisibility API](https://developer.mozilla.org/en-US/docs/Web/API/Element/checkVisibility) for robust element detection
- [DataTransfer API](https://developer.mozilla.org/en-US/docs/Web/API/DataTransfer) for file upload simulation
- [localStorage API](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage) for state persistence
- [js-yaml](https://github.com/nodeca/js-yaml) for YAML parsing

Inspired by:

- [Cucumber](https://cucumber.io/) — Gherkin syntax
- [Codecept.js](https://codecept.io/) — natural-language step descriptions
- [Playwright](https://playwright.dev/) — modern browser automation

---

Made with ❤️ for QA engineers, developers, and anyone who wants **fast, private, no-setup BDD testing** directly in the browser.
