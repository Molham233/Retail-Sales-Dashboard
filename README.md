# 📊 Retail Sales Performance & Customer Analytics

An interactive **Power BI dashboard** built to analyze retail sales performance, product-category contribution, customer demographics, and monthly revenue trends.

The project follows an end-to-end analytics workflow: **data validation → Power Query transformation → data modeling → DAX measures → dashboard design → business insights**.

---

## 🎯 Project Overview

Retail businesses need a clear view of **what drives revenue, when sales peak, and which customer segments contribute most to transactions and revenue**.

This project answers four main business questions:

- Which product categories contribute the most revenue?
- How does revenue change over time?
- How are sales distributed across gender and age groups?
- What business actions can be considered from the observed purchasing patterns?

---

## 🛠️ Tools & Technologies

- **Power BI** — Dashboard development and data visualization
- **Power Query** — Data cleaning and transformation
- **DAX** — KPI calculations and analytical measures
- **CSV** — Source dataset
- **Star Schema** — Data modeling approach

---

## 📂 Dataset

The project uses a retail sales dataset containing **1,000 transactions** and **9 fields**.

### Dataset fields

| Field | Description |
|---|---|
| `Transaction ID` | Unique transaction identifier |
| `Date` | Transaction date |
| `Customer ID` | Customer identifier |
| `Gender` | Customer gender |
| `Age` | Customer age |
| `Product Category` | Product category purchased |
| `Quantity` | Number of units purchased |
| `Price per Unit` | Unit price |
| `Total Amount` | Total transaction value |

### Data scope

- **Transactions:** 1,000
- **Date range:** January 1, 2023 – January 1, 2024
- **Product categories:** Electronics, Clothing, Beauty
- **Customer age range:** 18–64
- **Missing values:** None
- **Duplicate transaction IDs:** None

### Data source

The dataset is based on the publicly available **Retail Sales Dataset** commonly distributed through Kaggle.

> The dataset is used here for portfolio and analytical demonstration purposes.

---

## 🧹 Data Preparation

The data preparation workflow was performed using **Power Query**.

Key steps included:

1. Validated column data types.
2. Checked for missing values and duplicate transaction IDs.
3. Converted the `Date` field into a proper date type.
4. Prepared demographic groupings for customer analysis.
5. Prepared the dataset for a relational Power BI model.
6. Created a dedicated **Calendar** table for time-based analysis.

---

## 🧩 Data Modeling

The model follows a **Star Schema** approach with a dedicated Calendar table.

The Calendar table enables time-based analysis such as:

- Monthly revenue trends
- Previous-period comparisons
- Time-intelligence calculations
- Date-range filtering

---

## 🧮 DAX Measures

The dashboard uses DAX measures to calculate the main KPIs.

### Total Revenue

```DAX
Total Revenue =
SUM(Sales[Total Amount])
```

### Total Transactions

```DAX
Total Transactions =
COUNTROWS(Sales)
```

### Average Order Value

```DAX
Average Order Value (AOV) =
DIVIDE(
    [Total Revenue],
    [Total Transactions]
)
```

These measures are used throughout the dashboard to provide dynamic KPI calculations based on the selected filters.

---

## 📊 Dashboard

### Dashboard Preview

![Retail Sales Performance Dashboard](Retail_Sales_Dashboard.png)

The dashboard provides an interactive view of:

- Total Revenue
- Average Order Value (AOV)
- Total Quantity Sold
- Total Transactions
- Monthly Revenue Trend
- Revenue by Gender
- Revenue by Product Category
- Transactions by Age Group

### Interactive Filters

Users can dynamically filter the dashboard by:

- Product Category
- Date
- Gender

---

## 📈 Key Results

Based on the dataset:

| KPI | Result |
|---|---:|
| Total Revenue | **$456,000** |
| Total Transactions | **1,000** |
| Total Quantity Sold | **2,514** |
| Average Order Value | **$456** |

### Revenue by Product Category

| Category | Revenue | Share |
|---|---:|---:|
| Electronics | $156,905 | 34.4% |
| Clothing | $155,580 | 34.1% |
| Beauty | $143,515 | 31.5% |

Electronics generated the largest revenue contribution, followed very closely by Clothing.

### Revenue by Gender

| Gender | Revenue | Share |
|---|---:|---:|
| Female | $232,840 | 51.1% |
| Male | $223,160 | 48.9% |

Revenue is relatively balanced between the two gender segments, with female customers accounting for a slightly larger share.

### Monthly Revenue

- **Highest month:** May 2023 — **$53,150**
- **Lowest month:** September 2023 — **$23,620**
- **December 2023 revenue:** **$44,690**

The monthly trend shows noticeable fluctuations rather than a consistent upward or downward pattern.

---

## 💡 Business Insights

### 1. Product Performance

Electronics and Clothing are the two largest revenue contributors, each representing roughly one-third of total revenue.

**Business implication:** These categories can be monitored closely for pricing, promotions, and inventory planning.

### 2. Customer Demographics

The transaction distribution is concentrated in the older age groups used in the dashboard.

**Business implication:** Customer segmentation can help tailor promotions and product campaigns to different age segments rather than using a single marketing strategy.

### 3. Gender Distribution

Female customers generated **51.1%** of revenue compared with **48.9%** for male customers.

**Business implication:** The relatively balanced split suggests that the business should avoid relying on a single gender segment when planning broad campaigns.

### 4. Monthly Sales Fluctuation

Revenue peaked in May 2023 and reached its lowest point in September 2023.

**Business implication:** Investigating the causes of monthly variation could support better promotional planning and inventory allocation.

---

## 🎯 Business Recommendations

Based on the observed patterns:

1. **Monitor Electronics and Clothing closely** because they represent the largest revenue categories.
2. **Use demographic segmentation** when designing targeted promotions.
3. **Investigate high- and low-performing months** to identify promotional, seasonal, or operational drivers.
4. **Align inventory planning with observed demand patterns** instead of using a constant stocking level.
5. **Track AOV and transaction volume together** to distinguish between growth driven by more customers and growth driven by larger purchases.

---

## 🧠 What I Learned

This project strengthened my practical understanding of:

- Power Query data transformation
- Power BI data modeling
- Star Schema design
- DAX measures
- Time-based analysis
- Interactive dashboard design
- Business-oriented data storytelling
- Turning descriptive analysis into actionable recommendations

---

## 🚀 Future Improvements

Potential extensions to the project include:

- Add **Month-over-Month Revenue Growth %**
- Add **Previous Month Revenue**
- Add **Revenue vs. Target**
- Add more advanced customer segmentation
- Implement **Row-Level Security (RLS)** for multi-store scenarios
- Add a Python-based forecasting model for future sales
- Publish the dashboard to **Power BI Service**
- Add a dedicated executive summary page

---

## 📁 Project Structure

```text
Retail-Sales-Dashboard/
│
├── README.md
├── Retail_Sales_Dashboard.pbix
├── Retail_Sales_Dashboard.png
└── retail_sales_dataset.csv
```

---

## 📌 Project Summary

**Retail Sales Performance & Customer Analytics** demonstrates an end-to-end Power BI workflow, from raw transactional data to an interactive dashboard and business-focused insights.

The project focuses on answering practical retail questions through **data modeling, DAX, visualization, and analytical storytelling**.

