# E-Commerce Sales Dashboard

A single-page Power BI report that summarizes profit, sales, and order volume across an e-commerce dataset — broken down by time, geography, product category, and payment method.

## Overview

The dashboard connects to a Power BI semantic model built from two tables, **Orders** and **Details**, and gives a quick, filterable view of overall business performance.

## Data Model

| Table | Key Fields Used in This Report |
|---|---|
| **Orders** | Order ID, Order Date, State |
| **Details** | Category, Sub-Category, Payment Mode, Amount, Profit, Quantity |

## Report Layout (Page 1)

### KPI Cards (top of page)
- **Total Profit** — sum of `Details[Profit]`
- **Total Amount** — sum of `Details[Amount]` (total sales value)
- **Total Quantity** — sum of `Details[Quantity]` (units sold)
- **Order Reference** — based on `Orders[Order ID]`

### Visuals

| Visual | Type | Measures / Fields |
|---|---|---|
| Profit by Month | Column chart | Profit vs. Order Date (Month) |
| Profit by State | Pie chart | Profit vs. State |
| Profit by Sub-Category | Bar chart | Profit vs. Sub-Category |
| Profit by Category | Donut chart | Profit vs. Category |
| Quantity by Payment Mode | Donut chart | Quantity vs. Payment Mode |
| Quantity by Category | Column chart | Quantity vs. Category |

### Filters (Slicers)
- **Quarter** — filters the report by Order Date (quarter level)
- **Category** — filters the report by product Category

## How to Use

1. Open `E-Commerce_Sales.pbix` in Power BI Desktop, or view the published report in the Power BI / Fabric service.
2. Use the **Quarter** and **Category** slicers at the top of the page to narrow the view.
3. Click any chart segment (e.g., a state on the pie chart, a category on the donut chart) to cross-filter the rest of the page.
4. Hover over cards and charts for exact values via tooltips.

## Key Questions This Dashboard Answers

- Which months are most profitable?
- Which states/regions drive the most profit?
- Which product categories and sub-categories are the biggest profit contributors?
- How do customers prefer to pay, and how does that break down by quantity sold?
- What are the overall totals for profit, sales amount, and units sold?

## Notes

- This report is connected to a Power BI/Fabric semantic model (live connection) rather than an embedded local dataset — the underlying data is managed and refreshed in the connected workspace.
- To modify the report, open the `.pbix` file in Power BI Desktop with access to the connected semantic model.

---
*Generated from the report structure of `E-Commerce_Sales.pbix`.*

![(https://github.com/Sumaiya-Kareem/E-COMMERECE/blob/main/Screenshot%202026-09-22%20103606.png)]

