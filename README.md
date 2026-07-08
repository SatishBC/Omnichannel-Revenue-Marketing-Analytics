# Omnichannel Revenue Analytics & Vendor Settlement System

## 📌 Project Overview
This repository contains a comprehensive, production-ready Business Intelligence solution built in Power BI. The project addresses the real-world operational and analytical challenges of a high-growth D2C Beauty & Personal Care (BPC) brand managing fragmented multi-channel sales architectures, complex vendor contract rates, and performance marketing spend attribution.

## 📊 Dashboard Pages

### 🏛️ Page 1 – Executive Performance Index
![Executive Performance Index](Screenshot%202026-06-30%20222052.png)

**What it shows:**
- **High-Level Financials:** Real-time visibility into Gross Revenue (₹5M), Gross Margin % (51.88%), Attributed Revenue, and Blended ROAS (11.40).
- **Channel Performance Ledger:** Deep-dive breakdown of Month-over-Month (MoM) growth benchmarks across D2C, DCart, and Nile channels categorized by product divisions (Haircare, Bodycare, Skincare, etc.).
- **Omnichannel Sales Mix Share:** A descriptive donut chart visualizing exact transaction weight splits across distributed marketplace channels (Website leading at 60.7%).

---

### 🎯 Page 2 – Performance Marketing Insights
![Performance Marketing Insights](Screenshot%202026-06-30%20222118.png)

**What it shows:**
- **Acquisition Efficiency:** Centralized tracking for Total Ad Spend (₹4M), Attributed Gross Sales, Click-Through Rate (CTR %), and a healthy Blended ROAS of 10.31.
- **Campaign Performance Ledger:** Comprehensive matrix monitoring categorical ad expenditures against target return logic to isolate underperforming ad-sets.
- **Performance Marketing Funnel:** A structural multi-tier conversion waterfall monitoring volume conversion progression straight from initial Clicks (3142K) down to finalized Units Sold (67K).

---

### 💼 Page 3 – Vendor Settlement & Cost Ledger
![Vendor Settlement & Cost Ledger](Screenshot%202026-06-30%20222135.png)

**What it shows:**
- **Settlement Architecture:** Clear baseline calculations showing Total Units Sold (6,196), Total Contract Cost (₹2.07M), Volume Discounts (₹32K), and net settlement liabilities (₹2.04M Net Payable).
- **Vendor Cost & Settlement Ledger:** A granular, row-by-row relational matrix mapping product cost scales, volume tiers, and dynamic contract windows to prevent margin erosion.
- **Net Payable Share by Category:** A clean horizontal inventory visualization prioritizing payment scales across core operational segments, led by Skincare and Makeup.

## 🛠️ Key Business Challenges Solved
* **Data Fragmentation:** Consolidated highly inconsistent data formats across internal ERP servers (D2C Website), Nile marketplace, and DCart (comprising Scheduled and Quick Commerce sub-channels) into a scalable framework.
* **Delayed Vendor Settlements:** Automated a manual, error-prone 5–6 day reporting lag down to a near-real-time data refresh system.
* **Dark Marketing Spend:** Formulated granular KPI tracking for a 40–45 Lakh performance marketing budget across Google and Meta platforms, enabling dynamic sales attribution modeling.

## 🚀 Technical Architecture & Features

### 1. Robust ETL & Star Schema Data Modeling
* Engineered an automated ETL pipeline using **Power Query** to ingest multi-source files dynamically, ensuring zero code changes are required when new operational datasets are appended.
* Architected a centralized **Star Schema** utilizing a multi-directional `CategoryYearKey` bridge table to map dimension properties across transactional fact tables seamlessly.

### 2. Advanced DAX Engineering
* **Time-Bound Contract Evaluation:** Handled a Just-In-Time (JIT) inventory cost model by authoring DAX measures that dynamically look up and apply product-specific unit rates based on active contract validity windows.
* **Variable Volume Discount Automation:** Programmed dynamic logical flags to calculate a conditional 10% contract discount whenever a specific product's monthly sales volume surpasses a 150-unit threshold.
* **Defensive Metrics:** Applied rigid error-handling logic (using `DIVIDE`, `CALCULATE`, and `ALLSELECTED`) to accurately surface real-time cumulative sales metrics and Click-Through Rates (CTR%).

### 3. Executive Investor Dashboarding
Designed a multi-tier interactive interface explicitly structured for Investor Committee presentations, replacing static slide decks with dynamic visual pillars:
* **Executive Performance Index:** Tracks Gross Revenue, Gross Margin %, MoM Growth, and Omnichannel Mix Share.
* **Vendor Settlement Ledger:** Displays line-by-line category and product cuts for Units Sold, Gross Sales, Contract Costs, and Volume Discounts to manage vendor payments effortlessly.
* **Performance Marketing Funnel:** Visualizes the top-to-bottom customer acquisition funnel (Clicks $\rightarrow$ Add To Carts $\rightarrow$ Units Sold) alongside Blended Return on Ad Spend (ROAS).

## 📂 Repository Structure
* `Omnichannel_Retail_Analytics.pbix`: The core Power BI desktop application file housing the data model, DAX measures, and interactive reporting views.
* `README.md`: Project business context and technical documentation.
