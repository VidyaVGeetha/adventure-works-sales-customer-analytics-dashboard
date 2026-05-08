# Adventure Works Executive Sales & Customer Analytics Dashboard

## Project Overview

This project is an Executive Sales and Customer Analytics Dashboard developed in Power BI using the Adventure Works dataset.

The dashboard was designed to help business executives monitor:
- Sales performance
- Customer distribution
- Product category trends
- Payment method behavior
- Order pipeline activity
- Sales performance over time

The objective of this project was to transform raw transactional sales data into meaningful business insights using interactive Power BI visualizations and analytical reporting techniques.

---

# Business Scenario

Adventure Works executives required a centralized dashboard to:
- Monitor company-wide sales performance
- Understand customer purchasing behavior
- Analyze sales contribution by product category
- Track payment method usage
- Monitor operational order status
- Identify sales trends and business opportunities

The dashboard was designed for executive-level decision-making with a clean, interactive, and business-focused reporting experience.

---

# Dashboard Features

## KPI Cards
The dashboard includes KPI cards for:
- Total Sales (£173.7K)
- Total Customers (48)
- Number of Cities (14)

These KPIs provide quick executive-level performance summaries.

---

## Sales Trend Analysis
A line chart was created to analyze:
- Daily sales movement
- High and low sales periods
- Sales fluctuations over time

An average benchmark line was implemented to compare daily sales performance against overall average sales.

### Key Trend Insights
- March recorded the highest sales peak (£15.6K).
- April showed lower sales volatility compared to March.
- Daily sales fluctuated significantly around the average benchmark line.

---

## Sales by Product Category
A clustered column chart was used to compare revenue performance across product categories.

Additional tooltips included:
- Order Quantity
- Product Weight

### Product Category Insights
| Product Category | Total Sales |
|---|---|
| Mountain Bikes | £63.5K |
| Road Bikes | £52.3K |
| Touring Bikes | £35.1K |
| E-Bikes | £16.6K |
| Hybrid Bikes | £3.9K |
| BMX Bikes | £1.8K |
| Kids Bikes | £0.5K |

### Business Findings
- Mountain Bikes generated the highest revenue contribution.
- Road Bikes ranked second in overall sales.
- Kids Bikes generated the lowest sales revenue.

---

## Sales Distribution by Payment Method
A donut chart was used to analyze:
- Revenue contribution by payment method
- Customer payment preferences

### Payment Method Insights
| Payment Method | Contribution |
|---|---|
| Credit Card | 54.35% |
| PayPal | 45.65% |

### Monthly Payment Trend Insights
- Credit Card usage dominated sales during January, February, and March.
- PayPal usage increased significantly during April.
- April recorded the highest PayPal contribution (60.94%).

---

## Customer and City Analysis
Customer distribution and revenue contribution by city were analyzed.

### Customer & Sales Insights by City
| City | Customers | Total Sales |
|---|---|---|
| Los Angeles | 9 | £27.4K |
| Bellflower | 4 | £22.7K |
| Daly City | 5 | £16.1K |
| Baldwin Park | 3 | £13.5K |
| Eureka | 4 | £12.7K |

### Business Findings
- Los Angeles generated the highest sales revenue and customer count.
- Bellflower showed strong sales performance despite a smaller customer base.
- Smaller cities like Berkeley generated high sales with fewer customers, indicating higher-value purchases.

---

## Order Pipeline Overview
A table visualization was created to monitor:
- Product details
- Order IDs
- Order status
- Revenue values

### Order Status Insights
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

---

# Data Modeling

A dedicated Date Table was created using DAX to support:
- Time intelligence
- Proper month sorting
- Trend analysis

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

Several validation and cleaning steps were performed during dashboard development.

## Data Type Validation

Validated and corrected:
- Date fields
- Currency values
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

---

## Visual Validation

Validated:
- KPI calculations
- Slicer functionality
- Tooltip calculations
- Chart aggregations
- Month sorting behavior
- Visual interaction behavior

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

---

# Tools and Technologies

- Power BI Desktop
- DAX
- Data Modeling
- Interactive Dashboard Design
- Data Visualization
- Business Intelligence Reporting

---

# Skills Demonstrated

- Data Cleaning
- Data Validation
- Data Modeling
- DAX Calculations
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
