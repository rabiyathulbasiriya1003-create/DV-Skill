Superstore Sales Data Visualization

Project Overview

This project focuses on analyzing and visualizing **Superstore sales data** using Python. The main goal is to understand sales performance, product categories, sales distribution, and delivery time through **data analysis and visualization**.

The project uses **Pandas, NumPy, Matplotlib, and Seaborn** to perform data preprocessing, analysis, and visualization.

 Objectives

* Analyze the Superstore sales dataset.
* Understand sales performance across different categories.
* Convert and process date-related data.
* Calculate delivery days for each order.
* Check the dataset for missing values.
* Visualize category-wise sales.
* Understand the distribution of sales values.

 Technologies Used

* **Python**
* **Pandas** – Data loading and analysis
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Google Colab** – Development environment

 Dataset

The project uses the **Sample Superstore Dataset**, which contains sales and order-related information.

Important columns used in the analysis include:

* `Order Date`
* `Ship Date`
* `Category`
* `Sales`

Data Analysis Process

### 1. Importing Libraries

The required Python libraries are imported for data analysis and visualization.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### 2. Loading the Dataset

The Superstore CSV file is loaded using Pandas.

```python
df = pd.read_csv("samplesuperstore.csv")
```

### 3. Exploring the Dataset

The dataset is explored using:

```python
df.head()
df.info()
df.describe()
```

These functions help to understand the dataset structure, columns, data types, and statistical information.

### 4. Date Conversion

The `Order Date` and `Ship Date` columns are converted into datetime format.

```python
df['Order Date'] = pd.to_datetime(df['Order Date'])
df['Ship Date'] = pd.to_datetime(df['Ship Date'])
```

### 5. Calculating Delivery Days

The number of days taken to ship each order is calculated.

```python
df['Delivery Days'] = (df['Ship Date'] - df['Order Date']).dt.days
```

### 6. Category Analysis

The unique product categories are identified and total sales are calculated for each category.

```python
category_sales = df.groupby('Category')['Sales'].sum()
```

### 7. Sales Visualization

A bar chart is created to visualize total sales by category.

```python
category_sales.plot(kind='bar', figsize=(8,5))
plt.title("Sales by Category")
plt.ylabel("Total Sales")
plt.show()
```

### 8. Sales Distribution

A histogram is used to understand how sales values are distributed.

```python
sns.histplot(df['Sales'], bins=30)
plt.title("Sales Distribution")
plt.show()
```

 Visualizations

The project includes the following visualizations:

* **Sales by Category – Bar Chart**
* **Sales Distribution – Histogram**

These visualizations make it easier to understand sales patterns and category-wise performance.

Data Preprocessing

The following preprocessing steps are performed:

* Dataset loading
* Dataset inspection
* Date format conversion
* Delivery days calculation
* Category identification
* Missing-value checking

Missing values are checked using:

```python
df.isnull().sum()
```

Project Structure

```text
Superstore-Sales-Data-Visualization/
│
├── samplesuperstore.csv
├── superstore_sales_data_dv_week_1.py
└── README.md
```

 How to Run the Project

1. Download or clone this repository.
2. Make sure Python is installed.
3. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

4. Keep the CSV dataset in the same project folder.
5. Run the Python file:

```bash
python superstore_sales_data_dv_week_1.py
```

 Key Learning Outcomes

Through this project, I learned how to:

* Work with CSV datasets using Pandas.
* Explore and understand real-world data.
* Perform basic data preprocessing.
* Work with date and time data.
* Calculate new columns from existing data.
* Group and analyze data using Pandas.
* Create meaningful visualizations using Matplotlib and Seaborn.
* Understand sales distribution and category-wise sales.

Future Improvements

The project can be further improved by adding:

* Region-wise sales analysis
* Monthly and yearly sales trends
* Profit analysis
* Customer segmentation
* Shipping mode analysis
* Interactive dashboards
* Advanced statistical analysis

Author

M. Rabiyathul Basiriya
