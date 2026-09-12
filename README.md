# 📈 Shopify (SHOP) Stock — Exploratory Data Analysis

A complete **Exploratory Data Analysis (EDA)** of Shopify Inc. (`SHOP`) historical stock market data using Python, Pandas, and Matplotlib. This project focuses on understanding stock price movements, trading activity, daily returns, and price volatility through data cleaning, feature engineering, statistical analysis, and visualization.

---

## 🔍 Project Overview

This project performs an end-to-end analysis of Shopify's historical daily stock data.

The analysis covers:

* 📂 Loading and inspecting the raw stock dataset
* 🧹 Cleaning missing, invalid, and duplicate records
* 📅 Converting and organizing date information
* 📊 Generating descriptive statistics
* ⚙️ Creating new financial features
* 📈 Analyzing price movements and trading volume
* 📉 Studying daily return distribution
* 📏 Measuring daily price ranges and return volatility
* 📊 Visualizing important trends using Matplotlib

The objective is to transform raw historical stock data into meaningful insights about **price behavior, trading activity, and market variability**.

---

## 🎯 Objectives

The primary objectives of this project are to:

1. Understand the structure and quality of the Shopify stock dataset.
2. Identify and handle missing or duplicate observations.
3. Prepare the dataset for reliable financial analysis.
4. Create meaningful derived financial indicators.
5. Analyze statistical characteristics of stock prices and returns.
6. Visualize trading volume and price movements over time.
7. Understand the distribution and variability of daily returns.
8. Identify periods of relatively high or low price movement.

---

## 🗂️ Dataset

The analysis uses historical daily stock-market data for **Shopify (SHOP)**.

### Dataset File

```text
SHOP_2015-05-21.csv
```

### Expected Columns

| Column   | Description                          |
| -------- | ------------------------------------ |
| `date`   | Trading date                         |
| `open`   | Opening stock price                  |
| `high`   | Highest price during the trading day |
| `low`    | Lowest price during the trading day  |
| `close`  | Closing stock price                  |
| `volume` | Number of shares traded              |

The dataset contains historical observations that allow us to analyze Shopify's stock-price behavior across different trading periods.

---

## 🛠️ Technologies Used

| Technology          | Purpose                                              |
| ------------------- | ---------------------------------------------------- |
| 🐍 Python           | Data analysis and programming                        |
| 🐼 Pandas           | Data loading, cleaning, transformation, and analysis |
| 📊 Matplotlib       | Data visualization                                   |
| 📓 Jupyter Notebook | Interactive analysis                                 |
| ☁️ Google Colab     | Optional cloud-based execution environment           |

---

## ⚙️ Analysis Workflow

### 1. 📥 Data Loading

The CSV file is loaded into a Pandas DataFrame.

The initial inspection includes:

* Number of rows and columns
* Column names
* Data types
* Sample records
* Missing-value counts
* Basic dataset information

This provides an initial understanding of the dataset before performing any transformations.

---

### 2. 🔎 Data Inspection

The dataset is examined to identify potential quality issues.

The following checks are performed:

* Dataset dimensions
* Data types
* Null values
* Duplicate records
* Invalid date values
* Missing financial values

This step ensures that problems in the raw dataset are identified before analysis.

---

### 3. 🧹 Data Cleaning

The following cleaning operations are performed:

* Remove duplicate rows
* Convert `date` into a proper datetime format
* Identify invalid dates
* Handle missing values
* Remove records containing invalid or incomplete financial data
* Sort observations chronologically
* Set `date` as the DataFrame index

After cleaning, the resulting dataset is suitable for further financial analysis.

---

## ⚙️ Feature Engineering

Additional financial indicators are created from the original columns.

### 1. Daily Price Change

Measures the difference between the closing and opening price.

```text
Daily_Price_Change = close - open
```

A positive value indicates that the stock closed above its opening price, while a negative value indicates that it closed below its opening price.

---

### 2. Daily Return (%)

Measures the percentage change between the opening and closing price of the same trading day.

```text
Daily_Return_% = ((close - open) / open) × 100
```

This provides a normalized measure of the stock's daily price movement.

* Positive return → price increased during the day
* Negative return → price decreased during the day
* Return near zero → relatively small intraday movement

---

### 3. Price Range

Measures the difference between the highest and lowest price recorded during a trading day.

```text
Price_Range = high - low
```

A larger price range indicates greater intraday price movement.

---

## 📊 Statistical Analysis

Descriptive statistics are calculated for the numerical variables.

The analysis includes:

* Count
* Mean
* Standard deviation
* Minimum
* 25th percentile
* Median
* 75th percentile
* Maximum

The statistical summary helps identify the central tendency, spread, and extreme values within the dataset.

### Return Variability

The project also calculates:

* **Variance of daily returns**
* **Standard deviation of daily returns**

These measures help quantify how widely daily returns vary around their average.

