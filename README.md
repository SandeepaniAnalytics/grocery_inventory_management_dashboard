# 🛒 Grocery Inventory Management Dashboard
### Power BI Dashboard | Grocery Inventory Analytics

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)

---

## 📋 Project Overview

An interactive 4-page Power BI dashboard built for an Indonesian e-grocery business managing 999 SKUs across 5 warehouses. The dashboard provides end-to-end visibility into inventory health, risk monitoring, supplier performance, and stock detail, enabling data-driven decisions for warehouse managers, inventory planners, and executives.
The original dataset contained 1,000 SKUs, after data cleaning and removing null values in Power Query, 999 SKUs were used for analysis. The dashboard covers the full inventory management lifecycle from executive-level financial overview to SKU-level operational detail.

---

## 🎯 Purpose of the Dashboard

The purpose of this dashboard is to help business users and decision-makers:

- 💰 Monitor inventory value and financial health
- ⚠️ Identify and act on stockout and expiry risks before they occur
- 🚚 Track supplier delivery performance and reliability
- 📦 Measure inventory accuracy and warehouse data quality
- 📈 Analyse forecast accuracy and demand planning effectiveness
- 🔍 Drill down to SKU-level detail for operational decisions
- 🏭 Compare performance across warehouses and product categories

---

## 🗃️ Dataset

| Detail | Value |
|---|---|
| **Source** | Kaggle |
| **Total SKUs** | 999 |
| **Warehouses** | 5 locations across Indonesia |
| **Product categories** | 10 |
| **Suppliers** | 10 |
| **Date range** | March 2025 – September 2025 |
| **Source format** | Excel (.xlsx) |
| **Total columns** | 36 |

### Key Dataset Columns

| Column | Description |
|---|---|
| `SKU_ID` | Unique product identifier |
| `SKU_Name` | Product name |
| `Category` | Product category |
| `ABC_Class` | Inventory classification (A/B/C) |
| `Warehouse_ID` | Warehouse identifier |
| `Warehouse_Location` | Physical warehouse location |
| `Quantity_On_Hand` | Current physical stock units |
| `Quantity_Reserved` | Units locked for pending orders |
| `Quantity_Committed` | Units being actively fulfilled |
| `Safety_Stock` | Minimum buffer stock level |
| `Reorder_Point` | Stock level that triggers reorder |
| `Lead_Time_Days` | Supplier delivery days |
| `Stock_Age_Days` | Days since stock was received |
| `Damaged_Qty` | Units damaged and unsellable |
| `Returns_Qty` | Units returned by customers |
| `Avg_Daily_Sales` | Historical average daily sales rate |
| `Forecast_Next_30d` | Predicted demand next 30 days |
| `Days_of_Inventory` | Days current stock will last |
| `Unit_Cost_USD` | Standard cost per unit |
| `Last_Purchase_Price_USD` | Most recent purchase price |
| `Total_Inventory_Value_USD` | QoH × Unit cost |
| `Supplier_OnTime_Pct` | Supplier delivery reliability % |
| `Count_Variance` | Difference between system and physical count |
| `Audit_Variance_Pct` | Count variance as percentage |
| `Demand_Forecast_Accuracy_Pct` | Forecast vs actual accuracy % |
| `SKU_Churn_Rate` | Demand volatility rate |
| `FIFO_FEFO` | Stock rotation method |
| `Inventory_Status` | Current health status |

---

## 📊 Dashboard Pages

### Page 1 - Executive Overview
High-level financial and operational snapshot for managers and directors.

### KPI Cards
- Total Inventory Value 
- Total Quantity On Hand
- Low Stock SKUs 
- Expiry Risk Rate

### Visuals
| Visual | Type |
|---|---|
| Total Inventory Trend by Month | Area chart |
| Total Inventory Value by Category | Bar chart |
| Total SKUs by ABC Class | Donut chart |
| Total SKUs by Inventory Status | Donut chart |

