
```markdown
# 📊 Data Analyst Real-Time Project — Sales Analytics Dashboard (MySQL + Python + Power BI)

🚀 A complete end-to-end **Data Analytics Project** simulating a real-world business scenario.  
This project demonstrates how a data analyst connects to live databases, performs ETL (Extract-Transform-Load) operations, and builds insightful dashboards in Power BI.

---

## 🧠 Project Overview

The project focuses on **sales data analytics** for a fictional retail company.  
It covers every stage of the analytics pipeline:

1. 🗄️ **Database Creation (MySQL)**
2. 🧱 **Table Design (schema.sql)**
3. 📥 **Data Generation & Insertion (seed_data.py)**
4. 🔄 **ETL Process (fetch_data.py)**
5. 🕒 **Automation (scheduler.py)**
6. 📈 **Power BI Dashboard & Insights**

---

## 🧩 Folder Structure

```

📦 data-analyst-realtime-project
│
├── db/
│   ├── schema.sql          # Database schema (tables for regions, customers, products, sales)
│   └── seed_data.py        # Script to populate sample data
│
├── etl/
│   ├── fetch_data.py       # Fetch data from MySQL → CSV for Power BI
│   └── scheduler.py        # Automate ETL using schedule library
│
├── powerbi/
│   └── sales_data.csv      # Output data file used in Power BI
│
├── requirements.txt        # Required Python dependencies
└── README.md               # Project documentation

````

---

## ⚙️ Step-by-Step Setup

### 1️⃣ Create MySQL Database

```sql
CREATE DATABASE sales_db;
USE sales_db;
````

### 2️⃣ Create Tables

Run the SQL script inside `db/schema.sql` to create all tables:

* regions
* customers
* products
* sales

### 3️⃣ Insert Sample Data

Run the following Python script to populate data:

```bash
cd db
python seed_data.py
```

✅ This will generate 100 customers, 1000 random sales transactions, and insert them into your MySQL tables.

---

## 🧰 Install Required Libraries

```bash
pip install -r requirements.txt
```

**Requirements include:**

```
mysql-connector-python
pandas
schedule
openpyxl
numpy
```

---

## 🔄 ETL — Data Extraction and CSV Export

The `etl/fetch_data.py` script performs the ETL process:

* Connects to MySQL
* Joins multiple tables
* Loads the data into a Pandas DataFrame
* Exports it to `powerbi/sales_data.csv`

```bash
cd etl
python fetch_data.py
```

✅ Output:

```
✅ Data exported successfully to: ../powerbi/sales_data.csv
```

---

## 🕒 Automate ETL Using Scheduler

To make the data pipeline run automatically every few minutes:

```bash
python scheduler.py
```

By default, the job runs **every 1 minute** (configurable).
It re-fetches the latest data and updates your Power BI CSV source automatically.

---

## 🧩 SQL Query Logic

The SQL query joins 4 tables — **sales, customers, regions, products** — to create a wide, analysis-ready dataset.

```sql
SELECT 
    s.sale_id,
    s.sale_date,
    c.customer_name,
    c.email,
    r.region_name,
    p.product_name,
    p.category,
    s.quantity,
    s.sale_amount
FROM sales s
JOIN customers c ON s.customer_id = c.customer_id
JOIN regions r ON s.region_id = r.region_id
JOIN products p ON s.product_id = p.product_id;
```

💡 **Key Concepts**

* INNER JOIN ensures consistent data across dimensions
* Denormalized table for Power BI reporting
* Optimized for performance (indexes recommended)
* Easy to add WHERE conditions for date filters or incremental loads

---

## 📊 Power BI Analysis Documentation

### 🎯 Objective

To uncover actionable business insights from sales data — improving decisions related to products, regions, and customers.

### 🧮 Key KPIs

* **Total Revenue (₹ / $)**
* **Total Quantity Sold**
* **Average Order Value (AOV)**
* **Top Customers & Repeat Buyers**
* **Profitability by Product & Region**
* **Monthly Sales Growth**

### 🔍 Data Insights & Dashboards

#### 1️⃣ Sales Overview

* Total revenue, sales volume, and average sale per transaction
* Quick executive summary view
* Updated in near real-time using Python ETL

#### 2️⃣ Customer Performance

* Top 10 revenue-contributing customers
* Repeat customer patterns & CLV trends
* Identify underperforming customer segments

#### 3️⃣ Product Category Insights

* Revenue distribution by product & category
* Seasonal and promotional trends
* Supports inventory and marketing strategy

#### 4️⃣ Regional Sales Distribution

* Compare regions to identify growth markets
* Highlight weak-performing regions
* Aid in decision-making for expansion or restructuring

#### 5️⃣ Sales Trends Over Time

* Time-series analysis (daily / monthly trends)
* Detect growth or dips
* Helps with forecasting & budgeting

#### 6️⃣ Customer Retention

* New vs. returning customer ratios
* Loyalty analysis
* Retention-driven insights for CRM strategies

---

## ⚡ Dashboard Features

✅ Interactive filters: Region, Product, Date Range
✅ Drill-through: Click to explore region or customer details
✅ Auto-updated data via Python scheduler
✅ Export options: Excel / PDF
✅ Real-time business impact tracking

---

## 🧰 Tech Stack

| Component     | Technology Used                            |
| ------------- | ------------------------------------------ |
| Database      | MySQL                                      |
| ETL           | Python (mysql-connector, pandas, schedule) |
| Visualization | Power BI                                   |
| Storage       | CSV / Excel                                |
| Automation    | Python Scheduler                           |

---

## 🚀 Project Impact

✅ Improved business decision-making
✅ Fully automated ETL workflow
✅ Real-time Power BI dashboard
✅ Scalable architecture for real-world datasets

---

## 🧑‍💻 Author

**👋 Shahid Pathan**
🎓 Data Analyst | Python Developer | Instructor
📍 Shiddat Programming Institute
📧 [Your Email or Portfolio Link]

---

## 🌟 Contributing

Pull requests are welcome!
For major changes, please open an issue first to discuss your ideas.

---

## 📄 License

This project is open-source under the **MIT License**.

---

```

---

```
