# 💻 IT Equipment Sales Analysis

> IT equipment sales analysis using Excel and Power BI to explore sales performance, profitability, customer segments, and employee performance.

---

## 📌 Project Overview

This project analyzes IT equipment sales data to understand overall business performance across sales, products, customers, and employees.

The analysis covers **sales performance, profitability, product and customer performance, employee target attainment, and bonus eligibility** to identify key business insights and areas for improvement.

The project uses **Microsoft Excel** for data preparation, validation, calculations, and initial analysis, followed by **Power BI** for interactive dashboards and data visualization.

---

## 🎯 Business Questions

The analysis was designed around the following business questions:

1. How are sales and profit performing across over time?
2. Which departments generate the highest sales and profit?
3. Which products and categories contribute the most to sales and profitability?
4. Which customer segments and tiers generate the most value?
5. How is each employee performing in terms of sales and performance?
6. How well are employees performing against their sales targets?
7. How is employee performance distributed across target attainment levels?
8. How many employees are eligible for bonuses?
9. How are bonus rates distributed among eligible employees?
10. How are bonus payouts distributed across departments?

---

## 🗂️ Dataset

The dataset contains sales transactions and supporting information related to products, customers, employees, employee performance, and operating costs.

### Main Tables

| Table | Description |
|---|---|
| `Sales` | Sales ID, Sales Date, Month, Employee ID, Customer ID, Product ID, Quantity, Discount, Sales Amounth, Cost Amounth, Profit, Region, and Order status |
| `Products` | Product ID, Product Name, Category, Count Unit, Unit Cost, List Price, Net Cost, Net Profit, and Margin % |
| `Customers` | Customer information including Customer ID, Customer Name, Segment, Region, and Customer tier |
| `Employees` | Employee information including Employee ID, Employee Name, Department, Level, Monthly Salary, and Performance Target |
| `Performance_KPI` | Employee Performance Scores, Target Attainment, Review Status, and Bonus Information |
| `Overhead_Costs` | Overhead costs by Year, Month, Department, Overhead Cost, and Cost Type |

---

## 🧹 Data Preparation

Data preparation focused on **checking data quality, correcting inconsistent values, validating calculations, and combining related tables** before performing the analysis.

### 1. Data Cleaning & Validation

The raw sales data was reviewed to ensure that key fields were complete, consistent, and suitable for analysis.

- Removed leading and trailing spaces from key fields using `TRIM()`
- Checked for missing values across important columns
- Reviewed `Quantity`, `Discount`, `Region`, and `Order_Status` for invalid or inconsistent values
- Standardized `Order_Status` values such as `Completed`, `Pending`, and `Cancelled`
- Checked for duplicate `Sale_ID` records
- Verified the consistency of `Employee_ID`, `Customer_ID`, and `Product_ID`
- Reviewed regional values and standardized inconsistent region names
- Validated sales-related figures by checking whether **quantity, price, discount, and sales amount** were consistent with the expected transaction values

### 2. Data Combining

Related information was combined to create a more complete dataset for analysis.

- Added employee name and department information to the sales data
- Added customer name, segment, and tier information to the sales data
- Added product name, category, cost, and list price information to the sales data
- Aggregated `Sales` by `Employee_ID` to calculate `Net_Sales` and `Profit`
- Added `Net_Sales` and `Profit` to the `Employees` table for employee performance analysis
- Aggregated `Sales` by `Product_ID` to calculate `CountUnit`, `Net_Cost`, `Net_Sales`, `Net_Profit`, and `Margin_%`
- Combined employee information with performance data to create the `Performance_KPI` table for KPI and bonus analysis

### 3. Calculated Fields & KPI Preparation

Additional fields were created to support the analysis:

- Calculated `Net Sales` from quantity, list price, and discount
- Compared calculated `Net Sales` with the original `Sales_Amount` to validate transaction accuracy
- Calculated total sales, total profit, and profit margin
- Calculated `Target Attainment` as Actual Result ÷ Performance Target
- Classified employees based on target attainment levels
- Determined bonus eligibility based on the required Overall Score threshold
- Calculated bonus percentage and bonus payout based on the defined bonus rules

---

## 🔎 Analysis Approach

The analysis was divided into several areas to answer the business questions and evaluate business performance from different perspectives.

### 1. Sales Performance

Analyzed sales performance across departments and over time using:

- Net Sales
- Total Profit
- Profit Margin
- Order Volume
- Quantity Sold
- Monthly Sales Trends
- Sales by Department

The analysis helps identify which departments contribute most to revenue and profit and how sales performance changes over time.

### 2. Product & Category Analysis

Evaluated product and category performance based on:

- Net Sales
- Total Profit
- Profit Margin
- Quantity Sold

The analysis compares high- and low-performing products and identifies categories that generate strong sales or profitability.

### 3. Customer Analysis

Analyzed customers based on:

- Customer Segment
- Customer Tier
- Sales Contribution
- Profit Contribution

This helps identify which customer groups generate the most value for the business.

### 4. Employee Performance

Employee performance was evaluated using both sales results and performance scores.

Key metrics include:

- Performance Target
- Actual Result
- Target Attainment
- Overall Score
- Review Status
- Sales and Profit by Employee
- Department Performance

This provides a view of both **sales achievement and broader employee performance**.

### 5. Bonus Analysis

Bonus analysis evaluates how employee performance translates into incentive payments.

The analysis covers:

- Bonus Eligibility
- Bonus Rate
- Bonus Payout
- Bonus Eligible Employees by Department
- Bonus Payout by Department
- Individual Employee Bonus Details

This helps understand how bonus costs are distributed and which employees or departments receive the largest payouts.

---

## 📊 Dashboard

The Power BI dashboard provides an interactive view of the analysis across four main areas.

### 01 — Sales Overview

Provides an overview of overall sales performance, including sales trends, profit, regional performance, product categories, and order status.

### 02 — Product Analysis

Examines product and category performance based on sales, profit, quantity sold, and margin.

### 03 — Customer Analysis

Explores customer segments, customer tiers, and their contribution to sales and profit.

### 04 — Employee Performance

Evaluates employee sales performance, target attainment, overall performance scores, bonus eligibility, and bonus payouts.

---

## 💡 Key Insights

Key insights from the analysis include:

- Identifying departments with the highest sales and profit contribution
- Comparing sales performance with profitability across departments
- Identifying high- and low-performing product categories and products
- Understanding which customer segments and tiers contribute the most value
- Evaluating employee performance against sales targets
- Comparing overall performance scores with target attainment
- Identifying the number of employees eligible for bonuses
- Understanding how bonus payouts are distributed across departments and employees

---

## 🛠️ Tools & Skills

### Tools

- **Microsoft Excel** — Data cleaning, validation, transformation, formulas, KPI calculations, and analysis
- **Power BI** — Data modeling, DAX, interactive dashboards, and data visualization

### Skills Demonstrated

- Data Cleaning & Validation
- Data Transformation
- Data Combining
- Exploratory Data Analysis
- Sales Performance Analysis
- Profitability Analysis
- Product Analysis
- Customer Analysis
- Employee Performance Analysis
- KPI Development
- Bonus Analysis
- Data Visualization
- Business Insight Generation

---

## 📁 Project Structure

```text
IT_Equipment_Sales/
│
├── README.md
│
├── Data/
│   └── IT_Equipment_Sales_Analysis.xlsx
│
├── Dashboard/
│   └── IT_Equipment_Sales_Dashboard.pbix
│
└── Images/
    ├── 01_Sales_Overview.png
    ├── 02_Product_Analysis.png
    ├── 03_Customer_Analysis.png
    └── 04_Employee_Performance.png
