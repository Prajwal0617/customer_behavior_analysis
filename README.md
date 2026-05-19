# 🛍️ Customer Shopping Behavior Analysis

> An end-to-end data analytics project analyzing customer purchasing patterns to uncover revenue drivers, customer segments, and actionable business insights.

---

## 📌 Overview

This project performs a full-cycle analysis of customer shopping behavior — from raw data exploration to an interactive dashboard and executive presentation. The goal is to understand how factors like demographics, discount usage, subscription status, and shipping preferences influence purchase behavior and revenue.

**Key Business Questions Answered:**
- Which customer segments drive the most revenue?
- How does discount usage vary across product categories?
- Do subscribed customers spend more than non-subscribed ones?
- What are the top-selling items per category?
- How does shipping type relate to average order value?

---

## 📂 Dataset

| Property | Details |
|---|---|
| **File** | `customer_shopping_behavior.csv` |
| **Rows** | ~3,900 customer records |
| **Source** | Synthetic retail dataset |

**Key Columns:**

| Column | Description |
|---|---|
| `Customer ID` | Unique identifier per customer |
| `Age` | Customer age |
| `Gender` | Male / Female |
| `Item Purchased` | Product name |
| `Category` | Product category (Clothing, Footwear, etc.) |
| `Purchase Amount (USD)` | Transaction value |
| `Location` | US state |
| `Season` | Season of purchase |
| `Review Rating` | Customer rating (1–5) |
| `Subscription Status` | Yes / No |
| `Shipping Type` | Standard, Express, Free Shipping, etc. |
| `Discount Applied` | Whether a discount was used |
| `Previous Purchases` | Count of past transactions |
| `Payment Method` | Venmo, Cash, Credit Card, PayPal, etc. |
| `Frequency of Purchases` | Weekly, Fortnightly, Monthly, etc. |

---

## 🛠️ Tools & Technologies

| Layer | Tool |
|---|---|
| **Data Analysis** | Python (Pandas, NumPy, Matplotlib, Seaborn) |
| **Notebook Environment** | Jupyter Notebook |
| **Database & Querying** | SQL (PostgreSQL / MySQL / SQL Server) |
| **Visualization & Dashboard** | Power BI |
| **Report Writing** | Microsoft Word / Google Docs |
| **Presentation** | Gamma (AI-powered PPT) |

---

## 🔢 Project Steps

### 1. 🐍 Python — Exploratory Data Analysis (EDA)
**File:** `Customer_Shopping_Behavior_Analysis.ipynb`

- Loaded and inspected the dataset (shape, dtypes, null values)
- Cleaned data: handled missing values, corrected data types, removed duplicates
- Performed univariate and bivariate analysis
- Visualized distributions, correlations, and trends using Matplotlib & Seaborn
- Engineered features such as `age_group` and `customer_segment`

### 2. 🗄️ SQL — Business Queries
**File:** `customer_behavior_sql.sql`

Ran structured queries on a relational database to extract business insights:

| Query | Purpose |
|---|---|
| Revenue by Gender | Compare male vs. female total spend |
| High-Value Discount Buyers | Customers using discounts AND spending above average |
| Shipping Type vs. Avg Spend | Compare Standard vs. Express order values |
| Subscription Revenue Analysis | Revenue and avg spend by subscription status |
| Top Discount Items | Top 5 items with highest discount application rate |
| Customer Segmentation (CTE) | Classify as New / Returning / Loyal by purchase count |
| Top Items per Category (Window Fn) | Ranked top 3 items per category using `ROW_NUMBER()` |
| Repeat Buyers by Subscription | Customers with 5+ purchases by subscription status |
| Revenue by Age Group | Total spend broken down by age demographics |

### 3. 📊 Power BI — Interactive Dashboard
**File:** `customer_behavior-dashboard.pbix`

Built an interactive dashboard featuring:
- Revenue by gender, age group, and season
- Subscription vs. non-subscription customer comparisons
- Discount usage patterns by product category
- Shipping type performance metrics
- Customer segmentation breakdown

### 4. 📝 Report
A structured written report summarizing the methodology, key findings, visualizations, and business recommendations derived from the analysis.

### 5. 📽️ Presentation
A clean, visual slide deck built using **Gamma** covering the project story — from problem statement to insights and recommendations — designed for a non-technical business audience.

---

## 📈 Dashboard Preview

> 📁 Open `customer_behavior-dashboard.pbix` in **Power BI Desktop** to explore the interactive dashboard.

**Dashboard Highlights:**
- 💰 Total Revenue & Average Order Value KPIs
- 👥 Customer Segments: New / Returning / Loyal
- 🛒 Top-Selling Categories and Items
- 📦 Shipping Preference Trends
- 🏷️ Discount Impact on Revenue

---

## 💡 Key Results & Insights

| Insight | Finding |
|---|---|
| **Subscribed customers** generate significantly higher revenue and avg spend than non-subscribed | Loyalty programs drive value |
| **Loyal customers** (10+ purchases) are the smallest segment but contribute disproportionate revenue | Retention is more valuable than acquisition |
| **Clothing** is the top-performing category with the most repeat purchases | Core category for promotions |
| **Express shipping** correlates with slightly higher average order values than Standard | Fast shipping attracts higher-intent buyers |
| **Discount usage** is highest for accessories and footwear items | Category-specific discount strategy needed |
| **Age group 35–54** drives the highest total revenue | Primary target demographic |

---

## ▶️ How to Run

### Python Notebook
```bash
# 1. Clone or download this repository
# 2. Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# 3. Launch Jupyter Notebook
jupyter notebook Customer_Shopping_Behavior_Analysis.ipynb
```

### SQL Queries
```sql
-- 1. Create a database and import customer_shopping_behavior.csv as the 'customer' table
-- 2. Open customer_behavior_sql.sql in your SQL client
--    (pgAdmin / MySQL Workbench / SSMS)
-- 3. Execute queries individually or all at once
```

### Power BI Dashboard
```
1. Download and install Power BI Desktop (free): https://powerbi.microsoft.com
2. Open customer_behavior-dashboard.pbix
3. Refresh the data source if prompted, pointing to customer_shopping_behavior.csv
4. Explore filters and visuals interactively
```

---

## 📁 Repository Structure

```
📦 customer-shopping-behavior-analysis
 ┣ 📓 Customer_Shopping_Behavior_Analysis.ipynb   ← Python EDA notebook
 ┣ 🗄️  customer_behavior_sql.sql                  ← SQL business queries
 ┣ 📊 customer_behavior-dashboard.pbix            ← Power BI dashboard
 ┣ 📄 customer_shopping_behavior.csv              ← Raw dataset
 ┗ 📘 README.md                                   ← Project documentation
```

---

## 👤 Author

Prajwal Virupaxi Marennavar
📧 marennavarprajwal34@gmail.com
🔗 https://www.linkedin.com/in/prajwal-marennavar/

---

*This project was built to demonstrate end-to-end data analytics skills including Python, SQL, and Business Intelligence reporting.*
