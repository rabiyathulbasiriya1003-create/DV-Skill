#  Superstore Sales Data Visualization – Week 02

##  Project Overview

This project focuses on analyzing the **Superstore Sales Dataset** using Python and creating different data visualizations.

The project explores **sales, profit, category performance, discounts, and relationships between numerical variables** using charts and plots.

##  Objectives

* Analyze sales and profit across different categories.
* Compare category-wise performance using bar plots.
* Understand profit distribution using box plots.
* Identify profit variation and outliers.
* Analyze the relationship between discount and profit.
* Understand relationships between numerical variables using a correlation heatmap.

##  Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Google Colab

##  Dataset

The project uses the **Sample Superstore Dataset** containing information related to sales, profit, categories, discounts, orders, and other business attributes.

The dataset is loaded using Pandas.

```python
df = pd.read_csv("samplesuperstore - samplesuperstore.csv")
```

## Data Preprocessing

The following basic preprocessing steps are performed:

* Load the dataset.
* Explore the dataset using `head()`, `info()`, and `describe()`.
* Convert `Order Date` and `Ship Date` into datetime format.
* Calculate `Delivery Days`.
* Check available categories.
* Check for missing values.

```python
df['Order Date'] = pd.to_datetime(df['Order Date'])
df['Ship Date'] = pd.to_datetime(df['Ship Date'])

df['Delivery Days'] = (df['Ship Date'] - df['Order Date']).dt.days
```

## Visualizations

### 1. Bar Plot

Bar plots are used to compare **sales and profit across categories**.

#### Visualizations:

* Profit by Category
* Sales Distribution by Category

Example:

```python
sns.barplot(
    data=df,
    x="Category",
    y="Profit"
)
```

This helps compare the performance of different product categories.

##  2. Box Plot

Box plots are used to understand:

* Data distribution
* Median value
* Outliers
* Variation

The project includes:

* Profit Distribution
* Profit Variation Across Categories

Example:

```python
sns.boxplot(
    data=df,
    x="Category",
    y="Profit"
)
```

This helps identify differences in profit and possible outliers between categories.

##  3. Discount vs Profit Analysis

A scatter plot is used to analyze the relationship between **Discount and Profit**.

```python
sns.scatterplot(
    data=df,
    x="Discount",
    y="Profit"
)
```

### Question Explored

**At what discount level does profit start decreasing?**

This visualization helps examine how changes in discount are associated with profit.

##  4. Correlation Heatmap

Correlation shows the relationship between numerical variables.

The numerical columns are selected using:

```python
numeric_df = df.select_dtypes(
    include="number"
)

corr = numeric_df.corr()
```

A heatmap is then created to visualize the correlations.

```python
sns.heatmap(
    corr,
    annot=True
)
```

The correlation heatmap makes it easier to identify relationships between numerical variables.

## Visualizations Included

| Visualization       | Purpose                                              |
| ------------------- | ---------------------------------------------------- |
| Bar Plot            | Compare sales and profit                             |
| Box Plot            | Analyze distribution, median, variation and outliers |
| Scatter Plot        | Analyze Discount vs Profit                           |
| Correlation Heatmap | Understand relationships between numerical variables |

## Project Structure

```text
Superstore-Sales-Data-Visualization/
│
├── samplesuperstore - samplesuperstore.csv
├── superstore_sales_data_dv_week_02.py
└── README.md
```

## How to Run

### Step 1: Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn
```

### Step 2: Keep the Dataset

Place the CSV file in the project folder.

### Step 3: Run the Python File

```bash
python superstore_sales_data_dv_week_02.py
```

You can also run the project using **Google Colab**.

## Learning Outcomes

Through this project, I learned how to:

* Perform basic data analysis using Pandas.
* Create bar plots using Seaborn.
* Analyze distributions using box plots.
* Identify outliers and variation.
* Study relationships using scatter plots.
* Analyze correlations between numerical variables.
* Create and interpret a correlation heatmap.
* Use data visualization to understand business data.
