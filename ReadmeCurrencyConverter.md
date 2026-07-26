# 💱 Currency Converter

<img src="https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5"> <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white" alt="CSS3"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript"> <img src="https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chart.js&logoColor=white" alt="Chart.js"> <img src="https://img.shields.io/badge/API-open.er--api-8DD6F9?style=flat-square&logo=json&logoColor=black" alt="API"> <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="License">

<div align="center">

**A sleek, bilingual currency converter with live exchange rates, historical charts, and full state persistence! 💹🇺🇦**

[Live Demo](https://currencyconverter.github.io) • [Report Bug](https://github.com/CurrencyConverter/CurrencyConverter.github.io/issues) • [Request Feature](https://github.com/CurrencyConverter/CurrencyConverter.github.io/issues)

</div>

---

## ✨ Features

- 💹 **Live Exchange Rates** - Real-time currency conversion powered by the free `open.er-api.com` API (no API key required)
- 🌍 **20 Currencies** - Convert between UAH, USD, EUR, GBP, PLN, JPY, CHF, CAD, CNY, TRY, AUD, NZD, SEK, NOK, DKK, CZK, HUF, INR, KRW, and MXN — each with a flag icon
- 📈 **Historical Charts** - Beautiful gradient-filled line charts rendered with Chart.js
- 📅 **9 Time Periods** - View rate history across 7D, 30D, 90D, 180D, 270D, 1Y, 3Y, 5Y, and 10Y
- 🇺🇦 **Ukrainian by Default** - Full Ukrainian interface with instant English toggle
- 🔄 **Bidirectional Conversion** - Type in either field and the other updates instantly
- ⇄ **Quick Swap** - Instantly swap source and target currencies with an animated button
- 💾 **State Persistence** - Language, currencies, amount, and chart period are saved to `localStorage` and restored on reload
- 📱 **Orientation Support** - Adaptive layouts for both portrait and landscape orientations
- 🎨 **Modern UI** - Glassmorphism card, gradient background, spinning icon, and smooth transitions
- 🔢 **Localized Formatting** - Numbers format according to the selected language locale

---

## 🚀 Quick Start

### Option 1: Visit Online
👉 **[CurrencyConverter.github.io](https://currencyconverter.github.io)**

### Option 2: Run Locally
```bash
# Clone the repository
git clone https://github.com/CurrencyConverter/CurrencyConverter.github.io.git

# Open index.html in your browser
cd CurrencyConverter.github.io
open index.html
```

### Option 3: Download
Download the ZIP file and open `index.html` in any modern browser.

---

## 🎮 Usage

**Conversion:**
- Enter an amount in either the **From** or **To** field — the other updates automatically
- Select currencies from the dropdown menus (20 options with flags)
- `⇄ Swap` - Instantly swap the source and target currencies

**Language:**
- `УКР` - Ukrainian interface (default)
- `ENG` - English interface

**Chart Periods:**
| Button | Period |
|--------|--------|
| 7Д / 7D | 7 days |
| 30Д / 30D | 30 days |
| 90Д / 90D | 90 days |
| 180Д / 180D | 180 days |
| 270Д / 270D | 270 days |
| 1Р / 1Y | 1 year |
| 3Р / 3Y | 3 years |
| 5Р / 5Y | 5 years |
| 10Р / 10Y | 10 years |

> 💡 Your language, currency pair, amount, and selected chart period are automatically saved and restored the next time you open the app.

---

## 📊 How the Rates & Charts Work

The app uses the **`open.er-api.com`** REST API to fetch live exchange rates entirely in the browser — no API key or backend required:

- **Live Rates** - Fetches the current rate for the selected currency pair (`base=from`, reads `rates[to]`)
- **Bidirectional Math** - Converts both directions from a single fetched rate
- **Historical Series** - Since free real-time APIs don't offer a free history endpoint, the historical chart builds a **deterministic, realistic series anchored to the real current rate**
- **Adaptive Sampling** - Long ranges (3–10 years) use ~80 sampled points instead of thousands, keeping the chart fast and readable
- **Scaled Volatility** - Larger time spans display bigger, realistic swings (`√time` scaling)
- **Adaptive Labels** - Short ranges show `DD.MM`; long ranges switch to `Mon YY`

---

## 🛠️ Built With

- Pure HTML5, CSS3, and Vanilla JavaScript
- **[Chart.js](https://www.chartjs.org/)** for responsive gradient line charts
- **[open.er-api.com](https://www.exchangerate-api.com/)** for live exchange-rate data
- **localStorage API** for state persistence
- **Intl.NumberFormat** for locale-aware number formatting
- CSS3 animations, glassmorphism, and responsive media queries
- Inline SVG favicon (no external assets)

---

## 🌐 Live Demo

👉 **[CurrencyConverter.github.io](https://CurrencyConverter.github.io)**

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

MIT License

---

<div align="center">

### 💱 Convert with Confidence! 💱

**Made with ❤️ and live exchange rates**

If you found this project useful, please ⭐ star the repository!

</div>
