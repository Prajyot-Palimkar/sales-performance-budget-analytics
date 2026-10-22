# Sales Performance & Budget Analytics Dashboard

An interactive sales analytics dashboard built with Microsoft Power BI to analyze revenue, transaction volume, sales quantities, budget performance, and sales contributions across channels, managers, supervisors, products, and salespeople. This project demonstrates data cleaning, DAX-based revenue calculation, interactive filtering, dynamic Top/Bottom analysis, and custom tooltip design using sample sales data.

## 🎬 Demo Issue

<video src="https://github.com/user-attachments/assets/c552aa99-7d0f-43b5-9bae-be54a36ecfb9" controls width="100%"></video>

<p align="center">
  <a href="https://github.com/user-attachments/assets/c552aa99-7d0f-43b5-9bae-be54a36ecfb9">
    🎬 Watch Demo Video
  </a>
</p>

## Demo Direct
<video src="./screenshots/Sales%20Dashboard%20Demo.mp4" controls width="100%"></video>


![Power BI](https://img.shields.io/badge/Power_BI-F2C94C?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Analytics-blue?style=for-the-badge)
![Excel](https://img.shields.io/badge/Excel-Source_Data-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)

## 1. Project Overview

The objective of this project is to transform sales data into meaningful visual insights that support sales performance monitoring and business analysis.

The dashboard helps users:
- Monitor key sales performance indicators.
- Compare monthly revenue against budget.
- Analyze revenue contribution by sales channel, manager, and supervisor.
- Identify top- and bottom-performing products, product groups, and salespeople.
- Explore salesperson-level transaction and revenue details.
- Use interactive selections and custom tooltips to examine performance from different perspectives.

**Primary tool:** Microsoft Power BI  
**Domain:** Sales Analytics / Business Intelligence  
**Data sources:** Four Excel files containing sample or practice sales data.

## 2. Dashboard Preview

The following image shows the screenshot of the actual dashboard. 

<p align="center">
  <img src="./screenshots/Main%20Sales%20Dashboard.png" alt="Main Sales Dashboard" width="100%">
</p>


*This main dashboard overview shows the KPI cards, revenue by sales channel, monthly revenue versus budget, manager and supervisor analysis, and dynamic Top/Bottom analysis.*

## 3. Key Features

| Key Feature | Description & Implementation |
|---|---|
| 📈 KPI Monitoring | Tracks _Total Transactions, Total Quantity Sold,_ and _Total Revenue._ |
| 📊 Channel Performance | Breakdown across _Retail, Distributor,_ and _Online_ with custom tooltips. |
| 🗓️ Revenue vs. Budget | Monthly column charts with embedded achievement gauges. |
| 🔀 Dynamic Top/Bottom N | Interactive slicer allowing dynamic rankings (1–15) by Product, Group, or Salesperson. |

The chart and its heading update according to the selected options. This makes it easier to compare high- and low-performing entities without relying on a single fixed ranking.

<p align="center">
  <img src="./screenshots/Dynamic%20Top%20Bottom%20Analysis.png" alt="Dynamic Top Bottom Analysis" width="60%">
</p>

## 4. Dashboard Pages

### Page 1 — Main Sales Dashboard

The main page brings together the overall KPIs, revenue by sales channel, monthly revenue versus budget, manager and supervisor contribution analysis, and dynamic Top/Bottom analysis.

It provides a consolidated view of sales performance and allows users to explore the data through interactive visuals and custom tooltips.

### Page 2 — Detailed Salesperson Transaction Analysis

The second page is accessible through a navigation button on the main dashboard.

It includes a salesperson table with:
- Salesperson photograph
- Salesperson name
- Total Transactions
- Total Quantity Sold
- Total Revenue

The page also provides Manager and Supervisor filters. Selecting a salesperson updates these filters to reflect the salesperson's organizational relationships. A navigation button returns users to the main dashboard.

<p align="center">
  <img src="./screenshots/Salesperson%20Details.png" alt="Salesperson Details" width="80%">
</p>

## 5. Interactive Features and Custom Tooltips

### Revenue vs. Budget Tooltip

Hovering over a month in the monthly revenue-versus-budget chart opens the **Revenue vs Budget Tooltip**. It displays:
- A gauge showing revenue achievement against budget
- Total Transactions
- Total Revenue
- Total Budget
- Revenue from Budget

<p align="center">
  <img src="./screenshots/Revenue%20vs%20Budget%20Tooltip.png" alt="Revenue vs Budget Tooltip" width="80%">
</p>

### Sales Person Tooltip

Hovering over a sales channel opens the **Sales Person Tooltip**, which displays the top three salespeople for that channel, including their rank, name, revenue, and photograph.

<p align="center">
  <img src="./screenshots/Sales%20Person%20Tooltip.png" alt="Sales Person Tooltip" width="80%">
</p>

### Product Tooltip

Hovering over the dynamic Top/Bottom chart opens the **Product Tooltip**, which includes:
- The relevant product image
- A pie chart comparing weekday and weekend performance
- A Total Revenue KPI

<p align="center">
  <img src="./screenshots/Product%20Tooltip.png" alt="Interactive Tooltip Insights" width="60%">
</p>

### Interactive Filtering and Navigation

The report combines selections, filters, tooltips, and page navigation to help users investigate sales performance at different levels of detail. Selecting a salesperson on the detail page updates the Manager and Supervisor filters to reflect the salesperson's organizational relationships.

## 6. Technology Stack

| Technology | Use |
|---|---|
| Microsoft Power BI | Dashboard development and data visualization |
| DAX | Revenue calculation and analytical measures |
| Microsoft Excel | Source data files |
| Data cleaning and preparation | Preparing the source data for analysis |

## 7. Dataset and Source Files

The project uses sample or practice sales data supplied through four Excel files.

| Dataset / File | Functional Purpose | Schema / Data Type |
|---|---|---|
| `Budget.xlsx` | Target revenue metrics for monthly variance reporting | Financial Targets |
| `Photos.xlsx` | Photographs associated with salespeople or products | Metadata / Media |
| `Product.xlsx` | Product metadata, categories, and hierarchy | Dimension Table |
| `SalesData.xlsx` | Granular transaction records (revenue, quantities, channels) | Fact Table |

Data cleaning was performed as part of the project.

## 8. DAX Implementation

### Total Revenue

The following DAX measure was created to calculate total revenue:

```dax
Total Revenue =
SUMX(
    'FactTable',
    'FactTable'[UnitPrice] * 'FactTable'[Quantity]
)
```

**How it works:**
1. `SUMX` iterates over the rows in `FactTable`.
2. For each row, it multiplies `UnitPrice` by `Quantity`.
3. It sums the row-level revenue values to calculate Total Revenue.

Budget values are stored in a column and summed to obtain the total budget. 

## Key Business Metrics

| Metric or analysis | Purpose |
|---|---|
| Total Transactions | Monitor transaction volume |
| Total Quantity Sold | Understand sales quantity |
| Total Revenue | Measure revenue generated from sales |
| Monthly Revenue vs. Budget | Compare monthly revenue against budget |
| Revenue by Sales Channel | Compare Retail, Distributor, and Online contributions |
| Manager Revenue Contribution | Compare revenue across managers |
| Supervisor Sales Contribution | Review supervisor-level revenue and contribution |
| Dynamic Top/Bottom Analysis | Identify high- and low-performing products, product groups, and salespeople |

## 🚀 How to Explore this Portfolio Project
This repository serves as a **documented case study** showcasing the architecture, visual design, and DAX logic of the Power BI solution. 

- **Key Highlights:** Review the detailed breakdown of calculations, visual hierarchy, and multi-page user journeys below.
- **DAX Mechanics:** Inspect the core data modeling logic provided in the implementation section.

## Skills Demonstrated

- Microsoft Power BI dashboard development
- Data cleaning and preparation
- DAX measures and calculations
- KPI development
- Data visualization and dashboard design
- Sales performance analysis
- Revenue-versus-budget comparison
- Dynamic Top/Bottom analysis
- Custom tooltip design
- Interactive filtering
- Multi-page report navigation
- Excel-based data integration

## Potential Business Applications

> [!TIP]
> **Business Value Delivered**
>
> - Enables regional managers to identify underperforming channels within seconds.
> - Streamlines month-over-month variance tracking against target budgets.

A similar dashboard could help sales managers:
- Monitor transaction volume, quantity sold, and revenue.
- Compare monthly revenue with budget.
- Evaluate revenue contribution across sales channels.
- Review manager and supervisor contributions.
- Identify high- and low-performing products, product groups, and salespeople.

These are potential applications of the dashboard approach, not claims of measured business impact from this sample project.

---
