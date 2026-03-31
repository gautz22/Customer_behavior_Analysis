🛍️ Customer Shopping Behavior Analysis

This project analyzes customer shopping behavior using transactional data from 3,900 purchases across multiple product categories.

The objective is to uncover actionable insights into:

-Customer spending patterns
-Product preferences
-Subscription behavior
-Customer segmentation

These insights help businesses make data-driven decisions to improve revenue, marketing strategies, and customer retention.

---
<img width="2268" height="1278" alt="Screenshot 2026-03-31 052632" src="https://github.com/user-attachments/assets/d2ac64f6-534e-460c-af85-6d99d05e86a8" />

---
📊 Dataset Summary
Feature	Description
Rows	3,900
Columns	18
Missing Values	37 (in review_rating)
Key Data Categories
Customer Demographics
Age, Gender, Location, Subscription Status
Purchase Details
Item Purchased, Category, Purchase Amount, Season, Size, Color
Behavioral Data
Discount Applied, Promo Code Used, Previous Purchases, Frequency, Review Rating, Shipping Type

---
⚙️ Tech Stack
Python → Data Cleaning & Preprocessing
Pandas, NumPy → Data manipulation
PostgreSQL → Data Analysis (SQL queries)
Power BI → Dashboard & Visualization
---
🧹 Data Cleaning & Preprocessing (Python)

Key steps performed:

Data Loading
df = pd.read_csv("dataset.csv")

Initial Exploration
df.info() → structure
df.describe() → statistical summary

Handling Missing Values
Filled missing review_rating using median rating per product category

Column Standardization
Converted column names to snake_case

Feature Engineering
Created age_group from age bins
Derived purchase_frequency_days

Data Consistency
Identified redundancy between discount_applied and promo_code_used
Dropped promo_code_used

Database Integration
Loaded cleaned dataset into PostgreSQL

---
🧠 Data Analysis (SQL)

Performed business-driven analysis using SQL:

🔹 Revenue Analysis
Revenue comparison by gender
Revenue contribution by age group
🔹 Customer Behavior
Subscribers vs Non-subscribers spending
Repeat buyers vs subscription likelihood
🔹 Product Insights
Top 5 products by average rating
Top 3 products per category
Discount-dependent products
🔹 Purchase Patterns
High-spending customers using discounts
Shipping type vs purchase amount
🔹 Customer Segmentation

Customers classified into:

🆕 New
🔁 Returning
⭐ Loyal
📈 Dashboard (Power BI)

An interactive dashboard was created to visualize:

Revenue trends
Customer segmentation
Product performance
Subscription impact
