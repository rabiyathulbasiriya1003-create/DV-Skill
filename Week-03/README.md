#  Apple Stock Data Analysis – DV Week 03

##  Project Overview

This project focuses on **Apple Stock Data Analysis** using Python and Pandas.

The project demonstrates how to load stock market data, inspect the dataset, clean the data, work with date values, sort the data, and generate basic statistical information.

The analysis is performed using **Python, Pandas, NumPy, and Matplotlib**.

##  Objectives

* Load Apple stock data from CSV and Excel files.
* Explore the structure of the dataset.
* Display the first and last records.
* Check columns and data types.
* Generate descriptive statistics.
* Remove missing values.
* Remove duplicate records.
* Convert the Date column into datetime format.
* Sort the data based on Date.
* Verify the cleaned dataset.

##  Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Google Colab**

## Dataset

The project uses **Apple historical stock data**.

The dataset is loaded from a CSV file:

```python
df = pd.read_csv("AAPL.csv")
```

The project also demonstrates loading the data from an Excel file:

```python
df = pd.read_excel("AAPL.xlsx")
```

##  Data Analysis Process

### 1. Importing Libraries

The required Python libraries are imported for data analysis.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

### 2. Loading the Dataset

The Apple stock dataset is loaded using Pandas.

```python
df = pd.read_csv("AAPL.csv")
```

The dataset is then displayed for analysis.

### 3. Exploring the Dataset

The project uses different Pandas functions to understand the dataset.

#### First Records

```python
print(df.head())
```

#### Last Records

```python
print(df.tail())
```

#### Dataset Information

```python
df.info()
```

#### Column Names

```python
print(df.columns)
```

#### Data Types

```python
print(df.dtypes)
```

#### Statistical Summary

```python
print(df.describe())
```

These operations help understand the structure, columns, data types, and statistical characteristics of the stock dataset.

##  Data Cleaning

Data cleaning is performed to improve the quality of the dataset.

### Remove Missing Values

```python
df = df.dropna()
```

This removes rows containing missing values.

### Remove Duplicate Records

```python
df = df.drop_duplicates()
```

This removes duplicate rows from the dataset.

##  Date Processing

The `Date` column is converted into datetime format.

```python
df["Date"] = pd.to_datetime(df["Date"])
```

This makes the date values easier to work with during analysis.

##  Sorting the Data

The stock data is sorted according to the `Date` column.

```python
df = df.sort_values("Date")
```

Sorting the data helps arrange the stock records in chronological order.

##  Analysis Performed

The project includes the following analysis steps:

| Analysis            | Purpose                      |
| ------------------- | ---------------------------- |
| `head()`            | View the first records       |
| `tail()`            | View the last records        |
| `info()`            | Check dataset information    |
| `columns`           | Identify column names        |
| `dtypes`            | Check data types             |
| `describe()`        | Generate statistical summary |
| `dropna()`          | Remove missing values        |
| `drop_duplicates()` | Remove duplicate records     |
| `to_datetime()`     | Convert Date values          |
| `sort_values()`     | Sort records by Date         |

##  Project Structure

```text
Apple-Stock-Data-Analysis/
│
├── AAPL.csv
├── AAPL.xlsx
├── apple_stock_data_dv_week_03.py
└── README.md
```

##  How to Run the Project

### Step 1: Install Required Libraries

```bash
pip install pandas numpy matplotlib openpyxl
```

### Step 2: Add the Dataset

Place the Apple stock dataset files in the project folder.

### Step 3: Run the Python Program

```bash
python apple_stock_data_dv_week_03.py
```

The project can also be executed using **Google Colab**.

##  Learning Outcomes

Through this project, I learned how to:

* Load CSV and Excel files using Pandas.
* Explore and understand a dataset.
* Check columns and data types.
* Generate descriptive statistics.
* Handle missing values.
* Remove duplicate records.
* Convert date values into datetime format.
* Sort data chronologically.
* Perform basic stock data preprocessing using Python.
