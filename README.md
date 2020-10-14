# A Whale Off the Port(folio)

To use Pandas to create a tool (an analysis notebook) that analyzes and visualizes the major metrics of the portfolios across all of these areas, and determine which portfolio outperformed the others. 

The historical daily returns of several portfolios: some from the firm's algorithmic portfolios, some that represent the portfolios of famous "whale" investors like Warren Buffett, and some from the big hedge and mutual funds. 

Use this analysis to create a custom portfolio of stocks and compare its performance to that of the other portfolios, as well as the larger market (S&P 500).

Will be accomplishing three main tasks:

1. [Read in and Wrangle Returns Data](#Prepare-the-Data)
2. [Determine Success of Each Portfolio](#Conduct-Quantitative-Analysis)
3. [Choose and Evaluate a Custom Portfolio](#Create-Custom-Portfolio)

### Prepare the Data

First, read and clean several CSV files for analysis. The CSV files include whale portfolio returns, algorithmic trading portfolio returns, and S&P 500 historical prices. Use the [Whale Analysis Starter Code](Starter_Code/whale_analysis.ipynb) to complete the following steps:

1. Use Pandas to read in each of the [CSV files](Starter_Code/Resources) as a DataFrame. Be sure to convert the dates to a `DateTimeIndex`.

2. Detect and remove null values.

3. Remove dollar signs from the numeric values and convert the data types as needed.

4. The whale portfolios and algorithmic portfolio CSV files contain daily returns, but the S&P 500 CSV file contains closing prices. Convert the S&P 500 closing prices to daily returns.

5. Join `Whale Returns`, `Algorithmic Returns`, and the `S&P 500 Returns` into a single DataFrame with columns for each portfolio's returns.

  ![returns-dataframe.png](Images/returns-dataframe.png)

### Conduct Quantitative Analysis

Analyze the data to see if any of the portfolios outperform the stock market (i.e., the S&P 500).

#### Performance Analysis

1. Calculate and plot cumulative returns. Does any portfolio outperform the S&P 500?

#### Risk Analysis

1. Create a box plot for each of the returns. Which box has the largest spread? Which has the smallest spread?

2. Calculate the standard deviation for each portfolio. Which portfolios are riskier than the S&P 500?

3. Calculate the annualized standard deviation (252 trading days).

#### Rolling Statistics

1. Plot the rolling standard deviation of the various portfolios along with the rolling standard deviation of the S&P 500 using a 21 day rolling window. Does the risk increase for each of the portfolios at the same time risk increases in the S&P?

2. Construct a correlation table for the algorithmic, whale, and S&P 500 returns. Which returns most closely mimic the S&P?

3. Choose one portfolio and plot a rolling beta between that portfolio's returns and S&P 500 returns. Does the portfolio seem sensitive to movements in the S&P 500?

4. An alternative way to calculate a rolling window is to take the exponentially weighted moving average. This is like a moving window average, but it assigns greater importance to more recent observations. Try calculating the ewm with a 21 day half-life.

### Plot Sharpe Ratios

Investment managers and their institutional investors look at the return-to-risk ratio, not just the returns. (After all, if you have two portfolios that each offer a 10% return, yet one is lower risk, you would invest in the lower-risk portfolio, right?)

1. Using the daily returns, calculate and visualize the Sharpe ratios using a bar plot.

2. Determine whether the algorithmic strategies outperform both the market (S&P 500) and the whales portfolios.

### Create Custom Portfolio

Doing the following:

1. Visit [Google Sheets](https://docs.google.com/spreadsheets/) and use the in-built Google Finance function to choose 3-5 stocks for your own portfolio.

2. Download the data as CSV files and calculate the portfolio returns.

3. Calculate the returns for each stock.

4. Using those returns, calculate the weighted returns for your entire portfolio assuming an equal number of shares for each stock.

5. Add the portfolio returns to the DataFrame with the other portfolios and rerun the analysis. 


## The analysis include the following:

- Using all portfolios:
  - The annualized standard deviation (252 trading days) for all portfolios.
  - The plotted rolling standard deviation using a 21 trading day window for all portfolios.
  - The calculated annualized Sharpe Ratios and the accompanying bar plot visualization.
  - A correlation table.
- Using the custom portfolio and one other of the choosing:
  - The plotted beta. 

---

## Resources

[Pandas API Docs](https://pandas.pydata.org/pandas-docs/stable/reference/index.html)

---
