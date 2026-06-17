# Flight Activity Analysis Report

## Introduction

This report analyzes flight activity data for loyalty program customers. The goal is to understand flying patterns, distance and points accumulation, redemption behavior, and top-performing customers over time.



## Data Overview

Key columns in the dataset:

- `loyalty_number` — unique customer identifier
- `year`, `month`, `activity_date` — date fields
- `total_flights` — number of flights in the period
- `distance` — total distance flown (km)
- `points_accumulated` — points earned through flights
- `points_redeemed` — points redeemed for rewards
- `dollar_conversion_pts` — dollar value of points redeemed



## Main Insights

### A. Flights, Distance, and Points — Monthly Overview

Each row aggregates a customer's activity for one month. Most customers log multiple flights per month, typically covering 5,000–9,000 km. Points accumulated track closely with distance flown. Redemption activity is sparse — many months show zero points redeemed.

### B. Monthly Aggregates

Flight, distance, and redemption activity is grouped by `activity_date`. High-frequency flyers are visible by total flight count.

| Activity Date | Total Flights | Distance   | Points Redeemed | Dollar Value Redeemed |
|:--------------|:-------------:|:----------:|:---------------:|:---------------------:|
| 2017-01       |        13,059 | 19,768,451 |         351,520 |               $63,293 |

### C. Average Flight Distance per Month

Average distance per flight is consistent across months, mostly in the 1,480–1,515 km range. This indicates stable route mix with few anomalous months.

### D. Top Performers

**Top 10 customers by total distance flown:**

| Loyalty Number | Distance (km) |
|:---------------|:-------------:|
| 689839         |       178,858 |
| 893866         |       168,640 |
| ...            |           ... |

**Top 10 customers by total points redeemed:**

| Loyalty Number | Points Redeemed |
|:---------------|:---------------:|
| 539704         |           4,479 |
| 211755         |           4,336 |
| ...            |             ... |


## Conclusions and Recommendations

The loyalty program has a clear core of high-engagement participants who fly frequently, cover long distances, and redeem significant points. Average distance per flight is broadly consistent, suggesting few outlier routes. Redemption rates and dollar value of points redeemed provide input for loyalty and marketing decisions — for example, targeting top flyers with exclusive offers.

**Suggested next steps:**

- Investigate inactivity periods — why do some customers show zero activity in certain months?
- Segment customers by activity level (distance, flight count, redemption) for targeted retention strategies.
- Cross-analyze flight activity with demographic data from the customer loyalty dataset for richer customer profiles.


## Plot Explanations

### 1. Monthly Aggregates

**What it shows:** Total flights, total distance, points redeemed, and dollar conversion totals for each month.
**Purpose:** Identifies monthly seasonality or trends in loyalty program activity.

### 2. Average Distance per Flight

**What it shows:** For each month, total distance divided by total flights — average journey length over time.
**Purpose:** Detects shifts in flight patterns (longer or shorter flights over time).

### 3. Top Distance Customers

**What it shows:** Customers ranked by cumulative distance flown.
**Purpose:** Surfaces high-value participants for targeted rewards or recognition.

### 4. Top Points Redeemers

**What it shows:** Customers ranked by total points redeemed.
**Purpose:** Highlights highly engaged users or frequent reward claimers.

### 5. Top Frequent Flyers

**What it shows:** Customers ranked by total number of flights taken.
**Purpose:** Identifies frequent travelers who may be business-focused and critical to program performance.
