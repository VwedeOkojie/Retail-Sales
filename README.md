# 🛍️ Retail KPI Analysis using PostgreSQL and Power BI


<img width="500" height="500" alt="RetailPix" src="https://github.com/user-attachments/assets/27a0666f-a36d-49a0-83f2-78f5ffeb13b6" />

## 📁 Project Description

This project showcases how to calculate essential **retail store performance KPIs** using **PostgreSQL** and visualize them in **Power BI**. It includes realistic sales data and walks through daily, weekly, monthly, quarterly, and yearly breakdowns of store performance.

---

## 📊 Key Performance Indicators (KPIs)

For each store and time period, the following KPIs are calculated:

1. **Conversion Rate (%)**  
   Formula: `(transactions / traffic_count) * 100`

2. **Average Transaction Value**  
   Formula: `sales / transactions`

3. **Units per Transaction**  
   Formula: `units_sold / transactions`

4. **Productivity**  
   Formula: `sales / staff_hours`

5. **Actual Sales vs Sales Goal (%)**  
   Formula: `(sales / sales_goal) * 100`

6. **CRM Signup Rate (%)**  
   Formula: `(crm_signups / transactions) * 100`

---

## 🧮 SQL Logic

All calculations are performed using **PostgreSQL**, ensuring:
- Proper data type handling (`NUMERIC`)
- Safe division with `NULLIF`
- Aggregations for time-based KPIs using `DATE_TRUNC()` and `DENSE_RANK()` for week labels.


## 📥 How to Use the Project

1. **Download the dataset**  
   Get the raw dataset `retail_sales.csv` from the repository or the provided source.

2. **Inspect the dataset**  
   Open the file and review the first few rows.

3.  **Create New Table pgAdmin 4**
   Open the file and review the first few rows.
    CREATE TABLE retail_sales(
      date DATE,
      store_id VARCHAR (50),
      traffic_count INTEGER,
      transactions INTEGER, 
      sales FLOAT,
      units_solds INTEGER,
      staff_hours FLOAT,
      crm_signups INTEGER,
      repeat_customers INTEGER,
      sales_goal FLOAT
      );
      
    
    Then right click on retail_sales Table
    Select IMPORT/EXPORT data
    Upload Retail Sales Data
    
    
    SELECT *
    FROM retail_sales;
    
4. **Clean the data**  
   Apply the data cleaning steps such as removing duplicates, correcting column names, fixing missing values, and standardizing entries.

5. **Analyze**
Using the SQL Scripts, calculate the following:
- Daily KPIs
- Weekly KPIs with labeled week numbers
- Monthly KPIs with month names
- Quarterly KPIs
- Yearly KPIs 
  
7. **visualize**  
Use Power BI to visualize
