# Data Documentation

This folder contains the dataset used for our commodity price forecasting project. The dataset was built from scratch through web scraping and data integration from various sources. The data spans from **December 30, 2019** to **March 31, 2025**.

## Dataset Descriptions

### 📈 Inflation (YoY)
- **Column**: `Inflasi YoY`
- **Description**: Year-on-Year inflation data for West Java Province.
- **Source**: [Badan Pusat Statistik (BPS)](https://jabar.bps.go.id/id/statistics-table/2/NDYjMg==/inflasi-bulanan-tujuh-kota-y-on-y-.html)

### 🌦️ Weather Data
- **Columns**: `Temp Avg`, `Humidity Avg`, `RR`
- **Description**: Average daily temperature, humidity, and rainfall in West Java.
- **Source**: [BMKG Online Climate Data](https://dataonline.bmkg.go.id/dataonline-home)

### 🌾 Commodity Production Data
- **Columns**: `Produksi BM`, `Produksi BP`, `Produksi CR`
- **Description**: Estimated production volume of shallots (bawang merah), garlic (bawang putih), and bird’s eye chili (cabai rawit) in West Java, measured in tons.
- **Source**:
  - 2013–2023 data from [Open Data Jabar](https://opendata.jabarprov.go.id/id/dataset/produksi-bawang-merah-berdasarkan-kabupatenkota-di-jawa-barat)
  - 2024–2025 data generated using linear regression forecasting.

### 💰 Price Data
- **Columns**: `Bawang Merah`, `Bawang Putih`, `Cabai Rawit`
- **Description**: Daily retail prices of shallots, garlic, and bird’s eye chili in West Java.
- **Source**: [PIHPS Nasional (PIHPSN)](https://www.bi.go.id/hargapangan)

### 📅 Event Data
- **Columns**: `is_tahun_baru`, `is_idul_fitri`, `is_natal`
- **Description**: Binary indicators for annual events that have significant correlation with commodity price increases (New Year, Eid al-Fitr, and Christmas).
- **Source**: Processed from an [open API on GitHub](https://github.com/kresnasatya/api-harilibur) to binary format.

---

Please cite the original sources if you use this data.
