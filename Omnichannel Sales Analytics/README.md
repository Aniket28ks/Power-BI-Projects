# Omnichannel Sales and Target Variance Analytics Dashboard
## Executive Summary 
Designed and built an end-to-end Power BI report tracking revenue streams across physical stores and e-commerce channels against target budgets. Modeled target variance across product categories to support performance management decisions.

---

## Data Architecture and Data Modelling
**Schema:** Star Schema connecting multiple transactional fact tables ('Fact_Online_Sale', 'Fact_Physical_Sale', 'Fact_Monthly_Target') to centralized dimension tables ('Dim_Calendar', 'Dim_Products'). ![Data Model](./Screenshot%202026-08-27%20010106.png)
**Time Intelligence:** Handled dual-date dynamics ('OrderDate' vs 'DeliveryDate') by implementing 'USERELATIONSHIP' in DAX to dynamically modify active relationship contexts for accurate time-series reporting.

---

## Core Technical Implementation
```dax
// Measure using dynamic date relationship override
Delivery Sales Amount = CALCULATE(SUM(Fact_Online_Sale[SalesAmount]), USERELATIONSHIP(Fact_Online_Sale[DeliveryDate], Dim_Calendar[Date]))
```
---

## Visual Insights and Features
**Target Variance Matrices:** Dynamic KPI card visuals and matrices evaluating target variance across product lines (Essentials, Electronics, EcoFriendly).
**Multi-Channel Tracking:** Evaluated cross-channel performance comparing physical store metrics against e-commerce channels.
