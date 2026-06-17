<div align="center">

<h1> <p> Airline Customer Loyalty and Flight Analytics</p> </h1>
</div>


This project analyzes customer loyalty and flight activity data for a fictional airline rewards program. Using Python, it examines customer segments, ticketing behavior, loyalty membership trends, and how points are earned and redeemed. The end goal is a set of findings that can inform decisions around retention, segmentation, and customer lifetime value (CLV).


## Table of Contents

- [Features](#features)
- [Dataset Overview](#dataset-overview)
- [Project Structure](#project-structure)
- [Tools and Libraries](#tools-and-libraries)
- [Installation](#installation)
- [Usage](#usage)
- [Reports](#reports)


## Features

- Enrollment and loyalty trend tracking, including sign-up surges, churn, and how customers move between card tiers over time.
- Flight activity aggregation and visualization, covering total flights, distance flown, and points redemptions broken out by period and customer cohort.
- Cross-referencing of loyalty status with demographic and activity data to connect card membership to flight and earnings patterns.
- A clear split between raw analytics and business-facing interpretation, so findings and recommendations are kept separate.


## Dataset Overview

The project relies on two datasets, both located in the `data/` directory.

**Customer Loyalty History** (`customer_loyalty_history.csv`) — customer demographics (gender, education, salary, country, city), loyalty card tier (Star, Nova, Aurora), marital status, enrollment and cancellation details, and cumulative CLV. This data enables segmentation by value, tenure, and engagement.

**Customer Flight Activity** (`customer_flight_activity.csv`) — monthly records per customer, including total flights, distance flown, points accumulated, points redeemed, and the dollar value of redeemed points. This supports trend analysis over time, engagement scoring, and tracking how points behavior shifts.



## Project Structure

```
.
├── data/
│   ├── customer_loyalty_history.csv      # Customer demographics and loyalty card data
│   ├── customer_flight_activity.csv      # Monthly per-customer flight and points data
│   ├── Airline Loyalty Data Dictionary.csv
│   └── Calendar.csv
├── notebooks/
│   ├── customer_loyalty_eda.ipynb        # EDA on loyalty history (demographics, CLV, trends)
│   └── flight_activity_analysis.ipynb   # EDA on flight activity (flights, distance, points)
├── customer_loyalty_analysis_report.md  # Written findings from the loyalty EDA
├── customer_loyalty_plots_report.md     # Plot-by-plot explanations for the loyalty EDA
├── flight_activity_report.md            # Written findings from the flight activity analysis
├── Plots.pdf                            # Exported plot collection from the EDA notebooks
├── requirements.txt                     # Python dependencies
├── .gitignore
└── Readme.md
```


## Tools and Libraries

| Library    | Purpose                              |
|------------|--------------------------------------|
| pandas     | Data manipulation and aggregation    |
| numpy      | Numerical operations                 |
| matplotlib | Plotting and visualization           |
| seaborn    | Statistical visualization            |
| plotly     | Interactive charts                   |
| jupyter    | Notebook environment                 |


## Installation

1. Clone the repository:

    ```bash
    git clone <repo-url>
    cd <repo-directory>
    ```

2. Set up a virtual environment:

    ```bash
    python -m venv venv
    source venv/bin/activate      # Linux / macOS
    venv\Scripts\activate         # Windows
    ```

3. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```


## Usage

Launch Jupyter from the project root:

```bash
jupyter notebook
```

Then open either notebook from the `notebooks/` directory:

- `notebooks/customer_loyalty_eda.ipynb` — customer demographics, card distribution, CLV, enrollment and cancellation trends
- `notebooks/flight_activity_analysis.ipynb` — flight counts, distance, points accumulation and redemption over time

Raw datasets are expected in the `data/` directory at the project root. The notebooks use relative paths and will resolve correctly when launched from the project root.


## Reports

Pre-generated written summaries are included alongside the notebooks:

| File | Contents |
|------|----------|
| `customer_loyalty_analysis_report.md` | Full EDA findings, tables, and recommendations for the loyalty dataset |
| `customer_loyalty_plots_report.md` | Plot-by-plot explanations and interpretation |
| `flight_activity_report.md` | Findings and plot explanations for the flight activity dataset |


## License

You are free to use and modify this software for personal or internal purposes.
However, redistribution or public distribution of this software or any modified versions is not permitted without explicit permission.
