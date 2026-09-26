# Nexus Pay - Enterprise Financial and Risk Analytics Dashboard 
## Project Overview
**Nexus Pay** is a pan-European (fictional) digital payments and fintech platform managing cross-border transactions across major European nations.This interactive **Power BI Financial Analytics Dashboard** provides executive stakeholders with real-time tracking of transaction processing, revenue performance, fee/tax collections, customer demographics, and operational risk metrics up to **September 2026**.

---
## Business Key Performance Indicators (KPIs)
* **Total Transaction Volume:** 272.82K euros (for the year 2025 for example) across 2K+ executed transactions (again for the year 2025).
* **Average Transaction Value:** 114.24 euros per transaction (again for the year 2025 as reference)
* **Total Fees Collected:** Highlight the total fees collected within each year and then compares that to the previous year for year-over-year comparison.
* **Total Tax Generated:** Tells total tax generation for a financial while providing an YoY comparison of the same

---

## Key Features and Data Engineering Workflow
### 1. Data Cleaning and Transformation Pipeline (Power Query) 
* Cleaned and structured raw European transaction and customer datasets.
* Applied `Text.Trim` functions in Power Query M to eliminate leading and trailing whitespace across text fields (e.g., payment channels, statuses).
* Standardized date formatting (`DD-MM-YYYY`) and aligned all financial values strictly to **Euros**

### 2. Data Modeling and Advanced DAX Calculations
* Built time-intelligence DAX measures to calculate Year-over-Year (YoY) performance metrics and prior-year comparisons.
* Implemented dynamic measure selection to seamlessly switch dashboard visualizations between *Total Amount*, *Total Fees*, *Total Transactions*.

### 3. Dashboard Architecture and User Experience
* **Two-Page Layout:**
  * `Overview Analysis`: Executive view featuring KPI callouts, monthly trend curves, transaction status distributions, country-wise revenue rankings, and demographic profiles.
  * `Transactions`: Detailed record-level grid with contextual drill-through capabilities for root-cause transaction auditing.
* **Navigation and Filtering:** Left-hand navigation pane equipped with active tab indicators and synced global slicers (**Year**, **Dynamic Metric**, **Occupation**, **Category**) across both pages.

* ---

* ## Tech Stack and Tools
* * **Business Intelligence:** Power BI Desktop
  * **Data ETL and Transformation:** Power Query (M Code)
  * **Calculated Metrics and Data Modeling:** DAX (Data Analytics Expression)
  * **Data Ingestion and Formatting:** CSV Data Files
 
  ---

  ## Dashboard Preview

  ### 1. Overview Analysis Page
  
