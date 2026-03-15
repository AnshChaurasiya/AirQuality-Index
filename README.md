# AQI Monitor – Greater Noida
IoT-Based Real-Time Air Quality Monitoring Dashboard

## Quick Start

### 1. Install dependencies
```bash
pip install -r requirements.txt
```

### 2. Add your data
Place your Excel file (named `data.xlsx`) in the same folder as `app.py`.

**Required columns:**
| Column | Description |
|--------|-------------|
| DATE | Date (YYYY-MM-DD) |
| TIME | Time (HH:MM:SS) |
| PM2.5 | Particulate matter 2.5 µg/m³ |
| PM10 | Particulate matter 10 µg/m³ |
| AQI | Air Quality Index |
| TEMP. | Temperature in °C |
| HUM. | Humidity in % |
| LATITUDE | GPS latitude |
| LONGITUDE | GPS longitude |

### 3. Run the dashboard
```bash
streamlit run app.py
```

## Features
- 4 KPI cards: PM2.5, PM10, Temperature, Humidity
- SDS011 sensor: PM2.5 & PM10 trend graphs + combined chart
- DHT11 sensor: Temperature & Humidity trends + dual-axis chart
- Color-coded status: Good / Moderate / Unhealthy
- Interactive sensor location map (Folium)
- Spatial PM2.5 pollution heatmap
- Time range filter (1h / 24h / 7d / All)
- Auto-refresh every 10 seconds (toggle)
- Raw data table (expandable)

## Standards Used
| Pollutant | CPCB 24-hr Limit |
|-----------|-----------------|
| PM2.5 | 60 µg/m³ |
| PM10 | 100 µg/m³ |
