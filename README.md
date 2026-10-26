# Severe Injuries in Texas Logistics Companies

## Project Overview

This project analyzes severe injury reports involving logistics companies in Texas. The OSHA dataset covers reports from January 2015 through November 2025. I first filtered the data to Texas records, then selected logistics companies using NAICS codes 484, 492, and 493.

The final dataset contains 517 incident records.

## Data Source

The original data was downloaded from OSHA’s Severe Injury Reports:

https://www.osha.gov/severe-injury-reports

The original CSV file, `January2015toNovember2025.csv`, is not included in this repository because of its large size. It can be downloaded from the OSHA page above.

## Data Preparation

1. I downloaded the original OSHA CSV and filtered it to Texas records.
2. In the `split data.ipynb` notebook, I selected logistics companies using NAICS codes 484, 492, and 493. I saved the result as `logistics_companies_all.csv`.
3. I opened `logistics_companies_all.csv` in Google Sheets and added two columns: `Types_of_accidents` and `Reason`. I used AI-assisted classifications based on the incident narratives and saved the file as `logistics_companies_add_columns.csv`.
4. I used the `cleaning data.ipynb` notebook to inspect and clean the data. After reviewing the initial classifications, I revised the `Reason` categories in Google Sheets because many records had been labeled as “unknown” or insufficient detail.
5. I saved the updated dataset as `logistics_cleaned_update.csv`.
6. I used the `Questions` notebook to analyze the cleaned dataset and create charts.

## Important Note About Classifications

`Types_of_accidents` and `Reason` are AI-assisted classifications created for this project using OSHA’s incident narratives. They are not official OSHA categories or confirmed causes. Some narratives may not provide enough information for a confident classification.

## Files

- `split data.ipynb` — filters Texas records to logistics companies.
- `logistics_companies_all.csv` — Texas logistics records selected using NAICS codes 484, 492, and 493.
- `logistics_companies_add_columns.csv` — logistics data with the added `Types_of_accidents` and `Reason` columns.
- `cleaning data.ipynb` — inspects and cleans the data.
- `logistics_cleaned_update.csv` — final cleaned dataset used for the analysis.
- `Questions.ipynb` — contains the analysis and charts.

## Tools

- Python
- pandas
- Matplotlib
- Seaborn
- Google Sheets
- Jupyter Notebook
