# Exploratory-Data-Analysis-for-Financial-Data

In this jupyter notebook, I have performed Exploratory Data Analysis on Financial data.

I have used stocks data of a company (named any XYZ) which contains the opening, closing, high and low stock prices per day.

Also performed data filtering and built some visualizations from the dataset.

---

## Contents

  - Importing the required libraries
    - pandas : pandas is a fast, powerful, flexible and easy to use open source data analysis and manipulation tool,
built on top of the Python programming language.
    - numpy : NumPy is a Python library that provides a simple yet powerful data structure: the n-dimensional array.
    - matplotlib : Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python.
    - seaborn : Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.
    
  - Knowing the dataset
  
  Analyzing historical price data is an important way to try to make future predictions. We will be using a dataset of stock data for the company XYZ. This data includes opening, closing, high, low prices and stocks traded per day.
  
  - Importing and Loading the dataset
    - The dataset is available in the repository.
    - Dataset: `HistoricalQuotes.csv`
        
  - Exploratory Data Analysis
    - df.shape
    - df.info()
    - df.head()
    - df.isna().sum()
    - df.drop() -
    - Changing the dtype of the `open`,`close`,`high` and `low` columns to `float`
      - df.open = df.open.astype(float)
    - Changing the dtype of the `volume` column to `int`
      - df.volume = pd.to_numeric(df['volume']).astype(int)
    - df.describe() - Summary statistics for all numeric columns (default)
      - df.describe(include='int') : Summary statistics only for columns whose type is "int"
    - Percentiles
      - df.describe(percentiles=[.3, .5, .9]) : Summary statistics for all numeric columns with percentiles .3, .5 and .9
  
  - Filtering Data 
    - Creating different dataframes using masks.
  
  - Filtering Data with dates
    - Selecting date from date ranges
    - Importing `datetime` package.
    - Creating mask of historical dates.
    
  - Data Visualizations
    - Line Plot showing Daily High Prices
    - Histogram of High Prices
    - Line plot of Volume over time
    - Daily Volume Frequency distribution
    - Filtering & Plotting data
      - Filtering data of year 2016 from the dataset and then plotting it on a line plot over time
      - `df.loc['2016'].plot(y='low'); plt.show()`
