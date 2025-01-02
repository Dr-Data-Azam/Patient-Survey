# Patient Satisfaction Analysis Using SQL and Tableau
This project focuses on analyzing patient satisfaction data and hospital bed information to derive actionable insights into healthcare services. By cleaning and preparing datasets in SQL and visualizing results in Tableau, the project categorizes hospitals based on bed capacity and benchmarks patient satisfaction metrics within peer groups.

## Project Overview
### Objectives
Standardize and clean hospital bed data for accurate peer group categorization (small, medium, large hospitals).
Integrate hospital bed data with patient satisfaction (HCAHPS) data while resolving formatting and duplication issues.
Create Tableau visualizations to present insights for healthcare stakeholders.
### Tools and Technologies
Database: PostgreSQL
Data Visualization: Tableau
Programming Concepts: SQL (CTEs, window functions, date formatting, and joins)
## Methodology
### 1. Data Cleaning and Preparation in SQL
Hospital Bed Data:
Reformatted dates from character strings to SQL date format using to_date.
Padded provider_ccn to 6 digits using lpad for standardization.
Used a combination of CTEs and row_number to filter only the most recent bed counts for hospitals.
HCAHPS Data:
Resolved formatting issues for facility IDs and date fields.
Ensured a one-to-one relationship between hospital bed data and HCAHPS records.
### 2. Joining and Transformation
Merged hospital bed data with HCAHPS survey data using a left join.
Applied filtering to exclude outdated records and handle duplicates.
### 3. Tableau Visualization
Analyzed patient satisfaction metrics and compared performance within categorized hospital groups.
Created visualizations to benchmark hospitals in states like Washington, Oregon, New York, and California.
## Key SQL Techniques
CTE (Common Table Expressions): Streamlined data preparation steps for readability and efficiency.
Window Functions: Utilized row_number() to prioritize recent records within hospital groups.
Date Formatting: Used to_date to convert Excel-style dates into SQL-compatible formats.
Joins and Filters: Combined datasets and ensured consistent, accurate relationships.
## Results
Hospitals categorized by size (small, medium, large) for peer comparison.
Patient satisfaction metrics visualized to identify improvement areas.
Insights into state-specific performance trends.
## Challenges and Solutions
Date Formatting: Reformatted incompatible date strings for SQL using to_date.
Data Standardization: Padded numerical identifiers to maintain consistency.
Handling Duplicates: Applied CTEs and window functions to isolate relevant records.
