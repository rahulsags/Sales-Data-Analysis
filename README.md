# Sales-Data-Analysis - Power BI Dashboard

This project is a complete Sales Insights analysis using MySQL for data preprocessing and Power BI for visualization. It helps in understanding customer behavior, market trends, and revenue generation across various regions.

![dashboard_preview](https://github.com/user-attachments/assets/605a168e-a4d0-40c2-97cf-d3945dacb473)

## 🔧 Project Setup

### 1. Install MySQL
Follow any latest video tutorial to install MySQL on your local machine.

### 2. Import Database
- Download the SQL dump file: `Db/db_dump.sql`
- Use the MySQL CLI or Workbench to import the database:
  ```sql
  SOURCE path/to/db_dump.sql;

## Data Analysis Using SQL

All SQL queries are available in the `queries/analysis_queries.sql` file.

## Power BI Dashboard

The Power BI file `Sales_Data_Analysis.pbix` includes:
- Revenue trend analysis
- Market-wise performance
- Monthly sales breakdown
- Customer segment insights

### Power Query Formula
To normalize the currency (USD to INR):

```m
= Table.AddColumn(#"Filtered Rows", "norm_amount",
    each if [currency] = "USD" or [currency] ="USD#(cr)"
    then [sales_amount] * 85 else [sales_amount], type any)
```

## Tools Used
- Power BI Desktop
- MySQL
- SQL Workbench / MySQL CLI

## Notes
- Currency conversion rate used: 1 USD = 85 INR

