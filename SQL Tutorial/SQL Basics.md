# The Topics

- [The Topics](#the-topics)
  - [What is a SQL?](#what-is-a-sql)
  - [What Can SQL do?](#what-can-sql-do)
  - [Semicolon after SQL Statements?](#semicolon-after-sql-statements)
  - [Some of The Most Important SQL Commands](#some-of-the-most-important-sql-commands)
  - [SQL SELECT Statement](#sql-select-statement)
  - [The SQL WHERE Clause](#the-sql-where-clause)
  - [Operators in The WHERE Clause](#operators-in-the-where-clause)
  - [Python Data Types](#python-data-types)
    - [Examples:](#examples)
  - [Setting the Specific Data Type](#setting-the-specific-data-type)
  - [Basic Operation](#basic-operation)
  - [Python Arithmetic Operators](#python-arithmetic-operators)
  - [Python Arithmetic Operators Examples](#python-arithmetic-operators-examples)
  - [Python Assignment Operators](#python-assignment-operators)
  - [Python Comparison Operators](#python-comparison-operators)
  - [Python Logical Operators](#python-logical-operators)
  - [Python Identity Operators](#python-identity-operators)
  - [Python Identity Operators](#python-identity-operators-1)
  - [Python Membership Operators](#python-membership-operators)
  - [Python Bitwise Operators](#python-bitwise-operators)
  - [Python Casting](#python-casting)
    - [Examples:](#examples-1)


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

## Python Data Types

*In programming, data type is an important concept,
Variables can store data of different types, and different types can do different things.
Python has the following data types built-in by default, in these categories:*
```
Text Type:	str 

Numeric Types:	int, float, complex

Sequence Types:	list, tuple, range

Mapping Type:	dict

Set Types:	set, frozenset

Boolean Type:	bool

Binary Types: bytes, bytearray, memoryview

None Type:	NoneType
```
### Examples:

| Example                                | Data Type   |
|----------------------------------------|-------------|
| `x = "Hello World"                     ` | str         |
| `x = 20                                ` | int         |
| `x = 20.5                              ` | float       |
| `x = 1j                                ` | complex     |
| `x = ["apple", "banana", "cherry"]     ` | list        |
| `x = ("apple", "banana", "cherry")     ` | tuple       |
| `x = range(6)                          ` | range       |
| `x = {"name" : "John", "age" : 36}     ` | dict        |
| `x = {"apple", "banana", "cherry"}     ` | set         |
| `x = frozenset({"apple", "banana", "cherry"})` | frozenset |
| `x = True                  `             | bool        |
| `x = b"Hello"             `              | bytes       |
| `x = bytearray(5)  `                     | bytearray   |
| `x = memoryview(bytes(5))`               | memoryview  |
| `x = None `                              | NoneType    |


## Setting the Specific Data Type

*If you want to specify the data type, you can use the following constructor functions:*

| Example                                       | Data Type   |
|-----------------------------------------------|-------------|
| `x = str("Hello World")                       ` | str         |
| `x = int(20)                                 `  | int         |
| `x = float(20.5)                             `  | float       |
| `x = complex(1j)                             `  | complex     |
| `x = list(("apple", "banana", "cherry"))     `  | list        |
| `x = tuple(("apple", "banana", "cherry"))    `  | tuple       |
| `x = range(6)                                `  | range       |
| `x = dict(name="John", age=36)               `  | dict        |
| `x = set(("apple", "banana", "cherry"))     `   | set         |
| `x = frozenset(("apple", "banana", "cherry"))`  | frozenset   |
| `x = bool(5)             `                      | bool        |
| `x = bytes(5)           `                       | bytes       |
| `x = bytearray(5)       `                       | bytearray   |
| `x = memoryview(bytes(5))`                      | memoryview  |


## Basic Operation
*Operators are used to perform operations on variables and values,*
*Python divides the operators into the following groups:*
* Arithmetic operators
* Assignment operators
* Comparison operators
* Logical operators
* Identity operators
* Membership operators
* Bitwise operators

## Python Arithmetic Operators
*Arithmetic operators are used with numeric values to perform common mathematical operations:*
| Operator | Name           | Example  |
|----------|----------------|----------|
| `+`        | Addition       | `x + y `  |
| `- `       | Subtraction    | `x - y  ` |
| `* `       | Multiplication | `x * y `  |
| `/ `       | Division       | `x / y  ` |
| `% `       | Modulus        | `x % y `  |
| `**`       | Exponentiation | `x ** y ` |
| `//`       | Floor division | `x // y ` |

## Python Arithmetic Operators Examples
```python
# Addition
x = 5
y = 3
result = x + y
print("Addition: ", result)

# Subtraction
result = x - y
print("Subtraction: ", result)

# Multiplication
result = x * y
print("Multiplication: ", result)

# Division
result = x / y
print("Division: ", result)

# Modulus
result = x % y
print("Modulus: ", result)

# Exponentiation
result = x ** y
print("Exponentiation: ", result)

# Floor division
result = x // y
print("Floor division: ", result)
```
## Python Assignment Operators
*Assignment operators are used to assign values to variables:*

| Operator | Example        | Same As       |
|----------|----------------|---------------|
| `=`        | x = 5          |` x = 5`       |
| `+=`       | x += 3         | `x = x + 3 `   |
| `-=`       | x -= 3         | `x = x - 3  ` |
| `*=`       | x *= 3         | `x = x * 3  ` |
| `/=`       | x /= 3         | `x = x / 3 `  |
| `%=`       | x %= 3         | `x = x % 3  ` |
| `//=`      | x //= 3        | `x = x // 3 ` |
| `**=`      | x **= 3        | `x = x ** 3  `|
| `&=`       | x &= 3         | `x = x & 3  ` |
| `^=`       | x ^= 3         | `x = x ^ 3 `  |
| `>>=`      | x >>= 3        | `x = x >> 3 ` |
| `<<=`      | x <<= 3        | `x = x << 3`  |


## Python Comparison Operators
*Comparison operators are used to compare two values:*

| Operator | Name                        | Example  |
|----------|-----------------------------|----------|
| `==`       | Equal                       | `x == y `  |
| `!=`       | Not equal                   | `x != y`   |
| `>`        | Greater than                | `x > y`    |
| `<`       | Less than                   | `x < y`    |
| `>=`      | Greater than or equal to    | `x >= y `  |
| `<=`       | Less than or equal to       | `x <= y`   |


## Python Logical Operators
*Logical operators are used to combine conditional statements:*

| Operator | Description                                    | Example                              |
|----------|------------------------------------------------|--------------------------------------|
| `and `     | Returns True if both statements are true       | `x < 5 and x < 10`                   |
| `or`       | Returns True if one of the statements is true  | `x < 5 or x < 4`                    |
| `not`      | Reverses the result, returns False if the result is true | `not(x < 5 and x < 10)`  |


## Python Identity Operators
*Identity operators are used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location:*

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