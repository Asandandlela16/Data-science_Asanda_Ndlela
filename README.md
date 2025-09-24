
🛒 Customer Experience Analysis with MySQL & Power BI
📌 Project Overview

This project explores a customer experience dataset using MySQL for data analysis and Power BI for visualization.

The aim is to uncover patterns in customer behavior, satisfaction, and engagement to answer key business questions such as:

Who are our most valuable and engaged customers?

How do demographics (age, gender, location) influence satisfaction?

Do higher engagement levels (time, interactions, product views) lead to more purchases?

Which products and regions perform best — and which need improvement?

By combining SQL queries with an interactive Power BI dashboard, this project demonstrates how raw data can be transformed into actionable insights.

📂 Dataset Description

The dataset contains the following columns:

Customer_ID – Unique identifier for each customer

Age, Gender, Location – Demographics

Interactions – Number of customer touchpoints (visits, queries, etc.)

Feedback_Score – Satisfaction rating (scale: 1–10)

Products_Viewed – Number of products viewed

Products_Purchased – Number of products purchased

Time_Spend_in_Shop – Engagement level in minutes

❓ Business Questions & SQL Queries
1. Who are the most engaged customers (high views + high purchases)?
SELECT 
    Customer_id, 
    Products_Viewed, 
    Products_Purchased AS Total_purchases, 
    Feedback_Score
FROM customer_experience_data
WHERE Products_Purchased > 18 
  AND Products_Viewed > 36;


Insight: Identifies loyal, high-value customers. Their satisfaction scores can guide retention strategies.

2. What is the average feedback score by age group?
SELECT 
    CASE 
        WHEN Age BETWEEN 18 AND 25 THEN '18-25'
        WHEN Age BETWEEN 26 AND 35 THEN '26-35'
        WHEN Age BETWEEN 36 AND 50 THEN '36-50'
        ELSE '50+'
    END AS Age_Group,
    AVG(Feedback_Score) AS Avg_Feedback
FROM customer_experience_data
GROUP BY Age_Group
ORDER BY Avg_Feedback DESC;


Insight: Highlights which age groups are most satisfied. Useful for targeted marketing.

3. Do customers who spend more time in the shop buy more?
SELECT 
    Time_Spend_in_Shop, 
    AVG(Products_Purchased) AS Avg_Purchases
FROM customer_experience_data
GROUP BY Time_Spend_in_Shop
ORDER BY Time_Spend_in_Shop DESC;


Insight: Tests if engagement (time spent) is correlated with purchases.

4. Which locations have the happiest customers?
SELECT 
    Location, 
    AVG(Feedback_Score) AS Avg_Feedback
FROM customer_experience_data
GROUP BY Location
ORDER BY Avg_Feedback DESC;


Insight: Identifies regions with the highest and lowest satisfaction — guiding operational decisions.

5. Which products are most viewed vs purchased?
SELECT 
    Product_Viewed, 
    COUNT(*) AS Total_Views, 
    SUM(Products_Purchased) AS Total_Purchases
FROM customer_experience_data
GROUP BY Product_Viewed
ORDER BY Total_Purchases DESC;


Insight: Finds products with high views but low purchases, suggesting potential conversion issues.

6. Do more interactions lead to higher satisfaction?
SELECT 
    Interactions, 
    AVG(Feedback_Score) AS Avg_Score
FROM customer_experience_data
GROUP BY Interactions
ORDER BY Interactions;


Insight: Tests if customer service interactions improve or worsen customer satisfaction.

7. Which gender purchases more products on average?
SELECT 
    Gender, 
    AVG(Products_Purchased) AS Avg_Purchases
FROM customer_experience_data
GROUP BY Gender;


Insight: Provides insights into purchasing behavior differences between genders.

📊 Power BI Dashboard

To complement SQL analysis, I created an interactive Power BI dashboard.

Dashboard Features:

📈 Satisfaction Analysis: Breakdown by age group, gender, and region

🛍️ Product Insights: Views vs purchases to identify conversion gaps

🕒 Customer Engagement: Relationship between time spent and purchases

🌍 Regional Performance: Average feedback scores and purchase volumes by location

🔄 Filters & Slicers: Drill-down by age, gender, or region for deeper exploration

👉 Example screenshot of the dashboard:


🔑 Key Insights (Sample)

Customers aged 26–35 reported the highest average satisfaction scores.

High engagement customers (view > 36, purchases > 18) show strong loyalty.

Some products attract high interest but low conversions, signaling pricing or positioning issues.

A few regions consistently underperform on satisfaction, suggesting areas for operational improvement.

📧 Email: asandandlela2004@gmail.com

📱 Phone: +27 74 780 5974 / +27 64 312 3670
🔗 GitHub: Asandandlela16/Data-science_Asanda_Ndlela

✨ Feedback and suggestions are always welcome as I continue improving my portfolio and skills!

