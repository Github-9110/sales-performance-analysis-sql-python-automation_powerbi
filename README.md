
# 📊 1- Sales Performance & Dashboard Automation Project

A comprehensive Power BI business intelligence solution designed to automate manual reporting workflows and track critical key performance indicators (KPIs) for sales performance.

👉 **[Live Dashboard Link](#)** *(Paste your Power BI Service publish link or NovyPro portfolio link here)*

---

## 🏢 2- Business Problem & Objective
The sales director faced challenges tracking cross-regional performance due to fragmented data sources, manually compiled Excel sheets, and delayed weekly reporting. 

**Project Goal:** Build an automated, interactive data pipeline and Power BI dashboard to deliver near real-time visibility into profit margins, sales trends, and regional targets.

---

## 🛠️ 3- Tech Stack & Tools Used
*   **Data Extraction & Mashup:** Power Query (M Language)
*   **Data Modeling & Metrics:** Power BI Desktop (DAX)
*   **Source Control & Tracking:** Git / GitHub
*   **Exploratory Data Analysis:** Jupyter Notebook (`Sales_data.ipynb`)

---

## 📂 4- Project Directory Structure
```text
Automated Analysis/
│
├── Data/                   # Ignored via .gitignore (Raw transactional records)
│   └── sales_raw_500s.xlsx 
├── Dashboard/              # Power BI Desktop development binaries
│   └── sales analysis Dashboard automation.pbix 
├── Notbooks/               # Python scripting and data health checks
│   └── Sales_data.ipynb    
├── Images/                 # Screenshots used for documentation
│   └── dashboard_automation.png
├── .gitignore              # Configured to prevent large binary and dataset caching
└── README.md               # Project documentation (This file)
```

---


## 🗃️ 5- Data Modeling & Relationships
The dataset follows a highly optimized **Star Schema** structure to support efficient DAX calculations and near-instant visual interactions across the dashboard cards and charts:
*   **Fact Table:** `Fact_Sales` (Tracks high-volume retail transactions and metric counts)
    *   *Core Columns:* `Order_ID`, `Sales_Amount`, `Profit_Amount`, `Quantity`, `CustomerKey`, `ProductKey`, `GeographyKey`, `DateKey`
*   **Dimension Tables:** 
    *   `Dim_Products`: Stores inventory attributes for device segments (`Product_Name` / `Product_Category`: Mobile, Laptop, Tablet, Printer).
    *   `Dim_Geography`: Tracks physical regional performance partitions (`Region`: South, North, West, East).
    *   `Dim_Calendar`: Connects date tables to support granular monthly tracking and timeline filtering (`Date`, `Month_Name`, `Quarter_Filter`).

---

## 🧪 6- Key DAX Formulas & Calculated Metrics
The following high-impact business metrics were engineered directly in DAX to populate the main executive card headers:

```dax
// 1. Total Revenue Generation (Populates the \$20M Gross Sales Card)
Sum of Sales = SUM(Fact_Sales[Sales_Amount])

// 2. Net Profit Contribution (Populates the \$5M Total Profits Card)
Sum of Profits = SUM(Fact_Sales[Profit_Amount])

// 3. Gross Transaction Volumetrics (Populates the 482 Sales Count Card)
Count of Sales = COUNT(Fact_Sales[Order_ID])

// 4. Unique Document Count (Populates the 604K Order Key KPI Card)
Sum of Order_ID = DISTINCTCOUNT(Fact_Sales[Order_ID])
```

---

## 📈 7- Dashboard Preview & Visual Layout
*Executive-level reporting layout demonstrating automated cross-functional tracking KPIs.*

<p align="center">
  <img src="Dashboard/sales analysis Dashboard automation.png" alt="Power BI Executive View" width="100%">
</p>

---
## 💡 8- Key Business Insights Discovered

*   📅 **Seasonal Trends (Orders by Month):** High-volume spikes are concentrated early in the fiscal year. Sales peak drastically in **March at 89K total orders**, closely followed by **February at 77K** and **January at 71K**. Conversely, volume flattens out significantly into the summer, hitting a baseline floor of **32K orders in April**.
*   📦 **Product Mix & Profitability:** Hardware distributions remain evenly split, but exhibit varied profit percentages. While **Printers hold the largest volume share (21% / 102 units)** with a healthy **2.60% profit index**, **Laptops trail slightly in overall volume (19% / 91 units)** but capture a lower **2.31% profit index** due to higher component overhead costs.
*   🗺️ **Regional Drivers & Contribution:** Regional performance is led by the **South Region with 5.2M in sales**, followed closely by the **North Region at 5.1M**. Interestingly, while the North captures slightly less top-line revenue than the South, it generates the absolute highest total profit yield (**1.35M in Net Profit** compared to the South's **1.24M**), pointing to higher operational margins in northern territory sales channels.

---

## 📬 9- Contact & Portfolio
*   **Name:** Shubham Kumar
*   **LinkedIn:** [://linkedin.com](https://linkedin.com)
*   **
