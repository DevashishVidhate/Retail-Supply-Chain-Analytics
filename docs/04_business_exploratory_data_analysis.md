# Business Exploratory Data Analysis (EDA)

## Objective

After understanding and integrating the datasets, the next stage of the project focused on exploring the retail business from a business intelligence perspective. Rather than simply analysing the data statistically, the aim was to answer practical business questions that management would ask when reviewing company performance.

The analyses performed during this phase investigate sales performance across multiple dimensions including time, stores, departments and geographical regions.

---

# Business Question 1: Weekly Sales Trend

## Objective

Understand how the company's weekly sales changed over time.

## Analysis Performed

- Aggregated weekly sales across all stores.
- Created a time-series line chart.
- Calculated:
  - Highest weekly sales
  - Lowest weekly sales
  - Average weekly sales

## Key Findings

- Weekly sales remained relatively stable throughout most of the year.
- Several significant sales spikes occurred during holiday periods.
- The highest weekly sales exceeded £109 million.
- Average weekly sales were approximately £56.5 million.

## Business Insight

The recurring sales spikes indicate clear seasonal purchasing behaviour. Understanding these trends enables management to improve inventory planning, staffing levels and promotional scheduling before peak demand periods.

---

# Business Question 2: Store Performance

## Objective

Identify the highest and lowest performing stores.

## Analysis Performed

- Aggregated sales by store.
- Ranked all stores by total sales.
- Visualised store performance using a horizontal bar chart.
- Calculated summary statistics.

## Key Findings

- Store 32 generated the highest total sales.
- Store 2 generated the lowest total sales.
- The highest-performing store generated approximately £303 million in sales.
- Store performance varied significantly across the retail network.

## Business Insight

Store-level performance differences suggest that operational factors, customer demand and store characteristics influence revenue generation. High-performing stores should be investigated to identify best practices that may be replicated across other locations.

---

# Business Question 3: Department Performance

## Objective

Determine which departments generate the highest revenue.

## Analysis Performed

- Aggregated total sales by department.
- Ranked departments by sales.
- Calculated each department's percentage contribution.
- Visualised department performance.

## Key Findings

- Department 20 generated the highest total revenue.
- No individual department contributed more than approximately 7% of total company sales.
- Sales were relatively evenly distributed across all departments.

## Business Insight

The balanced distribution of department sales indicates that the business does not rely heavily on a single product category. This diversified sales profile reduces business risk and supports balanced inventory investment.

---

# Business Question 4: Regional Performance

## Objective

Compare sales performance across geographical regions.

## Analysis Performed

- Aggregated total sales by region.
- Calculated each region's contribution to total company revenue.
- Visualised regional sales.
- Generated regional summary statistics.

## Key Findings

- East region contributed approximately 33% of total company revenue.
- North contributed approximately 28%.
- South contributed approximately 22%.
- West contributed approximately 17%.
- East and North together accounted for more than 60% of company sales.

## Business Insight

Regional performance is uneven across the business. The East region is the strongest-performing market and should be examined to identify operational practices that can be replicated in lower-performing regions. The West region requires further investigation to determine whether lower sales result from fewer stores, smaller store sizes or lower customer demand.

---

# Overall Findings

The first stage of Business Exploratory Data Analysis revealed several important insights:

- Weekly sales exhibit clear seasonal trends.
- Store performance varies considerably across the retail network.
- Department sales are well balanced with no over-reliance on individual departments.
- Regional sales are concentrated primarily within the East and North regions.
- Business performance appears to be influenced by both geographical and operational factors.

These findings establish a strong foundation for the next phase of analysis, which will investigate store characteristics and external variables that may explain the observed performance differences.

---

# Next Steps

The following analyses will be completed during the remainder of the Business EDA phase:

- Store Type Analysis
- Store Size Analysis
- Holiday Impact Analysis
- External Factors Analysis
- Correlation Analysis
- Outlier Detection

These analyses will provide a more comprehensive understanding of the factors driving sales performance before progressing to feature engineering, ETL development, SQL modelling and machine learning.