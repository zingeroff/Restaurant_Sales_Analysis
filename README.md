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

## Data Cleaning and Preparation

Notebook: [1_Data_Cleaning.ipynb](notebooks/1_Data_Cleaning.ipynb)

This notebook focuses on:

1. **Data Integrity**  
   - Ensuring each `menu_item_id` from the orders matches entries in the menu dataset,  
   - Verifying `client_id` references are consistent with the guests table.

2. **Datetime Conversion**  
   - Converting `order_date` and `order_time` columns into proper datetime formats.

3. **Categorizing Time of Day**  
   - Splitting orders into `Morning`, `Lunch`, `Afternoon`, and `Evening` intervals based on the restaurant's hours (8:00 AM to 11:00 PM).

4. **Handling Missing Values and Duplicates**  
   - Checking for null entries and removing duplicates to ensure clean, consistent data.


## Saving and Uploading Cleaned Data

After performing data cleaning in `1_Data_Cleaning.ipynb`, we generated a new CSV file named `orders_cleaned.csv`. Because Google Colab doesn't automatically push CSV files to our GitHub repository, we manually upload the file to our `/data` folder:

1. Download the CSV from Colab:
   ```python
   from google.colab import files
   files.download("orders_cleaned.csv")


By the end of this cleaning phase, we have a reliable dataset ready for **Exploratory Data Analysis (EDA)**.


Stay tuned for more updates and final insights!
