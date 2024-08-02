## Sales Insights Data Analysis Project
This is an interactive sales insight dashboard for a firm build to analyse the data of sales of the firm.
The data is fetched from MySQL server and connected to tableau for making the dashboard interactive and easy to analyse the sales trends.
The data can be analysed yearwise, monthwise, locationwise etc. as demanded by manager of the firm.

### Data Analysis Using SQL

1. Show all customer records

    `SELECT * FROM customers;`

1. Show total number of customers

    `SELECT count(*) FROM customers;`

1. Show transactions for Chennai market (market code for chennai is Mark001

    `SELECT * FROM transactions where market_code='Mark001';`

1. Show distrinct product codes that were sold in chennai

    `SELECT distinct product_code FROM transactions where market_code='Mark001';`

1. Show transactions where currency is US dollars

    `SELECT * from transactions where currency="USD"`

1. Show transactions in 2020 join by date table

    `SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;`

1. Show total revenue in year 2020,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";`
	
1. Show total revenue in year 2020, January Month,

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");`

1. Show total revenue in year 2020 in Chennai

    `SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020
and transactions.market_code="Mark001";`


Image of complete dashboard:
![complete](https://github.com/user-attachments/assets/7fe0a3c0-7dc4-4c79-99c8-afa74cc5dd22)

Image showing data analysis of Delhi:
![delhi](https://github.com/user-attachments/assets/34d97157-7d04-4311-89cd-60917fd6e56d)

Image showing data analysis of January Month:
![jan](https://github.com/user-attachments/assets/d8f5671a-add3-4019-9285-c54dfbc3084b)

Image showing data analysis of year 2018:
![2018](https://github.com/user-attachments/assets/f1ebf62b-6b6b-4ce3-a93e-6483be7c6fd5)









