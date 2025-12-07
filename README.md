# 🌍 Global Holidays & Travel Data Visualization

![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)

## 📖 Project Overview

The **Global Holidays and Travel Data Visualization** project is an interactive business intelligence tool designed to analyze the relationship between global holiday patterns, tourist arrivals, and travel expenditures.

By integrating historical tourism data (**1995–2025**) with a comprehensive database of global public holidays, this dashboard enables stakeholders—such as travel agencies, tourism boards, and policymakers—to identify seasonal trends, monitor post-pandemic recovery, and compare economic tourism metrics across different regions.

---

## 📊 Dashboard Previews & Features

This project contains three distinct dashboards, each focusing on specific KPIs.

### 1️⃣ Global Tourism Overview Dashboard
**Key Features:**
* Total arrivals, receipts, and growth indicators.
* Arrivals over the years vs. Receipts.
* High/Moderate/Declining growth distribution.
* Average growth patterns by region.
![Global Tourism Overview](https://github.com/aatisharote07/Global_Tourism_Dashboard/blob/main/Screenshots/Dashboard-1.png?raw=true)

### 2️⃣ Tourism Receipts & Trends Dashboard
**Key Features:**
* Global tourism receipts heat map.
* Yearly receipts trend by region.
* Receipts vs. Arrivals scatter visualization (Volume vs. Value).
* Country-level drill-down filters.

![Trends Dashboard](https://github.com/aatisharote07/Global_Tourism_Dashboard/blob/main/Screenshots/Dashboard-2.png?raw=true)
### 3️⃣ Global Holidays Dashboard
**Key Features:**
* Ranking of countries by holiday count.
* Global holiday distribution map.
* Holiday type breakdown (Public, Observance, Local, etc.).
* Trend of holidays over the years and seasonality by month.

![Holidays Dashboard](https://github.com/aatisharote07/Global_Tourism_Dashboard/blob/main/Screenshots/Dashboard-3.png?raw=true)
---

## 🎯 Business Objectives

This project aims to answer the following key business questions:

* **Trend Analysis:** How have global tourism arrivals and expenditures evolved over the last 30 years (1995–2025)?
* **Pandemic Impact:** Quantifying the economic impact of COVID-19 on the tourism sector and tracking the "V-shaped" recovery curve.
* **High-Value Destinations:** Identifying which countries generate the highest revenue per tourist (Receipts vs. Arrivals).
* **Holiday Context:** Providing a calendar view of public holidays to help travel planners anticipate demand spikes in specific regions.

---

## 🛠️ Tech Stack & Workflow

### 1. Data Collection
* **Tourism Data:** Historical data collected from **UNWTO** (United Nations World Tourism Organization) and World Bank Open Data.
* **Holiday Data:** Global holiday calendars fetched via public APIs and government tourism websites.

### 2. Data Preprocessing (Python & Excel)
* **Cleaning:** Handled missing values (NaNs) in the historical dataset using **Python (Pandas)** to ensure continuity in time-series visualization.
* **Transformation:** Standardized Country Codes (ISO3) to enable accurate mapping between the Holiday and Tourism datasets.
* **Feature Engineering:** Created a `COVID_Anomaly` flag to isolate 2020-2021 data for specific variance analysis.

### 3. Data Modeling (Power BI)
* **Star Schema Design:**
    * **Fact Tables:** `Global_Tourism` (Annual Granularity) and `Global_Holidays` (Daily Granularity).
    * **Dimension Tables:** Created a master `Date Table` to bridge the granularity difference between annual tourism numbers and daily holiday dates.
* **DAX Measures:** Calculated metrics for *Year-over-Year (YoY) Growth*, *Pre-Pandemic Recovery %*, and *Average Receipt per Arrival*.

---

## 💡 Key Insights

* **The 2020 Shock:** The dashboard visualizes a **~72% drop** in global tourist arrivals in 2020 compared to 2019, highlighting the severity of the pandemic's impact.
* **Recovery Trajectory:** 2024 and 2025 projections indicate a return to **95%+ of pre-pandemic volume**, driven largely by the reopening of Asian markets.
* **Volume vs. Value:** While countries like **France** lead in total *Arrivals*, the **United States** often leads in *Receipts*, indicating a higher average spend per visitor.
* **Micro-Seasons:** The Holiday dataset reveals clusters of public holidays in Q1 and Q4 for many regions, suggesting prime windows for domestic tourism marketing.
## 📂 File Structure

```text
├── Data/
│   ├── Global_Tourism_1995_2025_Cleaned.xlsx  # Annual tourism metrics
│   ├── global_holidays.csv                    # Daily holiday data
├── Dashboards/
│   ├── Tourism_Dashboard.pbix                 # The Power BI Source File
├── Images/
│   ├── Dashboard-1.png                        # Overview Screenshot
│   ├── Dashboard-2.png                        # Trends Screenshot
│   ├── Dashboard-3.png                        # Holidays Screenshot
└── README.md



```
---
## 🚀 Future Improvements
Granularity Upgrade: Sourcing monthly tourism arrival data to allow for direct correlation analysis between specific holidays and monthly travel spikes.

Predictive Modeling: Implementing Python forecasting scripts (ARIMA/Prophet) to predict 2026-2030 trends based on current growth rates.

Real-time API: Connecting the Power BI dashboard directly to a live flight API for real-time travel demand monitoring.

👤 Author
Aatish Arote 
