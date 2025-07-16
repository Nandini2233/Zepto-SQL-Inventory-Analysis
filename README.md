# 🛒 Zepto E-commerce SQL Data Analyst Portfolio Project

This is a professional, real-world SQL Data Analytics project built using an inventory dataset scraped from **Zepto**, one of India’s fastest-growing quick-commerce startups. The project replicates how data analysts handle raw e-commerce data — from exploration and cleaning to advanced business analysis — to derive actionable insights.

---

## 📌 Project Highlights

- ✔️ Real-world e-commerce inventory use case
- ✔️ 20+ SQL queries for revenue, pricing, and inventory analytics
- ✔️ Industry-grade data cleaning, EDA, and performance optimization
- ✔️ Built for job interviews, portfolios, and real analyst workflow simulation

---

## 🎯 Target Audience

This project is ideal for:

- 📊 Aspiring or entry-level **Data Analysts**
- 💼 Candidates applying to **retail**, **e-commerce**, or **product analyst** roles
- 🎓 Learners looking to strengthen their **SQL and business analysis skills**
- 👔 Professionals wanting to build top-tier **GitHub portfolio projects**

---

## 🧠 Project Objectives

The aim is to simulate the end-to-end process that data analysts perform in real-world scenarios:

- Design and create the inventory database schema
- Load and clean a large inventory dataset
- Perform structured EDA (Exploratory Data Analysis)
- Derive actionable business insights using advanced SQL queries
- Present metrics such as turnover ratio, stock-outs, and profitability

---

## 🧾 Dataset Overview

The dataset was sourced from **Kaggle**, based on product listings from Zepto’s app.

Each row is a **unique SKU (Stock Keeping Unit)**, which may belong to the same product but vary by size, weight, or offer — mimicking real inventory systems.

| Column                 | Description                                                |
|------------------------|------------------------------------------------------------|
| `sku_id`               | Unique ID for each SKU                                     |
| `name`                 | Product name                                               |
| `category`             | Product category (e.g. Fruits, Beverages, Snacks)          |
| `mrp`                  | Maximum Retail Price (in ₹, converted from paise)          |
| `discountPercent`      | Percentage discount applied                                |
| `discountedSellingPrice` | Final selling price post-discount                      |
| `availableQuantity`    | Stock available                                            |
| `weightInGms`          | Weight of the product in grams                             |
| `outOfStock`           | TRUE/FALSE for stock availability                          |
| `quantity`             | Units per package                                          |

---

## 🛠️ Tools & Technologies

- **PostgreSQL (SQL)**
- **pgAdmin 4**
- CSV (UTF-8 Format)
- Git & GitHub

---

## 🔧 Step-by-Step Project Workflow

### 1. Database Schema Creation

```sql
CREATE TABLE zepto (
  sku_id SERIAL PRIMARY KEY,
  category VARCHAR(120),
  name VARCHAR(150) NOT NULL,
  mrp NUMERIC(8,2),
  discountPercent NUMERIC(5,2),
  availableQuantity INTEGER,
  discountedSellingPrice NUMERIC(8,2),
  weightInGms INTEGER,
  outOfStock BOOLEAN,
  quantity INTEGER
);

