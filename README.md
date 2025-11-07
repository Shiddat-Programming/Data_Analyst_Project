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

📦 data-analyst-realtime-project
│
├── db/
│ ├── schema.sql # Database schema (tables for regions, customers, products, sales)
│ └── seed_data.py # Script to populate sample data
│
├── etl/
│ ├── fetch_data.py # Fetch data from MySQL → CSV for Power BI
│ └── scheduler.py # Automate ETL using schedule library
│
├── powerbi/
│ └── sales_data.csv # Output data file used in Power BI
│
├── requirements.txt # Required Python dependencies
└── README.md # Project documentation
