# Customer Segmentation Analysis

## 📌 Overview

This project performs **customer segmentation using K-Means clustering** on an e-commerce retail sales dataset.

The goal is to identify groups of customers with similar purchasing and demographic characteristics. These segments can help an e-commerce business understand its customer base and develop more targeted marketing strategies.

The analysis covers data cleaning, exploratory analysis, feature selection, standardization, the Elbow Method, K-Means clustering, cluster visualization, customer profiling, and marketing recommendations.

---

## 🎯 Objectives

* Explore and clean the retail sales dataset.
* Analyze customer purchasing patterns using descriptive statistics.
* Select meaningful features for customer segmentation.
* Standardize the selected features before clustering.
* Determine a suitable number of clusters using the **Elbow Method**.
* Apply **K-Means clustering** to segment customers.
* Visualize and profile the resulting customer segments.
* Develop potential marketing strategies for each segment.
* Identify limitations of the available dataset.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** — Data manipulation and analysis
* **NumPy** — Numerical operations
* **Scikit-learn** — StandardScaler and K-Means clustering
* **Matplotlib** — Data visualization
* **Seaborn** — Statistical visualization
* **Google Colab / Jupyter Notebook** — Development environment

---

## 📊 Dataset

The dataset contains **1,000 retail transactions** and includes the following attributes:

| Column             | Description                       |
| ------------------ | --------------------------------- |
| `Transaction ID`   | Unique transaction identifier     |
| `Date`             | Transaction date                  |
| `Customer ID`      | Unique customer identifier        |
| `Gender`           | Customer gender                   |
| `Age`              | Customer age                      |
| `Product Category` | Category of the purchased product |
| `Quantity`         | Number of items purchased         |
| `Price per Unit`   | Price of each item                |
| `Total Amount`     | Total transaction amount          |

Each customer appears exactly once in the dataset.

---

## 🔍 Methodology

### 1. Data Cleaning

The dataset was inspected for:

* Missing values
* Duplicate records
* Invalid numerical values
* Incorrect date formats
* Inconsistencies between `Quantity × Price per Unit` and `Total Amount`

The transaction date was converted to a datetime format and duplicate records were removed.

### 2. Descriptive Analysis

Basic statistics were calculated to understand:

* Average purchase value
* Total revenue
* Average quantity purchased
* Number of customers
* Number of transactions

### 3. Feature Selection

Traditional **RFM (Recency, Frequency, Monetary)** analysis was considered. However, each customer appears only once in this dataset, meaning purchase frequency is constant for all customers.

Therefore, the following features were selected for clustering:

* **Age**
* **Quantity Purchased**
* **Total Amount Spent**

These features provide meaningful variation between customers.

### 4. Feature Standardization

The selected features have different numerical scales. **StandardScaler** was used to standardize the variables before clustering so that features with larger numerical values would not disproportionately influence the K-Means algorithm.

### 5. Elbow Method

The Elbow Method was used to evaluate different values of K.

The resulting inertia curve showed a noticeable reduction in improvement after **K = 4**, so four clusters were selected for the final model.

### 6. K-Means Clustering

K-Means was applied with:

```text
Number of clusters: 4
Random state: 42
```

Each customer was assigned to one of four segments based on similarity in the standardized feature space.

---

## 📈 Customer Segments

The resulting clusters were profiled using their average age, quantity purchased, and total transaction amount.

| Segment                     | Customers | Avg. Age | Avg. Quantity | Avg. Spending |
| --------------------------- | --------: | -------: | ------------: | ------------: |
| Older, Moderate-Spending    |       283 |    52.31 |          1.47 |        233.06 |
| Younger, Lower-Spending     |       240 |    26.83 |          1.74 |        211.42 |
| High-Value                  |       228 |    39.63 |          3.39 |      1,344.74 |
| High-Quantity, Low-Spending |       249 |    44.63 |          3.64 |        131.35 |

### Segment Interpretation

**Older, Moderate-Spending Customers**

These customers have the highest average age and relatively low purchase quantities, with moderate transaction spending.

**Younger, Lower-Spending Customers**

This segment has the lowest average age and relatively low purchase quantity and spending.

**High-Value Customers**

This segment has significantly higher average spending and a relatively high purchase quantity, making it an important segment for retention and personalized marketing.

**High-Quantity, Low-Spending Customers**

These customers purchase the highest average quantity but have the lowest average transaction amount, suggesting opportunities for cross-selling and upselling.

---

## 📌 Marketing Insights

Different customer segments can be approached with different marketing strategies:

| Segment                     | Potential Marketing Strategy                                       |
| --------------------------- | ------------------------------------------------------------------ |
| Older, Moderate-Spending    | Personalized promotions and loyalty rewards                        |
| Younger, Lower-Spending     | Introductory discounts, bundles, and engagement campaigns          |
| High-Value                  | Loyalty programs, premium offers, and personalized recommendations |
| High-Quantity, Low-Spending | Cross-selling, product bundles, and upselling                      |

These strategies are based on the observed characteristics of each segment and can be refined further using additional customer history.

---

## 📊 Visualizations

The project includes:

* Customer distribution across clusters
* Elbow Method plot
* Quantity vs. Total Amount scatter plot
* Age vs. Total Amount scatter plot
* Cluster profile analysis
* Correlation analysis of selected features

---

## ⚠️ Limitations

The main limitation of the dataset is that **each customer appears only once**.

Therefore, the analysis cannot reliably measure:

* Repeat purchase behavior
* Purchase frequency over time
* Customer retention
* True customer lifetime value
* Long-term recency patterns

Because of this limitation, the analysis does not represent a complete RFM segmentation. Instead, it uses available demographic and transaction-level features.

A dataset containing multiple transactions per customer would allow a more comprehensive RFM-based segmentation.

---

## 🚀 Future Improvements

Future versions of this project could include:

* Multiple transactions per customer
* Full RFM analysis
* Customer Lifetime Value calculation
* Additional behavioral features
* Comparison with other clustering algorithms such as DBSCAN or Hierarchical Clustering
* Automated customer segment reporting
* Interactive dashboards using Power BI or Tableau
* Integration with marketing campaign data to measure segment performance

---

## 📁 Project Structure

```text
customer-segmentation/
│
├── customer_segmentation.ipynb
├── retail_sales_dataset.csv
├── README.md
└── visualizations/
```

---

## 💡 Key Takeaway

This project demonstrates how **unsupervised machine learning can be used to identify customer segments without predefined labels**.

By combining data preprocessing, feature engineering, standardization, the Elbow Method, and K-Means clustering, the analysis identifies four distinct customer groups with different purchasing characteristics. These segments provide a foundation for more targeted and data-driven marketing strategies.
