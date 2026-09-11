# Olist E-Commerce Sales Analytics

> An end-to-end e-commerce analytics project using SQL, Python, and Power BI to analyze sales performance, customers, products, payments, geography, and freight costs.

---

## Overview

This project analyzes the **Olist Brazilian E-Commerce dataset** to understand marketplace performance across revenue, orders, customers, product categories, payment methods, states, and logistics.

The project follows a complete analytics workflow:

**Business Understanding → Data Preparation → SQL Analysis → Python EDA → Power BI Dashboard → Business Insights**

The final output is a single-page Power BI dashboard designed to present key business metrics and insights in a clear and professional way.

---

## Problem Statement

E-commerce businesses generate large amounts of transactional data across multiple tables. Without proper analysis, it can be difficult to understand overall business performance and identify important trends.

This project aims to analyze the Olist e-commerce data and answer questions such as:

- How much revenue is being generated?
- How many orders and customers does the platform have?
- What is the average order value?
- Which product categories contribute most to revenue?
- Which states have the highest order volumes?
- Which payment methods are most commonly used?
- How does freight cost vary across product categories?
- What patterns can be observed in sales over time?
- What does customer repeat-purchase behavior look like?

---

## Dataset

The project uses the **Olist Brazilian E-Commerce dataset**, which contains information about:

- Customers
- Orders
- Order Items
- Products
- Payments
- Reviews
- Product Category Translations

The data was imported into PostgreSQL, cleaned and integrated into an analytical dataset, then explored using Python and visualized using Power BI.

> **Note:** The original raw CSV files are not included in this repository.

---

## Tools and Technologies

| Tool / Technology | Purpose |
|---|---|
| **PostgreSQL** | Data storage, cleaning, joins and analysis |
| **Python** | Data cleaning and exploratory data analysis |
| **Pandas** | Data manipulation |
| **NumPy** | Numerical operations |
| **Matplotlib** | Data visualization during EDA |
| **Power BI** | Dashboard creation and visualization |
| **DAX** | Measures and calculated fields |
| **GitHub** | Project documentation and version control |

---

## Methods

### 1. Data Preparation

The Olist dataset was imported into PostgreSQL and organized into related tables:

- `customers`
- `orders`
- `order_items`
- `products`
- `payments`
- `reviews`
- `product_category_name_translation`

The tables were cleaned and joined to create a master analytical dataset for further analysis.

---

### 2. SQL Analysis

SQL was used to:

- Join related tables
- Clean and prepare the data
- Handle missing and duplicate records
- Create analytical fields
- Calculate revenue and order metrics
- Analyze product categories
- Analyze state-wise order distribution
- Analyze payment methods
- Analyze freight costs
- Prepare the master dataset for Python and Power BI

---

### 3. Python Exploratory Data Analysis

Python was used to further inspect and explore the cleaned dataset.

The analysis included:

- Checking missing values
- Checking duplicate records
- Converting and working with date fields
- Exploring revenue patterns
- Analyzing order behavior
- Exploring product category performance
- Examining customer patterns
- Exploring geographic trends

---

### 4. Power BI Dashboard

The final analysis was presented through a **single-page Power BI dashboard**.

### Key Performance Indicators

- **Total Revenue**
- **Total Orders**
- **Total Customers**
- **Average Order Value**
- **Repeat Customer Rate**

### Dashboard Visuals

- **Sales Over Time**
- **Revenue by Category**
- **Top States by Orders**
- **Payment Method Distribution**
- **Freight Cost % by Category**
- **Key Takeaways**

The dashboard was designed to follow a simple analytical story:

**Performance → Trends → Categories → Geography → Payments → Logistics**

---

## Key Insights

The analysis highlights the following business patterns:

1. **Sales performance changes over time**, allowing periods of stronger and weaker activity to be identified.

2. **Revenue is distributed unevenly across product categories**, making category-level performance useful for understanding major revenue contributors.

3. **Order volume varies across Brazilian states**, showing geographic concentration in marketplace activity.

4. **Customers use multiple payment methods**, providing insight into purchasing preferences.

5. **Freight cost as a percentage of revenue differs across product categories**, which can have implications for pricing and profitability.

6. **The repeat-customer rate is relatively low**, suggesting an opportunity to improve customer retention and encourage repeat purchases.

---

## Dashboard / Output

The final Power BI dashboard provides a compact view of:

- Overall sales performance
- Sales trends
- Category performance
- State-wise order distribution
- Payment behavior
- Freight-cost patterns
- Customer repeat-purchase behavior

### Dashboard Preview


```text
dashboard/dashboard_preview.png
