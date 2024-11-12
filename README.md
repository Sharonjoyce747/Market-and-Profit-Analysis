## Atliq Business Analysis

### Project Overview

This market and profit analysis report provides insights into our dynamic market growth, identifying trends, opportunities and challenges. Recommendations will facilitate informed strategic decisions.

### Data Source
Sales: Sales.csv file, containing detailed information about the company's sales perfomance, (https://codebasics.io/resources/sales-insights-data-analysis-project)

### Tools
- Sql (Data Extraction)
- Powerbi (Power query edition for data transformation, data modelling and report)

### Data Cleaning/Preparation

- Data loading and Inspection
- Handling missing values
- Data cleaning and transforming

### Exploratory Data Analysis

Exploring the sales data to answer key business questions:

1. Revenue Breakdown by Market
2. Profit Margin Analysis
3. Sales Volume by Market
4. Year-over-Year Revenue Trend
5. Key Account Analysis, Top customers' revenue contribution
6. Product Performance Review
7. Geographic Profit Contribution


### Data Analysis
- Using Sql

 1. `SELECT * FROM sales.customers;`
 2. `SELECT * FROM sales.transactions;`
 3. `SELECT * FROM sales.products;`
 4. `SELECT * FROM sales.markets;`
 5. `SELECT * FROM sales.date;`

- Show transactions in 2020 join by date table
6. `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

- Show transactions where currency is US dollars
7. `SELECT * from transactions where currency="USD"`

- Using Powerbi
  
8. `= Table.AddColumn(#"Filtered Rows", "norm_amount", each if [currency] = "USD" or [currency] ="USD#(cr)" then [sales_amount]*75 else [sales_amount], type any)`

### Results/Findings

1. 42.66% revenue drop between Jan 1, 2020, and Jun 1, 2020.
2. 44.24% (₹11,673,543) between Mar 1, 2020, and Jun 1, 2020.
3. Top-Performing Market: Delhi NCR (₹77,732,602, 54.65% revenue share).
4. Lowest-Performing Market: Bhubaneshwar (₹161,571).
5. Market Variance: 48,010.49% difference between highest and lowest.
6. Regional Disparity: 48,010.49% difference between Delhi NCR and Bhubaneshwar.


### Recommendations

1. Analyze Delhi NCR's success: Identify factors driving high revenue.
2. Develop strategies for Bhubaneshwar and underperforming markets.
3. Diversify revenue streams
4. Adjust inventory, marketing, and pricing accordingly.
5. Regularly review market performance.
6. Align resources with high-growth markets.
7. Assess market competition.

### Reference

(https://codebasics.io/resources/sales-insights-data-analysis-project)














