---
name: Data Warehouse Project
tools: [SQL, ETL, Data modeling]
image: https://res.cloudinary.com/dn5snxslw/image/upload/v1769855656/Datawarehouse_td8wh2.webp
description: This project presents an interactive dashboard for analyzing online advertising campaigns.Welcome to the MySQL Data Warehouse & Analytics Repository! This project demonstrates how to design and implement a complete data warehouse solution, including data modeling, ETL processes, and SQL-driven analytics to convert raw datasets into valuable business insights.
---

## MySQL Data Warehouse & Analytics Project

### Project Summary

This project demonstrates the **end-to-end design and implementation of a data warehouse** using **MySQL**, transforming raw operational data from multiple source systems into a structured, analytics-ready environment.

The solution emphasizes **dimensional data modeling, ETL workflows, and SQL-driven analytics** to support business reporting, KPI tracking, and data-informed decision-making.

---

## Objective

- Design a **scalable analytical data warehouse** in MySQL  
- Consolidate ERP and CRM sales data into a **single source of truth**  
- Enable efficient querying through **star-schema dimensional modeling**  
- Deliver actionable business insights using SQL  

---

## Project Scope & Architecture

### Data Warehouse Design

The warehouse was purpose-built for **analytical workloads**, rather than transactional processing.

**Key Design Principles**

- Centralized storage for sales and performance analytics  
- Clean, consistent, and query-optimized schema  
- Easy interpretation for analysts and business stakeholders  
- Focus on current-state analytics  

---

## Data Modeling & Implementation

### Dimensional Modeling (Star Schema)

I designed a **star-schema data model** optimized for reporting performance and simplicity.

**Core Components**

- **Fact Table**
  - Sales metrics including revenue, quantity, and transaction-level measures  

- **Dimension Tables**
  - Customers  
  - Products  
  - Dates  
  - Sales channels  
  - Geographic attributes (where applicable)  

**Outcome**

A clean and intuitive schema that reduces query complexity and improves analytical performance.

![Data Model](/assets/image/data_model_main.webp)

---

## ETL Workflow & Data Preparation

### 1. Data Integration

- Integrated raw data from **ERP and CRM systems**  
- Standardized data formats across multiple sources  
- Aligned business keys to ensure accurate joins and relationships  

---

### 2. Data Cleaning & Transformation

- Removed duplicates and invalid records  
- Resolved inconsistencies in naming conventions, formats, and missing values  
- Applied SQL-based transformations to prepare fact and dimension tables  

**Outcome**

High-quality, analytics-ready data with consistent business definitions.

---

### 3. Data Loading

- Loaded transformed datasets into MySQL warehouse tables  
- Enforced referential integrity between fact and dimension tables  
- Optimized table structures for analytical querying

  
[Click here to explore the SQL queries](https://github.com/DavidAsikpo/DavidAsikpo.github.io/tree/master/assets/image/sql_scripts)


---

## Analytics & SQL Reporting

### Business Questions Answered

Using SQL queries, the warehouse supports analysis of:

- **Customer behavior**
  - Top customers by revenue  
  - Repeat purchase patterns  

- **Product performance**
  - Best-selling products  
  - Revenue contribution by product category  

- **Sales trends**
  - Revenue growth over time  
  - Time-based performance analysis  

---

### KPIs Delivered

- Total revenue and sales volume  
- Average order value  
- Customer contribution metrics  
- Product-level performance indicators  

**Outcome**

Actionable insights that support **strategic planning, sales optimization, and performance tracking**.

---

## Tools & Technologies

- **Database:** MySQL  
- **ETL & Transformation:** SQL, Python  
- **Data Modeling & Documentation:** Draw.io  
- **Architecture Style:** Star-schema dimensional model  
- **Analytics & Reporting:** SQL-based KPI analysis  

---

## Key Achievements

- Designed a **production-style analytical data warehouse**  
- Applied **dimensional modeling best practices**  
- Built end-to-end ETL workflows using SQL  
- Transformed raw operational data into **decision-ready insights**  
- Delivered clear documentation for both technical and non-technical users  

---

## Business Value

- Established a **single source of truth** for sales analytics  
- Improved reporting consistency and query efficiency  
- Enabled faster access to KPIs for business stakeholders  
- Created a foundation for future BI dashboards and analytics solutions  

---

## Future Enhancements

- Automate ETL pipelines using scheduling tools  
- Implement historical tracking with slowly changing dimensions  
- Integrate BI tools such as Power BI or Tableau  
- Extend the warehouse to support forecasting and predictive analytics  
