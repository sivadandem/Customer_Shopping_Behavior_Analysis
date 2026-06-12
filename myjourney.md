# 👤 Siva Dandem

## 🎓 Education

| Field | Details |
|-------|---------|
| **Degree** | B.Tech — Computer Science Engineering |
| **University** | Lovely Professional University (LPU) |
| **Year** | 2023 |

---

## 💡 Skills

| Tool | Usage |
|------|-------|
| 🐍 **Python** 
| 🗄️ **SQL**
| 📊 **Power BI** 
| 📗 **Excel**

---

## 📦 Project — Customer Shopping Behavior Analysis

> **Goal:** Uncover spending patterns, customer segments, and product preferences to help businesses make smarter decisions.

### Dataset Overview

| Attribute | Value |
|-----------|-------|
| **Total Transactions** | 3,900 |
| **Variables** | 18 |
| **Product Categories** | Clothing, Accessories, Footwear, Outerwear |

---

## 🔄 Project Pipeline

### Step 1 — 🐍 Python & Pandas · *Data Cleaning & Feature Engineering*

- Loaded and inspected the dataset
- Found and handled **37 missing values** in the `Review Rating` column
- Imputed using **median rating per product category** *(not global median — more accurate)*
- Standardized column names for consistency
- Engineered new features:
  - `Age Groups`
  - `Purchase Frequency`
- Dropped a redundant column

> 💡 **Why category-level imputation?** 

---

### Step 2 — 🗄️ SQL Server · *Business Question Queries*

Loaded the clean dataset into SQL Server and wrote queries to answer:

| Business Question | Query Focus |
|-------------------|-------------|
| 💰 Revenue analysis | Revenue breakdown by gender |
| ⭐ Product performance | Top-rated products per category |
| 🏷️ Subscription impact | Subscriber vs non-subscriber spending |
| 👥 Customer segmentation | Segment-level spend & behavior patterns |

> **Why SQL?** The data was relational and the queries needed to be precise 

---

### Step 3 — 📊 Power BI · *Interactive Dashboard*

Built a dashboard to visualize all findings in one place:

- ✅ Total Revenue KPI
- ✅ Customer Segments breakdown
- ✅ Category Performance comparison
- ✅ Revenue trends over time
- ✅ Top products by rating

---

## 🔑 Key Business Insights

### 1. Discounts don't always reduce spend

> 🛒 **839 customers** who used discounts **still spent above average.**

This challenges the common assumption that discounts erode revenue. **Recommendation:** Use discounts strategically as a loyalty driver, not just a clearance tool.

### 2. Category-aware data quality matters

Imputing missing review ratings at the **category level** rather than globally produced more reliable downstream analysis — a small data decision with a measurable accuracy impact.

---

## 🚀 Goal

Joining **Parentof Solutions** as a **Data Analyst** — excited to contribute by translating data into decisions that drive real business impact.

---
