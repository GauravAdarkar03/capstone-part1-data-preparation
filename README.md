# capstone-part1-data-preparation

## Data Cleaning Summary
Dataset
- UCI Facebook Metrics Dataset
- Total Records: 500
- Features: 19

## Missing Values
- The following columns contained missing values:

Paid -> Median -> Small number of missing values
Lifetime Post Consumers by Type -> Median -> Skewed distribution

## Outlier Treatment
Outliers were detected using the IQR Method.
Columns checked:
- Lifetime Post Total Reach
- Lifetime Post Total Impressions
Extreme values were capped instead of removed because they likely represent highly successful Facebook posts rather than data entry errors.

## Data Type Corrections
- The Category column was converted from integer/object to Categorical datatype to improve memory efficiency and represent categorical information correctly.


## SQL Database
The cleaned dataset was exported into a SQLite database using Pandas and SQLite for querying.
Six SQL queries were executed covering:
- WHERE
- GROUP BY
- Aggregate Functions
- ORDER BY
- LIMIT
- HAVING

## Visualizations
The notebook includes five visualizations:
- Box Plot
- Histogram
- Bar Chart
- Scatter Plot
- GroupBy Chart

Each chart includes:
Title
- X-axis label
- Y-axis label

### 5. Key Insights
*   **Insight 1 (Missing Values & Outliers):** Minimal missing values were imputed using the median, and extreme outliers were successfully capped, ensuring data quality and analytical robustness.
*   **Insight 2 (Engagement by Post Type):** 'Photo' posts generally exhibit higher average total interactions, suggesting visual content is more engaging for this page.
*   **Insight 3 (Impact of Paid Promotion):** Paid posts significantly outperform unpaid posts across all engagement metrics, highlighting the effectiveness of advertising in boosting post performance.
*   **Insight 4 (Top Performing Categories):** Categories 2 and 3 show the highest average lifetime engaged users, indicating these are strong content areas for audience resonance.
*   **Insight 5 (Optimal Posting Hours):** Posts made around 5 AM and 2 PM tend to receive higher average total interactions, suggesting these hours as potential optimal times for maximizing engagement.



## AI Assistance

AI tools were used to assist with code explanations, debugging, and documentation. All implementation, analysis, and final submission content were reviewed, understood, and verified by the author.