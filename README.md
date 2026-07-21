# 🔥 معاً نحمي غاباتنا — Wildfire Awareness Algeria

> A single-file Arabic wildfire awareness website for Algeria, featuring a live interactive SVG map of all 69 wilayas, real-time weather data, fire risk classification, and emergency contacts.

![HTML](https://img.shields.io/badge/HTML-single--file-orange)
![API](https://img.shields.io/badge/API-Open--Meteo-blue)
![Lang](https://img.shields.io/badge/Language-Arabic%20RTL-green)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## 📸 Preview

The site is fully self-contained in one `.html` file — no build step, no dependencies, no backend.

---

## ✨ Features

### 🗺️ Interactive SVG Map
- Full SVG map of Algeria with all **69 wilayas** drawn as individual paths
- Hover over any wilaya to see its name and fire risk level in a tooltip
- Click a wilaya on the map to instantly load its live weather in the weather widget
- Color-coded risk system:
  - 🔴 **High risk** — northern forested wilayas (Jijel, Béjaïa, Tizi Ouzou, Souk Ahras…)
  - 🟠 **Medium risk** — semi-arid and mixed coverage areas
  - 🟢 **Low risk** — sparse vegetation zones
  - 🟡 **Desert** — Saharan wilayas with no wildfire risk

### 🌤️ Live Weather (Open-Meteo API)
- Real-time temperature, humidity, and wind speed for any wilaya
- **7-day forecast strip** with weather icons and min/max temperatures
- **Auto-locate** using browser Geolocation API with IP-based fallback
- Batch fetches hottest/coldest wilaya rankings across all 69 at startup
- All data from [Open-Meteo](https://open-meteo.com/) — free, no API key required

### 📞 Emergency Contacts
- Dedicated section with free 24/7 emergency numbers (Forest Protection, Civil Protection, SAMU)

### 🛡️ Prevention Tips
- Practical wildfire prevention cards (no smoking, no open fires, no littering)
- Heatwave safety section

### 📊 Official Statistics
- Historical wildfire data sourced from the Direction Générale des Forêts (DGF)

---

## 🚀 Usage

No installation needed. Just open the file in any modern browser:

```bash
git clone https://github.com/your-username/wildfire-algeria.git
cd wildfire-algeria
# Open in browser
open wildfire_algeria.html
# or
start wildfire_algeria.html   # Windows
xdg-open wildfire_algeria.html  # Linux
```

Or deploy directly to **GitHub Pages**, **Netlify**, or any static host — it's one file.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Markup | Pure HTML5 |
| Styling | Vanilla CSS (RTL, Cairo font, responsive) |
| Map | Inline SVG — 69 hand-traced wilaya paths |
| Weather | [Open-Meteo API](https://open-meteo.com/) (free, no key) |
| Geolocation | Browser Geolocation API + IP fallback |
| Scripting | Vanilla JavaScript (no frameworks) |

---

## 📁 Structure

```
wildfire_algeria.html   ← entire project in one file
README.md
```

Everything — HTML, CSS, JavaScript, and the full SVG map — lives in a single file for maximum portability.

---

## 🌍 Language & Direction

The site is written entirely in **Arabic (RTL)** using the [Cairo](https://fonts.google.com/specimen/Cairo) font family, targeting Algerian audiences.

---

## 📡 API Details

Weather data is fetched from Open-Meteo with no authentication:

```
https://api.open-meteo.com/v1/forecast
  ?latitude={lat}&longitude={lon}
  &current=temperature_2m,relative_humidity_2m,wind_speed_10m,weather_code
  &daily=weather_code,temperature_2m_max,temperature_2m_min
  &forecast_days=7
  &timezone=auto
```

Wilaya coordinates are hardcoded for all 69 administrative divisions.

---

## 🤝 Contributing

Pull requests are welcome. If you spot an incorrect wilaya boundary, wrong risk classification, or outdated statistic, feel free to open an issue.

---

## 📜 License

MIT — free to use, modify, and distribute.

---

> Built with ❤️ for Algeria 🇩🇿 — *"معاً نحمي غاباتنا"* — Together we protect our forests.
