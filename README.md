# Sales Insights Data Analysis Project
### Problem statement- A computer hardware business is facing challenges in dynamically changing market, their sales profits are going down. Sales director decides to invest in data analysis project and he would want a Tableau dashboard built that can give him real time sales insights to unlock the insights that are not visible before the sales team for decision support and automate them to reduce the manual time spent in data gathering.

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for say- Mumbai market (market code is Mark002)

    `SELECT * FROM transactions where market_code='Mark002';`

1. Show distrinct product codes that were sold in Mumbai

    `SELECT distinct product_code FROM transactions where market_code='Mark002';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Mumbai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark002";`
