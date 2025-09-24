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
Insights: There are 10 custumers who engaged the most and 7 of them gave a satisfaction score of 7+ , while all of them viewed 40+ products and bought 19+products , thus this clearly shows that they are very satisfied with the products and we can clearly label them as our high value customers.

### 2. Do customers who spend more time in the shop buy more?
```sql
SELECT  ROUND(Time_Spent_on_Site,2) AS Time_spent_on_Site,
    AVG(Products_Purchased) AS Avg_Purchases
FROM asanda_sql.customer_experience_data
GROUP BY Time_Spent_on_Site
ORDER BY Time_Spent_on_Site DESC;
```
Insights : An individual spending 5 minutes and buying maybe 8 products could be buying lights and cheap products like sweets , and an individual who spend more than 50 minutes and buy 1 product could be buying something more costly I would assume.
It seems like the more time the customers spend at the site , the more products they are likely to buy and more money to be spend.

##3.How does time spent on the website relate to products purchased and customer satisfaction?
```sql
/*SELECT  ROUND(Time_Spent_on_Site,2) AS Time_spent_on_Site,
    AVG(Products_Purchased) AS Avg_Purchases
FROM asanda_sql.customer_experience_data
WHERE Time_Spent_on_Site>40
GROUP BY Time_Spent_on_Site
ORDER BY Time_Spent_on_Site DESC;
*/
SELECT
    CASE 
        WHEN Time_Spent_on_Site BETWEEN 0 AND 20 THEN '0-20 min'
        WHEN Time_Spent_on_Site BETWEEN 21 AND 40 THEN '21-40 min'
        WHEN Time_Spent_on_Site BETWEEN 41 AND 60 THEN '41-60 min'
        ELSE '60+ min'
    END AS Time_Range,
    COUNT(*) AS Num_Users,
    AVG(Products_Purchased) AS Avg_Purchases,
    AVG(Feedback_Score) AS Average_feedback
FROM asanda_sql.customer_experience_data
GROUP BY 
    CASE 
        WHEN Time_Spent_on_Site BETWEEN 0 AND 20 THEN '0-20 min'
        WHEN Time_Spent_on_Site BETWEEN 21 AND 40 THEN '21-40 min'
        WHEN Time_Spent_on_Site BETWEEN 41 AND 60 THEN '41-60 min'
        ELSE '60+ min'
    END
ORDER BY Time_Range;

```
Insights: Most users spent between 21 and 60 minutes on the site , with  average products purchased being 10 which is very bad as reflected by the average feedback score of 2.9. Thus many customers are not satisfied by the products being sold in the shop/site(accordig to these age groups alone.

### POWER BI DASHBOARD

So the project includes a Power Bi dashboard for interactive visuals :
 -------
 1.Products purchased by location: Bar chart
 2.Average satisfaction score : Gauge
 3.Products purchased by Gender

 ### KEY TAKEAWAYS
 1.Total of 10 000+ pruchases , an average rating score of 5.54 across every customer.
 2.70% custumer retention (Power BI) .
 3.Males were the more dominant buyers but that doesn't mean women shouldn't be prioritised.

 The project is a work in progress



   








