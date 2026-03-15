# 📊 Warehouse Sales Data Analysis 

A complete **SQL-based data analysis project** exploring warehouse sales data to uncover **customer purchasing behavior, product performance, and revenue trends over time**.

The project integrates multiple datasets and applies **SQL analytics techniques** to generate business insights that support data-driven decision making.

The entire analysis has been carried out using **Microsoft SQL Server**.

---

# 🚀 Project Overview

Using exploratory data analysis on warehouse sales data, this project examines **sales trends, customer spending behavior, and product performance** across multiple dimensions.

By analyzing **60K+ transactions across 18K+ customers and 295 products**, the project identifies:

- Revenue trends over time
- Customer purchasing patterns
- Product category performance
- Sales distribution across customers and products

---

# 🗂 Dataset Overview

The project uses **three relational datasets**.

### Customers Dataset
Contains customer demographic information.

**Key columns**
- `customer_key` - `customer_number`
- `first_name` - `last_name`
- `country`
- `gender`
- `birthdate`

**Total 18,484 customers**
### Products Dataset
Contains product catalog and category information.

**Key columns**
- `product_key` - `product_name`
- `category` - `subcategory`
- `cost`
- `product_line`

**Total Records:** 295 products
### Sales Dataset
Contains transaction-level sales data.

**Key columns**
- `order_number` - `order_date`
- `product_key`
- `customer_key`
- `sales_amount` - `quantity` - `price`

**Total Records:** 60,398 transactions

# 🏗 Data Model

The project follows a **simple star-schema structure**.
```
          dim_customers
                 │
                 │
dim_products──fact_sales
```
---

# 📈 Analysis Performed

### 1️⃣ Sales Trend Analysis
Analyzed monthly sales performance and revenue patterns over time.

Key analysis included:
- Monthly revenue trends
- Running total sales using window functions
- Seasonal patterns in sales

### 2️⃣ Product Performance Analysis

Evaluated product and category performance to identify:

- High-revenue product categories
- Best-performing products
- Quantity distribution across products

### 3️⃣ Customer Behavior Analysis

Analyzed customer purchasing behavior to compute:

- Total customer spending
- First purchase date
- Most recent purchase date
- Customer lifespan
---
# 👥 Customer Segmentation

Customers were segmented based on **spending and purchase lifespan**.

| Segment | Criteria |
|------|------|
| VIP | lifespan ≥ 12 months AND spending > 5000 |
| Regular | lifespan ≥ 12 months AND spending ≤ 5000 |
| New | lifespan < 12 months |

This segmentation helped to identify **high-value customers and retention opportunities**.

---

# 🧾 Analytical Views Created

To simplify reporting and downstream analysis, two analytical views were created.

### Customer Report View

Aggregated customer-level metrics including:

- Total spending
- First purchase date
- Last purchase date
- Customer lifespan

A glimpse of the view:

---

### Product Report View

Aggregated product-level performance metrics including:

- Total revenue per product
- Total quantity sold
- Product category performance

A glimpse of the view:

# 📁 Project Structure
```
Warehouse_Sales_Data_Analysis
│
├── datasets
│ ├── gold.dim_customers.csv
│ ├── gold.dim_products.csv
│ ├── gold.fact_sales.csv
│ │
│ └── View
│ ├── report_customers.csv
│ └── report_product.csv
│
├── SQL Scripts
│ ├── Data_exploration.sql
│ ├── Trend_over_time.sql
│ ├── Proportion_analysis.sql
│ ├── Data_segmentation.sql
│ ├── Cumulative_analysis.sql 
│ └── Performance_analysis.sql
├── LICENSE
└── README.md
```
---

# 🛠 Tools Used

- **SQL Server**
- **T-SQL**
- **SQL Server Management Studio (SSMS)**

---

# 👨‍💻 Author

**Dipean Dasgupta**

GitHub  
https://github.com/DipeanDas
