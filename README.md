# 👨🏻‍💻 Customer Shopping Behavior Analysis

A complete, end-to-end data analytics portfolio project analyzing **3,900 customer transactions** across product categories to uncover spending patterns, customer segments, product preferences, and subscription behavior.

---

## 📌 Project Overview

This project simulates a corporate-grade analytics workflow using **Python**, **SQL (PostgreSQL)**, and **Power BI**:

✅ **Data Preparation & EDA (Python)** – Clean, transform, and engineer features from raw transactional data.

✅ **Data Analysis (SQL)** – Run structured queries to extract insights on revenue, customer segments, discount behavior, and product performance.

✅ **Visualization & Insights (Power BI)** – Build an interactive dashboard highlighting key trends for stakeholder decision-making.

✅ **Report** – Summarize findings and business recommendations in a structured project report.

---

## 🗂️ Dataset Summary

| Attribute | Detail |
|---|---|
| Total Records | 3,900 rows |
| Total Columns | 18 features |
| Missing Data | 37 values in Review Rating column |
| Demographics | Age, Gender, Location, Subscription Status |
| Purchase Details | Item, Category, Amount (USD), Season, Size, Color |
| Behavioral Features | Discount Applied, Previous Purchases, Frequency, Rating, Shipping Type |

---

## 🛠️ Tech Stack

- **Python** – pandas, SQLAlchemy (EDA + database integration)
- **PostgreSQL** – Business query analysis
- **Power BI** – Interactive dashboard
- **Git** – Version control

---

## 🚀 How to Use This Project

1. **Clone the repository**
```bash
   git clone https://github.com/your-username/customer-shopping-behavior-analysis.git
   cd customer-shopping-behavior-analysis
```

2. **Open the Python Notebook** (`Customer_Shopping_Behavior_Analysis.ipynb`)
   - Data import and exploration
   - Missing value imputation (median by category)
   - Feature engineering: `age_group`, `purchase_frequency_days`
   - Data consistency checks
   - Load cleaned data into PostgreSQL

3. **Run SQL Queries** (`customer_behavior_sql_queries.sql`)
   - Revenue by Gender
   - High-Spending Discount Users
   - Top 5 Products by Rating
   - Shipping Type Comparison
   - Subscribers vs. Non-Subscribers
   - Discount-Dependent Products
   - Customer Segmentation (New / Returning / Loyal)
   - Top 3 Products per Category
   - Repeat Buyers & Subscriptions
   - Revenue by Age Group

4. **Open Power BI Dashboard** (`customer_behavior_dashboard.pbix`)
   - Connect to your PostgreSQL database
   - Explore KPIs: 3.9K customers, $59.76 avg purchase, 3.75 avg rating
   - Filter by Subscription Status, Gender, Category, Shipping Type

5. **Read the Project Report** (`Customer_Shopping_Behavior_Analysis.pdf` / `.docx`)
   - Full methodology, SQL results, and business recommendations

---

## 📊 Key Findings

| Insight | Finding |
|---|---|
| Top Revenue Gender | Male – $157,890 vs Female – $75,191 |
| Highest-Rated Product | Gloves (3.86 avg rating) |
| Most Discount-Dependent | Hat (50% of purchases used a discount) |
| Largest Customer Segment | Loyal – 3,116 customers |
| Top Revenue Age Group | Young Adult – $62,143 |
| Avg Spend: Subscribers vs Not | $59.49 vs $59.87 |
| Express vs Standard Shipping | $60.48 vs $58.46 avg spend |

---

## 💡 Business Recommendations

1. **Boost Subscriptions** – Promote exclusive perks to grow beyond the current 27% subscriber rate.
2. **Customer Loyalty Programs** – Reward repeat buyers to deepen engagement.
3. **Review Discount Policy** – Audit margins for high-discount products (Hat, Sneakers, Coat).
4. **Product Positioning** – Feature top-rated items (Gloves, Sandals, Boots) in campaigns.
5. **Targeted Marketing** – Focus on Young Adults and Express-shipping users.
6. **High-Value Discount Segment** – Re-engage 839 high-spending discount users with personalised offers.
7. **Customer Acquisition** – Invest in acquisition channels; only 83 New customers recorded.
8. **Gender Revenue Gap** – Investigate and address the 2:1 male-to-female revenue disparity.

---

## 📂 Project Structure

```
customer-shopping-behavior-analysis/
│
├── Customer_Shopping_Behavior_Analysis.ipynb   # Python EDA + DB integration
├── customer_behavior_sql_queries.sql           # PostgreSQL business queries
├── customer_behavior_dashboard.pbix            # Power BI dashboard
├── Customer_Shopping_Behavior_Analysis.pdf     # Project report (PDF)
├── Customer_Shopping_Behavior_Analysis.docx    # Project report (Word)
└── README.md
```

---

