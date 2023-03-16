# Databaser - SQL 2 - 28-02-2023

- **Fag:** Programmering 2
- **Oprettet:** February 27, 2023 6:27 PM
- **Type:** Forberedelse

# Materialer

[SQL Tutorial](https://github.com/Teller501/KEA_Notesbog/blob/main/Programmering2/Materialer/SQL%20Tutorial%209c431b873272445d8fec6ea3fde048f1.md)


# SQL 2

More commands:

- `ORDER BY`
- `LIMIT`
- `GROUP BY`
- `HAVING`
- `LIKE`
- `BETWEEN`
- `INSERT INTO`
- `JOIN`
    - `INNER JOIN`
    - `LEFT JOIN`
    - `RIGHT JOIN`
- `UPDATE`
- `DELETE`

## ORDER BY

The `ORDER BY` clause is used to sort the result set in ascending or descending order based on one or more columns.

Here's an example:

```sql
SELECT * FROM customers
ORDER BY last_name ASC;

```

This will return all rows from the `customers` table, sorted in ascending order by the `last_name` column. The `ASC` keyword specifies that the sorting should be done in ascending order. To sort in descending order, use the `DESC` keyword instead:

```sql
SELECT * FROM customers
ORDER BY last_name DESC;

```

This will return all rows from the `customers` table, sorted in descending order by the `last_name` column.

You can also sort by multiple columns. In that case, the sorting is done by the first column, then by the second column, and so on. Here's an example:

```sql
SELECT * FROM customers
ORDER BY last_name ASC, first_name ASC;

```

This will return all rows from the `customers` table, sorted in ascending order by the `last_name` column and then by the `first_name` column.

## LIMIT

The `LIMIT` clause is used to limit the number of rows returned by a query. It is especially useful when working with large tables that contain thousands or even millions of rows.

Here's an example:

```sql
SELECT * FROM customers
LIMIT 10;

```

This will return the first 10 rows from the `customers` table. If you only want to return a certain range of rows, you can also specify a starting point and a number of rows to return:

```sql
SELECT * FROM customers
LIMIT 5, 10;

```

This will return 10 rows starting from the 6th row (since we're skipping the first 5 rows with the `5` parameter). This is useful for pagination, where you only want to display a certain number of rows per page.

Note: the exact syntax may vary depending on the SQL database you are using.

## GROUP BY

The `GROUP BY` clause is used to group rows that have the same values in a specified column or set of columns. It is often used together with aggregate functions, such as `SUM`, `AVG`, `COUNT`, and `MAX`, to perform calculations on each group of rows.

Here's an example:

```sql
SELECT department, COUNT(*) FROM employees
GROUP BY department;

```

This will return the number of employees in each department. The `GROUP BY` clause groups the rows by the `department` column, and the `COUNT(*)` function counts the number of rows in each group.

You can also group by multiple columns. In that case, the grouping is done by the first column, then by the second column, and so on. Here's an example:

```sql
SELECT department, gender, COUNT(*) FROM employees
GROUP BY department, gender;

```

This will return the number of male and female employees in each department. The `GROUP BY` clause groups the rows by the `department` and `gender` columns, and the `COUNT(*)` function counts the number of rows in each group.

Note: the exact syntax may vary depending on the SQL database you are using.

## HAVING

The `HAVING` clause is used in conjunction with the `GROUP BY` clause to specify a search condition for a group or an aggregate. It is used to filter the groups that are returned by a query.

Here's an example:

```sql
SELECT department, AVG(salary) as avg_salary
FROM employees
GROUP BY department
HAVING AVG(salary) > 50000;

```

This will return the departments where the average salary is greater than 50,000. The `GROUP BY` clause groups the rows by the `department` column, and the `AVG(salary)` function calculates the average salary for each group. Then, the `HAVING` clause filters the groups and returns only those where the average salary is greater than 50,000.

You can also use other aggregate functions, such as `SUM`, `COUNT`, and `MAX`, in conjunction with the `HAVING` clause to further filter the groups.

Note: the exact syntax may vary depending on the SQL database you are using.

## LIKE

The `LIKE` operator is used to search for a specified pattern in a column. It is often used with the `%` wildcard character, which matches any string of zero or more characters.

Here's an example:

```sql
SELECT * FROM customers
WHERE last_name LIKE 'S%';

```

This will return all rows from the `customers` table where the `last_name` column starts with the letter 'S'. The `%` wildcard character matches any string of zero or more characters, so this will include last names such as 'Smith', 'Stewart', and 'Sanders'.

You can also use the `_` wildcard character, which matches any single character, to search for patterns with a specific length. Here's an example:

```sql
SELECT * FROM customers
WHERE last_name LIKE '__ith';

```

This will return all rows from the `customers` table where the `last_name` column has a length of 5 and ends with the letters 'ith'. This will include last names such as 'Smith' and 'Grith'.

Note: the exact syntax may vary depending on the SQL database you are using.

## BETWEEN

The `BETWEEN` operator is used to filter data based on a range of values. It is often used with the `WHERE` clause to filter rows in a table based on a range of column values.

Here's an example:

```sql
SELECT * FROM employees
WHERE salary BETWEEN 50000 AND 70000;

```

This will return all rows from the `employees` table where the `salary` column is between 50,000 and 70,000. The `BETWEEN` operator is used to specify the range of values.

Note that the `BETWEEN` operator is inclusive, meaning that it includes the boundary values in the range. In the example above, rows with a salary of exactly 50,000 or 70,000 will be included in the result set.

You can also use the `NOT BETWEEN` operator to exclude rows within a certain range of values. Here's an example:

```sql
SELECT * FROM employees
WHERE salary NOT BETWEEN 50000 AND 70000;

```

This will return all rows from the `employees` table where the `salary` column is not between 50,000 and 70,000.

Note: the exact syntax may vary depending on the SQL database you are using.

## INSERT INTO

The `INSERT INTO` statement is used to insert new rows into a table. Here's an example:

```sql
INSERT INTO customers (first_name, last_name, email)
VALUES ('John', 'Doe', 'john.doe@example.com');

```

This will insert a new row into the `customers` table with the values `John` for the `first_name` column, `Doe` for the `last_name` column, and `john.doe@example.com` for the `email` column. Note that you need to specify the names of the columns you're inserting into, and then provide the corresponding values for each column. If you don't specify a value for a column, it will either be set to `NULL` or to a default value, depending on the table schema.

You can also insert multiple rows at once by providing multiple sets of values, separated by commas:

```sql
INSERT INTO customers (first_name, last_name, email)
VALUES ('John', 'Doe', 'john.doe@example.com'),
       ('Jane', 'Doe', 'jane.doe@example.com'),
       ('Bob', 'Smith', 'bob.smith@example.com');

```

This will insert three new rows into the `customers` table, one for each set of values.

Note: the exact syntax may vary depending on the SQL database you are using.

## JOIN

The `JOIN` clause is used to combine rows from two or more tables based on a related column between them.

Here's an example:

```sql
SELECT *
FROM orders
JOIN customers
ON orders.customer_id = customers.customer_id;

```

This will return all rows from the `orders` table and the `customers` table where the `customer_id` column matches between the two tables. The `JOIN` clause combines the rows from both tables based on this relationship.

You can also specify the type of join you want to perform. The most common types of joins are `INNER JOIN`, `LEFT JOIN`, and `RIGHT JOIN`.

- `INNER JOIN`: returns only the rows where there is a match in both tables. This is the default type of join if you don't specify a type.
- `LEFT JOIN`: returns all the rows from the left table and the matched rows from the right table. If there is no match in the right table, it returns `NULL` values for the right table columns.
- `RIGHT JOIN`: returns all the rows from the right table and the matched rows from the left table. If there is no match in the left table, it returns `NULL` values for the left table columns.

Here's an example of a `LEFT JOIN`:

```sql
SELECT *
FROM customers
LEFT JOIN orders
ON customers.customer_id = orders.customer_id;

```

This will return all rows from the `customers` table and the matching rows from the `orders` table. If there is no match in the `orders` table, it returns `NULL` values for the `orders` table columns.

Here's an example of an `INNER JOIN`:

```sql
SELECT *
FROM orders
INNER JOIN customers
ON orders.customer_id = customers.customer_id;

```

This will return only the rows where there is a match in both the `orders` table and the `customers` table based on the `customer_id` column. The `INNER JOIN` clause combines the rows from both tables based on this relationship.

Here's an example of a `RIGHT JOIN`:

```sql
SELECT *
FROM orders
RIGHT JOIN customers
ON orders.customer_id = customers.customer_id;

```

This will return all rows from the `orders` table and the matching rows from the `customers` table. If there is no match in the `customers` table, it returns `NULL` values for the `customers` table columns.

Note: the exact syntax may vary depending on the SQL database you are using.

## UPDATE

The `UPDATE` statement is used to modify existing rows in a table. It is often used to update records that have changed or to correct errors in the data.

Here's an example:

```sql
UPDATE customers
SET email = 'newemail@example.com'
WHERE customer_id = 1;

```

This will update the `email` column for the row in the `customers` table where the `customer_id` is `1`. The `SET` keyword is used to specify the new value for the `email` column, and the `WHERE` clause is used to specify which row or rows to update.

You can also update multiple columns at once:

```sql
UPDATE customers
SET first_name = 'John', last_name = 'Doe'
WHERE customer_id = 1;

```

This will update the `first_name` and `last_name` columns for the row in the `customers` table where the `customer_id` is `1`.

Note: the exact syntax may vary depending on the SQL database you are using.

## DELETE

The `DELETE` statement is used to delete one or more rows from a table. It is often used to remove records that are no longer needed or to correct errors in the data.

Here's an example:

```sql
DELETE FROM customers
WHERE customer_id = 1;

```

This will delete the row from the `customers` table where the `customer_id` is `1`. The `WHERE` clause is used to specify which row or rows to delete. If you omit the `WHERE` clause, all rows in the table will be deleted.

You can also use multiple conditions with the `AND` or `OR` operators to specify more complex deletion criteria:

```sql
DELETE FROM customers
WHERE last_name = 'Doe'
AND first_name = 'John';

```

This will delete all rows from the `customers` table where the `last_name` is 'Doe' and the `first_name` is 'John'.

Note: the exact syntax may vary depending on the SQL database you are using.
