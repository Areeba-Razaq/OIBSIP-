# Retail Sales Exploratory Data Analysis

## 📌 Project Overview

This project performs an Exploratory Data Analysis (EDA) on a retail sales dataset to identify sales trends, customer purchasing patterns, and product-category performance.

The analysis focuses on understanding how sales vary over time, how customer demographics are distributed, and which product categories contribute most to sales and revenue.

---

## 🎯 Objectives

The main objectives of this project are to:

* Inspect and understand the retail sales dataset
* Identify missing values and duplicate records
* Calculate descriptive statistics for numerical variables
* Analyze monthly and quarterly sales trends
* Examine customer age-group and gender distributions
* Analyze product-category sales performance
* Identify revenue contribution by product category
* Explore relationships between numerical variables using correlation analysis
* Identify additional customer spending patterns
* Generate actionable business recommendations

---

## 📊 Dataset

The dataset contains **1,000 retail transactions** and includes the following variables:

| Column           | Description                            |
| ---------------- | -------------------------------------- |
| Transaction ID   | Unique identifier for each transaction |
| Date             | Date of the transaction                |
| Customer ID      | Unique customer identifier             |
| Gender           | Customer gender                        |
| Age              | Customer age                           |
| Product Category | Category of the purchased product      |
| Quantity         | Number of units purchased              |
| Price per Unit   | Price of one unit                      |
| Total Amount     | Total transaction amount               |

### Data Quality

The dataset was checked for:

* Missing values
* Duplicate records
* Incorrect data types

The `Date` column was converted from text format to datetime format for time-series analysis.

---

## 🔍 Analysis Performed

### 1. Dataset Overview

* Dataset dimensions
* Column data types
* Missing-value analysis
* Duplicate-record check

### 2. Descriptive Statistics

Calculated:

* Mean
* Median
* Mode
* Standard deviation

for the main numerical variables.

### 3. Time-Series Analysis

Analyzed:

* Monthly sales trends
* Quarterly sales trends

Line charts were used to identify changes and fluctuations in sales over time.

### 4. Customer Demographics

Analyzed:

* Customer age groups
* Gender distribution
* Age-group and gender purchasing patterns

### 5. Product Category Analysis

Analyzed:

* Sales quantity by product category
* Top-selling product categories
* Revenue by product category
* Average transaction value by category

> **Note:** The dataset contains product categories rather than individual product names. Therefore, the top-selling analysis was performed at the product-category level.

### 6. Correlation Analysis

A correlation matrix and heatmap were created to examine relationships between:

* Age
* Quantity
* Price per Unit
* Total Amount

### 7. Additional Analysis

Customer spending behaviour was explored by comparing average transaction values across different age groups.

---

## 💡 Key Business Insights

The analysis provides insights into:

* Variations in sales across different months and quarters
* Differences in purchasing activity across customer age groups and genders
* Product categories with higher sales volume and revenue contribution
* Differences in average transaction value across customer segments
* Relationships between transaction-level numerical variables

The detailed findings and visualizations are available in the Jupyter Notebook.

---

## 📈 Business Recommendations

Based on the analysis, the project provides recommendations related to:

1. **Inventory and sales planning**
   Use historical sales patterns to prepare inventory and promotional activities around stronger and weaker sales periods.

2. **Product-category management**
   Prioritize inventory and evaluate promotional strategies based on category-level revenue and sales performance.

3. **Customer segmentation**
   Use demographic and transaction-value patterns to develop more targeted marketing and promotional strategies.

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook
* Google Colab

---

## 📁 Project Structure

```text
retail-sales-eda/
│
├── retail_sales_eda.ipynb
├── retail_sales_dataset.csv
├── README.md
└── .gitignore
```

---

## ▶️ How to Run

### Option 1 — Google Colab

1. Open the `.ipynb` file in Google Colab.
2. Upload `retail_sales_dataset.csv` when prompted.
3. Run the notebook cells from top to bottom.

### Option 2 — Local Jupyter Notebook

Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

Then open the notebook:

```bash
jupyter notebook
```

Make sure `retail_sales_dataset.csv` is located in the same directory as the notebook.

---

## 👤 Author

**Areeba Razzaq**

Retail Sales Exploratory Data Analysis — Internship Project
