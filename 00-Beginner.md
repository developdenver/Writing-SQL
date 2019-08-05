# Beginner
## Basic SQL Statements
By the end of this section, you will be able to: 
1. Query a table to retrieve existing data
1. Filter data in a query using basic operators, including: 
    * `SELECT`, `FROM`, `WHERE`, AND, `DISTINCT`


### Assessment Solutions
* [Daily Challenge 4](https://www.sqlprep.com/sc_dailychallenge/daily-challenge-4/)

```sql
SELECT  firstname, lastname, jobtitle
FROM employees
WHERE jobtitle ='Sales Rep'
```

* [Daily Challenge 1](https://www.sqlprep.com/sc_dailychallenge/daily-challenge-1/)

```sql
SELECT customerName
FROM customers c
WHERE EXISTS 
    (SELECT 1
    FROM payments p
    WHERE p.customerNumber = c.customerNumber
        AND amount > 100000)
```

* [Daily Challenge 15](https://www.sqlprep.com/sc_dailychallenge/daily-challenge-15) 

```sql
SELECT DISTINCT country
FROM customers
```
