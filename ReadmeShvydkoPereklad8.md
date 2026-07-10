# 🌻 ШвидкоПереклад

> Free AI translator with specialized context support for official documents, medical terms, and legal paperwork. Built especially for Ukrainians navigating life abroad.

**🔗 [Open Application](https://shvydkopereklad.github.io/)**

## ✨ Features

- 🌐 **Free translation** — no API keys, no registration, no signup
- 🗣️ **Live speech-to-speech** — speak in one language and hear the translation spoken back automatically in real-time
- 🎯 **Context-aware** — specialized modes for legal, medical, official documents, education, and banking
- 📷 **Photo OCR** — recognize and translate text from document photos directly in your browser
- 🗂️ **Scan history** — every OCR scan is automatically saved with a thumbnail (up to 100 entries)
- 🔍 **Search everywhere** — instantly find any translation across History, Saved & Scans with highlighted matches
- 🕐 **Human-friendly dates** — relative timestamps like "щойно", "5 хв тому", "вчора о 14:30"
- 🎤 **Voice input** — speak instead of typing
- 🔊 **Smart text-to-speech** — listen to translations with one-click stop toggle
- 💬 **Phrasebook** — curated useful phrases for emergencies, medicine, documents, housing, and work
- ➕ **Custom phrases & sections** — build your own phrasebook with auto-translation to fill every language in one click
- 💡 **Rotating tips** — helpful, auto-cycling hints introduce every feature at a glance (dismissible)
- 📚 **History** — automatic saving of your last 200 translations
- ⭐ **Saved translations** — bookmark important translations for quick access (up to 200)
- 💾 **Backup & Restore** — export all your data to a portable ZIP archive and restore it anytime, anywhere
- 🔒 **Privacy-first** — all data stored locally, never leaves your browser
- 📱 **Mobile-optimized** — responsive design for phones, tablets, and desktops
- 🌍 **5 languages** — Ukrainian 🇺🇦 · English 🇬🇧 · Polish 🇵🇱 · German 🇩🇪 · Czech 🇨🇿

## 🚀 How It Works

### Translation Providers (Automatic Fallback)
1. **Google Translate** — primary provider (fastest, best quality)
2. **MyMemory API** — fallback (5000 words/day free)
3. **LibreTranslate** — secondary fallback (public instances)

If one provider fails or is unavailable, the next one automatically takes over — you always get a translation.

### Live Speech-to-Speech Translation
A hands-free conversation mode that turns your device into a real-time interpreter:
- **Full pipeline** — speech recognition → automatic translation → spoken translation, all in one flow
- **Large tap-to-talk button** with clear visual states: idle 🎤, listening (pulsing red ⏹), and processing (⏳)
- **Live transcription** — see your words appear as you speak, with interim results shown in italics
- **🔁 Continuous mode** — after speaking the translation, the app automatically resumes listening for your next phrase, enabling natural back-and-forth conversation
- **🔊 Auto-speak toggle** — turn automatic voice output on or off
- **Swap languages** instantly with the ⇄ button
- **Conversation log** — every exchange is recorded with per-item speak and copy actions
- **Replay button** — hear the last translation again anytime
- Integrated with your translation history and respects daily usage limits

Powered by the Web Speech API for recognition, combined with the same translation providers and text-to-speech engine used throughout the app.

### OCR (Optical Character Recognition)
Powered by [Tesseract.js](https://tesseract.projectnaptha.com/) — runs entirely in your browser using WebAssembly. Images never leave your device. Every successful scan is automatically archived to your scan history with a generated thumbnail, recognized text, and translation.

### Scan History
- Each OCR scan is stored in **IndexedDB** with the full-resolution image, a lightweight thumbnail, recognized text, and translation
- Automatically keeps your **100 newest scans** (older ones are trimmed)
- Full-screen viewer to review the original image alongside text and translation
- Per-scan actions: View, Copy, Speak, Delete

### Custom Phrasebook
Build a personal phrasebook tailored to your own needs:
- **➕ Add phrase** — create your own entries in any built-in or custom section
- **📁 New section** — organize phrases into your own categories (with emoji icons)
- **✨ Auto-translate prefill** — type a phrase in one language, click "Перекласти решту", and all remaining language fields fill automatically using the translation providers
- **Smart fill** — only empty fields are populated, so your manual edits are never overwritten
- **Enter shortcut** — press Enter in the source field to trigger prefill instantly
- Custom phrases display a "Власна" badge and can be deleted individually
- Everything is saved locally and included in your ZIP backups

### Rotating Tips Bar
A friendly hints bar surfaces the app's capabilities without a tutorial:
- Auto-cycles through **17 helpful tips** every 8 seconds with a smooth fade transition
- **Progress bar** shows time until the next tip
- **Clickable dots** to jump to any tip manually (desktop)
- **Pause on hover** so you can read at your own pace
- **Dismissible** — the ✕ button hides it permanently (remembered via LocalStorage)
- **Battery-friendly** — rotation pauses when the browser tab is hidden
- **Random start** — a different tip greets you each session

### Backup & Restore
Portable data ownership powered by [JSZip](https://stuk.github.io/jszip/):
- **💾 Backup** — bundles everything into a single ZIP archive named `shvydkopereklad_YYMMDDHHMM.zip`
- The archive includes your settings, history, saved translations, custom phrases & sections, current photo, and **all scan images** (encoded inside the ZIP)
- **📥 Restore** — load a previously exported archive to instantly bring back all your data on the same or a different device
- Fully offline — no cloud, no server, your archive stays with you

### Text-to-Speech
Built on the Web Speech API with robust handling of browser quirks:
- Async voice loading with smart fallback matching
- Chrome 15-second cutoff bug workaround
- One-click toggle (start/stop) on every speak button
- `onDone` callback support enabling the live conversation flow to resume listening after speech ends
- Auto-stop on tab switch and page unload
- Visual feedback with pulsing red animation while speaking

### Localized Flags
Language selectors and list items use crisp **inline SVG flags** instead of emoji, ensuring consistent rendering across every operating system and browser.

## 📖 Usage

### Text Translation
1. Open the [application](https://shvydkopereklad.github.io/)
2. Select source and target languages
3. Choose a context (optional, improves accuracy for specialized vocabulary)
4. Type, paste, or speak (🎤) your text
5. Click **🔄 Перекласти** (Translate)
6. Listen (🔊), copy (📋), or save (⭐) the result

### Live Conversation
1. Go to the **🗣️ Розмова** tab
2. Select the language you'll speak and the language to translate into
3. Tap the large microphone button and start speaking
4. Watch your words transcribe live, then hear the translation spoken automatically
5. Enable **🔁 Безперервно** (Continuous) to keep the conversation flowing hands-free
6. Toggle **🔊 Автоозвучення** (Auto-speak) on or off as needed
7. Review the full exchange in the conversation log, replay any line, or copy it

### Photo Translation
1. Go to the **📷 Фото** tab
2. Upload a photo or take one with your camera
3. Select source and target languages
4. Click **🔍 Розпізнати і перекласти**
5. Listen to the result with the speak button
6. Your scan is automatically saved to the **🗂️ Сканування** tab

### Scan History
1. Go to the **🗂️ Сканування** tab
2. Browse thumbnails of all your past scans
3. Search by recognized text or translation
4. Tap a thumbnail to open the full viewer
5. View, copy, speak, or delete any scan individually

### Phrasebook
1. Go to the **💬 Фрази** tab
2. Pick a category (Emergency, Medical, Documents, Housing, Work — or your own)
3. Choose target language
4. Tap any phrase to copy and hear it aloud

### Adding Custom Phrases
1. In the **💬 Фрази** tab, click **➕ Додати фразу**
2. Pick the section where the phrase should live
3. Type your phrase in one language and pick it as the source
4. Click **✨ Перекласти решту** (or press Enter) to auto-fill the other languages
5. Review, tweak any translations, and click **Додати**
6. To create a new category, click **📁 Нова секція** and give it a name (emoji optional)

### Saved Translations
1. After translating, click **⭐ Зберегти**
2. Visit the **⭐ Збережені** tab to review
3. Search, open, copy, speak, or delete saved items individually

### Backing Up Your Data
1. Tap **💾** in the header to download a ZIP archive of all your data
2. Store the file safely (cloud drive, USB, email to yourself, etc.)
3. To restore, tap **📥**, select your `.zip` archive, and confirm
4. All history, saved translations, custom phrases, scans, and settings are brought back instantly

## 🛠️ Tech Stack

- Pure HTML, CSS, and JavaScript — no build step, no framework
- [Tesseract.js v5](https://github.com/naptha/tesseract.js) for in-browser OCR
- [JSZip v3](https://github.com/Stuk/jszip) for backup/restore archive handling
- Web Speech API for voice input, live speech recognition, and text-to-speech
- **IndexedDB (v2)** for image storage and scan history — with a dedicated time-indexed `scans` object store
- Canvas-based thumbnail generation (160px JPEG @ 70% quality)
- Inline SVG flags for consistent cross-platform rendering
- LocalStorage for settings, history, saved translations, custom phrases, live conversation preferences, and tips-dismissal state
- Custom modal system (no native browser dialogs) with async validation and form support
- Progressive Web App ready

## 🔒 Privacy

- ✅ No analytics tracking your translations
- ✅ No user accounts or registration
- ✅ Photos are processed locally with Tesseract.js
- ✅ Speech recognition uses your browser's built-in Web Speech API
- ✅ Scanned images and thumbnails are stored only in your browser's IndexedDB
- ✅ History, saved items, custom phrases, and conversation logs live only in your browser
- ✅ Backups are generated locally and never uploaded anywhere — you control the file
- ✅ Translation API calls send only the text being translated
- ✅ Granular clearing — wipe History, Saved, or Scans independently, or one-click "Clear all data" to remove everything instantly

## 🎨 Design

The visual identity draws inspiration from Ukrainian symbols — the blue and yellow flag and the sunflower 🌻 — representing resilience, warmth, and hope. Designed to feel friendly and accessible during stressful situations like medical appointments or document submissions.

## 🎯 Use Cases

- 📋 Translating official documents and government forms
- 🏥 Medical appointments and prescription instructions
- ⚖️ Legal paperwork, contracts, and notarized documents
- 🏠 Housing applications and rental agreements
- 💼 Job applications, CVs, and interview preparation
- 🎓 School enrollment forms and educational materials
- 🏦 Banking documents and financial paperwork
- 🗣️ Real-time conversations with doctors, officials, landlords, or employers
- 📷 Scanning and archiving printed documents for later reference
- 💬 Building a personal phrasebook of expressions you use often
- 💾 Moving your data between devices or keeping an offline backup
- 🆘 Emergency communication when you don't speak the local language

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests on [GitHub](https://github.com/ShvydkoPereklad/ShvydkoPereklad.github.io).

Ways you can help:
- 🐛 Report bugs and edge cases
- 🌍 Suggest additional languages or phrase categories
- 🎨 Improve UI/UX and accessibility
- 📝 Add translations for the interface itself
- ⭐ Star the repository to spread the word

## 📄 License

MIT © 2025-2026 Yuliya Kolesnikova

---

Made with 💙💛 for Ukrainians around the world.

