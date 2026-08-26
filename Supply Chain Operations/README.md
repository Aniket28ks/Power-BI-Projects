# Supply Chain Operations and Inventory Targets Dashboard

## Executive Summary
Designed a star-schema analytics dashboard modeling total revenue performance ($4.73K across product categories),  shipping status tracking, and inventory availability targets across global warehouse hubs.

---

## Data Architecture and Data Modelling
**Schema:** Designed a star schema connecting logistics operations, warehouse inventories, and shipping status data to unified dimension tables.
**Time Intelligence:** Applied dual-date modeling using DAX relationship overrides ('USERELATIONSHIP') to independently analyze volume metrics across order placement dates vs actual delivery completion dates.

---

## Core Technical Implementation
```dax
// Measure analyzing delivery lead times across dynamic order dates
Average Delivery Load Time = CALCULATE(AVERAGE(Fact_Shipments[DeliveryDays]), USERELATIONSHIP(Fact_Shipments[ActualDeliveryDate], Dim_Calendar[Date]))
```

---

## Visual Insights and Features
**Fulfillment Performance:** Built DAX measures to track key operational indicators, including average delivery lead times (5.67 days overall).
**Inventory Target Tracking:** Evaluated target stock levels against actual defect thresholds across product lines to optimize warehouse fulfillment efficiency.
