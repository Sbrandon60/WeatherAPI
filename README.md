# 🌤️ Weather App

A Python desktop application that fetches and displays real-time weather data for any city in the world, built with a PyQt5 GUI and the OpenWeatherMap API.

---

## 🔍 Overview

Weather App provides a clean, responsive desktop interface for looking up current weather conditions. Enter any city name and instantly see the temperature, weather description, and a contextual emoji — with full error handling for every failure mode.

---

## 📸 Screenshot

> _Add a screenshot of the running app here_

---

## ⚙️ Features

- **Real-time weather lookup** — fetches live data from the OpenWeatherMap API
- **Desktop GUI** — built with PyQt5, fully styled with custom CSS-like QSS
- **Dynamic weather emojis** — maps OpenWeatherMap condition codes to visual icons (thunderstorm, snow, fog, tornado, and more)
- **Comprehensive error handling** — catches and displays user-friendly messages for every HTTP error code (400, 401, 403, 404, 500, 502, 504) plus connection, timeout, and redirect errors
- **Secure API key management** — loaded from environment variable, never hardcoded

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.10+ | Core logic (uses `match/case` syntax) |
| PyQt5 | Desktop GUI framework |
| `requests` | HTTP calls to OpenWeatherMap API |
| OpenWeatherMap API | Live weather data source |
| `python-dotenv` | Environment variable management |

---

## 📂 Project Structure

```
weather-app/
│
├── weather_app.py       # Main application
├── .env.example         # Template for API key setup
├── .gitignore           # Excludes .env from version control
├── requirements.txt     # Dependencies
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/weather-app.git
cd weather-app
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Set up your API key
Get a free API key from [OpenWeatherMap](https://openweathermap.org/api), then:

```bash
cp .env.example .env
```

Open `.env` and add your key:
```
OPENWEATHER_API_KEY=your_api_key_here
```

### 4. Run the app
```bash
python weather_app.py
```

---

## 🌩️ Error Handling

The app handles every failure gracefully — no crashes, just clear user-facing messages:

| Error | Message Shown |
|-------|--------------|
| 400 Bad Request | "Bad request: Please check your input." |
| 401 Unauthorized | "Unauthorized: Invalid API key." |
| 404 Not Found | "Not found: City not found" |
| 500 Server Error | "Internal server error: Please try again later." |
| Connection Error | "Check your internet connection." |
| Timeout | "The request timed out." |

---

## 📄 requirements.txt

```
PyQt5
requests
python-dotenv
```

---

## 💡 Future Improvements

- [ ] Add 5-day forecast view
- [ ] Toggle between °F and °C
- [ ] Search history / saved cities
- [ ] Auto-detect location on launch

---

## 📄 License

MIT License — free to use and modify.
