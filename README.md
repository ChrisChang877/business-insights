# business-insights

Link of Document : https://drive.google.com/file/d/1GwIbxsZynURdtSG8T8vz1FTVgFcEHKmG/view?usp=sharing

Finance View
<img width="1004" alt="f7c3f73f5195b398f20a2abc83ba901" src="https://user-images.githubusercontent.com/103533857/232359392-4851ae44-1cf9-4662-97d4-412927697c36.png">

Sales View
<img width="1002" alt="012ffc773e31024bb724eeeb37015dd" src="https://user-images.githubusercontent.com/103533857/232359424-6392846f-424b-4c3b-a1bd-6c822c4aa804.png">

Marketing View
<img width="1003" alt="9f3e1091ef5bcef9afc72096226d3da" src="https://user-images.githubusercontent.com/103533857/232359460-42f9f0f8-eb8f-4bb2-9733-76901f11ce3d.png">

Supply Chain View
<img width="1003" alt="a25f9bccf876e3387ecf929fa611bdf" src="https://user-images.githubusercontent.com/103533857/232359486-7ce4abfa-16b8-410b-a525-30f24e89cda0.png">


Executive View
<img width="1000" alt="6f6ce4b6f79284f2d0d39f453d8abc0" src="https://user-images.githubusercontent.com/103533857/232359502-674cf34e-773e-41da-b8b5-56421cea03f5.png">


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
