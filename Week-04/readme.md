#  Shopify Stock Data Visualization – Week 04

##  Project Overview

This project is based on **Shopify stock data** and focuses on visualizing stock closing prices over time using Python.

The project uses **Pandas, NumPy, and Matplotlib** to load the dataset, explore the data, and create a line chart showing the Shopify stock price.

##  Objectives

* Load Shopify stock data using Pandas.
* Explore the dataset using the first few records.
* Analyze the `date` and `close` columns.
* Visualize Shopify's closing stock price over time.
* Create a clear line chart using Matplotlib.

##  Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Jupyter Notebook / Google Colab

##  Dataset

The project uses the **Shopify Stock Dataset**.

The dataset is loaded using:

```python
df = pd.read_csv("shopify_stock.csv.xls")
```

### Important Columns

| Column  | Description                |
| ------- | -------------------------- |
| `date`  | Date of the stock record   |
| `close` | Closing price of the stock |

##  Data Exploration

The first few records of the dataset are displayed using Pandas:

```python
print(df.head())
```

This provides an initial view of the Shopify stock data before visualization.

##  Data Visualization

### Shopify Stock Price

A **line plot** is used to visualize the closing stock price based on the date.

```python
plt.plot(df["date"], df["close"])

plt.xlabel("Date")
plt.ylabel("Closing Price")
plt.title("Shopify Stock Price")

plt.show()
```

###  Chart Details

* **Chart Type:** Line Chart
* **X-axis:** Date
* **Y-axis:** Closing Price
* **Title:** Shopify Stock Price

The visualization shows how the Shopify closing price changes across the available dates in the dataset.

##  Project Structure

```text
Shopify-Stock-Data-Visualization/
│
├── shopify_stock.csv.xls
├── Shopify_Stock_Data_DV_Week_04.ipynb
└── README.md
```

##  How to Run the Project

### 1. Install Required Libraries

```bash
pip install pandas numpy matplotlib
```

### 2. Open the Notebook

Open:

```text
Shopify_Stock_Data_DV_Week_04.ipynb
```

using **Jupyter Notebook** or **Google Colab**.

### 3. Add the Dataset

Make sure the Shopify stock dataset is available in the required location.

### 4. Run the Cells

Run the notebook cells to:

1. Import the required libraries.
2. Load the Shopify stock dataset.
3. Display the first few records.
4. Create the Shopify stock price line chart.

##  Learning Outcomes

Through this project, I learned how to:

* Load data using Pandas.
* Explore a dataset using `head()`.
* Work with stock market data.
* Select specific columns for visualization.
* Create line charts using Matplotlib.
* Add axis labels and chart titles.
* Visualize stock price changes over time.
