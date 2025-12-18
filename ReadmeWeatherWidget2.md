# Weather Widget

A beautiful, animated weather widget with real-time weather data. No API key required.

![Weather Widget Preview](https://raw.githubusercontent.com/weatherwidget/weatherwidget.github.io/main/preview.png)

## ✨ Features

- 🌐 **No API Key Required** - Uses free Open-Meteo API
- 📍 **Default Location** - Kyiv, Ukraine
- 💾 **Local Storage** - Saves preferences and weather data
- 🎨 **Animated Weather Icons** - Sun, moon, clouds, rain, snow, storms, fog
- 🌡️ **Unit Toggle** - Celsius / Fahrenheit
- 📱 **Responsive Design** - Works on all screen sizes
- 🔄 **Auto-refresh** - Updates every 15 minutes
- 📍 **Geolocation** - Use current location
- 🔍 **City Search** - Search any city worldwide
- ✨ **Glass Morphism** - Modern frosted glass UI
- 🌈 **Dynamic Themes** - Changes based on weather conditions

## 🌤️ Weather Animations

| Weather | Animation |
|---------|-----------|
| ☀️ Clear (Day) | Rotating sun with glowing rays |
| 🌙 Clear (Night) | Moon with craters + twinkling stars |
| ⛅ Partly Cloudy | Sun with floating clouds |
| ☁️ Cloudy | Multiple floating clouds |
| 🌧️ Rain | Falling raindrops |
| ❄️ Snow | Drifting snowflakes |
| ⛈️ Storm | Heavy rain + lightning flashes |
| 🌫️ Fog | Moving mist layers |

## 🚀 Demo

**Live Demo:** [https://weatherwidget.github.io](https://weatherwidget.github.io)

## 📦 Installation

### Option 1: Direct Use

Simply open `index.html` in your browser.

### Option 2: Clone Repository

```bash
git clone https://github.com/weatherwidget/weatherwidget.github.io.git
cd weatherwidget.github.io
```

Then open `index.html` in your browser.

### Option 3: Download

1. Download the repository as ZIP
2. Extract the files
3. Open `index.html` in your browser

## 🛠️ Usage

### Basic Usage

Just open the widget in any modern browser. It will automatically:
- Load weather for Kyiv, Ukraine (default)
- Save your preferences to local storage
- Auto-refresh weather data every 15 minutes

### Search for a City

1. Type city name in the search box
2. Press Enter or click Search button
3. Weather updates automatically

### Use Current Location

1. Click the location button (📍)
2. Allow browser location access
3. Weather updates for your location

### Change Temperature Unit

Click **°C** or **°F** button to toggle between Celsius and Fahrenheit.

## 💾 Local Storage

The widget saves the following data locally:
- Current location (name, country, coordinates)
- Temperature unit preference
- Last weather data (for offline viewing)
- Last update timestamp

## 🌐 APIs Used

| API | Purpose | Key Required |
|-----|---------|--------------|
| [Open-Meteo](https://open-meteo.com/) | Weather data | ❌ No |
| [Open-Meteo Geocoding](https://open-meteo.com/en/docs/geocoding-api) | City search | ❌ No |
| [Nominatim](https://nominatim.org/) | Reverse geocoding | ❌ No |

## 📁 Project Structure

```
weatherwidget.github.io/
├── index.html      # Main application file
├── README.md       # Documentation
├── LICENSE         # MIT License
└── preview.png     # Preview image
```

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

MIT

## 🔗 Links

- **Repository:** [https://github.com/weatherwidget/weatherwidget.github.io](https://github.com/weatherwidget/weatherwidget.github.io)
- **Live Demo:** [https://weatherwidget.github.io](https://weatherwidget.github.io)
- **Issues:** [https://github.com/weatherwidget/weatherwidget.github.io/issues](https://github.com/weatherwidget/weatherwidget.github.io/issues)

## 🙏 Acknowledgments

- Weather data by [Open-Meteo](https://open-meteo.com/)
- Geocoding by [Nominatim](https://nominatim.org/)
- Font by [Google Fonts (Poppins)](https://fonts.google.com/specimen/Poppins)