A higher standard deviation indicates greater variability in daily returns.

---

## 📈 Data Visualization

The project uses Matplotlib to create visual representations of important characteristics of Shopify's stock data.

### 📊 1. Trading Volume Trend

A time-series visualization is used to examine trading volume across the historical period.

This helps identify:

* Periods of unusually high trading activity
* Changes in market participation
* Significant volume spikes
* Long-term changes in trading activity

---

### 📉 2. Daily Return Distribution

A histogram is used to visualize the distribution of daily returns.

This helps analyze:

* Typical daily return behavior
* Concentration around the center
* Positive and negative return frequencies
* Potential extreme return observations
* Overall variability of daily returns

---

### 📏 3. Price Range Trend

A time-series plot shows the daily difference between the highest and lowest stock prices.

This provides an indication of **intraday price movement** and helps identify periods when Shopify experienced larger price fluctuations.

---

## 📊 Key Outputs

After running the notebook, the project produces:

### Console Outputs

* Dataset shape
* Data types
* Missing-value summary
* Duplicate-record information
* Descriptive statistics
* Daily return variance
* Daily return standard deviation

### Visual Outputs

* 📈 Trading volume trend
* 📊 Daily return distribution
* 📉 Price range trend

---

## 📁 Project Structure

```text
EDAtask3/
│
├── 📓 EDAtask3.ipynb
├── 📄 SHOP_2015-05-21.csv
└── 📄 README.md
```

---

## 📦 Installation

Install the required Python libraries using:

```bash
pip install pandas matplotlib
```

If you are using Google Colab, these libraries are generally available by default.

---

## ▶️ How to Run

### Option 1 — Google Colab

1. Open the notebook in Google Colab.
2. Upload the Shopify CSV dataset.
3. Update the dataset path if required.
4. Run the notebook cells sequentially.
5. Review the generated statistics and visualizations.

### Option 2 — Jupyter Notebook

Clone or download the project and place the dataset in the appropriate directory.

Then start Jupyter:

```bash
jupyter notebook
```

Open:

```text
EDAtask3.ipynb
```

and execute the cells sequentially.

---

## 📌 Dataset Path

The original notebook is configured for a Google Colab environment and may contain a path similar to:

```text
/content/SHOP_2015-05-21_2025-03-16 - SHOP_2015-05-21_2025-03-16 (1).csv.xls
```

If the notebook is executed locally or with a differently named dataset, update the file path accordingly.

> **Note:** Although the file extension shown above is `.xls`, the project expects the data to be read as CSV-formatted data. Make sure the file format and Pandas loading method match the actual dataset.

---

## 📷 Sample Visualizations

Add your generated charts below to showcase the results of the analysis.

### Trading Volume

```html
<img width="1326" height="603" alt="Trading Volume Trend" src="YOUR_IMAGE_URL_HERE" />
```

### Daily Return Distribution

```html
<img width="1221" height="606" alt="Daily Return Distribution" src="YOUR_IMAGE_URL_HERE" />
```

### Price Range Trend

```html
<img width="1330" height="611" alt="Price Range Trend" src="YOUR_IMAGE_URL_HERE" />
```

---

## 💡 Insights

The analysis can be used to understand several characteristics of Shopify's historical stock behavior:

* How trading volume changed over time
* How frequently positive and negative daily price movements occurred
* The typical magnitude of daily price changes
* Periods of increased intraday price movement
* The overall variability of daily returns
* The distribution of daily stock returns

> **Important:** This project is an exploratory analysis of historical data and is **not intended to provide investment advice or predict future stock prices**.

---

## 🚀 Possible Future Improvements

The project can be extended with additional financial analysis, including:

* 📈 Moving averages such as 20-day, 50-day, and 200-day averages
* 📊 Cumulative returns
* 📉 Rolling volatility
* 📈 OHLC/candlestick charts
* 🔗 Correlation analysis between stock variables
* 📅 Monthly and yearly performance analysis
* 📊 Comparison with market indices
* 📉 Drawdown analysis
* 🤖 Basic time-series forecasting
* 📊 Interactive visualizations using Plotly

---

## 🎓 Learning Outcomes

Through this project, the following practical data-analysis skills are demonstrated:

* Working with real-world financial datasets
* Data cleaning and preprocessing
* Handling missing and duplicate data
* Date/time data manipulation
* Feature engineering
* Descriptive statistical analysis
* Financial-return calculations
* Data visualization
* Time-series exploratory analysis
* Communicating analytical findings

---

## 📄 License

This project is intended for educational and analytical purposes.

If distributing the project publicly, add an appropriate open-source license such as the **MIT License**.

---

## 👤 Author

**Shopify Stock EDA — Task 3**

Built as part of a Python/Data Analysis exploratory data analysis project.

---

⭐ **If you found this project useful, consider giving the repository a star!**
