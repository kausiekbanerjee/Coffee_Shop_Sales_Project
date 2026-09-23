# ☕ Coffee Shop Sales Performance Dashboard

An end-to-end data analysis project that transforms raw coffee shop transaction records into an interactive management dashboard. This project uncovers key business trends, tracks monthly sales growth, identifies peak operating hours, and pinpoints top-selling product categories to drive data-backed business decisions.

## ✨ Key Features & Insights
* **Interactive Executive Summary:** Dynamic KPIs tracking **Total Revenue**, **Total Orders**, and **Total Quantity Sold**.
* **Temporal Trend Analysis:** Line charts mapping month-over-month sales velocity to identify growth trajectories.
* **Peak Hour Optimization:** Visual breakdowns of transaction volumes by hour and day of the week to streamline staff scheduling.
* **Product Performance Matrices:** Top-performing categories and items filtered by revenue generation and volume.
* **Dynamic Slicers:** On-the-fly dashboard filtering by **Location** and **Month** for granular local performance reviews.

## 📊 Data Pipeline & Architecture
The project follows a standard three-stage data lifecycle entirely executed within Microsoft Excel:
`[ Raw CSV/XLSX Data ] ➡️ [ ETL & Data Cleaning ] ➡️ [ Pivot Table Aggregations ] ➡️ [ Interactive Dashboard ]`

### 🛠️ Step 1: Data Cleaning & Transformation (ETL)
* Converted raw transaction dates and times using date/time parsing functions for unified formatting.
* Extracted temporal attributes using `MONTH()`, `HOUR()`, and `WEEKDAY()` to enable time-series slicing.
* Derived total revenue per transaction using `=[@quantity] * [@unit_price]`.
* Standardized product names and locations using conditional formatting to catch and fix structural inconsistencies.

### 🎛️ Step 2: Pivot Table Aggregations
* **Revenue by Month:** Aggregated transaction metrics to compute sequential growth rates.
* **Sales by Category:** Segmented performance across Coffee, Tea, Bakery, and Merchandise lines.
* **Hourly Foot Traffic:** Grouped sales counts by operational hours to isolate peak morning rushes.

### 🖼️ Step 3: Dashboard Design
* Created a clean visual hierarchy using specialized Excel charts (Line, Clustered Bar, and Combo charts).
* Embedded linked **Slicers** connecting all Pivot Charts simultaneously for synchronized cross-filtering.
* Formatted numerical properties into clean currency (`$#,##0`) and accounting notations for professional review.

## 📁 Repository Structure
```text
├── README.md
└── coffee shop sales.xlsx      # Core workbook containing raw data, ETL grids, pivots, and the final dashboard
```

## 🚀 How to View and Use the Dashboard
1. **Download the File:** Clone this repository or download the `coffee shop sales.xlsx` file directly.
2. **Open in Microsoft Excel:** For the best interactive experience, open the workbook in the **Microsoft Excel Desktop Application**. *Note: Web versions or alternative spreadsheet tools may limit slicer functionality.*
3. **Interact:** Use the vertical slicer panels on the left side of the dashboard sheet to filter all visual outputs by city branch or target month.

## 📄 License
This project is open-source and available under the MIT License.
