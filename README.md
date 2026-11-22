# Healthcare Telemedicine Workforce Planning

**Hourly Patient Demand Analysis, Forecasting and Doctor Staffing Optimization**

## Project Overview

This project explores workforce planning for a healthcare telemedicine callback service using Python and simulated operational data.

The objective is to analyze hourly patient demand, estimate doctor staffing requirements across different shifts, forecast future demand, and understand how consultation duration affects workforce requirements.

**Important:** This project uses simulated data for portfolio and learning purposes. It does not contain actual company or patient data.

## Project Objectives

- Analyze hourly patient demand patterns.
- Identify busy and low-demand periods.
- Estimate doctor staffing requirements.
- Develop a weekly staffing recommendation.
- Forecast average daily patient demand.
- Evaluate staffing sensitivity under different Average Handling Time (AHT) scenarios.

## Dataset

A simulated dataset covering January–June 2025.

| Description | Value |
|---|---:|
| Total records | 4,344 |
| Total simulated requests | 35,729 |
| Time coverage | 6 months |
| Hourly combinations | 168 |
| Baseline AHT | 12.5 minutes |
| Shrinkage | 20% |

## Tools and Technologies

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

## Methodology

1. Generated a six-month simulated hourly demand dataset.
2. Analyzed demand by weekday and hour.
3. Identified demand patterns across morning, evening and night shifts
