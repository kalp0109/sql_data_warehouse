# SQL Data Warehouse Project

## 📌 Project Overview

This project demonstrates the design and implementation of a modern SQL Data Warehouse using SQL Server. It follows the **Medallion Architecture (Bronze → Silver → Gold)** to ingest, cleanse, transform, and model data into an analytics-ready data warehouse.

The solution integrates CRM and ERP source systems, performs data quality checks, and builds a Star Schema for reporting and business intelligence.

---
## 🎯 Project Objective

The objective of this project is to design and implement a scalable SQL Data Warehouse that consolidates CRM and ERP data into a centralized analytical model. The solution demonstrates ETL development, data cleansing, dimensional modeling, and Star Schema implementation using SQL Server.

## 🏗️ Architecture

<p align="center">
  <img src="https://github.com/user-attachments/assets/de2d9267-275c-4e40-afce-6ed9240599bb" width="900">
</p>


## 🚀 Features

- Database and schema creation
- Bronze, Silver, and Gold layers
- ETL using SQL Server Stored Procedures
- Data cleansing and standardization
- Duplicate removal
- Data quality validation
- Incremental data loading
- Star Schema implementation
- Fact and Dimension Views
- Business-ready analytical model

---

## 🛠️ Technologies Used

- SQL Server
- T-SQL
- SQL Server Management Studio (SSMS)
- Git
- GitHub

---

## Integration Model

<img width="2256" height="1192" alt="image" src="https://github.com/user-attachments/assets/65720c22-1a1f-45e2-a1f6-e185a03f5df6" />

---

## 📊 Data Model

### Dimension Tables

- dim_customers
- dim_products

### Fact Table

- fact_sales

<img width="1716" height="1262" alt="image" src="https://github.com/user-attachments/assets/f4ab6970-defc-450a-94bf-de5342a8bf29" />


## 🔄 ETL Pipeline

### Bronze Layer
- Load raw CRM and ERP CSV files
- Bulk insert into Bronze tables
- Preserve raw source data

### Silver Layer
- Remove duplicates
- Handle missing values
- Standardize formats
- Normalize data
- Apply business rules

### Gold Layer
- Build dimension tables
- Create fact table
- Implement Star Schema
- Prepare analytics-ready datasets

---

## 📈 Project Workflow

1. Create Database
2. Create Schemas
3. Create Bronze Tables
4. Load Bronze Data
5. Create Silver Tables
6. Transform Bronze → Silver
7. Create Gold Views
8. Build Star Schema
9. Query Business Data

---

## ▶️ How to Run

1. Clone the repository

```bash
git clone https://github.com/your-username/sql_data_warehouse.git
```

2. Open SQL Server Management Studio.

3. Execute the scripts in the following order:

```
scripts/init_database.sql

scripts/bronze/
    ddl_bronze.sql
    proc_load_bronze.sql

scripts/silver/
    ddl_silver.sql
    proc_load_silver.sql

scripts/gold/
    ddl_gold.sql
```

4. Execute the ETL procedures

```sql
EXEC bronze.load_bronze;

EXEC silver.load_silver;
```

---

## 📷 Future Improvements

- Incremental Loading
- Error Logging Framework
- SQL Server Agent Scheduling
- Data Quality Dashboard
- Automated Testing
- Power BI Dashboard Integration

---
## ✅ Project Outcomes

- Built a three-layer SQL Data Warehouse
- Implemented reusable ETL stored procedures
- Designed a Star Schema for analytics
- Standardized and cleansed CRM and ERP data
- Created business-ready dimension and fact views
