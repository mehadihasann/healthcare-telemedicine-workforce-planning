# Healthcare Telemedicine Workforce Planning

**Hourly Patient Demand Analysis, Forecasting and Doctor Staffing Optimization**

## Project Overview

This project analyzes simulated telemedicine consultation demand to explore how healthcare operations teams can estimate hourly workload, forecast demand, and plan doctor staffing across different shifts.

The project is based on a callback-based telemedicine service model, where patients submit consultation requests and doctors contact them by phone.

The analysis uses Python, pandas, data visualization, forecasting techniques, and workload estimation to develop an illustrative workforce planning model.

## Important Dataset Disclaimer

**This project uses a simulated dataset generated for analytical and educational purposes.**

It does not contain actual patient records or confidential company operational data. The demand patterns, forecasts, workload estimates, and staffing recommendations are illustrative assumptions and must not be interpreted as actual mHealth performance figures.

## Project Objectives

- Analyze hourly telemedicine consultation demand.
- Identify weekday and hourly demand patterns.
- Examine monthly demand trends.
- Forecast future consultation demand.
- Estimate hourly doctor workload requirements.
- Develop a weekly doctor shift staffing plan.
- Evaluate staffing requirements under different Average Handling Time (AHT) assumptions.

## Dataset Information

| Item | Description |
|---|---|
| Dataset type | Simulated |
| Period | January–June 2025 |
| Total records | 4,344 |
| Number of days | 181 |
| Time intervals | Hourly |
| Total simulated requests | 35,729 |
| Weekday-hour combinations | 168 |

The dataset contains hourly consultation request counts, dates, weekdays, and hour information.

## Tools and Technologies

- Python
- Jupyter Notebook
- pandas
- NumPy
- Matplotlib
- scikit-learn
- Excel

## Project Methodology

### 1. Data Generation and Preparation

Created a synthetic hourly consultation dataset covering six months. Organized the data by date, weekday, and hour, and checked the dataset for missing values and consistency.

### 2. Demand Pattern Analysis

Analyzed hourly and weekday demand patterns to identify periods of relatively high and low consultation demand.

### 3. Monthly Demand Analysis

Compared monthly consultation volumes and average daily demand to understand the illustrative demand trend.

### 4. Demand Forecasting

Applied linear regression to estimate the July 2025 average daily consultation demand using the six-month simulated dataset.

### 5. Workload Estimation

Estimated hourly doctor requirements using the following workload formula:

`Required Doctors = CEILING((Hourly Requests × AHT) / (60 × (1 − Shrinkage)))`

Baseline assumptions:

- Average Handling Time (AHT): 12.5 minutes
- Shrinkage: 20%
- Effective available working time: 48 minutes per doctor-hour

These are modelling assumptions, not measured operational averages.

### 6. Weekly Shift Staffing Plan

Developed an illustrative weekly staffing plan based on three shifts:

| Shift | Working Hours |
|---|---|
| Morning | 08:00–14:00 |
| Evening | 14:00–22:00 |
| Night | 22:00–08:00 |

**Estimated weekly doctor-shift assignments: 79**

This represents doctor-shift assignments, not 79 individual doctors.

### 7. AHT Sensitivity Analysis

Compared estimated staffing requirements under three AHT scenarios:

| AHT | Total Hourly Staffing Requirements | Peak Hourly Requirement |
|---|---:|---:|
| 10 minutes | 377 | 4 doctors |
| 12.5 minutes | 448 | 5 doctors |
| 15 minutes | 515 | 6 doctors |

The totals represent the sum of staffing requirements across hourly time slots, not unique doctor headcount.

## Key Illustrative Results

| Metric | Result |
|---|---:|
| Total simulated requests | 35,729 |
| Dataset records | 4,344 |
| Baseline AHT | 12.5 minutes |
| Shrinkage | 20% |
| Peak hourly doctor requirement | 5 |
| Weekly doctor-shift assignments | 79 |
| Forecast July average daily demand | 207.45 requests |
| Forecast model in-sample MAE | 2.08 |
| Forecast model in-sample RMSE | 2.53 |

**Note:** Forecast error metrics are calculated on the training period and do not represent out-of-sample forecasting performance.

## Weekly Staffing Plan

| Shift Day | Morning | Evening | Night |
|---|---:|---:|---:|
| Saturday | 4 | 4 | 3 |
| Sunday | 5 | 4 | 2 |
| Monday | 5 | 5 | 2 |
| Tuesday | 5 | 5 | 3 |
| Wednesday | 5 | 5 | 3 |
| Thursday | 4 | 4 | 3 |
| Friday | 3 | 3 | 2 |

These figures are illustrative staffing estimates based on the simulated demand and stated assumptions.

## Important Assumptions and Limitations

1. The dataset is entirely simulated and does not represent actual company or patient data.
2. The baseline AHT of 12.5 minutes is a modelling assumption, not a measured company average.
3. The 20% shrinkage assumption includes break allowance; breaks are not deducted separately.
4. The workload formula estimates staffing based on hourly workload. It does not independently validate queue performance.
5. Erlang C is designed for queued inbound contacts. A callback-based consultation service has different operational characteristics.
6. An hourly dataset cannot establish whether a doctor successfully starts a consultation within a 30-minute service commitment.
7. Validating a 30-minute callback target would require timestamp-level request and callback-start data, followed by an appropriate callback simulation or service-level analysis.
8. The six-month forecasting period is limited, and additional historical data would be needed for stronger validation.

## Project Structure

```text
healthcare-telemedicine-workforce-planning/
│
├── data/
│   ├── raw/
│   │   └── hourly_patient_requests.csv
│   │
│   └── processed/
│       ├── weekly_staffing_plan.csv
│       ├── forecast_results.csv
│       ├── monthly_weekday_hourly_demand.csv
│       ├── june_busiest_hours.csv
│       └── aht_sensitivity_analysis.csv
│
├── notebooks/
│   └── MHealth_Capacity_Analysis.ipynb
│
├── outputs/
│   └── final_project_summary.csv
│
├── reports/
│   ├── mHealth_Capacity_Planning_Project_Report.pdf
│   └── mHealth_Capacity_Planning_Results.xlsx
│
└── README.md
```

## Conclusion

This project demonstrates how Python-based data analysis, demand forecasting, workload estimation, and sensitivity analysis can support healthcare workforce planning.

The analysis provides an illustrative approach to identifying demand patterns and estimating doctor staffing requirements across different shifts.

The model is an educational portfolio project and would require real timestamp-level operational data, further validation, and callback-specific modelling before being used for actual workforce decisions.

## Author

**Md Mehadi Hasan**

GitHub: https://github.com/mehadihasann
