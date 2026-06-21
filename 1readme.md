# Global Fleet Telemetry & Risk Analytics Dashboard

## 📌 Project Overview
This repository contains an end-to-end data pipeline and business intelligence solution designed to monitor global fleet performance, analyze logistical delays, and track revenue realization for an international supply chain network. 

The project bridges backend data engineering using **Python (Pandas)** and advanced analytical reporting using **Power BI** over a simulated corporate cycle (2024–2026).

---

## 🛠️ Tech Stack & Architecture
* **Data Engineering:** Python 3.x, Pandas, NumPy (Data cleaning, timeline scaling, geospatial clustering)
* **Database Logic:** SQL (Structured queries for master telemetry data consolidation)
* **Business Intelligence:** Power BI Desktop (DAX modeling, interactive UI design, UI/UX optimization)

---

## 🚀 Key Features & Operational Logic

### 1. Geospatial Optimization (Fixed Hub Analysis)
To prevent map cluttering and overlapping coordinates, raw geospatial data was clustered around **6 major European shipping hubs** (Paris, London, Lyon, Amsterdam, Brussels, Marseille) using Pandas. 
* **Dynamic Interaction:** Slicing by `Asset_ID` dynamically scales the **bubble sizes** on the map rather than scattering dots, instantly pinpointing high-load bottlenecks and waiting-time spikes for individual trucks.

### 2. Clean Data Modeling
* Utilized a high-performance **Denormalized Flat-Table Architecture** optimized for streaming IoT telemetry feeds.
* Isolated business metrics by writing **Explicit DAX Measures** housed inside a dedicated `All_measures` table to keep the data model pristine.

### 3. Multi-Page Synchronized Application
* **Page 1: Executive Summary:** Tracks overall fleet waiting times and categorizes primary drivers of delays (Traffic, Weather, Mechanical).
* **Page 2: Fleet & Risk Analytics:** Monitors core asset distribution across dynamic traffic statuses (*Clear, Heavy, Detour*).
* **Page 3: Supply Chain & Finance:** Benchmarks actual transactional revenue against demand forecasts to spot financial deficits.

---

## 📊 Dashboard Previews
*Insert your dashboard page screenshots below to instantly impress recruiters browsing your repository.*

### Page 1: Executive Summary
![Executive Summary](Screenshots/executive_summary.png)

### Page 2: Fleet & Risk Analytics
![Fleet Analytics](Screenshots/fleet_risk_analytics.png)

---

## 📝 How to Run This Project
1. Clone the repository: `git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git`
2. Run `Scripts/data_cleaning.py` to regenerate the scaled geospatial dataset.
3. Open `Dashboard/Fleet_Telemetry_Dashboard.pbix` in Power BI Desktop and hit **Refresh** to reload the pipeline.