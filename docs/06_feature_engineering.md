# 06 – Feature Engineering

## Objective

The objective of this phase was to transform the integrated retail dataset into a richer analytical dataset by engineering new features that capture historical sales behaviour, temporal patterns and business characteristics.

Feature engineering improves the quality of predictive models by creating variables that better represent underlying business processes.

---

# Calendar Features

The following calendar-based variables were extracted from the transaction date:

- Year
- Month
- Month Name
- Quarter
- Week Number

These features enable models to capture seasonal and temporal sales patterns.

---

# Holiday Features

The holiday information was standardised using a single binary variable:

- `is_holiday`

Additional holiday-related flags were evaluated but simplified to avoid redundant information.

---

# Sales Features

Historical sales behaviour was captured using the following engineered variables:

## Previous Week Sales

The previous week's sales were calculated for every Store–Department combination using lag features.

Purpose:

- Historical context
- Demand forecasting
- Trend analysis

---

## Four-Week Rolling Average

A rolling mean over the previous four weeks was calculated.

Purpose:

- Smooth short-term fluctuations
- Identify longer-term trends
- Reduce noise

---

## Weekly Sales Growth (%)

The percentage change in sales compared to the previous week was calculated.

Purpose:

- Monitor business performance
- Detect rapid increases or declines
- Support KPI reporting

---

## Cumulative Sales

A running total of sales was calculated for each Store–Department combination.

Purpose:

- Long-term performance tracking
- Revenue accumulation analysis

---

## Four-Week Rolling Standard Deviation

A rolling standard deviation was calculated to measure sales volatility.

Purpose:

- Measure demand stability
- Identify highly variable departments
- Improve forecasting

---

# Feature Selection

After feature engineering, redundant variables were removed.

Removed features:

- holiday_name
- month_name
- holiday_flag

These variables duplicated information already represented by other features.

---

# Encoding Categorical Variables

The remaining categorical variables were converted into numerical representations using One-Hot Encoding.

Encoded variables:

- season
- store_type
- region

One-Hot Encoding avoids introducing artificial ordering between categories while producing machine-learning-ready features.

---

# Model Dataset Preparation

Rows containing engineered missing values were removed.

These missing values were expected because the first observation of every Store–Department combination has no historical sales available for lag-based calculations.

The processed dataset was saved as:

```
data/processed/model_dataset.csv
```

This dataset will serve as the input for all subsequent predictive modelling.

---

# Key Outcomes

By the end of this phase:

- Calendar features were engineered.
- Historical sales features were created.
- Sales trend and volatility measures were added.
- Redundant variables were removed.
- Categorical variables were encoded.
- A clean modelling dataset was produced.
- The processed dataset was exported for machine learning.

---

# Next Phase

The next stage of the project focuses on predictive analytics.

This will include:

- Loading the processed dataset
- Time-based train/test splitting
- Building forecasting models
- Model evaluation
- Feature importance analysis
- Business recommendations