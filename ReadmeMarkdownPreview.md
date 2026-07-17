# 📝 Markdown Переглядач / Markdown Previewer

A beautiful, feature-rich Markdown editor with live preview, syntax highlighting, and multi-format export capabilities. Built as a single-file HTML application, hosted on [Base44](https://base44.com).

![Version](https://img.shields.io/badge/version-1.0-7c3aed)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-Base44-ec4899)

## ✨ Features

### 📝 Editor & Preview
- **Live preview** with real-time Markdown rendering
- **Syntax highlighting** for code blocks (powered by highlight.js)
- **GitHub Flavored Markdown (GFM)** support — tables, task lists, strikethrough, and more
- **Split-pane interface** with toggle between horizontal and vertical layouts
- **Character, word, and line counter** in the status bar
- **Tab key support** for indentation in the editor

### 🌍 Internationalization
- **Ukrainian** (Українська) and **English** interface
- One-click language toggle
- Language preference saved between sessions

### 🎨 Themes
- **Dark theme** (default) with purple/pink gradient accents
- **Light theme** for daytime reading
- Smooth transitions between themes
- Syntax highlighting adapts to the selected theme

### 💾 Import & Export
- **Import from local file** (.md, .markdown, .txt)
- **Import from URL** — load Markdown files from any public URL
- **Drag & drop** file support
- **Export as Markdown** (.md)
- **Export as HTML** — standalone styled HTML document
- **Export as PDF** — with full Cyrillic and Unicode support using system fonts

### 🔒 Storage
- **Server-side storage** via Base44 platform
- **Automatic saving** — your content is preserved between sessions
- Settings (language, theme, layout, last URL) are persisted
- No data loss on page reload

### 🎯 Additional Features
- **Copy HTML** to clipboard
- **Load sample content** to explore features quickly
- **Toast notifications** for user feedback
- **Fully responsive** design — works on desktop, tablet, and mobile
- **Accessibility** — semantic HTML and keyboard navigation

## 🚀 Getting Started

### Using the App

1. **Open the application** on Base44
2. **Start writing** Markdown in the left panel (or top panel in vertical mode)
3. **See instant preview** in the right panel (or bottom panel)
4. **Use the toolbar** to switch languages, themes, or export your work

### Quick Actions

| Button | Action |
|--------|--------|
| 🇺🇦 UA / EN | Switch interface language |
| 🌙 / ☀️ | Toggle dark/light theme |
| ⬌ / ⬍ | Switch between horizontal and vertical layout |
| 📂 Файл / File | Load a local Markdown file |
| 🔗 URL | Load Markdown from a web URL |
| 🗑 Очистити / Clear | Clear the editor |
| ✨ Приклад / Sample | Load sample content |
| 📋 Копіювати HTML / Copy HTML | Copy rendered HTML to clipboard |
| 💾 MD | Export as Markdown file |
| 🌐 HTML | Export as standalone HTML file |
| 📄 PDF | Export as PDF (with Cyrillic support) |

## 🛠️ Technology Stack

Built with vanilla JavaScript and industry-standard libraries — no build tools required:

- **[marked.js](https://github.com/markedjs/marked)** — Fast Markdown parser
- **[highlight.js](https://github.com/highlightjs/highlight.js)** — Syntax highlighting for 190+ languages
- **[html2canvas](https://github.com/niklasvh/html2canvas)** — HTML rasterization for PDF export
- **[jsPDF](https://github.com/parallax/jsPDF)** — Client-side PDF generation

All dependencies are loaded from CDN — no installation needed.

## 📖 Supported Markdown Features

- **Headings** (H1–H6)
- **Emphasis** — bold, italic, strikethrough
- **Lists** — ordered, unordered, nested
- **Links** and **images**
- **Code** — inline and fenced blocks with syntax highlighting
- **Blockquotes**
- **Tables** with header styling
- **Horizontal rules**
- **Task lists** (GFM)
- **Line breaks** and paragraphs

## 🌐 Hosting

This application is hosted on **[Base44](https://base44.com)** with server-side storage, ensuring:

- �� Persistent user data across sessions
- ✅ Reliable uptime and fast delivery
- ✅ No client-side data loss
- ✅ Automatic scaling

## 📄 File Structure

Single-file application — everything (HTML, CSS, JavaScript) is contained in `index.html`. This makes the app:

- Easy to deploy
- Easy to modify
- Portable across platforms
- Fast to load

## 🎨 Design Highlights

- **Gradient accents** — purple to pink signature palette
- **Smooth animations** — button hovers, toasts, theme transitions
- **Custom scrollbars** matching the theme
- **Backdrop blur effects** on modals
- **Pulse animation** on the autosave indicator
- **Modern typography** with system font stack

## 🐛 Known Limitations

- **PDF export** rasterizes text (rendered as image) to guarantee correct Unicode/Cyrillic display using system fonts. Text in the PDF is not selectable — this is a deliberate trade-off for zero font downloads.
- **URL import** requires the target server to allow CORS.

## 📜 License

MIT
