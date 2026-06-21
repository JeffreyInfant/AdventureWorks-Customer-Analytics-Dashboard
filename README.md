AdventureWorks Customer Analytics Dashboard
Project Overview

Built an interactive Customer Analytics Dashboard using Microsoft AdventureWorksDW2019 to analyze customer demographics, purchasing behavior, income distribution, and country-level performance. The project combines SQL-based data validation, Power BI data modeling, DAX calculations, and interactive visual analytics to support business decision-making.

Business Objectives
Understand customer order patterns across countries.
Analyze purchasing behavior by gender and income.
Identify high-value customer segments.
Compare customer income across sales territories.
Create an interactive analytical dashboard for business users.
Data Validation & SQL Analysis

Before dashboard development, SQL Server (AdventureWorksDW2019) was used to validate data quality and model relationships.

Key Findings
Geography Limitation

FactInternetSales contains SalesTerritoryKey but not GeographyKey.

As a result:

Country-level analysis is supported.
True city-level sales attribution is not supported.
Attempting city-level reporting would produce misleading results.

This validation prevented incorrect business conclusions and became a key modeling decision.

Product Data Quality Review

Validated:

Null values
Relationship integrity
Duplicate checks
Fact-to-dimension connectivity
Data Model
Fact Table
FactInternetSales
Dimension Tables
DimCustomer
DimDate
DimProduct
DimProductSubcategory
DimProductCategory
DimSalesTerritory
DimGeography

Implemented a star-schema model optimized for analytical reporting.

Dashboard Features
KPI Cards
Total Orders
Average Customer Income
Customer Analytics
Orders by Gender
Orders by Country
Income Distribution Analysis
Custom Visualization
Bowtie Chart showing:
Gender → Total Orders → Country
Territory Performance
Average Income by Country
Income Distribution
Order frequency across customer income ranges
DAX Highlights
Dynamic Ranking

Used RANKX() to dynamically identify top-performing countries and income segments.

Conditional Formatting

Applied dynamic color formatting to automatically highlight:

Highest income country
Highest performing income segment

Selections automatically recalculate rankings based on filters and slicers.

Interactive Features
Slicers
Country
Calendar Year
Cross Filtering

All visuals respond dynamically to user selections.

Tools Used
SQL Server (SSMS)
AdventureWorksDW2019
Power BI Desktop
Power Query
DAX
GitHub
Key Skills Demonstrated
Data Validation
SQL Analysis
Star Schema Modeling
Power Query ETL
DAX Development
RANKX
Conditional Formatting
Dashboard Design
Business Intelligence Reporting
