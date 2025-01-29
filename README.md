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

## Exploratory Analysis (Advanced)

Notebook: [2_Exploratory_Analysis.ipynb](notebooks/2_Exploratory_Analysis.ipynb)

This notebook includes:
- **Daily Revenue Trends**
- **Order Distribution by Time of Day**
- **Top-Selling Items** 
- **AOV (Average Order Value) Distribution**
- **Discount Analysis**
- **Heatmap (Day of Week × Time of Day)**

By exploring these aspects, we uncover operational patterns, highest-demand periods, and overall customer behavior, guiding informed business decisions.

### Advanced Metrics & Visualization

Notebook: [3_Advanced_Metrics.ipynb](notebooks/3_Advanced_Metrics.ipynb)

- Calculate advanced financial metrics:
  - **Overall Profit Margin**: Total profit divided by total sales
  - **Average Items per Order**: Total quantity of items divided by the number of unique orders
  - **Average Revenue per Guest**: Total sales divided by the number of unique guests

- **Visualizations**:
  - **Top 5 Categories by Profit**: Bar chart showcasing the most profitable categories
  - **Top 5 Items by Profit**: Bar chart highlighting the top-performing menu items
  - **Revenue by Referral Source**: Pie chart illustrating the distribution of revenue across different referral channels
  - **Key KPIs**: Textual summary of critical metrics

###  Advanced Analytics

Notebook: [4_Advanced_Analytics.ipynb](notebooks/4_Advanced_Analytics.ipynb)

In this notebook, we perform **deeper customer-centric analyses** to gain further insights into the restaurant’s performance and identify strategies to improve customer retention, lifetime value, and overall profitability:

- **RFM Analysis**  
  - Segment customers based on **Recency**, **Frequency**, and **Monetary** metrics.  
  - Identify high-value customers and develop targeted marketing strategies.

- **Cohort Analysis**  
  - Examine **customer retention** over time by grouping users based on their first purchase month (cohort).  
  - Track and compare how different cohorts engage and remain active in subsequent months.

- **Customer Lifetime Value (CLV)**  
  - Estimate the total revenue a customer is expected to generate over their entire relationship with the restaurant.  
  - Understand how investing in customer acquisition and retention can yield higher returns.

By incorporating these advanced analytical methods, the notebook reveals **patterns in customer loyalty**, **high-value segments**, and **long-term profitability drivers**, enabling the restaurant to make data-driven decisions that enhance both customer satisfaction and business performance.

---

###  Prepare Data for Tableau

To facilitate further **interactive visualizations** in Tableau, we export key outputs:

- **Export RFM Data** → `rfm_results.csv` (data/rfm_results.csv)  
- **Export Cohort Data** → `cohort_retention_tableau.csv` (data/cohort_retention_tableau.csv)  
- **Export CLV Data** → `clv.csv` (data/clv.csv)   

These files can be imported into Tableau to create in-depth dashboards, such as **heatmaps** of cohort retention or **segmentation charts** for RFM, providing a **dynamic view** of customer behavior and revenue potential.



Stay tuned for more updates and final insights!
