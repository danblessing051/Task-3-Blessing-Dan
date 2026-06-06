# 🗄️ Project 3 — SQL Data Analysis
**Blessing Ekom Dan | DecodeLabs | Batch 2026**

![SQL](https://img.shields.io/badge/SQL-SQLite-blue)
![Python](https://img.shields.io/badge/Python-3.14-green)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## 📌 Overview
Project 3 is the extraction phase of the DecodeLabs Data Analytics Internship. Using SQL queries on a real-world e-commerce dataset of 1,200 orders, I extracted business intelligence through structured querying, filtering, grouping, and aggregation. As DecodeLabs states: *"This track isn't about viewing spreadsheets — it's about Querying for Truth."*

---

## 🎯 Goal
Use SQL queries to extract insights from a dataset by writing SELECT queries, using WHERE, ORDER BY, GROUP BY, and performing COUNT, SUM, AVG aggregations.

---

## 📦 Dataset

| Detail | Info |
|--------|------|
| Records | 1,200 orders |
| Columns | 14 |
| Period | Jan 2023 – Jun 2025 |
| Type | E-Commerce Orders |
| Source | DecodeLabs Industrial Training |

---

## 🔑 Key SQL Queries Written

| # | Query | Purpose |
|---|-------|---------|
| 1 | SELECT * LIMIT 10 | View first 10 records |
| 2 | COUNT(*) | Count total orders |
| 3 | SUM(TotalPrice) | Calculate total revenue |
| 4 | AVG, MIN, MAX | Order value statistics |
| 5 | GROUP BY OrderStatus | Order status breakdown |
| 6 | GROUP BY Product + SUM | Revenue per product |
| 7 | WHERE OrderStatus = 'Cancelled' | Filter cancelled orders |
| 8 | WHERE TotalPrice > 2000 | High value orders |
| 9 | GROUP BY ReferralSource | Channel performance |
| 10 | GROUP BY PaymentMethod | Payment analysis |
| 11 | SUBSTR(Date,1,7) GROUP BY | Monthly revenue trend |
| 12 | WHERE Cancelled + GROUP BY | Cancellations by product |
| 13 | CASE WHEN + COUNT | Full business summary |

---

## 📊 Key Findings

| Finding | Result |
|---------|--------|
| Total Orders | 1,200 |
| Total Revenue | $1,264,762 |
| Average Order Value | $1,054 |
| Cancelled Orders | 250 (20.8%) |
| Delivered Orders | 231 (19.3%) |
| Top Product by Revenue | Chair |
| Top Referral Source | Instagram (21.6%) |
| Monthly Revenue Range | $28,000 – $67,000 |

---

## 💡 SQL Concepts Used

### SELECT
Chooses specific columns and assigns aliases to computed metrics.
```sql
SELECT Product, SUM(TotalPrice) AS Total_Revenue
FROM orders
GROUP BY Product
ORDER BY Total_Revenue DESC
```

### WHERE
Filters rows based on specific conditions before grouping or aggregation.
```sql
SELECT * FROM orders
WHERE OrderStatus = 'Cancelled'
ORDER BY TotalPrice DESC
```

### GROUP BY
Organizes raw rows into categorical buckets for executive-level insights.
```sql
SELECT OrderStatus, COUNT(*) AS Number_of_Orders
FROM orders
GROUP BY OrderStatus
ORDER BY Number_of_Orders DESC
```

### Aggregations
Turns raw data into mathematical summaries that leadership relies on.
```sql
SELECT 
    COUNT(*) AS Total_Orders,
    SUM(TotalPrice) AS Total_Revenue,
    AVG(TotalPrice) AS Avg_Order_Value,
    MIN(TotalPrice) AS Min_Order,
    MAX(TotalPrice) AS Max_Order
FROM orders
```

---

## 🧠 Key Concepts Learned

**SQL Execution Order:**  

FROM     — Locate the data source
WHERE    — Filter individual rows
GROUP BY — Categorize into buckets
HAVING   — Filter aggregated buckets
SELECT   — Pick columns and calculate
ORDER BY — Sort the final output


**Important Rules:**
- COUNT(*) includes NULL values
- SUM() and AVG() ignore NULL values
- Always filter early using WHERE
- Never use aliases in WHERE clause
- The database does NOT execute top to bottom

---

## 📈 Business Insights Generated

**Finding 1 — High Cancellation Rate:**
250 orders (20.8%) were cancelled. Combined with returns (20.6%), a total of 41.4% of orders never reached customers successfully. This is a critical operational problem requiring urgent investigation.

**Finding 2 — Revenue Distribution:**
Chair generates the highest total revenue while Phone has the highest average unit price. Revenue is fairly balanced across all 7 products showing no single dominant product.

**Finding 3 — Channel Performance:**
Instagram drives the most orders (21.6%) followed closely by Email (20.8%). All 5 channels perform within a similar range showing a healthy diversified acquisition strategy.

**Finding 4 — High Value Orders:**
Orders above $2,000 were identified as potential outliers requiring further investigation to confirm whether they are genuine high-value purchases or data errors.

**Finding 5 — Monthly Trend:**
Revenue fluctuates between $28,000 and $67,000 per month with no consistent upward trend suggesting seasonal patterns worth investigating further.

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Python | Load and run SQL in Colab |
| SQLite | In-memory SQL database engine |
| Pandas | Read CSV and display results |
| Google Colab | Development environment |
| GitHub | Version control and portfolio |

---

## ▶️ How to Run

1. Open **Google Colab** at colab.research.google.com
2. Click **File → Upload Notebook**
3. Upload `Project3_SQL_Analysis.ipynb`
4. Click the **folder icon** on the left panel
5. Upload `dataset.csv` to the Colab session
6. Run each cell one by one using **Shift + Enter**
7. Results appear below each cell

---

## 📁 Files

| File | Description |
|------|-------------|
| `Project3_SQL_Analysis.ipynb` | Full SQL analysis notebook |
| `Cleaned_|Dataset' | E-commerce orders dataset |
| `README.md` | Project documentation |

---

## 🎓 About

**Intern:** Blessing Ekom Dan
**Email:** danblessing051@gmail.com
**LinkedIn:** linkedin.com/blessing-dan_888b27374
**Institution:** University of Uyo, Akwa Ibom State, Nigeria
**Course:** B.Sc Accounting
**Organization:** DecodeLabs Industrial Training
**Batch:** 2026

---

## 📞 Contact
- 📧 danblessing051@gmail.com
- 💼 linkedin.com/blessing-dan_888b27374
- ⚡ GitHub: 

---

*DecodeLabs Batch 2026 — Data Analytics Internship*
*"Think like the database, filter early, and build your queries logically." — DecodeLabs*
