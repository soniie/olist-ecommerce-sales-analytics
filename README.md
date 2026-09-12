# Olist E-Commerce Sales Analytics

> End-to-end e-commerce analytics project using SQL, Python, and Power BI to transform transactional data into business insights.

![Dashboard Preview](dashboard/dashboard_preview.png)

---

## Overview

This project analyzes the **Brazilian E-Commerce Public Dataset by Olist** to understand sales performance, customer behavior, product categories, payment methods, geographic demand, and freight costs.

The project follows an end-to-end analytics workflow, starting from raw transactional data and progressing through database analysis, exploratory data analysis, and business intelligence reporting.

### Project Workflow

**Raw Data → PostgreSQL → SQL Analysis → Python EDA → Power BI → Business Insights**

The final output is a single-page Power BI dashboard designed to provide a concise view of overall e-commerce performance.

---

## Problem Statement

E-commerce businesses generate large volumes of transactional data across multiple related tables.

The objective of this project is to combine and analyze this data to answer important business questions such as:

- What is the overall revenue generated?
- How many orders and customers does the platform have?
- What is the average order value?
- Which product categories contribute most to revenue?
- Which states generate the highest number of orders?
- Which payment methods are most commonly used?
- How does freight cost vary across product categories?
- How do sales change over time?
- What proportion of customers make repeat purchases?

---

## Dataset

### Brazilian E-Commerce Public Dataset by Olist

The dataset contains approximately **100,000 orders from 2016–2018** across multiple marketplaces in Brazil.

It includes information related to:

- Orders
- Customers
- Products
- Sellers
- Order items
- Payments
- Reviews
- Product categories
- Customer and seller locations

### Dataset Source

The original dataset is available on Kaggle:

**Brazilian E-Commerce Public Dataset by Olist**

https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

### Dataset Tables Used

| Table | Description |
|---|---|
| `customers` | Customer information and location |
| `orders` | Order status and timestamps |
| `order_items` | Products purchased in each order |
| `products` | Product information and attributes |
| `payments` | Payment methods and payment values |
| `reviews` | Customer review information |
| `product_category_name_translation` | Portuguese-to-English category translation |

> The original raw CSV files are not stored in this repository. They can be downloaded from the original Kaggle source above.

---

## Tools & Technologies

| Technology | Purpose |
|---|---|
| **PostgreSQL** | Data storage, integration and analysis |
| **pgAdmin** | Database management |
| **SQL** | Data cleaning, joins and business analysis |
| **Python** | Exploratory data analysis |
| **Pandas** | Data manipulation |
| **NumPy** | Numerical operations |
| **Matplotlib** | EDA visualization |
| **Power BI** | Dashboard and reporting |
| **DAX** | Measures and calculated fields |
| **GitHub** | Project documentation and version control |

---

## Project Methodology

### 1. Business Understanding

The project began by identifying the key business areas to analyze:

- Sales performance
- Customer activity
- Product categories
- Geographic demand
- Payment behavior
- Freight costs
- Repeat purchasing

---

### 2. Data Preparation

The Olist datasets were imported into PostgreSQL and organized into related tables.

The data was prepared by:

- Checking data quality
- Handling missing values
- Identifying duplicate records
- Converting date fields
- Joining related tables
- Translating product categories
- Creating analytical fields

A master analytical dataset was then created for downstream analysis.

---

### 3. SQL Analysis

SQL was used as the main data preparation and analysis layer.

Key tasks included:

- Joining customers, orders, products, payments and reviews
- Calculating revenue
- Counting orders and customers
- Analyzing product categories
- Analyzing state-wise order distribution
- Analyzing payment methods
- Calculating freight costs
- Preparing data for Python and Power BI

---

### 4. Python Exploratory Data Analysis

Python was used to explore the cleaned analytical dataset.

The EDA focused on:

- Missing values
- Duplicate records
- Data types
- Date ranges
- Revenue trends
- Order behavior
- Product category performance
- Customer activity
- Geographic distribution

Libraries used:

```text
pandas
numpy
matplotlib
```

---

### 5. Power BI Dashboard

The final analysis was converted into a one-page Power BI dashboard.

### KPI Cards

The dashboard contains:

- **Total Revenue:** ~R$13.21M
- **Total Orders:** ~99K
- **Total Customers:** ~95K
- **Average Order Value:** ~R$133.93
- **Repeat Customer Rate:** ~3.05%

### Dashboard Visuals

The dashboard includes:

