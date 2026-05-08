# Repository Name

adventure-works-executive-sales-analytics-dashboard

---

# Project Title

Adventure Works Executive Sales & Customer Analytics Dashboard

---

# Repository Description

Interactive executive-level Power BI dashboard built using the Adventure Works dataset to analyze sales performance, customer insights, payment behavior, product category trends, KPI metrics, and operational order activity using DAX, data modeling, and business intelligence reporting techniques.

---

# Adventure Works Executive Sales & Customer Analytics Dashboard

## Project Overview

This project is an interactive Executive Sales & Customer Analytics Dashboard developed in Power BI using the Adventure Works dataset.

The dashboard was designed to help business executives monitor and analyze:
- Sales performance
- Customer distribution
- Product category performance
- Payment method behavior
- Order pipeline activity
- Sales trends over time
- Average order value performance
- Month-over-month sales growth

The main objective of this project was to transform raw transactional sales data into meaningful business insights using interactive visualizations, DAX calculations, KPI reporting, and executive-level analytics.

---

# Business Scenario

Adventure Works executives required a centralized analytical dashboard to:
- Monitor overall business performance
- Track revenue growth and sales fluctuations
- Understand customer purchasing behavior
- Analyze product category performance
- Monitor operational order status
- Evaluate payment method trends
- Support executive-level business decision-making

The dashboard was designed to provide a clean, interactive, and business-focused reporting experience for executives and stakeholders.

---

# Dashboard Features

## Executive KPI Cards

The dashboard includes KPI cards for:
- Total Sales (£173.7K)
- Total Customers (48)
- Total Cities (14)
- Average Order Value (AOV)
- Month-over-Month Growth %

These KPIs provide quick executive-level business summaries and performance tracking.

---

# DAX Measures Created

Several business-focused DAX measures were created to support KPI reporting, time intelligence analysis, and business performance tracking.

| Measure | Purpose |
|---|---|
| Total Sales | Calculates overall sales revenue |
| Total Orders | Counts total orders |
| Total Customers | Counts unique customers |
| Total Cities | Counts customer locations |
| Sales YTD | Calculates year-to-date sales |
| Previous Month Sales | Tracks previous month sales |
| AOV (Average Order Value) | Calculates average revenue per order |
| MoM Growth % | Measures month-over-month sales growth |

---

# Sales Trend Analysis

A line chart was created to analyze:
- Daily sales movement
- High and low sales periods
- Sales fluctuations over time

An average benchmark line was implemented to compare daily sales performance against overall average sales.

## Key Trend Insights
- March recorded the highest sales peak (£15.6K).
- April showed lower sales volatility compared to March.
- Daily sales fluctuated significantly around the average benchmark line.
- Sales performance remained highly dynamic throughout the reporting period.

---

# Sales by Product Category

A clustered column chart was created to compare revenue performance across product categories.

Additional tooltips included:
- Order Quantity
- Product Weight

## Product Category Insights

| Product Category | Total Sales |
|---|---|
| Mountain Bikes | £63.5K |
| Road Bikes | £52.3K |
| Touring Bikes | £35.1K |
| E-Bikes | £16.6K |
| Hybrid Bikes | £3.9K |
| BMX Bikes | £1.8K |
| Kids Bikes | £0.5K |

## Business Findings
- Mountain Bikes generated the highest revenue contribution.
- Road Bikes ranked second in overall sales performance.
- Kids Bikes generated the lowest revenue contribution.
- Premium bike categories dominated total company revenue.

---

# Sales Distribution by Payment Method

A donut chart was used to analyze:
- Revenue contribution by payment method
- Customer payment preferences

## Payment Method Insights

| Payment Method | Contribution |
|---|---|
| Credit Card | 54.35% |
| PayPal | 45.65% |

## Monthly Payment Trend Insights
- Credit Card usage dominated sales during January, February, and March.
- PayPal usage increased significantly during April.
- April recorded the highest PayPal contribution (60.94%).

---

# Customer and City Analysis

Customer distribution and revenue contribution by city were analyzed to understand customer concentration and regional sales performance.

## Customer & Sales Insights by City

| City | Customers | Total Sales |
|---|---|---|
| Los Angeles | 9 | £27.4K |
| Bellflower | 4 | £22.7K |
| Daly City | 5 | £16.1K |
| Baldwin Park | 3 | £13.5K |
| Eureka | 4 | £12.7K |

## Business Findings
- Los Angeles generated the highest customer count and sales revenue.
- Bellflower showed strong sales performance despite a smaller customer base.
- Smaller cities like Berkeley generated high sales with fewer customers, indicating higher-value purchases.

---

# KPI Insights

## Average Order Value (AOV)

| Month | AOV (£) |
|---|---|
| January | £2.50 |
| February | £4.19 |
| March | £3.20 |
| April | £3.20 |

### AOV Findings
- February recorded the highest average order value.
- Customer purchasing value increased significantly from January to February.
- AOV stabilized during March and April.

---

## Month-over-Month Growth %

| Month | MoM Growth % |
|---|---|
| February | 9.63% |
| March | -0.08% |
| April | -0.083% |

### Growth Findings
- February showed strong positive business growth.
- March and April recorded slight negative growth trends.
- Sales momentum slowed after February's performance peak.

---

# Order Pipeline Overview

A table visualization was created to monitor:
- Product details
- Order IDs
- Order status
- Revenue values

## Order Status Insights
- Most orders were successfully shipped.
- Cancelled orders were minimal.
- PayPal was heavily used for processing-stage orders.

---

# Slicers and Interactivity

Interactive slicers were implemented for:
- Month
- Product Category
- City
- Order Status

Dashboard interactions were optimized to:
- Keep KPI cards stable
- Prevent unnecessary cross-filtering
- Improve executive usability
- Enhance interactive analysis

---

# Data Modeling

A dedicated Date Table was created using DAX to support:
- Time intelligence calculations
- Proper month sorting
- Trend analysis
- Time-based filtering

## Date Table DAX

```DAX
DateTable =
ADDCOLUMNS(
    CALENDAR(
        MIN(Sales[OrderDate]),
        MAX(Sales[OrderDate])
    ),
    "Year", YEAR([Date]),
    "Month", FORMAT([Date], "MMMM"),
    "MonthNumber", MONTH([Date]),
    "Quarter", "Q" & FORMAT([Date], "Q")
)
```

The Month column was sorted using MonthNumber to ensure chronological month ordering.

---

# Data Validation and Quality Checks

Several validation and cleaning steps were performed during dashboard development to improve reporting accuracy and consistency.

## Data Type Validation

Validated and corrected:
- Date fields
- Currency fields
- Whole number fields
- Decimal values

| Column | Data Type |
|---|---|
| OrderDate | Date |
| Order Total | Currency |
| Product Weight | Whole Number |
| Customer ID | Whole Number |

---

## Relationship Validation

A one-to-many relationship was created and validated between:
- DateTable[Date]
- Sales[OrderDate]

This improved:
- Time analysis
- Filtering consistency
- Reporting accuracy
- Visual performance

---

## Visual Validation

Validated:
- KPI calculations
- Slicer functionality
- Tooltip calculations
- Chart aggregations
- Month sorting behavior
- Visual interaction behavior
- DAX calculation outputs

---

# Dashboard Design Improvements

Several professional dashboard design improvements were implemented:
- Executive-focused layout
- Compact table formatting
- Consistent visual color palette
- Improved spacing and alignment
- Interactive slicers
- Optimized visual titles
- Reduced visual clutter
- Professional light-gray dashboard canvas background
- Stable KPI interaction behavior

---

# Tools and Technologies

- Power BI Desktop
- DAX
- Excel
- SQL
- Python
- Data Modeling
- Data Visualization
- Interactive Dashboard Design
- Business Intelligence Reporting

---

# Skills Demonstrated

- Data Cleaning
- Data Validation
- Data Modeling
- DAX Calculations
- KPI Development
- Time Intelligence Analysis
- Dashboard Design
- Executive Reporting
- Business Intelligence Analytics
- Interactive Reporting
- Analytical Thinking
- Data Storytelling

---

# Dashboard Preview

(Add dashboard screenshot here)

---

# Author

Vidya V G

Aspiring Data Analyst focused on:
- Power BI
- Data Analytics
- Business Intelligence
- Dashboard Development
- Data Visualization
- SQL
- Python
- Excel
