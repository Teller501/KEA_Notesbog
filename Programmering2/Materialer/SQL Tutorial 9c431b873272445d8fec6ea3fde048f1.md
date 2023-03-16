# SQL Tutorial

[https://www.w3schools.com/sql/default.asp](https://www.w3schools.com/sql/default.asp)

SQL is a standard language for storing, manipulating and retrieving data in databases.

Our SQL tutorial will teach you how to use SQL in: MySQL, SQL Server, MS Access, Oracle, Sybase, Informix, Postgres, and other database systems.

[Start learning SQL now »](https://www.w3schools.com/sql/sql_intro.asp)

## Examples in Each Chapter

With our online SQL editor, you can edit the SQL statements, and click on a button to view the result.

### Example[Get your own SQL Server](https://www.w3schools.com/spaces/)

SELECT * FROM Customers;

[Try it Yourself »](https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_all)

Click on the "Try it Yourself" button to see how it works.

## SQL Exercises

## SQL Examples

Learn by examples! This tutorial supplements all explanations with clarifying examples.

[See All SQL Examples](https://www.w3schools.com/sql/sql_examples.asp)

## SQL Quiz Test

Test your SQL skills at W3Schools!

[Start SQL Quiz!](https://www.w3schools.com/sql/sql_quiz.asp)

## My Learning

Track your progress with the free "My Learning" program here at W3Schools.

Log in to your account, and start earning points!

This is an optional feature. You can study W3Schools without using My Learning.

![SQL%20Tutorial%209c431b873272445d8fec6ea3fde048f1/mylearning.png](SQL%20Tutorial%209c431b873272445d8fec6ea3fde048f1/mylearning.png)

## SQL References

At W3Schools you will find a complete reference for keywords and function:

[SQL Keyword Reference](https://www.w3schools.com/sql/sql_ref_keywords.asp)

[MYSQL Functions](https://www.w3schools.com/sql/sql_ref_mysql.asp)

[SQLServer Functions](https://www.w3schools.com/sql/sql_ref_sqlserver.asp)

[MS Access Functions](https://www.w3schools.com/sql/sql_ref_msaccess.asp)

[SQL Quick Reference](https://www.w3schools.com/sql/sql_quickref.asp)

## SQL Data Types

Data types and ranges for Microsoft Access, MySQL and SQL Server.

SQL is a standard language for accessing and manipulating databases.

## What is SQL?

- SQL stands for Structured Query Language
- SQL lets you access and manipulate databases
- SQL became a standard of the American National Standards Institute (ANSI) in 1986, and of the International Organization for Standardization (ISO) in 1987

## What Can SQL do?

- SQL can execute queries against a database
- SQL can retrieve data from a database
- SQL can insert records in a database
- SQL can update records in a database
- SQL can delete records from a database
- SQL can create new databases
- SQL can create new tables in a database
- SQL can create stored procedures in a database
- SQL can create views in a database
- SQL can set permissions on tables, procedures, and views

## SQL is a Standard - BUT....

Although SQL is an ANSI/ISO standard, there are different versions of the SQL language.

However, to be compliant with the ANSI standard, they all support at least the major commands (such as 
`SELECT`, `UPDATE`, 
`DELETE`, `INSERT`, 
`WHERE`) in a similar manner.

**Note:** Most of the SQL database programs also have their own proprietary extensions in addition to the SQL standard!

## Using SQL in Your Web Site

To build a web site that shows data from a database, you will need:

- An RDBMS database program (i.e. MS Access, SQL Server, MySQL)
- To use a server-side scripting language, like PHP or ASP
- To use SQL to get the data you want
- To use HTML / CSS to style the page

## RDBMS

RDBMS stands for Relational Database Management System.

RDBMS is the basis for SQL, and for all modern database systems such as MS SQL Server, IBM DB2, Oracle, MySQL, and Microsoft Access.

The data in RDBMS is stored in database objects called tables. A table is a collection of related data entries and it consists of columns and rows.

Look at the "Customers" table:

Every table is broken up into smaller entities called fields. The fields in the Customers table consist of CustomerID, CustomerName, ContactName, Address, City, PostalCode and Country. A field is a column in a table that is designed to maintain specific information about every record in the table.

A record, also called a row, is each individual entry that exists in a table. For example, there are 91 records in the above Customers table. A record is a horizontal entity in a table.

A column is a vertical entity in a table that contains all information associated with a specific field in a table.

## Database Tables

A database most often contains one or more tables. Each table is identified by a name (e.g. "Customers" or "Orders"). Tables contain records (rows) with data.

In this tutorial we will use the well-known Northwind sample database (included in MS Access and MS SQL Server).

Below is a selection from the "Customers" table:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |

The table above contains five records (one for each customer) and seven columns (CustomerID, CustomerName, ContactName, Address, City, PostalCode, and Country).

## SQL Statements

Most of the actions you need to perform on a database are done with SQL statements.

The following SQL statement selects all the records in the "Customers" table:

In this tutorial we will teach you all about the different SQL statements.

## Keep in Mind That...

- SQL keywords are NOT case sensitive: `select` is the same as  `SELECT`

In this tutorial we will write all SQL keywords in upper-case.

## Semicolon after SQL Statements?

Some database systems require a semicolon at the end of each SQL statement.

Semicolon is the standard way to separate each SQL statement in database systems that allow more than one SQL statement to be executed in the same call to the server.

In this tutorial, we will use semicolon at the end of each SQL statement.

## Some of The Most Important SQL Commands

- `SELECT` - extracts data from a database
- `UPDATE` - updates data in a database
- `DELETE` - deletes data from a database
- `INSERT INTO` - inserts new data into a database
- `CREATE DATABASE` - creates a new database
- `ALTER DATABASE` - modifies a database
- `CREATE TABLE` - creates a new table
- `ALTER TABLE` - modifies a table
- `DROP TABLE` - deletes a table
- `CREATE INDEX` - creates an index (search key)
- `DROP INDEX` - deletes an index

The `SELECT` statement is used to select data from a database.

The data returned is stored in a result table, called the result-set.

### SELECT Syntax

Here, column1, column2, ... are the field names of the table you want to select data from. If you want to select all the fields available in the table, use the following syntax:

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

## SELECT Column Example

The following SQL statement selects the "CustomerName" and "City" columns from the "Customers" table:

## SELECT * Example

The following SQL statement selects all the columns from the "Customers" table:

The `SELECT DISTINCT` statement is used to return only distinct (different) values.

Inside a table, a column often contains many duplicate values; and sometimes you only want to list the different (distinct) values.

### SELECT DISTINCT Syntax

SELECT DISTINCT *column1*, *column2, ...*
 FROM *table_name*;

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

## SELECT Example Without DISTINCT

The following SQL statement selects all (including the duplicates) values from the "Country" column in the "Customers" table:

Now, let us use the `SELECT DISTINCT` statement and see the result.

## SELECT DISTINCT Examples

The following SQL statement selects only the DISTINCT values from the "Country" column in the "Customers" table:

The following SQL statement lists the number of different (distinct) customer countries:

Here is the workaround for MS Access:

# SQL WHERE Clause

[❮ Previous](https://www.w3schools.com/sql/sql_distinct.asp) [Next ❯](https://www.w3schools.com/sql/sql_and_or.asp)

The `WHERE` clause is used to filter records.

It is used to extract only those records that fulfill a specified condition.

### WHERE Syntax

SELECT *column1*, *column2, ...*
 FROM *table_name*
 WHERE *condition*;

**Note:** The `WHERE` clause is not only used in 
`SELECT` statements, it is also used in `UPDATE`, `DELETE`, etc.!

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

| CustomerID | CustomerName | ContactName | Address | City | PostalCode | Country |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | Alfreds Futterkiste | Maria Anders | Obere Str. 57 | Berlin | 12209 | Germany |
| 2 | Ana Trujillo Emparedados y helados | Ana Trujillo | Avda. de la Constitución 2222 | México D.F. | 05021 | Mexico |
| 3 | Antonio Moreno Taquería | Antonio Moreno | Mataderos 2312 | México D.F. | 05023 | Mexico |
| 4 | Around the Horn | Thomas Hardy | 120 Hanover Sq. | London | WA1 1DP | UK |
| 5 | Berglunds snabbköp | Christina Berglund | Berguvsvägen 8 | Luleå | S-958 22 | Sweden |

## WHERE Clause Example

The following SQL statement selects all the customers from the country "Mexico", in the "Customers" table:

### Example[Get your own SQL Server](https://www.w3schools.com/spaces/)

SELECT * FROM Customers
 WHERE Country='Mexico';

[Try it Yourself »](https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_where)

## Text Fields vs. Numeric Fields

SQL requires single quotes around text values (most database systems will also allow double quotes).

However, numeric fields should not be enclosed in quotes:

### Example[Get your own SQL Server](https://www.w3schools.com/spaces/)

SELECT * FROM Customers
 WHERE CustomerID=1;

[Try it Yourself »](https://www.w3schools.com/sql/trysql.asp?filename=trysql_select_where_number)

## Operators in The WHERE Clause

The following operators can be used in the `WHERE` clause:

| Operator | Description | Example |
| --- | --- | --- |
| = | Equal | https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_equal_to |
| > | Greater than | https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_greater_than |
| < | Less than | https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_less_than |
| >= | Greater than or equal | https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_greater_than2 |
| <= | Less than or equal | https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_less_than2 |
| <> | Not equal. Note: In some versions of SQL this operator may be written as != | https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_not_equal_to |
| BETWEEN | Between a certain range | https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_between |
| LIKE | Search for a pattern | https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_like |
| IN | To specify multiple possible values for a column | https://www.w3schools.com/sql/trysql.asp?filename=trysql_op_in |

## Test Yourself With Exercises

## Exercise:

Select all records where the `City` column has the value "Berlin".

The `WHERE` clause can be combined with 
`AND`, `OR`, and 
`NOT` operators.

The `AND` and `OR` operators are used to filter records based on more than one condition:

- The `AND` operator displays a record if all the conditions separated by  `AND` are TRUE.
- The `OR` operator displays a record if any of the conditions separated by  `OR` is TRUE.

The `NOT` operator displays a record if the condition(s) is NOT TRUE.

### AND Syntax

SELECT *column1*, *column2, ...*
 FROM *table_name*
 WHERE *condition1* AND *condition2* AND *condition3 ...*;

### OR Syntax

SELECT *column1*, *column2, ...*
 FROM *table_name*
 WHERE *condition1* OR *condition2* OR *condition3 ...*;

### NOT Syntax

## Demo Database

The table below shows the complete "Customers" table from the Northwind sample database:

## AND Example

The following SQL statement selects all fields from "Customers" where country is "Germany" AND city is "Berlin":

## OR Example

The following SQL statement selects all fields from "Customers" where city is "Berlin" OR "München":

The following SQL statement selects all fields from "Customers" where country is "Germany" OR "Spain":

## NOT Example

The following SQL statement selects all fields from "Customers" where country is NOT "Germany":

## Combining AND, OR and NOT

You can also combine the `AND`, 
`OR` and `NOT` operators.

The following SQL statement selects all fields from "Customers" where country is "Germany" AND city must be "Berlin" OR "München" (use parenthesis to form complex expressions):

The following SQL statement selects all fields from "Customers" where country is NOT "Germany" and NOT "USA":

The `ORDER BY` keyword is used to sort the result-set in ascending or descending order.

The `ORDER BY` keyword sorts the records in ascending order by default. To sort the records in descending order, use the 
`DESC` keyword.

### ORDER BY Syntax

SELECT *column1*, *column2, ...*
 FROM *table_name*
 ORDER BY *column1, column2, ...* ASC|DESC;

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

## ORDER BY Example

The following SQL statement selects all customers from the "Customers" table, sorted by the "Country" column:

## ORDER BY DESC Example

The following SQL statement selects all customers from the "Customers" table, sorted DESCENDING by the "Country" column:

## ORDER BY Several Columns Example

The following SQL statement selects all customers from the "Customers" table, sorted by the "Country" and the "CustomerName" column. This means that it orders by Country, but if some rows have the same Country, it orders them by CustomerName:

## ORDER BY Several Columns Example 2

The following SQL statement selects all customers from the "Customers" table, sorted ascending by the "Country" and descending by the "CustomerName" column:

The `INSERT INTO` statement is used to insert new records in a table.

### INSERT INTO Syntax

It is possible to write the `INSERT INTO` statement in two ways:

1. Specify both the column names and the values to be inserted:

INSERT INTO *table_name* (*column1*, *column2*, *column3*, ...)
 VALUES (*value1*, *value2*, *value3*, ...);

2. If you are adding values for all the columns of the table, you do not need to specify the column names in the SQL query. However, make sure the order of the values is in the same order as the columns in the table. Here, the 
`INSERT INTO` syntax would be as follows:

INSERT INTO *table_name*
 VALUES (*value1*, *value2*, *value3*, ...);

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

## INSERT INTO Example

The following SQL statement inserts a new record in the "Customers" table:

The selection from the "Customers" table will now look like this:

## Insert Data Only in Specified Columns

It is also possible to only insert data in specific columns.

The following SQL statement will insert a new record, but only insert data in the "CustomerName", "City", and "Country" columns (CustomerID will be updated automatically):

The selection from the "Customers" table will now look like this:

## What is a NULL Value?

A field with a NULL value is a field with no value.

If a field in a table is optional, it is possible to insert a new record or update a record without adding a value to this field. Then, the field will be saved with a NULL value.

**Note:** A NULL value is different from a zero value or a field that contains spaces. A field with a NULL value is one that has been left blank during record creation!

## How to Test for NULL Values?

It is not possible to test for NULL values with comparison operators, such as =, <, or <>.

We will have to use the `IS NULL` and 
`IS NOT NULL` operators instead.

### IS NULL Syntax

SELECT *column_names*FROM *table_name*
 WHERE *column_name* IS NULL;

### IS NOT NULL Syntax

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

## The IS NULL Operator

The `IS NULL` operator is used to test for empty values (NULL values).

The following SQL lists all customers with a NULL value in the "Address" field:

## The IS NOT NULL Operator

The `IS NOT NULL` operator is used to test for non-empty values (NOT NULL values).

The following SQL lists all customers with a value in the "Address" field:

The `UPDATE` statement is used to modify the existing records in a table.

### UPDATE Syntax

UPDATE *table_name*
 SET *column1* = *value1*, *column2* = *value2*, ...
 WHERE *condition*;

**Note:** Be careful when updating records in a table! Notice the 
`WHERE` clause in the `UPDATE` statement. The `WHERE` clause specifies which record(s) that should be updated. If you omit the `WHERE` clause, all records in the table will be updated!

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

## UPDATE Table

The following SQL statement updates the first customer (CustomerID = 1) with a new contact person *and* a new city.

The selection from the "Customers" table will now look like this:

## UPDATE Multiple Records

It is the `WHERE` clause that determines how many records will be updated.

The following SQL statement will update the ContactName to "Juan" for all records where country is "Mexico":

The selection from the "Customers" table will now look like this:

## Update Warning!

The selection from the "Customers" table will now look like this:

The `DELETE` statement is used to delete existing records in a table.

### DELETE Syntax

DELETE FROM *table_name* WHERE *condition*;

**Note:** Be careful when deleting records in a table! Notice the 
`WHERE` clause in the `DELETE` statement. The `WHERE` clause specifies which record(s) should be deleted. If you omit the `WHERE` clause, all records in the table will be deleted!

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

## SQL DELETE Example

The following SQL statement deletes the customer "Alfreds Futterkiste" from the "Customers" table:

The "Customers" table will now look like this:

## Delete All Records

It is possible to delete all rows in a table without deleting the table. This means that the table structure, attributes, and indexes will be intact:

The following SQL statement deletes all rows in the "Customers" table, without deleting the table:

## The SQL SELECT TOP Clause

The `SELECT TOP` clause is used to specify the number of records to return.

The `SELECT TOP` clause is useful on large tables with thousands of records. Returning a large number of records can impact performance.

**Note:** Not all database systems support the 
`SELECT TOP` clause. MySQL supports the `LIMIT` clause to select a limited number of records, while Oracle uses 
`FETCH FIRST *n* ROWS ONLY` and `ROWNUM`.

**SQL Server / MS Access Syntax:**

SELECT TOP *number*|*percent* *column_name(s)*
 FROM *table_name*WHERE *condition*;

**MySQL Syntax:**

**Oracle 12 Syntax:**

**Older Oracle Syntax:**

**Older Oracle Syntax (with ORDER BY):**

## Demo Database

Below is a selection from the "Customers" table in the Northwind sample database:

## SQL TOP, LIMIT and FETCH FIRST Examples

The following SQL statement selects the first three records from the "Customers" table (for SQL Server/MS Access):

The following SQL statement shows the equivalent example for MySQL:

The following SQL statement shows the equivalent example for Oracle:

## SQL TOP PERCENT Example

The following SQL statement selects the first 50% of the records from the "Customers" table (for SQL Server/MS Access):

The following SQL statement shows the equivalent example for Oracle:

## ADD a WHERE CLAUSE

The following SQL statement selects the first three records from the "Customers" table, where the country is "Germany" (for SQL Server/MS Access):

The following SQL statement shows the equivalent example for MySQL:

The following SQL statement shows the equivalent example for Oracle:

The `MIN()` function returns the smallest value of the selected column.

The `MAX()` function returns the largest value of the selected column.

### MIN() Syntax

SELECT MIN(*column_name*)
 FROM *table_name*
 WHERE *condition*;

### MAX() Syntax

SELECT MAX(*column_name*)
 FROM *table_name*
 WHERE *condition*;

## Demo Database

Below is a selection from the "Products" table in the Northwind sample database:

## MIN() Example

The following SQL statement finds the price of the cheapest product:

## MAX() Example

The following SQL statement finds the price of the most expensive product:
