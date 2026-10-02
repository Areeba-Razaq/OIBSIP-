# Task 3 – Cleaning Data

## Overview

This task focuses on cleaning and preprocessing a deliberately messy crime incident dataset to transform it into a clean and analysis-ready dataset.

The cleaning process was performed using **Python, Pandas, NumPy, and Jupyter/Google Colab**, with each major cleaning decision documented in the notebook.

## Objectives

* Inspect the dataset and identify data quality issues
* Analyze missing values and handle them appropriately
* Remove duplicate records
* Standardize inconsistent categorical values and formatting
* Detect and handle invalid values and outliers
* Correct inappropriate data types
* Compare the dataset before and after cleaning
* Export the final cleaned dataset as a CSV file

## Data Cleaning Steps

The following preprocessing tasks were performed:

1. **Initial Data Quality Assessment**

   * Checked dataset dimensions, data types, missing values, duplicates, and invalid values.

2. **Duplicate Removal**

   * Identified and removed exact duplicate rows.

3. **Missing Value Handling**

   * Applied suitable strategies based on the type and meaning of each column.
   * Numerical values were handled using appropriate statistical measures where applicable.
   * Categorical fields were standardized and missing values were handled using suitable placeholders or mode imputation.
   * Missing incident dates were retained rather than artificially assigning dates.

4. **Data Standardization**

   * Standardized inconsistent capitalization, spacing, abbreviations, and spelling variations in categorical fields such as crime type, gender, race, weapon, case status, resolution, and severity.

5. **Invalid Value Correction**

   * Identified invalid ages and geographic coordinates and treated them as missing values rather than retaining logically impossible values.

6. **Data Type Correction**

   * Converted dates to datetime format.
   * Converted monetary values to numeric format.
   * Converted identifier columns to string format.
   * Converted boolean fields to an appropriate boolean representation.

7. **Outlier Detection**

   * Used statistical techniques such as the IQR method to identify potential numerical outliers.
   * Distinguished between genuine extreme values and logically invalid values.

8. **Before vs. After Comparison**

   * Compared row count, duplicate count, missing values, and data types before and after cleaning.

## Files

* `data_cleaning.ipynb` – Complete data cleaning process, analysis, and documentation.
* `cleaned_crime_incident_dataset.csv` – Final cleaned dataset ready for analysis.

## Tools & Technologies

* Python
* Pandas
* NumPy
* Jupyter Notebook / Google Colab

## Outcome

The final dataset is cleaned, standardized, and prepared for further exploratory analysis or machine learning tasks.
