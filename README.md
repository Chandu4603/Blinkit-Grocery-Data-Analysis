# Blinkit-Grocery-Data-Analysis
This project analyzes grocery sales data from Blinkit using Power BI to uncover business insights related to sales performance, customer behavior, product demand, and revenue trends.
The goal was to transform raw transactional data into an interactive dashboard that helps stakeholders make data-driven decisions regarding inventory, pricing, and marketing strategies.

# Problem Statement
This dashboard comprises the sales of Blinkit.To conduct a comprehensive analysis of Blinkit's sales performance,customer satisfaction, and inventory distribution to identify key insights and opportunities for optimization using various KPI's and Visualization in Power BI.

## KPI'S Requirements
Total Sales : The overall revenue generated from all items sold.
Average Sales : The average revenue per sale.
Number of items : The total count of different items sold.
Average Rating : The average customer rating for items sold.

## 🎯 Project Objectives
Monitor overall sales performance.
Identify top-performing products and categories.
Analyze customer purchasing behavior.
Evaluate impact of discounts on revenue.
Compare sales performance across cities.
Create an interactive and dynamic dashboard.

## 📂 Dataset Details
Data Set used Link: 
- <a href="https://github.com/Chandu4603/Blinkit-Grocery-Data-Analysis/blob/main/BlinkIT%20Grocery%20Data.xlsx"> Data Set </a>

The dataset includes:
1. Order ID
2. Order Date
3. Customer ID
4. Product Name
5. Category
6. Quantity
7. Unit Price
8. Discount (%)
9. Total Sales
10. City
11. Payment Method

## 🛠️ Tools Used
1. Power BI Desktop
2. Power Query (Data Cleaning)
3. DAX (Data Analysis Expressions)
4. Excel (Data Source)

#  🔄 Project Workflow in Power BI
## 1. Data Import & Cleaning (Power Query)
   Removed null and duplicate records
   Changed data types (Date, Currency, Whole Number)
   # Created new calculated columns:
       Revenue = Quantity × Unit Price
       Discounted Price
       Profit (if cost available)
## 2. Data Modeling
   Established relationships between:
   Orders Table
   Customer Table
   Product Table
   Date Table (Created Calendar Table using DAX)
   Created Star Schema Model for better performance.

## DAX Measures Created
Examples:
  Total Revenue = SUM(Sales[Total Sales])
  Total Orders = DISTINCTCOUNT(Sales[Order ID])
  Average Order Value = DIVIDE([Total Revenue], [Total Orders])
  Total Quantity Sold = SUM(Sales[Quantity])
  Repeat Customers = 
  CALCULATE(
    DISTINCTCOUNT(Sales[Customer ID]),
    FILTER(Sales, CALCULATE(COUNT(Sales[Order ID])) > 1)
)
##  📊 Dashboard Features

🔹 KPI Cards
Total Revenue
Total Orders
Total Customers
Average Order Value

🔹 Sales Trend Analysis
Monthly Revenue Line Chart
Year-over-Year Growth

🔹 Product Analysis
Top 10 Products by Revenue
Category-wise Sales (Bar / Donut Chart)

🔹 City-wise Performance
Revenue by City (Map Visualization)
Order Distribution by Location

🔹 Customer Insights
New vs Repeat Customers
Payment Method Distribution

🔹 Discount Impact
Revenue vs Discount % Scatter Plot
Discount Contribution to Sales

## 📈 Key Insights from the Dashboard
Fruits & Vegetables and Dairy categories generated the highest revenue.
Weekend sales were 20–30% higher than weekdays.
Metro cities contributed the majority of revenue.
30% of customers contributed nearly 65% of total revenue.
Discounts between 10–20% optimized both revenue and volume.

## 💡 Business Recommendations
Increase inventory for high-demand categories
Introduce loyalty programs for repeat customers
Optimize discount strategies to maintain profit margins
Expand marketing in high-performing cities
