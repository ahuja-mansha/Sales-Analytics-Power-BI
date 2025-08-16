# 📊 Sales Insights Dashboard Project

## Overview
This project builds a dynamic, one-page **Sales Insights Dashboard** using multiple data sources. It visualizes key metrics such as revenue, cost, profit, and growth trends across products, geographies, and time periods. Designed for quarterly or monthly business reviews, the dashboard emphasizes resilience, scalability, and actionable insights.

---

## Data Sources
- **Sales**: Folder containing yearly Excel files
- **Categories**: Excel
- **SubCategories**: Excel
- **Geography**: Excel
- **SalesRep**: Excel
- **Product**: CSV

---

## Tasks & Implementation

### 1. Data Gathering & Ingestion
- Load all yearly sales files into a unified Sales fact table.
- Ensure:
  - No errors if files are removed
  - Automatic inclusion of new files upon refresh

### 2. Data Transformation & Modeling
- **Location Field**: Split into `Country` and `City`; format for Geo maps
- **Date Field**: Standardize for time-based analysis
- **GeoKey**: Create unique keys in Sales and Geography tables
- **ID Cleanup**: Reusable function to clean “ID - ” prefixes in SalesRep and SubCategory tables
- **Model Integration**: Connect all tables using existing Calendar table

### 3. DAX Calculations
- `Total Revenue` = Retail Price × Units
- `Total Cost` = Standard Cost × Units
- `Gross Profit` = Revenue – Cost
- `Gross Profit MoM Growth %` = Month-over-month change
- `Average Sales per Day` = Total Revenue / Active Sales Days
- `QoQ Growth` = Quarter-over-quarter change

### 4. Dashboard Design
- Visuals to highlight:
  - Revenue trends
  - Profit margins
  - Geographic performance
  - Product-level insights
- Ensure month sorting from Jan to Dec on x-axis

---

## Deliverables
- Power BI (.pbix) file with:
  - Integrated data model
  - DAX measures
