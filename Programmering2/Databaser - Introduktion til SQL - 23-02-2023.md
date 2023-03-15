# Databaser - Introduktion til SQL - 23-02-2023

- **Fag:** Programmering 2
- **Oprettet:** February 27, 2023 2:40 PM
- **Type:** Forberedelse

# Materialer

[SQL Tutorial](Databaser%20-%20Introduktion%20til%20SQL%20-%2023-02-2023%201324be59a18b49419052db32904a5052/SQL%20Tutorial%2076e2a12128cb47c9b6b1e7b51f1d4e31.md)

![Databaser%20-%20Introduktion%20til%20SQL%20-%2023-02-2023%201324be59a18b49419052db32904a5052/Rectangle_234red_round_shadow.png](Databaser%20-%20Introduktion%20til%20SQL%20-%2023-02-2023%201324be59a18b49419052db32904a5052/Rectangle_234red_round_shadow.png)

# Intro til SQL

Here are the most useful `SELECT` SQL commands from the [SQL Tutorial](Databaser%20-%20Introduktion%20til%20SQL%20-%2023-02-2023%201324be59a18b49419052db32904a5052/SQL%20Tutorial%2076e2a12128cb47c9b6b1e7b51f1d4e31.md):

- `SELECT`
- `FROM`
- `WHERE`
- `DISTINCT`

## SELECT

Here are some examples of how to use the `SELECT` command in SQL:

- Select all columns from a table:
    
    ```
    SELECT * FROM table_name;
    
    ```
    
- Select specific columns from a table:
    
    ```
    SELECT column1, column2, ... FROM table_name;
    
    ```
    
- Select distinct values from a column:
    
    ```
    SELECT DISTINCT column_name FROM table_name;
    
    ```
    
- Select values from multiple tables:
    
    ```
    SELECT column_name(s) FROM table1 INNER JOIN table2 ON table1.column_name = table2.column_name;
    
    ```
    
- Select values based on a condition:
    
    ```
    SELECT column_name(s) FROM table_name WHERE condition;
    
    ```
    
- Select values and order them by a column:
    
    ```
    SELECT column_name(s) FROM table_name ORDER BY column_name ASC|DESC;
    
    ```
    
- Select values and group them by a column:
    
    ```
    SELECT column_name(s) FROM table_name GROUP BY column_name;
    
    ```
    
- Select values and filter them by a group condition:
    
    ```
    SELECT column_name(s) FROM table_name GROUP BY column_name HAVING condition;
    
    ```
    

## FROM

Here are some basic examples of how to use the `FROM` keyword in SQL:

- Select all columns from a table:
    
    ```
    SELECT * FROM table_name;
    
    ```
    
- Select specific columns from a table:
    
    ```
    SELECT column1, column2, ... FROM table_name;
    
    ```
    

The `FROM` keyword is used to specify the table or tables that you want to select data from in your SQL query. In the examples above, `table_name` is the name of the table that is being selected from.

## WHERE

The `WHERE` keyword is used to filter data in SQL queries based on a specified condition. Here are some basic examples of how to use the `WHERE` keyword:

- Select values where a column equals a specific value:
    
    ```
    SELECT column_name(s) FROM table_name WHERE column_name = value;
    
    ```
    
- Select values where a column does not equal a specific value:
    
    ```
    SELECT column_name(s) FROM table_name WHERE column_name != value;
    
    ```
    
- Select values where a column is greater than a specific value:
    
    ```
    SELECT column_name(s) FROM table_name WHERE column_name > value;
    
    ```
    
- Select values where a column is less than a specific value:
    
    ```
    SELECT column_name(s) FROM table_name WHERE column_name < value;
    
    ```
    
- Select values where a column is between two specific values:
    
    ```
    SELECT column_name(s) FROM table_name WHERE column_name BETWEEN value1 AND value2;
    
    ```
    
- Select values where a column matches a pattern:
    
    ```
    SELECT column_name(s) FROM table_name WHERE column_name LIKE pattern;
    
    ```
    

In the examples above, `column_name` is the name of the column that is being filtered and `value` is the value that is being compared to. The `BETWEEN` keyword is used to specify a range of values. The `LIKE` keyword is used to specify a pattern that the column values must match.

## DISTINCT

Suppose you have a table named `employees` with a column named `department`. The `department` column contains duplicate values. Here's how you can use `DISTINCT` to retrieve a list of unique departments:

```
SELECT DISTINCT department FROM employees;

```

This query will return only the unique department names from the `employees` table, without any duplicates.

## Aggregatfunktioner

Aggregate functions in SQL are used to perform calculations on multiple rows of a table and return a single value. These functions include:

- `AVG()`: calculates the average value of a column
- `COUNT()`: counts the number of rows in a table or the number of rows that meet a specific condition
- `MAX()`: returns the maximum value in a column
- `MIN()`: returns the minimum value in a column
- `SUM()`: calculates the sum of values in a column

These functions can be used in conjunction with other SQL commands, such as `SELECT`, `FROM`, and `WHERE`, to perform more complex queries on large amounts of data. For example, you could use `AVG()` and `GROUP BY` to calculate the average value of a column for each group in a table.

### AVG

Here's an example of how to use the `AVG()` function in SQL:

```
SELECT AVG(column_name) FROM table_name;

```

The `AVG()` function is used to calculate the average value of a column in a table. In the example above, `column_name` is the name of the column that you want to calculate the average value for, and `table_name` is the name of the table that you are selecting data from.

### COUNT

Here's an example of how to use the `COUNT()` function in SQL:

```
SELECT COUNT(column_name) FROM table_name;

```

The `COUNT()` function is used to count the number of rows in a table. You can specify a specific column to count the number of non-null values in that column. In the example above, `column_name` is the name of the column that you want to count the number of non-null values for, and `table_name` is the name of the table that you are selecting data from.

### MAX

Here's an example of how to use the `MAX()` function in SQL:

```
SELECT MAX(column_name) FROM table_name;

```

The `MAX()` function is used to find the maximum value in a column. In the example above, `column_name` is the name of the column that you want to find the maximum value for, and `table_name` is the name of the table that you are selecting data from.

### MIN

Here's an example of how to use the `MIN()` function in SQL:

```
SELECT MIN(column_name) FROM table_name;

```

The `MIN()` function is used to find the minimum value in a column. In the example above, `column_name` is the name of the column that you want to find the minimum value for, and `table_name` is the name of the table that you are selecting data from.

### SUM

Here's an example of how to use the `SUM()` function in SQL:

```
SELECT SUM(column_name) FROM table_name;

```

The `SUM()` function is used to calculate the sum of values in a column. In the example above, `column_name` is the name of the column that you want to calculate the sum of, and `table_name` is the name of the table that you are selecting data from.