- **Sales Over Time**
- **Revenue by Product Category**
- **Top States by Orders**
- **Payment Method Distribution**
- **Freight Cost % by Category**
- **Key Takeaways**

The dashboard was intentionally kept to a single page to make the main business story easy to understand.

---

## Dashboard / Output

The final output is a **single-page Power BI dashboard** designed to present the most important e-commerce performance metrics in a clear and concise format.

### Dashboard Flow

**Performance → Trends → Categories → Geography → Payments → Logistics**

### Dashboard Preview

![Olist E-Commerce Sales Analytics Dashboard](dashboard/dashboard_preview.png)

---

## Key Insights

### 1. Sales Performance

Sales activity changes over time, making the sales trend useful for understanding periods of stronger and weaker marketplace performance.

### 2. Category Performance

Revenue is distributed unevenly across product categories, allowing high-performing categories to be identified and compared.

### 3. Geographic Demand

Order volume varies considerably across Brazilian states, showing that marketplace activity is geographically concentrated.

### 4. Payment Behavior

Customers use multiple payment methods, providing insight into purchasing and transaction preferences.

### 5. Freight Cost

Freight cost as a percentage of revenue varies across product categories.

Categories with relatively high freight-to-revenue ratios may require closer attention to pricing, shipping strategy, and profitability.

### 6. Customer Retention

The repeat customer rate is approximately **3.05%**, indicating that repeat purchasing represents a relatively small portion of the customer base.

This highlights a potential opportunity for stronger customer retention and repeat-purchase strategies.

---

## Project Structure

```text
olist-ecommerce-sales-analytics/
│
├── README.md
│
├── dashboard/
│   ├── Olist_Ecommerce_Sales_Analytics.pbix
│   └── dashboard_preview.png
│
├── python/
│   └── Olist_Sales_EDA.ipynb
│
├── sql/
│   └── olist_sales_analysis.sql
│
└── data/
    └── README.md
```

---

## How to Run the Project

### Step 1 — Download the Dataset

Download the original **Brazilian E-Commerce Public Dataset by Olist** from Kaggle:

https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce

Extract the CSV files locally.

The raw dataset is not included in this repository.

---

### Step 2 — Set Up PostgreSQL

Create a PostgreSQL database and import the required Olist CSV files.

The project uses the following tables:

```text
customers
orders
order_items
products
payments
reviews
product_category_name_translation
```

---

### Step 3 — Run the SQL Analysis

Open:

```text
sql/olist_sales_analysis.sql
```

Run the SQL queries in PostgreSQL / pgAdmin.

The SQL workflow prepares the data required for analysis and reporting.

---

### Step 4 — Run the Python Notebook

Open:

```text
python/Olist_Sales_EDA.ipynb
```

Run the notebook cells in order.

Install the required libraries if needed:

```bash
pip install pandas numpy matplotlib
```

---

### Step 5 — Open the Power BI Dashboard

Open:

```text
dashboard/Olist_Ecommerce_Sales_Analytics.pbix
```

If required, update the PostgreSQL data source to match your local database connection.

---

## Results & Conclusion

This project demonstrates how raw e-commerce transaction data can be transformed into a structured analytics workflow.

Using **SQL, Python, and Power BI**, the project moves from data preparation and exploration to visual storytelling and business insights.

The final dashboard provides a concise view of:

- Revenue performance
- Order activity
- Customer activity
- Category contribution
- Geographic demand
- Payment behavior
- Freight-cost patterns
- Customer retention opportunities

The project demonstrates an end-to-end approach to turning transactional data into information that can support business decision-making.

---

## Limitations

- The analysis is based on historical Olist marketplace data from 2016–2018.
- The dataset represents Olist marketplace activity and may not represent the entire Brazilian e-commerce market.
- The analysis is descriptive and does not attempt to predict future sales.
- Profitability cannot be measured directly because the dataset does not contain complete business cost information.

---

## Future Improvements

Possible extensions of this project include:

- Sales forecasting
- Customer segmentation
- Customer lifetime value analysis
- Product recommendation systems
- Delivery-time analysis
- Seller performance analysis
- Profitability analysis
- Advanced customer retention analysis

---

## Author

**Soni Kumari**

B.Sc. Computer Science & Data Analytics  
IIT Patna

**Skills:** SQL • Python • Power BI • Data Analytics • UI/UX Design

---

## Acknowledgements

Dataset provided by **Olist** through the Brazilian E-Commerce Public Dataset.

Dataset source:

https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce



