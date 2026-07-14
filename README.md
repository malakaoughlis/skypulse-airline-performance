# SkyPulse – Airline Performance Analysis

SkyPulse is a data analysis project about US domestic flight performance in 2025. It explores flight delays, cancellations, airlines, airports and routes using Python and Power BI.

## Data Source

The data comes from the **US Bureau of Transportation Statistics (BTS)**:

[Reporting Carrier On-Time Performance Data](https://www.transtats.bts.gov/DL_SelectFields.aspx?QO_fu146_anzr=b0-gvzr&gnoyr_VQ=FGJ)

## Data Collection and Merge

I downloaded the 12 monthly CSV files for 2025 from BTS. I extracted each file, selected the same columns, and combined all the monthly datasets into one raw CSV file using Python and pandas. The merged data was then cleaned and prepared for the analysis and Power BI dashboard.

## Project Structure

- `data/raw/` – raw merged dataset
- `data/cleaned/` – cleaned dataset
- `notebook/` – data cleaning and exploratory analysis
- `dashboard/` – Power BI dashboard
- `docs/` – data dictionary
- `reports/` – final analysis report

## Tools

Python, pandas, matplotlib and Power BI.
