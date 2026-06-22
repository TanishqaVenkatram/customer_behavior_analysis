🛍️ Customer Shopping Behavior Analytics

An end-to-end data analytics project that transforms raw retail transaction data into actionable business intelligence. This project demonstrates data cleaning and Exploratory Data Analysis (EDA) in Python, relational database modeling and querying in PostgreSQL, and interactive executive reporting in Power BI.

🛠️ Tech Stack & Skills
Data Engineering & EDA: Python, Pandas, Jupyter Notebook

Database Management: PostgreSQL (Aggregations, CTEs)

Business Intelligence: Power BI (Data Modeling, Visual Analytics)

🚀 Project Architecture
```text
[ Raw Data: CSV ] ---> [ Python / Pandas ] ---> [ PostgreSQL ] ---> [ Power BI Dashboard ]
```

📊 Dashboard Visuals

<img width="914" height="503" alt="Customer_behavior_dashboard" src="https://github.com/user-attachments/assets/398bf6fc-c7ae-4e96-9c75-b652e54a489f" />

🔍 Step-by-Step Implementation

🎯 Phase 1: Python Data Cleaning & EDA
The raw transaction data of 3,900 records was profiled using Pandas in a Jupyter Notebook to ensure data integrity prior to database ingestion:

✅ Checked and resolved missing value distributions.

✅ Standardized text categorical variables and verified numerical metrics (Ages, Purchase Amounts).

✅ Analyzed initial spending distributions using Seaborn.


🎯 Phase 2: PostgreSQL Deep-Dive Analysis
Cleaned data was migrated into PostgreSQL to perform advanced transactional and demographic analysis.

Below is an example feature query used to analyze product category and gender performance:
```sql
SELECT
category,
gender,
COUNT(customer_id) AS total_orders,
SUM(purchase_amount_usd) AS total_revenue,
ROUND(AVG(review_rating), 2) AS average_rating
FROM customer_behavior
GROUP BY category, gender
ORDER BY total_revenue DESC;
```

📈 Key Business Insights
1. Customer Spending vs. Frequency

The Revenue Reality: While repeat buyers are valuable, the data shows that "Fortnightly" and "Weekly" shoppers have a lower average spend per transaction (~$55.00) compared to those who shop "Bi-Weekly" or "Annually" (~$63.00).

The Takeaway: Frequent shoppers buy smaller baskets, while less frequent shoppers buy higher-value carts.

2. Premium Shipping Pricing Opportunity

The Logistics Metric: Customers choosing premium shipping options like "Next Day Air" and "Express" maintain a high average purchase amount (~$60.00).

The Takeaway: High-value purchasers are less price-sensitive about shipping costs. Premium logistics fees can be scaled up slightly without risking cart abandonment.

3. Promo Codes and Customer Satisfaction

The Sentiment Data: Transactions utilizing a Promo Code yield an average review rating of 3.75 out of 5. Transactions with No Promo Code yield an average rating of 3.74 out of 5.

The Takeaway: Discounts keep order satisfaction steady but do not significantly increase customer happiness scores, meaning promotions primarily drive order volume rather than sentiment.

📂 Repository Directory Structure
```text
-- customer_shopping_behavior.csv - Raw retail transaction dataset

-- customer_behavior_eda.ipynb - Jupyter Notebook containing Python data cleaning and visualizations

-- customer_behavior_eda.sql - PostgreSQL production scripts and deep-dive analytical queries

-- customer_behavior_dashboard.pbix - Compiled Power BI Dashboard file

-- README.md - Documentation and project guide
```

💻 How to Run This Project
Run Python EDA: Open customer_behavior_eda.ipynb in Jupyter Notebook and execute the cells to clean the raw data.

Database Setup: Open pgAdmin or any PostgreSQL client, run the queries inside customer_behavior_sql_queries.sql to build the database layer.

View Dashboard: Open customer_behavior_dashboard.pbix using Power BI Desktop, or upload the file to app.powerbi.com to interact with it directly in your web browser.

Developed as a personal data portfolio project under the MIT License.
