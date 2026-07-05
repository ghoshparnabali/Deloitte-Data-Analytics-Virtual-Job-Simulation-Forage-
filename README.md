# Deloitte Data Analytics Virtual Job Simulation (Forage)
This repository documents the completion of the [Deloitte Australia Data Analytics Virtual Job Simulation Experience](https://www.theforage.com/simulations/deloitte-au/data-analytics-s5zy) on Forage. The simulation involved two data analytics tasks for a fictional client, Daikibo Industrials — a factory telemetry analysis built in Tableau, and a gender pay equality classification task in Excel.

---

## Task 1 — Factory Downtime Analysis (Tableau)
The client provided a unified JSON telemetry dataset of 160,704 records collected across 4 factories over May 2021, with 9 machine types each reporting status every 10 minutes.
- **Calculated field —** An "Unhealthy" measure was created in Tableau, assigning a value of 10 to every unhealthy status record, representing 10 minutes of potential downtime since the previous message.
- **Downtime per Factory (bar chart) —** Aggregated unhealthy minutes across all four locations: Daikibo Factory Seiko (Osaka) emerged as the highest with 480 minutes of downtime, followed by Daikibo Shenzhen (420 mins), Daikibo Factory Meiyo (110 mins), and Daikibo Berlin (20 mins).
- **Downtime per Device Type (bar chart)** — A second sheet breaking down downtime by machine type, filtered dynamically by factory selection from the first chart.
- **Interactive Dashboard —** Both charts were combined into a dashboard with the factory chart set as a filter. Selecting Daikibo Factory Seiko in the first chart revealed that 100% of its downtime originated from a single device type — the LaserWelder (48 events, 480 mins). Every other machine in Seiko was healthy across the entire month.

![result_image](Deloitte_Job_Simulation/task_1/result_image.png)

## Task 2 — Gender Pay Equality Classification (Excel)
The Forensic Tech team provided an Excel file with 37 rows of employee compensation data across all four factories and various job roles, each assigned an Equality Score from -100 to +100 (0 being ideal).
- **Classification of Equality Score —** A 4th column — Equality Class — was added to classify each score:
    1. Fair (score within ±10)
    2. Unfair (score beyond ±10 but within ±20)
    3. Highly Discriminative (score beyond ±20)
- **Evaluation —** Across the dataset, 18 roles were classified as Fair, 12 as Unfair, and 7 as Highly Discriminative. Notably, almost all scores are negative — indicating a consistent pattern of women being paid less across all four locations — and the gap worsens with seniority, with leadership roles (C-Level, VP, Director) carrying the most negative scores.

---

## Repository Structure

```
Deloitte-Data-Analytics-Virtual-Job-Simulation-Forage/
├── Deloitte_Job_Simulation/
|   ├── task_1/
│   |   ├── dataset.zip
│   |   ├── result_dashboard.twbx
│   |   └── result_image.png
|   └── task_2/
│       ├── dataset.xlsx
│       └── result_equality_table.xlsx
└── README.md
```

---

## Tools Used
| Tool | Purpose |
|------|---------|
|Tableau Public | Telemetry data visualisation and dashboard |
| Microsoft Excel | Equality score classification |
