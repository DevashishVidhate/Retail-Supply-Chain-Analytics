# Dataset Overview

## Objective

Understand the structure, quality, and relationships of the datasets before designing the ETL pipeline.

---

## Datasets

Three datasets were provided:

- Sales
- Features
- Stores

---

## Sales Dataset

Purpose: Contains weekly sales for every department within each store.

Rows: 156,000

Columns: 5

Columns:
- store_id
- department
- date
- weekly_sales
- is_holiday

Observation:
- No missing values
- No duplicate records
- Date stored as string
- Weekly sales stored as float

---

## Features Dataset

Purpose: Contains environmental and economic indicators that may influence sales.

Rows: 7,800

Columns: 14

Important Variables:
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

Observation:
- holiday_name contains 6900 missing values.
- Missing values are expected because most weeks are not holidays.
- No duplicate records.
- Date stored as string.

---

## Stores Dataset

Purpose: Contains metadata describing each store.

Rows: 50

Columns:4

Column:
- store_id
- store_type
- store_size
- region

Observation:
- No missing values.
- No duplicate records.

---

## Dataset Relationships

Sales

Primary Key:
- store_id
- department
- date

Relationships:
Sales ←store_id→ Stores

Sales ←store_id + date→ Features

---

## Data Quality Assessment

### Missing Values

Sales: None

Features: holiday_name only

Stores: None

---

### Duplicate Records

Sales: 0

Features: 0

Stores: 0

---

## Initial Conclusions

The datasets are generally clean and suitable for analysis.

The only apparent missing values occur in holiday_name and are expected rather than indicative of poor data quality.These missing values indicate that there were no holidays in the weeks with null values.

The date columns require conversion from string to datetime before further analysis.

The three datasets can be integrated using store_id and date.

---

## Next Steps

- Convert date columns to datetime.
- Explore temporal coverage.
- Analyse store and department distributions.
- Design the ETL pipeline.