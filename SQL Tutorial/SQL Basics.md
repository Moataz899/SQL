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
  - [Python Identity Operators](#python-identity-operators)
  - [Python Membership Operators](#python-membership-operators)
  - [Python Bitwise Operators](#python-bitwise-operators)
  - [Python Casting](#python-casting)
    - [Examples:](#examples)


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


## Python Identity Operators
| Operator | Description                                | Example       |
|----------|--------------------------------------------|---------------|
| `is`       | Returns True if both variables are the same object | `x is y`      |
| `is not`   | Returns True if both variables are not the same object | `x is not y`  |


## Python Membership Operators
*Membership operators are used to test if a sequence is presented in an object:*

| Operator | Description                                          | Example     |
|----------|------------------------------------------------------|-------------|
| `in`      | Returns True if a sequence with the specified value is present in the object | `x in y`    |
| `not in`   | Returns True if a sequence with the specified value is not present in the object | `x not in y`|


## Python Bitwise Operators
*Bitwise operators are used to compare (binary) numbers:*


| Operator | Name | Description                                                                                   | Example     |
|----------|------|-----------------------------------------------------------------------------------------------|-------------|
| `&`  | AND  | Sets each bit to 1 if both bits are 1                                                         | `x & y`     |
| `\|`  | OR   | Sets each bit to 1 if one of two bits is 1|`x \|  y`     |
| `^  `      | XOR  | Sets each bit to 1 if only one of two bits is 1                                               | `x ^ y`     |
| `~ `       | NOT  | Inverts all the bits                                                                          | `~x`        |
| `<<  `     | Zero fill left shift | Shift left by pushing zeros in from the right and let the leftmost bits fall off | `x << 2`    |
| `>>`       | Signed right shift | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off | `x >> 2`    

## Python Casting

*There may be times when you want to specify a type on a variable. This can be done with casting. Python is an object-oriented language, and as such, it uses classes to define data types, including its primitive types.*

*Casting in Python is done using constructor functions:*

- **`int()`**: Constructs an integer number from an integer literal, a float literal (by removing all decimals), or a string literal (providing the string represents a whole number).
- **`float()`**: Constructs a float number from an integer literal, a float literal, or a string literal (providing the string represents a float or an integer).
- **`str()`**: Constructs a string from a wide variety of data types, including strings, integer literals, and float literals.

### Examples:

```python
# Casting to integer
x = int(3.14)    # x will be 3
y = int("42")    # y will be 42

# Casting to float
a = float(7)     # a will be 7.0
b = float("3.14")# b will be 3.14

# Casting to string
m = str(10)      # m will be '10'
n = str(3.14)    # n will be '3.14'
```