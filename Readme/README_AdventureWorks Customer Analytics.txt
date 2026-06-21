# AdventureWorks Customer Analytics Dashboard

## Overview

This project showcases an end-to-end Customer Analytics Dashboard built using Microsoft AdventureWorksDW2019, SQL Server, and Power BI. The dashboard analyzes customer demographics, purchasing behavior, income distribution, and country-level performance through interactive visualizations and DAX-driven insights.

The objective was not only to build a dashboard but also to perform data validation, verify model relationships, and ensure analytical accuracy before reporting.

---

## Business Objectives

* Analyze customer order patterns across countries.
* Understand purchasing behavior by gender and income levels.
* Identify top-performing customer segments.
* Compare customer income distribution across sales territories.
* Deliver an interactive dashboard for business users and decision-makers.

---

## Data Source

**Database:** AdventureWorksDW2019

### Fact Table

* FactInternetSales

### Dimension Tables

* DimCustomer
* DimDate
* DimProduct
* DimProductSubcategory
* DimProductCategory
* DimSalesTerritory
* DimGeography

---

## Data Validation & SQL Analysis

Before building the dashboard, SQL Server was used to validate the dataset and verify relationships between fact and dimension tables.

### Key Finding: Geography Limitation

During data-model validation, it was identified that:

* FactInternetSales contains **SalesTerritoryKey**
* FactInternetSales does **not** contain **GeographyKey**

As a result:

✅ Country-level analysis is supported

❌ True city-level sales attribution is not supported

This discovery prevented inaccurate reporting and served as an important business validation exercise.

---

## Data Modeling

A star-schema model was implemented to support efficient reporting and analysis.

The model integrates customer, product, date, geography, and territory dimensions with FactInternetSales as the central fact table.

---

## Dashboard Features

### KPI Monitoring

* Total Orders
* Average Customer Income

### Customer Analysis

* Orders by Gender
* Orders by Country
* Income Distribution Analysis

### Territory Performance

* Average Customer Income by Country

### Bowtie Analysis

Visual representation of:

Gender → Total Orders → Country

This helps identify how customer demographics contribute to overall order distribution across territories.

---

## DAX Highlights

### Dynamic Ranking

Implemented RANKX() measures to dynamically rank countries and customer segments based on performance metrics.

### Conditional Formatting

Applied DAX-driven conditional formatting to automatically highlight:

* Highest-performing country
* Top income segment

The rankings recalculate dynamically based on user selections and filters.

---

## Interactive Features

### Slicers

* Country
* Calendar Year

### Cross Filtering

All visuals respond dynamically to user interaction, enabling detailed exploratory analysis.

---

## Tools & Technologies

* Power BI Desktop
* SQL Server (SSMS)
* AdventureWorksDW2019
* Power Query
* DAX
* GitHub

---

## Key Skills Demonstrated

* Data Validation
* SQL Analysis
* Star Schema Modeling
* Power Query ETL
* DAX Development
* RANKX
* Conditional Formatting
* Dashboard Design
* Business Intelligence Reporting

---


## Conclusion

This project demonstrates the complete Power BI development lifecycle, from SQL-based data validation and model design to DAX development and interactive dashboard creation. A key outcome was identifying a data-model limitation that prevented inaccurate city-level reporting, reinforcing the importance of validating business requirements before building analytical solutions.
