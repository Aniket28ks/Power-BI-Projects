# Healthcare Operations and Financial Analysis Dashboard

## Executive Summary
Designed an operational analytics dashboard modeling $11.5K in patient treatment costs against a $53K department budget across Emergency, ICU, and Pediatrics units to highlight patient flow efficiency and financial allocation.

---

## Data Architecture and Data Modelling
**Schema:** Integrated multi-fact schemas connecting patient admission logs, department budgets, and clinical treatment cost tables to shared dimension models.
**Time Intelligence:** Handled dual-date relationships using DAX relationship overrides ('USERELATIONSHIP') between patient admission and discharge timestamps for accurate dynamic time-series modeling.

---

## Core Technical Implementation
```dax
// Measure calculating Average Length of Stay using dynamic discharge dates
Average Length of Stay = CALCULATE(AVERAGE(Fact_Admissions[LengthOfStayDays]), USERELATIONSHIP(Fact_Admissions[DischargeTimeStamp], Dim_Calendar[Date]))
```

---

## Visual Insights and Features
**Operational Efficiency:** Calculated key healthcare KPIs including Average Length of Stay (4.14 days), patient triage scores, and discharge status trends.
**Budget vs Actual Variance:** Modeled patient treatment cost distributions against overall departmental budget allocations across critical care units.
