# XML ⇄ JSON Converter

A free, fast, and modern online tool to convert between XML and JSON formats. Convert, format, and download your data instantly with a clean, responsive interface.

🔗 **Live Demo:** [xmltojson.github.io](https://xmltojson.github.io)

## Features

- **Bidirectional Conversion**
  - XML → JSON
  - JSON → XML
  - XML → JSON (Minimum)
  - JSON → XML (Minimum)

- **Flexible Input Methods**
  - Paste content directly
  - Upload local files (📁 File)
  - Load from a URL (with automatic CORS proxy fallback)

- **Formatting Options**
  - Multiple indentation styles: 2 Spaces, 3 Spaces, 4 Spaces, Tabs, or Compact
  - One-click format for both input and output

- **Convenient Layout & Controls**
  - Horizontal or vertical panel layout
  - Swap input/output with a single click
  - Copy to clipboard
  - Download results with custom filenames
  - Keyboard shortcut: `Ctrl+Enter` / `Cmd+Enter` to convert

- **Smart UX**
  - Auto-detects conversion direction based on content
  - Persists your session state in local storage
  - Clean, modern gradient UI with modal dialogs
  - Fully responsive (mobile-friendly)

## Usage

1. Open the application in your browser.
2. Choose your conversion direction (or let it auto-detect).
3. Provide input by pasting, uploading a file, or loading from a URL.
4. Click **⚡ Convert** (or press `Ctrl+Enter`).
5. Copy or download the converted result.

### URL Loading

When loading data from a URL, the app attempts a direct fetch first, then falls back through several public CORS proxies (`allorigins`, `corsproxy.io`, `codetabs`) if needed. If all attempts fail, download the file locally and use the **📁 File** option.

## Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl+Enter` / `Cmd+Enter` | Convert |
| `Enter` (in URL field) | Load from URL |
| `Esc` | Close open modal |

## Technology

- Pure HTML, CSS, and JavaScript — no build step required.
- Conversion logic powered by a compiled GWT library (`xmltojson.nocache.js`).
- Runs entirely in the browser; your data never leaves your machine (except when using URL proxies).

## Installation

No installation needed for usage. To run locally:

```bash
git clone https://github.com/xmltojson/xmltojson.github.io.git
cd xmltojson.github.io
```

Open `index.html` in your browser, or serve it with any static file server:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request at the [repository](https://github.com/xmltojson/xmltojson.github.io).

## License

MIT
