# powerbi-online-sales-insights

# Online Sales Insights Report (Power BI)

## Project Overview

This project is a multi-page Power BI business intelligence report designed to analyse sales performance, profitability, and customer behaviour using transactional e-commerce data.

The objective was to transform raw order and sales records into a decision-support dashboard for stakeholders through KPI reporting, interactive filtering, and commercial insights.

---

## Tools & Skills Used

- Power BI
- Data Modelling
- DAX Measures
- KPI Dashboard Design
- Profitability Analysis
- Customer Analytics
- Interactive Filters / Slicers
- Business Storytelling

---

## Data Model

Two related tables were used:

### Orders
Contains:
- Order ID
- Order Date
- Customer Name
- City
- State

### Details
Contains:
- Revenue (Amount)
- Profit
- Quantity
- Category
- Sub-Category
- Payment Mode

### Relationship

Orders (1) → Details (*) via Order ID

---

# Report Pages

---

## 1. Sales Overview

### KPIs
- Total Revenue: 438K
- Total Profit: 37K
- Total Orders: 500

### Visuals
- Revenue trend over time
- Sales by category
- Sales by state
- Sales by payment mode

### Key Insights
- Electronics generated the highest revenue.
- Maharashtra and Madhya Pradesh were leading states.
- COD was the most common payment mode.
- Revenue fluctuated significantly across time.

![Overview](screenshots/overview.png)

---

## 2. Profit Analysis

### KPIs
- Total Profit: 37K
- Profit Margin: 8.44%
- Avg Profit per Order: 73.93

### Visuals
- Profit by category
- Profit by sub-category
- Revenue vs Profit comparison
- Low-profit products table

### Key Insights
- Clothing and Electronics delivered the strongest profit contribution.
- Some sub-categories operated at a loss.
- High revenue did not always translate to high profitability.

![Profit Analysis](screenshots/profit-analysis.png)

---

## 3. Customer Insights

### KPIs
- Total Customers: 336
- Revenue per Customer: 1.30K
- Orders per Customer: 1.49

### Visuals
- Top customers by revenue
- Sales by city
- Orders by state
- Customer detail table

### Key Insights
- Revenue was concentrated among a smaller group of customers.
- Indore, Mumbai, and Pune were leading cities.
- Repeat purchases were present across the customer base.

![Customer Insights](screenshots/customer-insights.png)

---

# Business Recommendations

## Revenue Growth
- Expand successful product categories.
- Focus campaigns in top-performing states and cities.

## Profitability
- Review negative-margin sub-categories.
- Improve pricing strategy for weak performers.

## Customer Strategy
- Retain top customers through loyalty campaigns.
- Encourage repeat purchases.

---

# Key DAX Measures

```DAX
Profit Margin =
DIVIDE(SUM(Details[Profit]), SUM(Details[Amount]))

Avg Profit per Order =
DIVIDE(SUM(Details[Profit]), DISTINCTCOUNT(Orders[Order ID]))

Revenue per Customer =
DIVIDE(SUM(Details[Amount]), DISTINCTCOUNT(Orders[CustomerName]))
```

---

# What This Project Demonstrates

- Building a multi-page Power BI report
- Designing KPI dashboards
- Writing DAX measures
- Using relational data models
- Translating data into business insights
- Presenting findings clearly to stakeholders

---

# Author

Xingyu Chen  
Sydney, Australia
