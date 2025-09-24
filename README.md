# 🛒 Customer Experience Analysis with MySQL & Power BI  

## 📌 Project Overview  
This project explores a **customer experience dataset** using **MySQL for data analysis** and **Power BI for visualization**.  

The aim is to uncover patterns in **customer behavior, satisfaction, and engagement** to answer key business questions such as:  
- Who are our most valuable and engaged customers?  
- How do age, gender, location influence satisfaction of the customers?  
- Do higher engagement levels (time, interactions, product views) lead to more purchases?  
- Which products and regions perform best — and which need improvement?  

By combining **SQL queries** with an **interactive Power BI dashboard**, this project demonstrates how raw data can be transformed into **actionable insights** and ofcourse the project was very demanding to carry out.  

---

## 📂 Dataset Description  
The dataset contains the following columns:  

- **Customer_ID** – Unique identifier for each customer  
- **Age, Gender, Location** – Demographics  
- **Interactions** – Number of customer touchpoints (visits, queries, etc.)  
- **Feedback_Score** – Satisfaction rating (scale: 1–10)  
- **Products_Viewed** – Number of products viewed by each customer 
- **Products_Purchased** – Number of products purchased by each customer 
- **Time_Spend_in_Shop** – Engagement level in minutes for each customer
- **Retention Status** - is the customer still engaging with the business??
- **satisfaction score** - it indicates if the customers are satisfied with the business products

---

## ❓ Business Questions & SQL Queries  

### 1. Who are the most engaged customers (high views + high purchases)?  
```sql
SELECT Customer_id , Products_Viewed , Products_Purchased AS Total_purchases , Satisfaction_Score
FROM asanda_sql.customer_experience_data
WHERE 	Products_Purchased>18 AND Products_Viewed >36
```
Insights: There are 10 custumoers who engaged the most and 7 of them gave a satisfaction score of 7+ , while all of them viewed 40+ products and bought 19+products , thus this clearly shows that they are very satisfied with the products and we can clearly label them as our high value customers.






   








