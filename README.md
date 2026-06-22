🛍️ End-to-End Customer Shopping Behavior Analytics
An end-to-end data pipeline that transforms raw retail transaction data into actionable business intelligence. This project demonstrates data cleaning and Exploratory Data Analysis (EDA) in Python, relational database modeling and querying in PostgreSQL, and interactive executive reporting in Power BI.

🛠️ Tech Stack & Skills
Data Engineering & EDA: Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook

Database Management: PostgreSQL (Schema Design, Aggregations, CTEs)

Business Intelligence: Power BI (Data Modeling, Visual Analytics)

🚀 Project Pipeline Architecture
[ Raw Data: CSV ] ---> [ Python / Pandas ] ---> [ PostgreSQL ] ---> [ Power BI Dashboard ]
(Data Cleaning/EDA)     (Deep-Dive SQL)       (Interactive Report)

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

📈 Key Business Insights
1. The Subscription Conversion Gap
The Metric: Only 27% of shoppers are active subscribers (1,053 out of 3,900).

The Opportunity: SQL filtering revealed that a large segment of non-subscribers are frequent, repeat buyers (5+ previous transactions). This represents a highly primed audience for target marketing campaigns to lock in predictable recurring revenue.

2. Demographic Purchasing Power
Gender Disparity: Order volume is heavily weighted toward male consumers (68% vs. 32% female).

Age Stability: The Average Order Value (AOV) hovers tightly around $59.76 across all generations (ages 18 to 70), indicating uniform purchasing power regardless of age.

3. Inventory Velocity
Sizing Bottlenecks: Size M captures roughly 45% of all sales. Supply chain capital should lean heavily into standard sizes to avoid stockouts in high-velocity categories like Clothing.

📂 Repository Directory Structure
-- customer_shopping_behavior.csv - Raw retail transaction dataset

-- customer_behavior_eda.ipynb - Jupyter Notebook containing Python data cleaning and visualizations

-- customer_behavior_eda.sql - PostgreSQL production scripts and deep-dive analytical queries

-- customer_behavior_dashboard.pbix - Compiled Power BI Dashboard file

-- README.md - Documentation and project guide

💻 How to Run This Project
Run Python EDA: Open customer_behavior_eda.ipynb in Jupyter Notebook and execute the cells to clean the raw data.

Database Setup: Open pgAdmin or any PostgreSQL client, run the queries inside customer_behavior_sql_queries.sql to build the database layer.

View Dashboard: Open customer_behavior_dashboard.pbix using Power BI Desktop, or upload the file to app.powerbi.com to interact with it directly in your web browser.

Developed as a personal data portfolio project under the MIT License.
