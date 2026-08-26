# SaaS Subscription Revenue and Churn Analytics Dashboard

## Executive Summary
Built an interactive SaaS analytics report tracking Monthly Recurring Revenue (MRR), add-on revenue streams, and churned revenue losses across subscription tiers (Basic, Standard, Premium).

---

## Data Architecture and Data Modelling
**Schema:** Modeled a multi-fact schema connecting subscription life cycles ('Fact_Subscriptions') and one-time purchases ('Fact_AddOn_Purchases') to shared plan and date dimensions. ![Data Model Schema](./Screenshot%202026-08-27%20012011.png)
**Time Intelligence:** Applied DAX  relationship overrides ('USERELATIONSHIP') between 'Dim_Calendar', 'SignupDate', and 'CancellationDate' to calculate customer acquisition vs churn rates over time.

---

## Core Technical Implementation
```dax
// Measure calculating churned revenue using inactive cancellation date relationship
Churned Revenue = CALCULATE(SUM(Fact_Subscriptions[CancellationDate], Dim_Calendar[Date]), NOT(ISBLANK(Fact_Subscriptions[CancellationDate])))
```

---

## Visual Insights and Features 
**Tiered Subscription Tracking:** Side-by-side revenue breakdown across Basic, Standard, and Premium membership tiers.
**Churn and Retention KPI:** Visualized dynamic MRR growth vs lost subscription value across custom date ranges.
