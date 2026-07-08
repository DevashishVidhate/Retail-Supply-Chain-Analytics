# Data Understanding and Integration

## Objective: The objective of this phase was to gain a thorough understanding of the available datasets, assess their quality, and prepare a consolidated analytical dataset for subsequent exploratory analysis, feature engineering, SQL modelling, and machine learning.

---

## 1. Sales Dataset

Purpose: Contains weekly sales for every department within each retail store.

Primary Columns
- store_id
- department
- date
- weekly_sales
- is_holiday

Rows: 156,000

Columns: 5

---

## 2. Features Dataset

Purpose: Contains external factors that may influence weekly sales.

Primary Columns
- temperature
- fuel_price
- markdown_1
- markdown_2
- markdown_3
- markdown_4
- markdown_5
- cpi
- unemployment
- holiday_name
- season

Rows: 7,800

Columns: 14

---

## 3. Stores Dataset

Purpose: Contains descriptive information about each retail store.

Primary Columns
- store_type
- store_size
- region

Rows: 50

Columns: 4

---

# Initial Data Quality Assessment

The following checks were performed on every dataset.

## Dataset Structure

The following characteristics were inspected:

- Dataset dimensions
- Column names
- Data types
- Sample records

---

## Missing Values

Results

Sales: No missing values.

Features: Missing values found only in `holiday_name`.
These missing values are expected because most weeks are not associated with a holiday and therefore do not represent poor data quality.

Stores: No missing values.

---

## Duplicate Records

Duplicate records were checked before any analysis.

Results

| Dataset  | Duplicate Rows |
|----------|---------------:|
| Sales    | 0              |
| Features | 0              |
| Stores   | 0              |

No duplicate records were identified.

---

## Summary Statistics

Descriptive statistics were generated for:

- Numerical variables
- Categorical variables

This helped verify data ranges and identify the categorical structure of each dataset.

---

## Date Conversion

The `date` column in both the Sales and Features datasets was converted from string format to the `datetime` datatype.

This enables:

- Time-series analysis
- Date filtering
- Feature engineering
- Forecasting
- Seasonal analysis

---

## Business Understanding

Initial exploration identified:

- 50 unique stores
- Multiple departments within each store
- Several store types
- Multiple geographic regions

These observations helped establish the business entities that will be analysed throughout the project.

---

# Data Integration

To enable comprehensive analysis, the three datasets were merged into a single analytical dataset.

## Merge Strategy

Sales + Features

Join Keys:
- store_id
- date

Join Type: LEFT JOIN

Reason: Every sales record should be preserved while enriching it with environmental and economic information.

---

Merged Resulting_dataset + Stores

Join Key:
- store_id

Join Type: LEFT JOIN

Reason: Each store has a single descriptive record that can be attached to every sales observation.

---

# Merge Validation

Several validation checks were performed after merging.

## Dataset Shape

Expected: 156,000 rows

Actual: 156,000 rows

This confirms that no sales records were lost during the merge.

---

## Missing Values

No unexpected missing values were introduced.

The only remaining missing values occur in `holiday_name`, which is expected.

---

## Duplicate Holiday Columns

Both Sales and Features contained an `is_holiday` column.

These columns were validated to ensure they contain identical values before retaining a single version in the analytical dataset.

---

# Analytical Dataset

The final analytical dataset contains:

- Sales information
- Economic indicators
- Promotional markdowns
- Store characteristics
- Regional information

This dataset forms the foundation for:

- Business Exploratory Data Analysis
- Feature Engineering
- SQL Data Warehouse
- Machine Learning
- Demand Forecasting
- Power BI Dashboard Development

---

# Key Learnings

This phase established that:

- The datasets are well structured and require minimal cleaning.
- Missing values are business-related rather than data quality issues.
- Date conversion is essential for time-series analysis.
- LEFT JOINs preserve every sales record while enriching the dataset.
- Merge validation is an important step before any downstream analysis.

---

# Next Steps

The next phase focuses on Business Exploratory Data Analysis (EDA), where the integrated dataset will be analysed to answer key business questions, identify trends, evaluate store and department performance, investigate seasonality, and uncover actionable insights.