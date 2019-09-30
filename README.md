## Financial Report

This financial report has two parts, a budget analysis and a retirement analysis. The budget analysis reviews past transactions and evaluates total monthly expenses per category.  The retirement analysis projects future performance to estimate the potential portfolio value using Monte Carlo simulations. 

### Budget Analysis 

The budget analysis includes 90 days of transactions from Plaid's Developer Sandbox. As per the table below, the Transfer Category had the largest spend over the last 90 days and the Travel category had the least spend.   


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

By reviewing transactions per category, the categories with the largest spend did not have the largest number of transactions. The categories with the largest number of transactions are Travel and Food and Drink.  



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

In the retirement analysis, a portfolio made up of 60% stocks represented by ticker SPY and 40% bonds represented by ticker AGG was used to perform Monte Carlo simulations to project portfolio performance at 30 years. An IEX API was used to gather five years of historical closing prices for both SPY and AGG. This data was used to calculate a historical average daily price return and standard deviation that was used as inputs to project future performance by the Monte Carlo Simulations. The Monte Carlo simulation was run 500 times for the 30-year time period. Below is a chart illustrating the cumulative returns from each of the simulations run for the portfolio.

![Chart](/Images/Portfolio_Simulations.png)

The ending cumulative returns from the Monte Carlo simulation produced 90% confidence intervals between 2.56 and 10.61, as shown in the bar chart below. 

![Chart](/Images/confidence_interval.png)

The expected cumulative returns at 30 years was also analyzed by percentile.  The expected cumulative returns were 2.94 at the 10th percentile, 5.10 at the 50th percentile, and 8.88 at the 90th percentile.   Given an initial investment of $20,000, the expected portfolio return in dollars at the 10th percentile was $78,973, at the 50th percentile was $122,015, and at the 90th percentile was $197,657. 

A 4% withdraw rate from the retirement portfolio at the 10th percentile is $3,158, that does not exceed the projected annual income of $6,085 projected annual income from the Plaid analysis and therefore, would not be enough to reach the desired retirement goals. But given a higher initial investment of $50,000, the expected portfolio return in dollars at the 10th percentile is $197,432, at the 50th percentile is $305,038, and at the 90th percentile is $494,144.  A 4% withdraw rate from the retirement portfolio at the 10th percentile is $7,897, and that does exceed the projected annual income helping to achieve the desired retirement savings. 

With an initial investment of $50,000 at the 5th, 50th, and 95th percentiles, the chart below illustrates the cumulative portfolio returns over the life of the investment.

![Chart](/Images/Portfolio_performance_overtime.png)

