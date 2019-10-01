## Financial Report

The financial report has two parts, a budget analysis and a retirement analysis. The budget analysis reviews past transactions and evaluates total monthly expenses per category.  The retirement analysis projects future performance to estimate the potential portfolio value using Monte Carlo simulations. 

### Budget Analysis 

The budget analysis includes 90 days of transactions from Plaid's Developer Sandbox. 

As per the table below, the Transfer category had the largest spend over the last 90 days and the Travel category had the least spend.   


| Category       |   Amount |
|:---------------|---------:|
| Transfer       | 20537.34 |
| Payment        |  6310.50 |
| Food and Drink |  3317.19 |
| Shops          |  1500.00 |
| Recreation     |   235.50 |
| Travel         |    35.19 |


The pie chart below provides a visual comparison of spend per category. 

![Pie Chart](/Images/PieChart_BudgetAnalysis.png)

Below is a table of transactions per category, the categories with the largest spend did not have the largest number of transactions. Dissecting and grouping the data by various metrics can provide a bigger picture into spending habits that can be more useful in setting budget goals. 

| Category       |   Number of Transactions |
|:---------------|-------------------------:|
| Food and Drink |                    15.00 |
| Payment        |                     6.00 |
| Recreation     |                     3.00 |
| Shops          |                     3.00 |
| Transfer       |                     9.00 |
| Travel         |                    12.00 |


![Bar_Chart](/Images/NumberofTrxns_budgetAnalysis.png)

Total expenses were also divided per month. As shown in the data, expenses have been consistent each month.

|   Date(Month) |   Expenses per Month |
|--------------:|---------------------:|
|             7 |             10645.24 |
|             8 |             10645.24 |
|             9 |             10645.24 |


![Bar Chart](/Images/BarChart_BudgetAnalysis.png)


### Retirement Analysis 

In the retirement analysis, a portfolio made up of 60% stocks represented by ticker SPY and 40% bonds represented by ticker AGG was used to perform Monte Carlo simulations to project portfolio performance at 30 years. An IEX API was used to gather five years of historical closing prices for both SPY and AGG. This data was used to calculate a historical average daily price return and standard deviation that was used as inputs for the analysis. The Monte Carlo simulation was run 500 times for a 30-year time period. Below is a chart illustrating the cumulative returns from each of the simulations run for the portfolio.

![Chart](/Images/Portfolio_Simulations.png)

The ending cumulative returns from the Monte Carlo simulation produced 90% confidence intervals between 2.42 and 11.04, as shown in the bar chart below. There is a 90% certainty that the portfolio's mean return falls between this range. 

![Chart](/Images/confidence_interval.png)

To better understand the distribution of cumulative returns the data was divided by percentiles. The expected cumulative returns were 3.06 at the 10th percentile, 5.23 at the 50th percentile, and 9.13 at the 90th percentile. Applying an initial investment of $20,000, the expected portfolio return in dollars at the 10th percentile is $81,333.33, at the 50th percentile is $124,738.32, and at the 90th percentile is $202,687.83. 

A 4% withdraw rate from the retirement portfolio at the 10th percentile is $3,253.33. This falls below the projected annual income from the Plaid analysis of $6,085, therfore, would not be enough to reach the desired retirement goals. But given a higher initial investment of $50,000, the expected portfolio return in dollars at the 10th percentile is $203,333.33 at the 50th percentile is $311,845.80, and at the 90th percentile is $366,3408.94. A 4% withdraw rate from the retirement portfolio at the 10th percentile is $8,133.33, and that does exceed the projected annual income helping to achieve the desired retirement savings. 

In summary, given a balanced portfolio of stocks and bonds over a 30 year time period, an initial investment of $50,000 provides a greater likelihood of reaching the retirement income stream goals. 

The chart below illustrates the cumulative portfolio returns at the 5th, 50th, and 95th percentiles and helps to provide a visual of the portfolio's potential value at each year over the course of the 30 years to retirement. 

![Chart](/Images/Portfolio_performance_overtime.png)

