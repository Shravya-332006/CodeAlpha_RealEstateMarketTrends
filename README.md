# 🏡 Real Estate Market Trends & Investment Insights

**CodeAlpha Power BI Data Analytics Internship — Task 3**

---

## 📌 Project Overview
A real estate intelligence and investment analysis dashboard designed to evaluate property pricing, rental yield performance, market supply-demand dynamics, and regional market hotspots.

---

## 🖼️ Dashboard Preview
![Dashboard Preview](task3_dashboard.png)

---

## 🔑 Key Features & Insights
* **Market Benchmark KPIs:** Real-time monitoring of Average Property Price ($678.81K), Price per Sq Ft ($383.74), Gross Rental Yield (5.26%), and Total Active Listings (18.78K).
* **Geographic Market Hotspots:** Interactive map visualization identifying state-level listing density and valuation trends.
* **Property Type Dynamics:** Comparative pricing evaluation across Single Family, Multi-Family, Condos, Townhouses, and Apartments.
* **Inventory Distribution:** Donut chart breakdown of active listings vs. market liquidity (Recently Sold).
* **High-Valuation City Analysis:** Top 10 metropolitan markets filtered by average listing valuations.

---

## 📐 Key DAX Measures
* `Avg Property Price = AVERAGE(property_listings[price])`
* `Avg Price per SqFt = DIVIDE(SUM(property_listings[price]), SUM(property_listings[livingArea]), 0)`
* `Avg Rental Yield = DIVIDE(AVERAGE(property_listings[rentZestimate]) * 12, AVERAGE(property_listings[price]), 0)`
* `Total Listings = COUNTROWS(property_listings)`

---

## 🧹 Data Cleaning & Preprocessing (Power Query)
* **Type Casting:** Converted numeric fields (`price`, `rentZestimate`, `livingArea`) and categorical attributes (`city`, `state`, `homeType`, `homeStatus`).
* **Data Cleansing:** Filtered out zero/placeholder entries (`price > $1,000`) to remove unrepresentative outliers.
* **Geographic Structuring:** Cleaned location parameters for map rendering.

---

## 🛠️ Tech Stack & Tools
* **BI Platform:** Microsoft Power BI Desktop
* **Analytical Modeling:** DAX (Data Analysis Expressions)
* **ETL Transformation:** Power Query
* **Source Data:** Zillow Real Estate Dataset (`property_listings.csv`)

---

## 📁 Repository Structure
```text
├── CodeAlpha_Task3_RealEstateTrends.pbix      # Power BI Report File
├── property_listings.csv                      # Source Dataset
├── task3_dashboard.png                        # Dashboard Screenshot
└── README.md                                  # Project Documentation
