# Retail Customer Retention Analytics 

A Power BI project analyzing customer churn, loyalty, and lifetime value for a retail business ("Target" case study), built across a structured task list (2.1 → 6.3) plus a final four-page executive dashboard.

## 📁 Files

| File | Description |
|---|---|
| `Retail_Customer_Retention_Analytics___TARGET.pbix` | Main Power BI report file (data model + all report pages) |
| `power_bi.pdf` | One-page summary of top business recommendations |

## 🗂️ Data Model

The report is built on a star-schema-style model with the following tables:

- **Customer_Demographics** — customer attributes (Region, Age_Group, Income_Level, Preferred_Channel, Loyalty_Tier)
- **Customer_Transactions** — transaction-level records (Product_Category, Promotion_Applied, transaction amounts/dates)
- **Loyalty_Program** — points earned/redeemed by loyalty tier
- **Store_Locations** — store attributes (Store_Type, Opening_Year)
- **Churn_Labelled_Customers** — churn status and Churn_Reason per customer
- **Measures_Table** — a dedicated disconnected table holding all DAX measures

### Key DAX Measures

- `Churn_Rate (%)`
- `Retention Rate (%)`
- `Repeat Rate (%)`
- `Total Customers`
- `Churned Customers`
- `Repeat_Customers`
- `Total_Transactions`
- `Avg_Transaction_Amount`
- `Purchases_Per_Customer`
- `Avg.Purchase_Frequency`
- `Loyal_Purchases`
- `Total_Points_Earned` / `Total_Points_Redeemed`
- `% Transactions_with_Promotion`
- `CLV` / `Average CLV`

### Key Derived/Segmentation Columns

- `CLV Segment` (e.g., Low/High CLV tiers)
- `Days Since Last Purchase`
- `Loyalty_Tier` (and a demographics-linked variant, `Loyalty_Tier(from Demographics)`)

##  Report Pages

The `.pbix` contains **18 pages**, organized as a task-by-task build-out followed by four polished summary dashboards.

### Task Pages (Analysis Build-Out)

| Page | Focus |
|---|---|
| Task 2.1 | Churn Rate KPI (card visual) |
| Task 2.2 | Churn rate broken down by Region, Income Group, Channel, and Loyalty Tier (bar/column charts) |
| Task 2.3 | Customer journey funnel chart |
| Task 3.1 | Customer segmentation into Low / Mid / High tiers (table) |
| Task 3.2 | Average purchase frequency by Region, Age Group, Loyalty Tier |
| Task 3.3 | Most purchased product categories among loyal customers |
| Task 4.1 | % of transactions with a promotion applied (card) |
| Task 4.2 | Average purchase amount: with promotion vs. without |
| Task 4.3 | Churn rate across loyalty tiers |
| Task 4.4 | Points Earned vs. Redeemed by Tier (clustered column chart) |
| Task 5.2 | Store Type & Opening Year vs. Avg. Transaction Amount, Churn Rate, Active Customers |
| Task 6.1 | Customer Lifetime Value (CLV) KPI |
| Task 6.2 | Customer segmentation into Low/High CLV (donut + table) |
| Task 6.3 | CLV vs. Days Since Last Purchase, and CLV by Loyalty Tier & Region (scatter) |

### Executive Summary Dashboards

| Page | Focus |
|---|---|
| **Executive KPIs** | Top-level KPI cards, churn/retention charts, funnel — filterable by Region, Loyalty Tier, Channel, and other slicers |
| **Loyalty and Promotion Impact** | Promotion effectiveness (avg. purchase with/without promo), loyalty tier performance, points distribution |
| **Store and Channel Insights** | Store type and channel performance vs. churn rate, transaction amount, and active customers |
| **Customer Segmentation** | CLV segment breakdown, churn reasons, demographic-driven segmentation (scatter + donuts) |

##  Key Business Recommendations

Based on the analysis, the top recommendations for Target are:

1. **Prioritize retention of high-CLV customers** in the Premium and Elite loyalty tiers.
2. **Strengthen online loyalty programs** to reduce churn in digital channels.
3. **Boost points redemption** through gamification and personalized offers to increase engagement.

*(Source: `power_bi.pdf`)*

##  How to Use

1. Open `Retail_Customer_Retention_Analytics___TARGET.pbix` in **Power BI Desktop**.
2. Use the slicers on the Executive KPIs, Loyalty and Promotion Impact, Store and Channel Insights, and Customer Segmentation pages to filter by Region, Loyalty Tier, Channel, etc.
3. Refer to the Task 2.1–6.3 pages to see the step-by-step analytical build-out behind the final dashboards.

##  Notes

- All DAX measures are centralized in the `Measures_Table` for easy discovery and reuse.
- Report theme: **Innovate** (built-in Power BI theme).