### Business Insights
- Beverages holds the highest inventory value at **$274.5K** of total stock
- **32.9%** of SKUs are expiring soon - holding $337.3K at risk of becoming waste
- Class A SKUs represent only **20% of products** but hold **$674.2K of total value**
- **57.2%** of SKUs are not in a healthy stock state - Low Stock, Expiring Soon or Out of Stock
- Inventory value peaked in **May 2025** then dropped sharply by September - signals restocking or demand issues

  
![Dashboard Overview](https://github.com/SandeepaniAnalytics/grocery_inventory_management_dashboard/blob/main/screenshots/page1_executive_overview.png)

---

### Page 2 - Risk Monitoring
Identify and act on inventory risks before they become stockouts or losses.

### KPI Cards
- Expiring Soon SKUs 
- Stockout Risk SKUs
- Aged Stock SKUs 
- Damaged Loss Value

### Visuals
| Visual | Type |
|---|---|
| Expiring Soon SKUs by Category | Bar chart |
| Inventory Levels by Category | Line chart |
| SKUs by Stock Age Band | Column chart |
| Top 20 SKUs Closest to Stockout | Table |

### Business Insights
- **Fresh Produce (81), Meat (70) and Dairy (67)** are the top 3 categories with expiring SKUs - all perishables needing urgent action
- **75.8%** of SKUs will run out within 14 days at current sales rates
- Only **157 SKUs** have fresh stock aged 0-30 days - majority of stock is aging
- **52.35%** of SKUs are older than 90 days - significant dead stock accumulation
- True available stock is only **61.5%** of total QoH after subtracting reserved, committed and safety stock

![Dashboard Overview](https://github.com/SandeepaniAnalytics/grocery_inventory_management_dashboard/blob/main/screenshots/page2_risk_monitoring.png)


---

### Page 3 - Supplier & Inventory Quality
Track supplier performance, inventory accuracy and forecast reliability.

### KPI Cards
- Supplier On-Time %
- Inventory Accuracy % 
- Forecast Accuracy % 
- Damaged Rate % 

### Visuals
| Visual | Type |
|---|---|
| Supplier On-Time % by Supplier | Bar chart |
| Actual vs Forecast Demand by Category | Line chart |
| Inventory Accuracy by Category | Stacked bar chart |
| Damaged Qty Root Cause Analysis | Decomposition tree |

### Business Insights
- All 10 suppliers score between **84.1–85.7%** on-time delivery - Moderate
- **Beverages is underforecast** - actual demand exceeds predicted, causing stockouts in the highest value category
- **Pantry has the most damaged units (164)** - PT Indo Fresh supplier and Medan warehouse identified as root cause via decomposition tree
- Forecast accuracy of **79%** means 1 in 5 SKUs is over or under predicted 

![Dashboard Overview](https://github.com/SandeepaniAnalytics/grocery_inventory_management_dashboard/blob/main/screenshots/page3_supplier_inventory_quality.png)

---

### Page 4 - Inventory Overview Table
Full SKU-level detail for warehouse managers and analysts.
<br>
![Dashboard Overview](https://github.com/SandeepaniAnalytics/grocery_inventory_management_dashboard/blob/main/screenshots/page4_inventory_overview.png)


---

## 💡 Key Business Insights

📦 **32.9%** of SKUs are expiring soon - holding **$337K** worth of stock at risk of becoming unsellable waste

🔴 **75.8%** of SKUs will run out within 14 days at current sales rates - immediate reorder action required

💰 Only **61.5%** of total stock is truly available for new orders after accounting for reserved and committed quantities

🥤 **Beverages** is the most critical category - highest inventory value (21.8%), most expiring SKUs, and most underforecast category

🚚 Supplier on-time delivery at **84.7%** is below the industry benchmark of 95% - 15% of orders arriving late directly increases stockout risk

📊 Inventory accuracy of **25.1%** (zero variance SKUs) is far below the industry standard of 99% - data quality is a major operational risk

🏭 **Pantry category** has the most damaged units (164) - PT Indo Fresh and Medan warehouse are the root cause identified via decomposition tree

📈 Average stock age of **91.5 days** with 179 SKUs over 150 days indicates significant dead stock problem

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Dashboard development and visualization |
| **DAX** | Measures, KPI calculations and colour logic |
| **Power Query** | Data transformation and cleaning |
| **Data Modeling** | Table relationships and schema design |
| **Excel** | Source data format |
| **GitHub** | Version control and project sharing |

---

## 📁 Repository Structure

```
📦 grocery-inventory-management-dashboard
 ┣ 📂 data
 ┃ ┗ 📄 InventoryData.xlsx
 ┣ 📂 screenshots
 ┃ ┣ 🖼️ page1_executive_overview.png
 ┃ ┣ 🖼️ page2_risk_monitoring.png
 ┃ ┣ 🖼️ page3_supplier_inventory_quality.png
 ┃ ┗ 🖼️ page4_inventory_overview.png
 ┣ 📄 GroceryInventoryDashboard.pbix
 ┗ 📄 README.md
```

## 🏅 Skills Demonstrated

| Skill | Description |
|---|---|
| **Business Intelligence** | Translating raw inventory data into actionable business insights |
| **Dashboard Design** | 4-page structured layout with consistent dark theme |
| **DAX Calculations** | 30+ custom measures including KPIs and colour logic |
| **Data Modeling** | Star schema with fact and dimension tables |
| **Power Query** | Data cleaning, type fixing and locale handling |
| **Conditional Formatting** | Dynamic colour coding based on business thresholds |
| **Decomposition Tree** | AI-powered root cause analysis visual |
| **Slicer Sync** | Cross-page filter synchronisation |

---

## 👤 Author

**Sandeepani Rathnayake** <br>
*Power BI & Data Analytics Enthusiast*
