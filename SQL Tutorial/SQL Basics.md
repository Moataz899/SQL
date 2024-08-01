# The Topics

- [The Topics](#the-topics)
  - [What is a SQL?](#what-is-a-sql)
  - [What Can SQL do?](#what-can-sql-do)
  - [Semicolon after SQL Statements?](#semicolon-after-sql-statements)
  - [Some of The Most Important SQL Commands](#some-of-the-most-important-sql-commands)
  - [SQL SELECT Statement](#sql-select-statement)
  - [The SQL WHERE Clause](#the-sql-where-clause)
  - [Operators in The WHERE Clause](#operators-in-the-where-clause)
  - [The SQL ORDER BY](#the-sql-order-by)
  - [The SQL AND Operator](#the-sql-and-operator)
  - [The SQL OR Operator](#the-sql-or-operator)
  - [Combining AND and OR](#combining-and-and-or)
  - [SQL NOT Operator](#sql-not-operator)
  - [The SQL INSERT INTO Statement](#the-sql-insert-into-statement)
  - [Insert Multiple Rows](#insert-multiple-rows)
  - [SQL NULL Values](#sql-null-values)
  - [The IS NOT NULL Operator](#the-is-not-null-operator)
  - [The SQL UPDATE Statement](#the-sql-update-statement)
  - [The SQL DELETE Statement](#the-sql-delete-statement)
  - [Delete a Table](#delete-a-table)
  - [The SQL SELECT TOP Clause](#the-sql-select-top-clause)
  - [SQL Aggregate Functions](#sql-aggregate-functions)
    - [The most commonly used SQL aggregate functions are:](#the-most-commonly-used-sql-aggregate-functions-are)
  - [The SQL MIN() and MAX() Functions](#the-sql-min-and-max-functions)
  - [The SQL COUNT() Function](#the-sql-count-function)
  - [The SQL SUM() Function](#the-sql-sum-function)
  - [The SQL AVG() Function](#the-sql-avg-function)
  - [The SQL LIKE Operator](#the-sql-like-operator)
    - [There are two wildcards often used in conjunction with the `LIKE` operator:](#there-are-two-wildcards-often-used-in-conjunction-with-the-like-operator)
  - [SQL Wildcard Characters](#sql-wildcard-characters)
  - [The SQL IN Operator](#the-sql-in-operator)
  - [The SQL BETWEEN Operator](#the-sql-between-operator)
  - [SQL Aliases](#sql-aliases)


## What is a SQL?
*SQL stands for Structured Query Language.*
*SQL lets you access and manipulate databases*
*SQL became a standard of the American National Standards Institute (ANSI) in 1986, and of the International Organization for Standardization (ISO) in 1987*

## What Can SQL do?

*SQL can execute queries against a database
SQL can retrieve data from a database
SQL can insert records in a database
SQL can update records in a database
SQL can delete records from a database
SQL can create new databases
SQL can create new tables in a database
SQL can create stored procedures in a database
SQL can create views in a database
SQL can set permissions on tables, procedures, and views*

## Semicolon after SQL Statements?
*Some database systems require a semicolon at the end of each SQL statement.*

*Semicolon is the standard way to separate each SQL statement in database systems that allow more than one SQL statement to be executed in the same call to the server.*

*In this tutorial, we will use semicolon at the end of each SQL statement.*

```sql
Keep in Mind That...

SQL keywords are NOT case sensitive: select is the same as SELECT
```
## Some of The Most Important SQL Commands

***`SELECT`** - extracts data from a database*

***`UPDATET`**  - updates data in a database*

***`DELETET`**  - deletes data from a database*

***`INSERT INTO T`** - inserts new data into a database*

***`CREATE DATABASET`**  - creates a new database*

***`ALTER DATABASET`**  - modifies a database*

***`CREATE TABLET`**  - creates a new table*

***`ALTER TABLET`**  - modifies a table*

***`DROP TABLET`**  - deletes a table*

***`CREATE INDEXT`**  - creates an index (search key)*

***`DROP INDEXT`**  - deletes an index*

## SQL SELECT Statement
*The *`SELECT`* statement is used to select data from a database.*
* Example
```SQL
SELECT CustomerName, City FROM Customers;
```

*The SELECT *` * `* statement is used to Return all the columns from the table*
* Example
```SQL
SELECT * FROM Customers;
```

*The *`SELECT DISTINCT`* statement is used to return only distinct (different) values.*
* Example
```SQL
SELECT DISTINCT Country FROM Customers;
```

*By using the *`DISTINCT`* keyword in a function called *`COUNT`*, we can return the number of different countries.


* Example
```SQL
SELECT COUNT(DISTINCT Country) FROM Customers;
```

## The SQL WHERE Clause
*The *`WHERE`* clause is used to filter records.*
*It is used to extract only those records that fulfill a specified condition.*

* Example
```SQL
SELECT * FROM Customers
WHERE Country='Mexico';
```
## Operators in The WHERE Clause
* Examples

| Operator | Description                       | Example                  |
|----------|-----------------------------------|--------------------------|
| `=`        | Equal                             | `SELECT * FROM table WHERE column = 10;` |
| `>`        | Greater than                      | `SELECT * FROM table WHERE column > 10;` |
| `<`        | Less than                         | `SELECT * FROM table WHERE column < 10;` |
| `>=`       | Greater than or equal             | `SELECT * FROM table WHERE column >= 10;` |
| `<=`       | Less than or equal                | `SELECT * FROM table WHERE column <= 10;` |
| `<>`       | Not equal (or `!=` in some SQL)   | `SELECT * FROM table WHERE column <> 10;` |
| `BETWEEN`  | Between a certain range           | `SELECT * FROM table WHERE column BETWEEN 10 AND 20;` |
| `LIKE`     | Search for a pattern              | `SELECT * FROM table WHERE column LIKE 'A%';` |
| `IN`       | Specify multiple possible values  | `SELECT * FROM table WHERE column IN (10, 20, 30);` |

## The SQL ORDER BY

*The *`ORDER BY`* keyword is used to sort the result-set in ascending or descending order.*

* Example
```SQL
SELECT * FROM Products
ORDER BY Price;
```
*The *`ORDER BY`* keyword sorts the records in ascending order by default. To sort the records in descending order, use the *`DESC`* keyword.*

* Example
```SQL
SELECT * FROM Products
ORDER BY Price DESC;
```



## The SQL AND Operator

*The *`AND`* operator is used to combine two or more conditions in a `WHERE`*

* Example
```SQL
SELECT *
FROM Customers
WHERE Country = 'Spain' AND CustomerName LIKE 'G%';
```
* The `AND` operator displays a record if all the conditions are TRUE.

* The `OR` operator displays a record if any of the conditions are TRUE.

## The SQL OR Operator

*The `OR` operator is used to combine two or more conditions in a `WHERE` clause*

* Example
```SQL
SELECT *
FROM Customers
WHERE Country = 'Germany' OR Country = 'Spain';
```

## Combining AND and OR

*The `AND` and `OR` operators can be combined to create more complex conditions.*

* Example
```SQL
SELECT * FROM Customers
WHERE Country = 'Spain' AND (CustomerName LIKE 'G%' OR CustomerName LIKE 'R%');
```

## SQL NOT Operator
*The `NOT` operator is used to negate a condition, also called the negative result.*

* Example
```SQL
SELECT * FROM Customers
WHERE NOT Country = 'Spain';
```
## The SQL INSERT INTO Statement

*The `INSERT INTO` statement is used to add new records to a database table.*

* Example
```SQL
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES ('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway');
```

## Insert Multiple Rows
*The `INSERT INTO` statement can be used to insert multiple rows at once.*

* Example
```SQL
INSERT INTO Customers (CustomerName, ContactName, Address, City, PostalCode, Country)
VALUES
('Cardinal', 'Tom B. Erichsen', 'Skagen 21', 'Stavanger', '4006', 'Norway'),
('Greasy Burger', 'Per Olsen', 'Gateveien 15', 'Sandnes', '4306', 'Norway'),
('Tasty Tee', 'Finn Egan', 'Streetroad 19B', 'Liverpool', 'L1 0AA', 'UK');
```

## SQL NULL Values
*In SQL, `NULL` is a special value that represents an unknown or missing value.*

* Example
```SQL
SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NULL;
```

## The IS NOT NULL Operator
*The `IS NOT NULL` operator is used to select records where the specified field is not NULL*

* Example
```SQL
SELECT CustomerName, ContactName, Address
FROM Customers
WHERE Address IS NOT NULL;
```

## The SQL UPDATE Statement
*The `UPDATE` statement is used to modify existing records in a database table.*

* Example
```SQL
UPDATE Customers
SET ContactName = 'Moataz Dahy', City= 'Cairo'
WHERE CustomerID = 1;
```

## The SQL DELETE Statement

*The `DELETE` statement is used to delete existing records in a database table.*

* Example
```SQL
DELETE FROM Customers WHERE CustomerName='Moataz Dahy';
```

## Delete a Table

*The `DROP TABLE` statement is used to delete a table from a database.*

* Example
```SQL
DROP TABLE Customers;
```


## The SQL SELECT TOP Clause
*The `SELECT TOP` clause is used to select the top n number of records from a database.*

*The `SELECT TOP` clause is useful on large tables with thousands of records. Returning a large number of records can impact performance.*

* Example
```SQL
SELECT TOP 3 * FROM Customers;
```



## SQL Aggregate Functions
*SQL `aggregate functions` are used to perform calculations on a set of values and return a single value.*

*`Aggregate functions` are often used with the `GROUP BY` clause of the `SELECT` statement. The `GROUP BY` clause splits the result-set into groups of values and the aggregate function can be used to return a single value for each group.*

### The most commonly used SQL aggregate functions are:
* `MAX()`: Returns the maximum value in a set of values.
* `MIN()`: Returns the minimum value in a set of values.
* `AVG()`: Returns the average value in a set of values.
* `SUM()`: Returns the total sum of a set of values.
* `COUNT()`: Returns the number of rows in a set of values.

## The SQL MIN() and MAX() Functions
*The `MIN()` and `MAX()` functions are used to find the smallest and largest values of the selected column.*

* Example
```SQL
SELECT MAX(Age)
FROM Employees;
```
```SQL
SELECT MIN(Age)
FROM Employees;
```

## The SQL COUNT() Function
*The `COUNT()` function is used to count the number of rows in a table.*

* Example
```SQL
SELECT COUNT(Age)
FROM Employees;
```
## The SQL SUM() Function
*The `SUM()` function is used to calculate the total of a set of values.*
* Example
```SQL
SELECT SUM(Age)
FROM Employees;
```

## The SQL AVG() Function
*The `AVG()` function is used to calculate the average of a set of values.*
* Example
```SQL
SELECT AVG(Age)
FROM Employees;
```

## The SQL LIKE Operator
*The `LIKE` operator is used to search for a specified pattern in a column.*

### There are two wildcards often used in conjunction with the `LIKE` operator:

* The percent sign `%` represents zero, one, or multiple characters.

* The underscore `_` represents a single character.

* Example
```SQL
SELECT * FROM Employees
WHERE EmployeeName LIKE 'a%';
```
```SQL
SELECT * FROM Employees
WHERE EmployeeName LIKE 'a__%';
```
## SQL Wildcard Characters
*A wildcard character is used to substitute one or more characters in a string.*

*Wildcard characters are used with the LIKE operator. The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.*

| Symbol | Description                                      |
|--------|--------------------------------------------------|
| `%`      | Represents zero or more characters               |
| `_`      | Represents a single character                    |
| `[]`     | Represents any single character within the brackets |
| `^`      | Represents any character not in the brackets     |
| `-`      | Represents any single character within the specified range |
| `{}`     | Represents any escaped character                 |

* Examples
```SQL
SELECT * FROM Employees
WHERE EmployeeName LIKE 'a%';
```
```SQL
SELECT * FROM Employees
WHERE EmployeeName LIKE 'a__%';
```
```SQL
SELECT * FROM Employees
WHERE EmployeeName LIKE '[bsp]%';
```
```SQL
SELECT * FROM Employees
WHERE EmployeeName LIKE 'a__%';
```
## The SQL IN Operator
*The `IN` operator is used to specify multiple values in a `WHERE` clause.*

*The `IN` operator is a shorthand for multiple `OR` conditions.*

* Example
```SQL
SELECT * FROM Employees
WHERE EmployeeName IN ('Moataz', 'Ahmed', 'Mohamed');
```

## The SQL BETWEEN Operator
*The `BETWEEN` operator is used to select values within a range.*

*The `BETWEEN` operator is inclusive: begin and end values are included.*

* Example
```SQL
SELECT *  FROM Employees
WHERE Age BETWEEN 10 AND 25;
```

## SQL Aliases
* SQL aliases are used to give a table, or a column in a table, a temporary name.

* Aliases are often used to make column names more readable.

* An alias only exists for the duration of that query.

* An alias is created with the `AS` keyword.

* Example
```SQL
SELECT EmployeeID AS ID  
FROM Employees;
```
