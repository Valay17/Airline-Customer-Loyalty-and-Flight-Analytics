# Project Report: Exploratory Data Analysis — Customer Loyalty

## 1. Introduction

This report presents the Exploratory Data Analysis (EDA) conducted on a customer loyalty dataset. The primary aim is to understand the demographic and behavioral characteristics of customers, the distribution and performance of different loyalty cards, enrollment and cancellation trends, and the factors that impact Customer Lifetime Value (CLV).

## 2. Data Overview

**Dataset columns:**

- Loyalty Number
- Country, Province, City, Postal Code
- Gender, Education, Salary, Marital Status
- Loyalty Card Type (Aurora, Nova, Star)
- Customer Lifetime Value (CLV)
- Enrollment Type, Year, Month
- Cancellation Year, Month

**Key observations:**

- All customers are from Canada, spread across various provinces and cities.
- Key categorical variables: gender, education, marital status, loyalty card, enrollment type, and cancellation details.
- Salary and CLV are the primary numerical fields.
- Missing data is present — notably incomplete salary values and absent cancellation dates for active customers.

## 3. Data Cleaning and Preparation

**Actions taken:**

- Imported core Python libraries: pandas, numpy, matplotlib, seaborn.
- Standardized column names to snake_case.
- Handled missing values — NaN for absent salary and cancellation fields.
- Constructed combined date fields (`enrollment_date`, `cancellation_date`) from separate year and month columns.

## 4. Exploratory Data Analysis

### A. Distribution of Loyalty Cards by City

**Findings:**

- The top cities by loyalty card holders are Toronto, Vancouver, and Montreal.
- Each city has customers distributed across all three card tiers: Aurora, Nova, and Star.
- Toronto has the highest customer count across all card types.

| City      | Aurora | Nova | Star | Total |
|:----------|-------:|-----:|-----:|------:|
| Toronto   |    719 | 1123 | 1509 |  3351 |
| Vancouver |    526 |  869 | 1187 |  2582 |
| Montreal  |    412 |  693 |  954 |  2059 |

### B. Enrollment Type Breakdown

**Findings:**

- There are two enrollment types: Standard and 2018 Promotion.
- The vast majority of enrollments are Standard.
- The 2018 Promotion contributed a visible but relatively small share even in major cities.

| City      | 2018 Promotion | Standard | Total |
|:----------|---------------:|---------:|------:|
| Toronto   |            173 |     3178 |  3351 |
| Vancouver |            151 |     2431 |  2582 |
| Montreal  |            138 |     1921 |  2059 |

### C. Loyalty Card Performance — CLV Aggregation

**Findings:**

- Aurora cardholders have the highest average CLV ($10,672.69), followed by Nova ($8,045.62) and Star ($6,741.76).
- Median CLVs follow the same pattern, confirming Aurora's advantage is not driven by outliers.

| Loyalty Card | Total CLV      | Avg CLV   | Median CLV |
|:-------------|---------------:|----------:|-----------:|
| Aurora       | $36,596,641.41 | $10,672.69|   $8,140.00|
| Nova         | $45,626,688.31 |  $8,045.62|   $5,799.06|
| Star         | $51,486,831.60 |  $6,741.76|   $4,786.89|

### D. CLV by Marital Status

**Findings:**

- Divorced and married customers both show higher average CLV ($8,200.69 and $8,058.20 respectively) than single customers ($7,719.49).

| Marital Status | Mean CLV   | Median CLV | Count |
|:---------------|----------:|-----------:|------:|
| Divorced       | $8,200.69 |  $5,872.96 | 2,518 |
| Married        | $8,058.20 |  $5,824.77 | 9,735 |
| Single         | $7,719.49 |  $5,583.07 | 4,484 |

### E. Enrollment and Cancellation Trends

**Enrollment by year and marital status (sample):**

| Year | Divorced | Married | Single |
|-----:|---------:|--------:|-------:|
| 2012 |      254 |     979 |    453 |
| 2013 |      324 |    1411 |    662 |
| 2018 |      499 |    1717 |    794 |

**Cancellation patterns:**

- Cancellations rose steadily from 2013 to 2018 across all marital status groups.
- Married customers account for the highest cancellation count, followed by single and then divorced customers.

| Year | Divorced | Married | Single |
|-----:|---------:|--------:|-------:|
| 2014 |       30 |     103 |     48 |
| 2015 |       31 |     172 |     62 |
| 2016 |       56 |     263 |    108 |
| 2017 |       70 |     276 |    160 |
| 2018 |       95 |     376 |    174 |

### F. Additional Notes

- Gender, education, province, and card-type correlations may yield further insight but are not broken out in this report.
- Customers with salary recorded as zero or NaN may skew average salary calculations.
- All distribution charts and plots are generated and embedded in the notebook.

## 5. Summary and Recommendations

- **Toronto, Vancouver, and Montreal** are the largest markets — these cities should be the primary focus for loyalty marketing and program development.
- **Aurora cardholders are the most valuable** on average; consider designing incentives to encourage eligible customers to upgrade.
- **Married and divorced customers carry the highest CLV** but also appear prominently in cancellations — this suggests a lifecycle pattern worth investigating further.
- **The 2018 Promotion drove an enrollment spike** that may affect retention and loyalty metrics in subsequent years.
- Further analysis on salary distribution, gender, and education level and their relationship to CLV and cancellation is recommended.

## 6. Possible Next Steps

1. **Missing Data Handling** — Impute or analyze the effect of missing salary values on CLV calculations.
2. **Predictive Modeling** — Use the processed data to build churn prediction or CLV forecasting models.
3. **Segmentation Analysis** — Segment the customer base for targeted marketing campaigns.
4. **Deeper Time-Series Analysis** — Study how enrollment and cancellation patterns evolve over time.
