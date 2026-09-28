# Drawing Canvas — Studio

A browser-based drawing and painting studio with textured brushes, pen-pressure support, image import, and full-resolution export. Create digital artwork directly in your browser—no installation, account, or external dependencies required.

![License](https://img.shields.io/badge/license-MIT-green.svg)
![Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen.svg)

## 🎨 Live Demo

**[https://drawingcanvas.github.io](https://drawingcanvas.github.io)**

## ✨ Features

### Drawing Tools

- **Paintbrush** — Textured pigment with adjustable softness and bristle detail.
- **Pencil** — Fine strokes with simulated paper grain.
- **Airbrush** — Soft, gradual shading.
- **Marker** — Semi-transparent strokes with multiply blending.
- **Eraser** — Remove pigment to reveal transparency.

Draw with a mouse, touch screen, or pressure-sensitive pen. Supported pens vary stroke size with pressure; mouse and touch input use steady pressure.

### Brush Studio

Six ready-to-use presets:

| Preset | Style |
|--------|-------|
| Paintbrush | Soft, bristled pigment |
| Watercolor | Translucent washes |
| Graphite | Fine paper grain |
| Airbrush | Smooth light and shade |
| Ink | Crisp, clean strokes |
| Marker | Even, transparent ink |

Customize each brush with:

- **Size:** 1–180 px
- **Opacity:** 1–100%
- **Hardness:** 0–100%
- **Texture:** 0–100%
- Optional pen-pressure response
- Live stroke preview

### Shape Tools

- Line
- Rectangle
- Circle/Ellipse
- Triangle
- Filled shapes or outlines
- Adjustable outline width: 1–50 px

Hold **Shift** while drawing to constrain lines to 45-degree increments or use equal width and height for shapes.

### Additional Tools

- **Fill Bucket** — Fill connected areas with adjustable color tolerance and opacity.
- **Eyedropper** — Sample a nontransparent pixel from the canvas.
- **Text Tool** — Place multiline text with customizable typeface, size, bold, and italic styling.

### Color Options

- Native color picker
- Editable hexadecimal color value
- Curated 24-color palette
- Foreground and secondary color swapping

### Canvas Management

- Preset sizes:
  - **Landscape:** 1200 × 800
  - **Square:** 1080 × 1080
  - **Portrait:** 1080 × 1920
  - **Full HD:** 1920 × 1080
- Custom dimensions from 32 to 4096 px per side, up to **8 million total pixels**
- Paper color or transparent background
- Manual zoom from 5% to 400%
- Fit-to-workspace and 100% view
- Scroll to navigate larger canvases
- Clear canvas to transparency
- Undoable canvas creation and image replacement

### Image Import and Export

**Import:**

- PNG, JPEG, WebP, GIF, and BMP
- Replace the canvas or fit an image onto the current canvas
- Drag an image onto the workspace to replace the canvas
- Large images automatically scaled to canvas limits
- Maximum import file size: 40 MB

**Export:**

- **PNG** — Lossless, with transparency
- **JPEG** — Adjustable quality, with a white background
- **WebP** — Adjustable quality, with transparency where supported
- Original canvas resolution, independent of zoom

> GIF imports are treated as a still image. The application does not provide animation editing.

### Local Saving and Artwork Collection

- Save named, lossless PNG copies in **IndexedDB**
- Automatically save the working canvas after changes
- Recover the working canvas when reopening the application
- Browse recent and saved artwork
- Search by name and sort by name or date
- Open, rename, duplicate, download, or delete saved artwork
- Export the collection as a JSON backup
- Import compatible JSON backups
- Recover compatible saved data from the earlier application database

> Artwork is stored in the current browser and site origin—not in the cloud. Clearing site data, using private browsing, or browser storage eviction can remove it. Export important artwork or a collection backup regularly.

### Undo and Redo

- Dimension-aware history for drawing and canvas changes
- Up to **40 history states**
- Memory-managed history with an approximately **80 MiB image-data budget**

Large canvases retain fewer states. The application keeps at least the two most recent states, which may exceed that budget.

### Built-In Inspiration

Load a procedurally generated alpine landscape featuring:

- Atmospheric mountain ridges
- Snowfields and rock detail
- Distorted water reflections
- Textured trees, foreground rocks, and reeds
- Subtle grain and vignette

The landscape is generated locally without external image assets. Paint over it or start with a fresh canvas.

### User Interface

- Dark studio theme
- Responsive desktop and mobile layout
- Mobile settings drawer
- Mouse, touch, and pen input
- Brush-size cursor
- Keyboard shortcuts
- Save-status indicators and toast notifications
- Reduced-motion preference support

## ⌨️ Keyboard Shortcuts

Use **Ctrl** on Windows/Linux or **⌘** on macOS for modifier shortcuts.

| Shortcut | Action |
|----------|--------|
| `B` | Paintbrush |
| `P` | Pencil |
| `A` | Airbrush |
| `M` | Marker |
| `E` | Eraser |
| `L` | Line |
| `R` | Rectangle |
| `C` | Circle/Ellipse |
| `T` | Triangle |
| `F` | Fill bucket |
| `I` | Eyedropper |
| `X` | Text |
| `[` / `]` | Decrease/increase brush size by 2 px |
| `Ctrl/⌘ + Z` | Undo |
| `Ctrl/⌘ + Shift + Z` | Redo |
| `Ctrl/⌘ + Y` | Redo |
| `Ctrl/⌘ + S` | Open Save Artwork |
| `Ctrl/⌘ + 0` | Fit canvas to workspace |
| `+` / `=` | Zoom in |
| `-` | Zoom out |
| `Ctrl/⌘ + Mouse wheel` | Zoom |
| `Shift` while drawing a shape | Constrain proportions or line angle |
| `Esc` | Cancel the active stroke or close settings/dialogs |

Tool shortcuts are inactive while typing in form fields or while a dialog is open.

## 🚀 Getting Started

### Online Usage

Visit **[drawingcanvas.github.io](https://drawingcanvas.github.io)**.

1. Choose a brush preset and color.
2. Adjust size, opacity, hardness, and texture.
3. Paint on the landscape or select **New** for a blank canvas.
4. Select **Save** to keep a named copy in this browser.
5. Select **Export** to download your artwork.

### Run Locally

Open `index.html` directly in your browser, or serve the application directory locally for more consistent browser-storage behavior:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

No build step or package installation is required. Python is only needed for the optional local-server command.

> Browser storage is origin-specific. Artwork saved on the live site will not automatically appear on localhost, another port, or another browser. Use collection backups to transfer it.

## 💾 Backing Up and Restoring Artwork

### Export a Collection Backup

1. Save the artwork you want to include.
2. Open **Browse saved artwork**.
3. Select **Export backup**.
4. Keep the downloaded JSON file somewhere safe.

Collection backups include saved artwork copies, not an unsaved working canvas.

### Import a Collection Backup

1. Open **Browse saved artwork**.
2. Select **Import backup**.
3. Choose a compatible JSON backup.

Imported artwork is added as new saved copies. Backup imports are limited to **100 MB** and **500 entries** per file.

## 🛠️ Technologies Used

- **HTML5** — Application structure and native dialogs
- **CSS3** — Responsive layout, variables, Flexbox, and Grid
- **Vanilla JavaScript** — Application logic without frameworks
- **Canvas 2D API** — Painting, image processing, previews, and export
- **Pointer Events** — Unified mouse, touch, and pen input
- **IndexedDB** — Artwork collection and working-canvas recovery
- **File, Blob, and FileReader APIs** — Image import, downloads, and backups
- **ResizeObserver** — Workspace-aware canvas fitting

## 🔒 Privacy and Storage

Drawing, image processing, and file management run locally in the browser. The application code does not upload artwork to a server or require an account.

Available storage depends on browser settings and device capacity. If storage is unavailable or full, you can still draw and export images.

## 📁 Project Structure

```text
drawingcanvas.github.io/
├── index.html      # Complete application: HTML, CSS, and JavaScript
├── favicon.ico     # Browser tab icon
├── README.md       # Project documentation
└── LICENSE         # MIT License
```

## ⚠️ Current Limitations

- Artwork is edited as a single flattened canvas; there is no editable layer stack.
- Shapes and text become raster content after placement.
- Undo history is memory-limited and does not survive a page reload.
- Local saves are browser-specific, not cloud-synchronized.
- Animated image editing is not supported.
- Large canvases and extensive backups may affect performance on lower-memory devices.

## 🤝 Contributing

Contributions are welcome!

1. Fork the project.
2. Create a feature branch:

   ```bash
   git checkout -b feature/amazing-feature
   ```

3. Commit your changes:

   ```bash
   git commit -m "Add amazing feature"
   ```

4. Push your branch:

   ```bash
   git push origin feature/amazing-feature
   ```

5. Open a pull request.

Please test drawing, undo/redo, import/export, and local saving. For interface changes, also check a narrow mobile viewport.

### Ideas for Contributions

- [ ] Editable layer support
- [ ] Additional brush engines and presets
- [ ] Gradient tool
- [ ] Selection and transform tools
- [ ] Clipboard image paste
- [ ] Filters and effects
- [ ] Accessibility improvements
- [ ] Automated browser tests
- [ ] Optional cloud synchronization
- [ ] Collaborative drawing

## 📝 License

MIT. See [LICENSE](LICENSE) for details.

---

<p align="center">Made with ❤️ for artists and creators everywhere</p>
