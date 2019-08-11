# Learning Objectives
## Aliases, Joins, Functions and Operators
By the end of this section, you will be able to:
1. Rename a column and table using an alias 
1. Join tables to retrieve data across a database
1. Display data using the arithmetic operators `+`, `-`, `*` `/ ` and `%`
1. Display data using the aggregate functions `COUNT`, `MIN`, `MAX` and `AVG`
1. Filter aggregated data using `HAVING` and `GROUP BY`
1. Change the display of data using `NULL` and `CASE`

### Prerequisites
You can complete the 3 assessment items for the [Beginning Workshop](./00-Beginning.md).

### Assessment 
* [Daily Challenge 5](https://www.sqlprep.com/sc_dailychallenge/daily-challenge-5/)
```sql
select distinct e.firstName
    ,e.email
from products p
join orderdetails od on p.productCode=od.productCode
join orders o on od.orderNumber=o.orderNumber
join customers c on o.customerNumber=c.customerNumber
join employees e on c.salesRepEmployeeNumber=e.employeeNumber
where p.productName like '%Harley%';
```

* [Daily Challenge 7](https://www.sqlprep.com/sc_dailychallenge/daily-challenge-7/)
```sql
SELECT customerName
, MIN(orderDate) AS first_order
, MAX(orderDate) AS last_order
FROM customers AS c 
LEFT JOIN orders AS o
ON c.customerNumber = o.customerNumber
GROUP BY customerName;
```

* [Daily Challenge 9](https://www.sqlprep.com/sc_dailychallenge/daily-challenge-9/)
```sql
SELECT l.productLine, count(*) FROM productlines l
JOIN products p ON l.productLine = p.productLine
GROUP BY l.productLine
HAVING count(*) > 20;
```

* [Daily Challenge 10](https://www.sqlprep.com/sc_dailychallenge/daily-challenge-10/)
```sql
select customerNumber
    , SUM(CASE WHEN status = 'shipped' THEN 1 ELSE 0 END) AS 'shipped'
    , SUM(CASE WHEN status = 'in process' THEN 1 ELSE 0 END) AS 'in process'
    , SUM(CASE WHEN status = 'cancelled' THEN 1 ELSE 0 END) AS 'cancelled'
    , SUM(CASE WHEN status = 'disputed' THEN 1 ELSE 0 END) AS 'disputed'
    , SUM(CASE WHEN status = 'resolved' THEN 1 ELSE 0 END) AS 'resolved'
    , SUM(CASE WHEN status = 'on hold' THEN 1 ELSE 0 END) AS 'on hold'
FROM orders
GROUP BY customerNumber;
```


 
