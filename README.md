Healthcare Telemedicine Workforce Planning
Project Overview
This project analyses hourly patient consultation demand and estimates doctor staffing requirements for a callback-based telemedicine service. It uses Python to explore demand patterns, produce a simple monthly demand forecast, compare staffing needs under different average handling time (AHT) assumptions, and develop a weekly shift-level staffing plan.
> **Data disclaimer:** This project uses a simulated dataset generated for analytical and educational purposes. It contains no actual patient records or confidential company operational data. Demand patterns, forecasts, and staffing estimates are illustrative modelling results, not actual mHealth performance figures.
Project Objectives
Analyse hourly consultation-request patterns by weekday and hour.
Calculate indicative doctor workload requirements.
Compare staffing estimates under different AHT assumptions.
Explore monthly demand and produce an illustrative next-month forecast.
Summarise a weekly staffing plan across morning, evening, and night shifts.
Dataset
The analysis uses a synthetic dataset covering 1 January to 30 June 2025:
4,344 hourly records
181 calendar days
35,729 simulated consultation requests
168 weekday-hour combinations
The dataset was generated to resemble broad demand patterns described for a telemedicine callback operation. It is not real operational data.
Tools
Python
Jupyter Notebook
pandas and NumPy
Matplotlib
scikit-learn
Excel and PDF reporting
Methodology
Generate and validate the simulated hourly dataset.
Calculate average demand for each weekday-hour combination.
Visualise hourly and monthly demand patterns.
Estimate workload using a baseline AHT of 12.5 minutes and 20% shrinkage.
Compare staffing estimates at AHT values of 10, 12.5, and 15 minutes.
Group hourly requirements into the operation's three shifts, accounting for the night shift crossing midnight.
Prepare summary tables and reports.
Key Illustrative Results
Simulated requests: 35,729
Dataset records: 4,344
Weekday-hour combinations: 168
Baseline AHT assumption: 12.5 minutes
Shrinkage assumption: 20%
Peak hourly doctor requirement in the model: 5
Weekly doctor-shift assignments in the model: 79
Illustrative July average daily demand forecast: 207.45 requests
Weekly Staffing Estimate
Shift day	Morning	Evening	Night
Saturday	4	4	3
Sunday	5	4	2
Monday	5	5	2
Tuesday	5	5	3
Wednesday	5	5	3
Thursday	4	4	3
Friday	3	3	2
The total of 79 represents doctor-shift assignments across 21 weekly shifts. It does not mean 79 distinct doctors.
Important Assumptions and Limitations
All demand records are simulated, not actual company or patient data.
AHT of 12.5 minutes is a modelling assumption, not a measured company average.
Shrinkage is assumed to be 20%; the break allowance is included in this assumption and is not deducted again.
The workload calculation is an indicative capacity estimate. It does not establish that a 30-minute callback commitment or a 95% service level is achieved.
The service operates through callbacks, whereas traditional Erlang C models are designed for queued inbound contacts. Erlang C results should therefore not be treated as proof of callback performance.
Hourly totals do not show the exact arrival time of each request or the time each callback begins. More granular timestamp data and an appropriate callback simulation would be needed to assess the 30-minute target reliably.
The six-month linear forecast is illustrative and based on a short history. Its reported training-period error is not an independent out-of-sample validation.
Repository Structure
```text
healthcare-telemedicine-workforce-planning/
├── data/
│   ├── raw/
│   └── processed/
├── notebooks/
├── outputs/
├── reports/
└── README.md
```
Conclusion
This portfolio project demonstrates a practical Python workflow for demand analysis, workload estimation, sensitivity analysis, and shift-level workforce planning. The results should be interpreted as an educational simulation and a starting point for a more detailed operational model—not as verified staffing requirements for a real service.
