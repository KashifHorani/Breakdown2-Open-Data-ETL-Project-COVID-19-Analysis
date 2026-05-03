# Open Data ETL Project – COVID-19 Analysis

## 📊 Data Source
This project uses COVID-19 data from Our World in Data:
https://raw.githubusercontent.com/owid/covid-19-data/master/public/data/latest/owid-covid-latest.json

## ⚙️ ETL Workflow

### Extract
- Data fetched using requests from public API

### Transform
- Selected relevant columns
- Renamed columns for clarity
- Removed aggregate rows (e.g., World)
- Created new metrics:
  - Death Rate (%)
  - Cases per 100k population
- Sorted data by total cases

### Load
- Saved cleaned dataset to:
  data/processed/output.csv

## ▶️ How to Run

1. Install dependencies:
   pip install -r requirements.txt

2. Run script:
   python -m src.main

## 📁 Output

The final dataset includes:
- country
- continent
- total_cases
- new_cases
- total_deaths
- new_deaths
- population
- death_rate
- cases_per_100k

## 📌 Example Output

| country | total_cases | death_rate |
|--------|------------|------------|
| USA    | ...        | ...        |
| India  | ...        | ...        |
