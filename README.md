# 🌦️ 7-Day Weather Forecast Dashboard | Power BI

An interactive **7-day weather forecasting dashboard** built in Power BI, designed to turn raw meteorological data into clear, actionable visual insights — temperature trends, humidity, wind speed, UV/air quality, and more, all in one clean, decision-ready view.

---

## 📊 Overview

This project transforms live weather data from **WeatherAPI.com** into a polished, business-intelligence-style dashboard. It's built for anyone who needs a fast, visual snapshot of current and upcoming weather conditions — from logistics and event planning to agriculture and everyday decision-making.

**Business Value:**
- Enables quick, data-driven decisions around weather-sensitive operations (travel, outdoor events, supply chain, agriculture).
- Consolidates multiple weather metrics into a single-pane, executive-friendly view.
- Demonstrates a full ETL → DAX → Visualization pipeline using industry-standard BI tools.

---

## ✨ Key Features & Visuals

- **🌡️ Current & Forecasted Temperature** — Real-time current temperature (`Curr_Temp_C`) alongside a 7-day forecast trend (`Forecast_Temp_C`).
- **💧 Humidity Tracker** — Visualizes relative humidity levels (`humidity`) across the forecast period.
- **🌬️ Wind Speed Gauge** — Displays current wind speed (`Wind_speed`) for quick situational awareness.
- **🫧 Air Quality (PM10) Indicator** — Tracks particulate matter levels (`LeftValue_pm10`) against safe thresholds (`MaxValue`).
- **🔽 Atmospheric Pressure** — Monitors barometric pressure (`Pressure`) trends.
- **🌧️ Rain Probability/Volume** — Highlights expected precipitation (`Rain`).
- **👁️ Visibility Index** — Displays visibility conditions (`visibility`) in km/miles.
- **🕒 Last Updated Timestamp** — Shows data freshness via `Last_updated_Date_curr` so users always know how current the data is.
- **📅 7-Day Rolling Forecast** — A day-by-day breakdown for short-term planning.

---

## 🔄 Data Source & ETL Process

- **Data Source:** [WeatherAPI.com](https://www.weatherapi.com/) — a REST API providing real-time and forecasted weather data in JSON format.
- **Extraction:** Data is pulled via API calls using **Power Query (M Language)**, with the endpoint URL parameterized for location and forecast range.
- **Transformation (Power Query):**
  - Flattened nested JSON responses (current conditions + 7-day forecast arrays) into structured tables.
  - Converted data types (dates, decimals, text) for consistency.
  - Renamed and cleaned columns for readability (e.g., `temp_c` → `Curr_Temp_C`).
  - Removed redundant/unused fields to optimize model size.
  - Applied error handling for null/missing API responses.
- **Modeling (DAX):** Custom measures were created to calculate derived metrics, thresholds (e.g., `MaxValue` for PM10 safety limits), and formatted date/time fields for the report.
- **Load:** Final cleaned tables are loaded into the Power BI data model and connected to report visuals.

---

## 🛠️ Tools & Technologies Used

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard design & data modeling |
| **Power Query (M Language)** | Data extraction & transformation (ETL) |
| **DAX (Data Analysis Expressions)** | Custom measures & calculated metrics |
| **WeatherAPI.com** | Live weather data source (REST API) |
| **Power BI Service** *(optional)* | Publishing & sharing the report online |

---

## 🖼️ Dashboard Preview

![Dashboard Preview](<img width="1281" height="720" alt="gif" src="https://github.com/user-attachments/assets/62757290-b512-40dd-8bf6-5ff8a669e363" />)

<!-- Tip: You can also embed a short GIF walkthrough here, e.g. images/dashboard_demo.gif -->

---

## 🚀 How to Use / View the Dashboard

**Open the .pbix File**
1. Clone or download this repository.
2. Ensure you have [Power BI Desktop](https://powerbi.microsoft.com/desktop/) installed (free).
3. Open `Weather_Forecast_Dashboard.pbix`.
4. If prompted, refresh the data source connection (you may need your own WeatherAPI.com API key — see below).

**Setting Up Your Own API Key:**
1. Sign up for a free key at [WeatherAPI.com](https://www.weatherapi.com/).
2. In Power BI, go to **Transform Data → Data Source Settings** and update the API key parameter.
3. Click **Refresh** to pull live data.

---

## 🔮 Future Enhancements

- 📈 **Historical Weather Trends** — Integrate historical data to enable year-over-year comparisons and seasonal analysis.
- 🚨 **Automated Weather Alerts** — Add conditional alerts (e.g., high wind, poor air quality) using Power Automate integration.
- 🌍 **Multi-City Comparison View** — Allow users to compare forecasts across multiple locations side-by-side.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🙋‍♂️ Author

Built with ☕ and curiosity by **Deepanshu Kumawat**.
📫 Connect on [LinkedIn](https://www.linkedin.com/in/deepanshukumawat31/) 

⭐ If you found this project useful or interesting, consider giving it a star!
