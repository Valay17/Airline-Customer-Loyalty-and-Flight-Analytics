# Customer Loyalty EDA — Plot and Analysis Summary

This document summarizes the main findings from the customer loyalty EDA and explains the plots and tables produced in the notebook.


## Data Overview

Key columns in the dataset:

- `loyalty_number`, `country`, `province`, `city`, `postal_code`
- `gender`, `education`, `salary`, `marital_status`
- `loyalty_card` (Aurora, Nova, Star)
- `clv` (Customer Lifetime Value)
- `enrollment_type` (Standard, 2018 Promotion), `enrollment_year`, `enrollment_month`
- `cancellation_year`, `cancellation_month`
- `enrollment_date`, `cancellation_date`

The dataset covers Canadian cities. Salary and cancellation date data contain missing values for a portion of customers.


## Summary of Main Insights

### A. City and Loyalty Card Distribution

Toronto, Vancouver, and Montreal are the top cities across all card tiers. Star is the most common card type overall; Aurora is the least common but carries the highest average CLV.

| City      | Aurora | Nova | Star | Total |
|:----------|-------:|-----:|-----:|------:|
| Toronto   |    719 | 1123 | 1509 |  3351 |
| Vancouver |    526 |  869 | 1187 |  2582 |
| Montreal  |    412 |  693 |  954 |  2059 |

### B. Enrollment and Promotion

Most enrollments are Standard. The 2018 Promotion drove a visible enrollment spike in that year, but the underlying base remains predominantly Standard across all major cities.

### C. Loyalty Card and CLV

Aurora members carry the highest average CLV ($10,672.69), followed by Nova ($8,045.62) and Star ($6,741.76). The median CLV mirrors this relationship, confirming it is not an outlier effect.

### D. Marital Status and CLV

Divorced and married customers have higher mean CLVs ($8,200.69 and $8,058.20) than single customers ($7,719.49). Divorced customers show the highest median CLV ($5,872.96).

### E. Enrollment and Cancellation Trends

Enrollments grew year-over-year, peaking in 2018 due to the promotion. Cancellations also rose steadily across all marital status groups over the same period.


## Plot Explanations

### 1. Loyalty Card Distribution by City

**Chart type:** Stacked horizontal bar chart.
**What it shows:** Customer count per city, broken down by loyalty card type (Aurora, Nova, Star).
**Interpretation:** Toronto, Vancouver, and Montreal dominate all card tiers. Star has the largest share in every city; Aurora customers are fewer but more valuable on average.

### 2. Enrollment Type by City

**Chart type:** Stacked horizontal bar chart.
**What it shows:** Customer count per city, split between Standard and 2018 Promotion enrollment types.
**Interpretation:** Standard enrollments account for the vast majority. The 2018 Promotion is a visible but small proportion even in the largest cities.

### 3. Loyalty Card CLV Analysis

**Chart type:** Pie chart.
**What it shows:** Total CLV share by loyalty card type.
**Interpretation:** Star holds the largest total CLV pool simply due to volume, but Aurora customers are individually the most valuable. Promotional efforts should target moving eligible customers to Aurora.

### 4. CLV by Marital Status

**Chart type:** Summary table (mean, median, count).
**What it shows:** CLV distribution across divorced, married, and single customers.
**Interpretation:** Divorced and married customers are more valuable on average. This pattern holds for both mean and median, suggesting it is not driven by outliers.

### 5. Quarterly Enrollment Trend by Card Type

**Chart type:** Line chart (quarterly).
**What it shows:** Enrollment count per quarter for each loyalty card type.
**Interpretation:** Enrollment grew steadily, with a notable spike around 2018 tied to the promotion.

### 6. Quarterly Cancellation Trend by Card Type

**Chart type:** Line chart (quarterly).
**What it shows:** Cancellation count per quarter for each loyalty card type.
**Interpretation:** Cancellations have risen over time for all card tiers — worth investigating to understand whether this is churn, expiration, or lifecycle-related.

### 7. Enrollment Trend by Marital Status

**Chart type:** Stacked area chart (yearly).
**What it shows:** Enrollment counts per year broken out by marital status.
**Interpretation:** Married customers make up the largest enrollment cohort each year. The 2018 spike is visible across all groups.

### 8. Loyalty Card Share by Marital Status

**Chart type:** Stacked horizontal bar chart (percentage).
**What it shows:** Card type distribution (as a percentage) within each marital status group.
**Interpretation:** Card preferences are broadly similar across marital status groups — Star dominates in all three, with Aurora carrying a slightly larger share among married and divorced customers.

### 9. Cancellation Trend by Marital Status

**Chart type:** Stacked area chart (yearly).
**What it shows:** Cancellation counts per year broken out by marital status.
**Interpretation:** Cancellations increased steadily for all groups, with married customers accounting for the largest share — consistent with their being the largest enrollment cohort overall.
