# Restaurant Sales Analysis

Welcome to the **Restaurant Sales Analysis** project! 
This repository is dedicated to exploring customer, menu, and orders data over multiple months, 
applying both Python-based and SQL-based analytics, and visualizing key insights in Tableau.

## Repository Structure
restaurant_sales_analysis/
                     ├─ data/ 
                     │     ├─ guests.csv 
                     │     ├─ menu-data.csv 
                     │     ├─ orders_04_2022.csv
                     |     ├─ orders_05_2022.csv
                     |     ├─ orders_06_2022.csv 
                     ├─ notebooks/
                     |     ├─ 0_Environment_Setup.ipynb
                     |     ├─ 1_Data_Collection_Loading.ipynb 
                     |     ├─ 2_Data_Cleaning.ipynb
                     |     ├─ 3_Exploratory_Analysis.ipynb
                     |     ├─ 4_Advanced_Metrics_and_SQL.ipynb 
                     |     ├─ 5_Advanced_Customer_Analytics.ipynb 
                     |     └─ 6_Advanced_Insights.ipynb 
                     ├─ dashboard/
                     |     └─ (Tableau dashboards or screenshots) 
                     └─ README.md

## Project Goals

- **Data Cleaning & Integrity**: Ensure all references (client IDs, menu item IDs) are consistent.
- **Exploratory Analysis**: Uncover initial patterns, top items, daily/weekly trends.
- **Advanced Analytics**: Profit calculations, RFM (Recency, Frequency, Monetary), cohort analysis, etc.
- **Tableau Visualization**: Interactive dashboards for business stakeholders.

## How to Use

1. **Clone or Fork** this repository.
2. **Open Notebooks** in Google Colab:
   - `0_Environment_Setup.ipynb` to install dependencies (`ipython-sql`, etc.).
   - Next notebooks for step-by-step analysis.
3. **Data Folder (`data/`)** contains the CSV files (guests, menu, orders).
4. **Tableau Dashboards** can be found in `dashboard/`.

Stay tuned for more updates and final insights!
