# 📊 Open Data ETL Project – COVID-19 Analysis

This project demonstrates a simple yet practical ETL (Extract, Transform, Load) pipeline built using Python and pandas. The workflow ingests real-time COVID-19 data from a public API, performs data cleaning and feature engineering, and outputs a structured dataset ready for analysis or visualization.

The goal of this project is to showcase fundamental data engineering concepts such as data extraction from APIs, transformation using pandas, and reproducible data workflows suitable for analytics and dashboarding.

---

## 🌍 Data Source

The dataset is sourced from Our World in Data:
https://raw.githubusercontent.com/owid/covid-19-data/master/public/data/latest/owid-covid-latest.json

It provides up-to-date global COVID-19 statistics including cases, deaths, and population metrics.

---

## ⚙️ Project Workflow

The pipeline follows a standard ETL process:

### 1. Extract
- Fetches JSON data from a public API using the `requests` library

### 2. Transform
- Selects relevant features (cases, deaths, population, etc.)
- Renames columns for clarity and consistency
- Filters out aggregate/global entries
- Creates derived metrics:
  - **Death Rate (%)**
  - **Cases per 100,000 population**
- Sorts data for easier analysis

### 3. Load
- Saves the cleaned dataset to:
