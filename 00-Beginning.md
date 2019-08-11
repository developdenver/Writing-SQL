# Beginning
## Basic SQL Statements
By the end of this section, you will be able to: 
1. Describe the structure of a SQL query 
1. Query a table to retrieve existing data
1. Filter data in a query using basic operators, including: 
    * `SELECT`, `FROM`, `WHERE`, `AND`, `BETWEEN`, `NOT BETWEEN`, `>`, `<`, `=`, `!=`, and `DISTINCT`
1. Explain how to read an entity relationship diagram (ERD)


### Assessment 
* [Daily Challenge 1](https://www.sqlprep.com/sc_dailychallenge/daily-challenge-1/)
    * Note: Use this alternate Challenge Prompt: Show all the information for the `offices` table. 
```sql
SELECT * FROM offices;
``` 
* [Daily Challenge 4](https://www.sqlprep.com/sc_dailychallenge/daily-challenge-4/)

```sql
SELECT  firstname, lastname, jobtitle
FROM employees
WHERE jobtitle ='Sales Rep'
```

* [Daily Challenge 15](https://www.sqlprep.com/sc_dailychallenge/daily-challenge-15) 
```sql
SELECT DISTINCT country FROM customers;
```