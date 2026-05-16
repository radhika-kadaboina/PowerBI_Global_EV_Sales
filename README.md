# EVision Analytics

## Overview
EVision Analytics is an interactive Power BI dashboard project built using the IEA Global EV Dataset. The project focuses on analyzing Electric Vehicle (EV) adoption trends, regional growth, powertrain technologies, charging infrastructure, and market insights through data visualization and business intelligence techniques.

The dashboard provides meaningful insights into EV sales, stock growth, charging infrastructure, and future EV projections using interactive Power BI visualizations and DAX calculations.

---

# Project Objectives

- Analyze regional EV adoption trends
- Compare EV sales and stock performance
- Study powertrain technologies such as BEV, PHEV, and FCEV
- Monitor charging infrastructure growth
- Perform year-over-year EV growth analysis
- Compare historical and projected EV scenarios
- Generate business insights using interactive dashboards

---

# Dataset Information

## Dataset Name
IEA Global EV Data 2024

## Total Records
12,654

## Dataset Features

| Column | Description |
|---|---|
| region | Country or geographic region |
| category | Historical and projected EV scenarios |
| parameter | EV metrics such as sales, stock, charging points |
| mode | Vehicle category such as cars, buses, trucks |
| powertrain | EV technology type such as BEV, PHEV, FCEV |
| year | Reporting year |
| unit | Measurement unit |
| value | Numeric metric value |

---

# Technologies Used

- Power BI
- Power Query
- DAX
- Data Modeling
- Data Visualization

---

# Project Workflow

1. Uploading the Dataset
2. Data Cleaning & Transformation
3. Data Modeling
4. Creating DAX Measures
5. Building Dashboard Visualizations
6. Adding Interactive Slicers & Filters
7. Business Insight Generation

---

# Data Cleaning & Transformation

The following preprocessing steps were performed:

- Verified data types
- Removed unnecessary/null values
- Standardized categorical values
- Created calculated columns
- Created date hierarchy for time-series analysis
- Optimized dataset structure for visualization

---

# DAX Measures Created

## Cumulative EV Value

```DAX
Cumulative EV Value =
CALCULATE(
    SUM('IEA Global EV Data 2024'[value]),
    FILTER(
        ALL('IEA Global EV Data 2024'[year]),
        'IEA Global EV Data 2024'[year]
            <= MAX('IEA Global EV Data 2024'[year])
    )
)
