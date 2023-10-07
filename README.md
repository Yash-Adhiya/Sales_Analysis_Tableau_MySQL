This Project was done for the real-time database for the company called AtliQ Hardware and for my practice for tableau and SQL for data analysis.  

Performed Data Analysis Using MySql, and a standard Tableau practice such as extracting, transforming, and Load (ETL) data using Tableau. 
Created a Dynamic Dashboard using a tableau that looks like the following: 
![image](https://github.com/Yash-Adhiya/Sales_Analysis_Tableau_MySQL/blob/main/dashboard.png)


Here is the Database Information from MySQL: 
![image](https://github.com/Yash-Adhiya/Sales_Analysis_Tableau_MySQL/blob/main/Database_Info.png)


Data Analysis Using SQL
Show all customer records

```SELECT * FROM customers;```

Show the total number of customers

```SELECT count(*) FROM customers;```

Show transactions for the Chennai market (the market code for Chennai is Mark001

```SELECT * FROM transactions where market_code='Mark001';```

Show distinct product codes that were sold in Chennai

```SELECT distinct product_code FROM transactions where market_code='Mark001';```

Show transactions where the currency is US dollars

```SELECT * from transactions where currency="USD"```

Show transactions in 2020 join by date table

```SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;```

Show total revenue in year 2020,

```SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r" or transactions.currency="USD\r";```

Show total revenue in year 2020, January Month,

```SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");```

Show total revenue in year 2020 in Chennai

```SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";```
