# 🎓 ДомашкаAI

> Free AI-powered homework helper for Ukrainian students. Explains solutions step by step in Ukrainian — for math, literature, history, and physics — following the national school curriculum.

**🔗 [Open Application](https://domashkaai.github.io/)**

## ✨ Features

- 🤖 **AI homework assistant** — powered by Google Gemini, explains solutions step by step
- 📚 **4 school subjects** — Math 🔢 · Ukrainian Literature 📖 · History of Ukraine 🏛 · Physics ⚡
- 🇺🇦 **Fully Ukrainian** — answers exclusively in Ukrainian, following the national curriculum
- 📸 **Image recognition** — attach a photo of a task and the AI reads and solves it
- 🧮 **Beautiful math formulas** — proper LaTeX rendering of equations (KaTeX)
- 📝 **Step-by-step explanations** — solutions broken into clear "Крок 1, Крок 2…" steps
- 💾 **Persistent dialogs** — all conversations and images saved in IndexedDB, restored on reload
- 🔢 **Per-subject counters** — see how many saved messages each subject has at a glance
- 🎯 **Quick prompts** — one-tap example questions tailored to each subject
- 🌗 **Demo mode** — works without an API key using a built-in knowledge base
- 🔒 **Privacy-first** — API key and history stored locally, nothing sent except to Google
- 📱 **Mobile-optimized** — responsive design for phones, tablets, and desktops (portrait & landscape)

## 🚀 How It Works

### AI Engine (Google Gemini)
The app connects directly to the **Google Gemini API** using your free personal key. You can choose between models:

1. **Gemini 3.5 Flash Lite** — fastest, great for quick questions
2. **Gemini 3.5 Flash** — balanced speed and quality (default)
3. **Gemini 2.5 Pro** — smartest, best for complex tasks

A system prompt tailors every answer to the selected subject, enforces Ukrainian responses, step-by-step formatting, LaTeX math, and child-friendly explanations.

### Demo Mode (No Key Needed)
Without an API key, the app runs in **Demo Mode** — a built-in knowledge base answers common questions (Pythagorean theorem, Ohm's law, "Заповіт" analysis, Cossack era, and more) with fully formatted step-by-step solutions.

### Image Recognition
Attach 📎 or paste a photo of a homework task. Images are automatically resized in-browser and sent to Gemini's multimodal API, which reads the task and solves it.

### Math Rendering
Powered by [KaTeX](https://katex.org/) — renders inline `$...$` and display `$$...$$` LaTeX formulas beautifully and instantly.

## 📖 Usage

### Getting Started
1. Open the [application](https://domashkaai.github.io/)
2. Open ⚙️ **Налаштування** (Settings)
3. Paste your free Gemini API key from [aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
4. Choose a model and save

### Asking a Question
1. Pick a subject from the sidebar (Math, Literature, History, Physics)
2. Type your question, tap a quick prompt, or attach 📎 a photo
3. Press **➤** or Enter
4. Read the step-by-step explanation — copy 📋 it anytime

### Photo Task
1. Click 📎 or paste an image from clipboard
2. Optionally add a text note
3. Send — the AI reads and solves the task from the photo
4. Tap any image to view it full-size in the lightbox

### Managing History
- All dialogs auto-save to IndexedDB and **restore on reload** from the top
- Subject badges show the number of saved messages per subject
- Click 🗑 **Очистити** (Clear) to delete all history after confirmation

## 🛠️ Tech Stack

- Pure HTML, CSS, and JavaScript — no build step, no framework
- [Google Gemini API](https://ai.google.dev/) for AI responses (text + vision)
- [KaTeX v0.16](https://katex.org/) for LaTeX math rendering
- Custom Markdown parser with tables, code blocks, blockquotes, and step highlighting
- IndexedDB for persistent dialogs and images (with auto-repair & version migration)
- LocalStorage for API key and model settings
- Custom modal & confirm system (no native browser dialogs)
- Progressive Web App ready

## 🔒 Privacy

- ✅ No analytics tracking your questions
- ✅ No user accounts or registration
- ✅ API key stored only in your browser
- ✅ Dialogs and images live only in your browser (IndexedDB)
- ✅ API calls send only the text/image being asked — directly to Google
- ✅ One-click "Clear history" button removes everything instantly

## 🎨 Design

The visual identity draws inspiration from Ukrainian symbols — the blue and yellow flag 🇺🇦 and the graduation cap 🎓 — representing knowledge, hope, and a bright future. Designed to feel friendly, encouraging, and easy for children to use while learning.

## 🎯 Use Cases

- 🔢 Solving equations and understanding math theorems step by step
- 📖 Analyzing Ukrainian literary works (theme, idea, artistic devices)
- 🏛 Learning historical events with causes, timeline, and consequences
- ⚡ Solving physics problems with calculations and verification
- 📸 Reading and solving tasks straight from a photo of a textbook
- 🧮 Understanding formulas with clean LaTeX rendering
- 💡 Getting encouraging, curriculum-aligned explanations at home

## 🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests on [GitHub](https://github.com/DomashkaAI/DomashkaAI.github.io).

Ways you can help:
- 🐛 Report bugs and edge cases
- 📚 Suggest additional subjects or curriculum topics
- 🎨 Improve UI/UX and accessibility
- 📝 Expand the demo-mode knowledge base
- ⭐ Star the repository to spread the word

## 📄 License

MIT © 2025-2026 Yuliya Kolesnikova

---

Made with 💙💛 for Ukrainian students.
