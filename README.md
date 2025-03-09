# 📊 Maji Ndogo Water Project | Power BI & SQL Analysis  

## 📌 Project Overview  
This project analyzes **water consumption trends and shortages** in Maji Ndogo village using **SQL and Power BI**.  
The goal is to identify key factors contributing to water shortages and propose solutions using **data-driven insights**.  

### 📸 **Maji Ndogo**  
![Power BI Dashboard](.Maji_Ndogo.PNG) 

---

## 📂 Data Sources  
- 📄 **Government Water Supply Reports (2018-2023)**  
- 🏠 **Survey Data on Household Water Usage**  
- 💧 **Weather & Rainfall Data**  

---

## 🔍 Key Insights  
✅ **Water supply dropped by 20% in 2022 due to drought conditions.**  
✅ **Rural households use 40% less water than urban areas due to supply limitations.**  
✅ **Investing in local water treatment plants can reduce shortages by 30%.**  
✅ **Peak water usage occurs between December and April.**  

---

## 🛠 Tools Used  
- **SQL** (Data Cleaning & Query Optimization)  
- **Power BI** (Interactive Dashboards & Data Visualization)  
- **Excel** (Data Preprocessing & Pivot Tables)  

---

## 📊 Power BI Dashboard & Visuals  
### 📌 **Interactive Dashboard**  
🔗 **Live Dashboard:** [View Here](https://yourpowerbidashboard.com)  

### 📸 **Dashboard Screenshot**  
![Power BI Dashboard](./dashboards/water_project_dashboard.png)  

---

## 📈 Exploratory Data Analysis (EDA)  
We performed **EDA** to uncover trends and patterns in the dataset.  
### 🔹 **Key Findings from EDA:**  
- **Water scarcity increased by 15% from 2020 to 2023.**  
- **Households with more than 5 people consume 30% more water.**  
- **Leakage and wastage contribute to 12% of total water loss.**  
- **Correlation found between seasonal rainfall and water availability.**  

📊 **Visualization Sample:**  
![Data Distribution](./screenshots/data_distribution_chart.png)  

---

## 🛢️ SQL Queries & Analysis  
### **🔍 Data Cleaning & Preprocessing**  
```sql
-- Remove duplicates & clean missing values
DELETE FROM water_usage
WHERE id NOT IN (
    SELECT MIN(id) FROM water_usage GROUP BY household_id, year
);
