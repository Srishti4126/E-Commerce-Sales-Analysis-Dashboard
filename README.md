# 🛒 E-Commerce Sales Analysis Dashboard

An end-to-end data analytics project that transforms raw e-commerce order data into meaningful business insights using **Python, Pandas, SQL, and Power BI**.

The project focuses on cleaning and preparing sales data, calculating key business metrics, performing SQL-based analysis, and presenting the results through an interactive Power BI dashboard.

## 📌 Project Overview

E-commerce businesses generate large amounts of data related to orders, products, customers, payments, and deliveries. Analyzing this data helps businesses understand sales performance, identify top-performing products and categories, evaluate payment preferences, and monitor order statuses.

This project demonstrates a complete data analysis workflow, from raw data preprocessing to SQL querying and interactive dashboard development.

## 🎯 Project Objectives

- Clean and preprocess an unclean e-commerce dataset.
- Handle missing values, duplicate records, and inconsistent data.
- Calculate sales, net revenue, and estimated profit.
- Perform business analysis using SQL queries.
- Build an interactive Power BI dashboard.
- Identify sales trends across products, categories, cities, months, payment modes, and order statuses.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Python | Data cleaning and transformation |
| Pandas | Data manipulation and analysis |
| NumPy | Handling missing and invalid values |
| SQL | Business queries and aggregations |
| SQLite | Storing and querying the processed dataset |
| Power BI | Interactive dashboard and data visualization |
| Google Colab | Running the Python notebook |

## ⚙️ Project Workflow

### 1. Data Loading and Exploration

The dataset is imported from an Excel file and explored to understand its structure and quality.

Key operations include:
- Inspecting the first few records.
- Checking column names and data types.
- Generating descriptive statistics.
- Identifying missing values and duplicate records.

### 2. Data Cleaning and Preprocessing

The raw dataset is cleaned using Pandas to improve data consistency and usability.

Cleaning operations include:

- Removing duplicate records.
- Replacing inconsistent missing-value indicators such as `N/A`, `NULL`, and `null` with proper missing values.
- Removing unnecessary whitespace from text fields.
- Standardizing column names to lowercase with underscores.
- Filtering out records with non-positive quantities.
- Handling missing discount and phone values.
- Filling missing delivery dates using order dates.
- Converting order dates into datetime format.
- Removing records with invalid or missing order dates.
- Filling missing product prices using the median price within the corresponding category.

### 3. Feature Engineering and Calculations

New columns are created to support business analysis.

| Metric | Calculation |
|---|---|
| Total Sales | Quantity × Unit Price |
| Net Amount | Total Sales × (1 − Discount / 100) |
| Estimated Profit | Net Amount × 20% |
| Order Month | Month extracted from the order date |
| Order Year | Year extracted from the order date |
| Order Weekday | Day of the week extracted from the order date |

**Note:** Profit is estimated using an assumed fixed 20% margin. It is not calculated from actual cost or expense data.

### 4. SQL-Based Business Analysis

The cleaned dataset is stored in a SQLite database, allowing SQL queries to answer important business questions.

The analysis covers:

- **Total Orders:** Counts the number of records in the processed orders table.
- **Total Sales:** Calculates total net sales.
- **Top 5 Products:** Identifies the five products with the highest net sales.
- **Top 5 Cities:** Finds the five cities generating the highest net sales.
- **Monthly Sales:** Aggregates net sales by order month.
- **Top 5 Products by Profit:** Identifies products with the highest estimated profit.
- **Payment Mode Distribution:** Counts orders by payment method.
- **Cancelled Orders:** Counts orders marked as cancelled.

These queries demonstrate the use of SQL aggregation, `GROUP BY`, `ORDER BY`, `COUNT()`, `SUM()`, and `LIMIT`.

### 5. Power BI Dashboard

The processed data is visualized in an **E-Commerce Sales Analysis Dashboard** built in Power BI.

The dashboard includes the following components:

| Visualization | Purpose |
|---|---|
| KPI Cards | Display Total Sales, Total Profit, Total Orders, and Average Order Value |
| Line Chart | Analyze Total Sales by Month |
| Column Chart | Compare sales across products |
| Bar Chart | Compare sales across categories |
| Map | Visualize sales by city |
| Donut Chart | Analyze sales by payment mode |
| Pie Chart | Show sales distribution by order status |
| Column Chart | Compare estimated profit across categories |

### 6. Interactive Filtering

The dashboard includes slicers for:

- Month
- Payment Mode
- City

These filters allow users to explore different segments of the sales data and analyze performance across selected dimensions.

## 📊 Key Business Questions Answered

This project helps explore questions such as:

1. What is the total sales revenue generated by the orders?
2. Which products generate the highest sales?
3. Which cities contribute the most to sales?
4. How do sales vary across months?
5. Which product categories generate the highest sales and estimated profit?
6. Which payment modes are most frequently used?
7. How are sales distributed across different order statuses?
8. How can sales performance be explored by month, city, and payment mode?

## 📁 Project Files

The repository contains the following main project files:

- `project2(1).ipynb` — Jupyter Notebook containing Python data cleaning, feature engineering, SQLite setup, and SQL analysis.
- `project2(1).pbix` — Power BI dashboard file.
- `Ecommerce_Unclean_Project.xlsx` — Original dataset required to execute the notebook.

*Rename the files to simpler names, such as `ecommerce_sales_analysis.ipynb` and `ecommerce_sales_dashboard.pbix`, before publishing if desired.*

## 🚀 How to Run the Project

### Prerequisites

- Python 3.x
- Jupyter Notebook or Google Colab
- Microsoft Power BI Desktop
- The original Excel dataset

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

Replace the placeholders with your GitHub username and repository name.

### Step 2: Install Python Libraries

```bash
pip install pandas numpy openpyxl
```

### Step 3: Run the Notebook

Open the notebook in Jupyter Notebook or upload it to Google Colab.

Upload the original Excel dataset when prompted and ensure that its filename matches the filename used in the notebook.

Run the cells sequentially to perform data cleaning, calculate the required metrics, create the SQLite database, and execute the SQL queries.

### Step 4: Open the Power BI Dashboard

Open the `.pbix` file using Power BI Desktop.

If you want to refresh the dashboard with new data, ensure the relevant source data and data model are configured correctly.

## 💡 Skills Demonstrated

- Data cleaning and preprocessing
- Exploratory data analysis
- Missing-value and duplicate handling
- Feature engineering
- Data aggregation and business metrics
- SQL querying and analysis
- Python–SQLite integration
- Data visualization and dashboard development
- Translating business questions into analytical queries

## 🔮 Future Improvements

Potential extensions to this project include:

- Adding customer-level analysis and customer segmentation.
- Analyzing repeat purchases and customer retention.
- Investigating cancellation rates and delivery performance.
- Adding more advanced time-based sales comparisons.
- Incorporating actual product costs to calculate profit more accurately.
- Expanding the dashboard with additional KPIs and drill-down analysis.

## 👩‍💻 Author

**Srishti Kukreti**

B.Tech Information Technology Student 

Interested in data analytics, SQL, Python, and business intelligence.

---

⭐ If you find this project useful, feel free to explore the repository and share your feedback.
