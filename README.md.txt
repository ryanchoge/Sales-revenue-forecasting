# 🧠 Customer Revenue Prediction – E-Commerce Dataset (Online Retail II)

This project uses the [UCI Online Retail II dataset](https://archive.ics.uci.edu/ml/datasets/Online+Retail+II) to build a Linear Regression model that predicts customer revenue based on purchasing behavior. It demonstrates end-to-end data science skills from cleaning and feature engineering to modeling and business insights.

## 🚀 Project Objectives

- Clean and prepare real-world e-commerce transaction data
- Engineer features related to customer behavior and product sales
- Build and evaluate a linear regression model to predict customer revenue
- Extract meaningful insights for business strategy (marketing, product targeting, seasonality)
- Present a structured notebook ready for production and team sharing

## 📦 Dataset

- Source: UCI Machine Learning Repository
- Period: 2010–2011 transactions
- Fields Include:
  - `InvoiceNo`: Unique transaction ID
  - `StockCode`: Product code
  - `Description`: Product name
  - `Quantity`: Units purchased
  - `InvoiceDate`: Transaction timestamp
  - `UnitPrice`: Price per unit
  - `CustomerID`: Unique identifier per customer
  - `Country`: Customer location

## 🧹 Step 1: Data Cleaning

- Removed:
  - Cancelled transactions (`InvoiceNo` starts with 'C')
  - Rows with missing `CustomerID`
  - Negative quantities or prices
- Created `TotalPrice = Quantity * UnitPrice`

## 🛠️ Step 2: Feature Engineering

Created customer-level features including:
- `NumOrders`: Number of unique transactions
- `TotalQuantity` & `TotalRevenue`: Aggregate totals
- `Recency`: Days since last purchase
- `AvgBasket`: Revenue per order
- `Month`, `DayOfWeek`, `Season`: Time features

## 📈 Step 3: Linear Regression Model

Target Variable: Total Revenue per Customer

Features Used:
- Number of Orders
- Total Quantity Purchased
- Recency (days since last purchase)
- Average Basket Size

Model Evaluation:
- R² Score: 0.8346
- RMSE: 3084.42

➡️ The model explains 83% of revenue variance — very strong for business forecasting.

## 📊 Step 4: Business Insights

- Top Products: Identified top 10 revenue-generating items
- Customer Segmentation: High-spend customers based on frequency and basket size
- Sales Trends: Month-over-month revenue patterns and seasonal spikes
- Marketing Implication: Recency and basket size are strong drivers of revenue



