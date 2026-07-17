# 05 – External Factors Analysis

## Project

Retail Supply Chain Analytics

---

# Objective

The purpose of this stage was to investigate whether external environmental, economic and promotional factors have a measurable relationship with retail sales.

Unlike the previous Business Exploratory Data Analysis, which focused on identifying high-performing stores, departments and regions, this stage aims to understand the potential drivers behind sales performance.

The analysis investigates the relationship between weekly sales and the following variables:

- Temperature
- Fuel Price
- Consumer Price Index (CPI)
- Unemployment Rate
- Promotional Markdown 1
- Promotional Markdown 2
- Promotional Markdown 3
- Promotional Markdown 4
- Promotional Markdown 5

---

# Work Completed

## 1. Selected Relevant Variables

A subset of the integrated dataset was created containing only the variables required for correlation analysis.

Selected variables:

- weekly_sales
- temperature
- fuel_price
- cpi
- unemployment
- markdown_1
- markdown_2
- markdown_3
- markdown_4
- markdown_5

This simplified subsequent analysis by removing unrelated columns.

---

## 2. Correlation Analysis

A Pearson correlation matrix was generated to measure the strength of the linear relationship between all numerical variables.

This analysis helps identify which external variables are most closely associated with weekly sales.

---

## 3. Weekly Sales Correlation

The correlation coefficients between weekly sales and each external factor were calculated.

| External Factor | Correlation |
|-----------------|------------:|
| Markdown 1 | 0.106 |
| Markdown 2 | 0.105 |
| Markdown 4 | 0.100 |
| Markdown 5 | 0.100 |
| Markdown 3 | 0.093 |
| CPI | -0.002 |
| Temperature | -0.002 |
| Fuel Price | -0.002 |
| Unemployment | -0.007 |

---

## 4. Visualisation

The relationships were visualised using:

- Correlation bar chart
- Scatter plot between Weekly Sales and the strongest external factor (Markdown 1)

These visualisations supported interpretation of the numerical correlation values.

---

## 5. Summary Statistics

Descriptive statistics were generated for each external variable including:

- Count
- Mean
- Standard deviation
- Minimum
- Quartiles
- Maximum

These statistics provide an understanding of the distribution and scale of each variable.

---

# Key Findings

## Promotional Markdowns

Promotional markdowns demonstrated the strongest positive relationship with weekly sales.

Although the correlation values were relatively small (approximately 0.10), they were consistently higher than all other external variables.

This suggests that promotional campaigns contribute positively to retail sales but are not the sole determinant of customer demand.

---

## Temperature

Temperature showed almost no relationship with weekly sales.

This indicates that weather conditions have little influence on overall sales performance within this dataset.

---

## Fuel Price

Fuel prices exhibited an almost zero correlation with weekly sales.

No meaningful linear relationship was identified.

---

## Consumer Price Index (CPI)

The Consumer Price Index showed virtually no correlation with weekly sales during the observed period.

---

## Unemployment

Weekly sales were largely unaffected by changes in unemployment levels according to the correlation analysis.

---

## Overall Conclusion

No individual external factor demonstrated a strong linear relationship with weekly sales.

Retail performance is likely influenced by multiple interacting factors including:

- Holidays
- Promotions
- Store characteristics
- Regional demand
- Seasonal effects
- Customer behaviour

These interactions are expected to be better captured by machine learning models later in the project.

---

# Business Value

This analysis provides valuable business insights by identifying which external variables are most closely associated with sales performance.

The findings support future stages of the project, particularly:

- Feature Engineering
- Forecasting Models
- Demand Prediction
- Business Intelligence Reporting

---

# Files Updated

- notebooks/EDA.ipynb

No additional datasets were created during this stage.

---

# Skills Demonstrated

- Data Exploration
- Correlation Analysis
- Statistical Interpretation
- Business Analytics
- Data Visualisation
- Retail Performance Analysis
- Exploratory Data Analysis (EDA)

---

# Next Stage

The next phase of the project is **Feature Engineering**.

New variables will be created from the existing data to improve downstream analysis and predictive modelling.

Planned features include:

### Date Features

- Year
- Month
- Quarter
- Week Number
- Day of Week

### Calendar Features

- Weekend Flag
- Holiday Flag
- Seasonal Features

### Sales Features

- Rolling Average Sales
- Lagged Weekly Sales
- Cumulative Sales
- Sales Growth
- Revenue Contribution

### Business Features

- Store Performance Categories
- Department Rankings
- High and Low Sales Classification

These engineered features will form the foundation for:

- SQL Analytics
- Forecasting Models
- Machine Learning
- Anomaly Detection
- Power BI Dashboards
- KPI Reporting

---

# Progress Summary

Completed Stages

- Project Setup
- Dataset Overview
- Data Understanding & Integration
- Business Exploratory Data Analysis
- External Factors Analysis

Upcoming Stages

- Feature Engineering
- Data Validation Pipeline
- ETL Pipeline Development
- SQLite Database Design
- SQL Business Queries
- Forecasting Models
- Anomaly Detection
- Excel KPI Report
- Power BI Dashboard
- Final Documentation