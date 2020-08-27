##### From Codecademy course

# How to Transform Tables with SQL

### Subqueries

- **Subqueries** are used to complete an SQL transformation by nesting one query within another query.

- A **non-correlated subquery** is a subquery that can be run independently of the outer query and can be used to complete a multi-step transformation.

- A **correlated subquery** is a subquery that cannot be run independently of the outer query. The order of operations in a correlated subquery is as follows:

  - A row is processed in the outer query.
  - Then, for that particular row in the outer query, the subquery is executed.

### Set Operations

- The `UNION` clause allows us to utilize information from multiple tables in our queries.

- The `UNION ALL` clause allows us to utilize information from multiple tables in our queries, including duplicate values.

- `INTERSECT` is used to combine two `SELECT` statements, but returns rows only from the first `SELECT` statement that are identical to a row in the second `SELECT` statement.

- `EXCEPT` returns distinct rows from the first `SELECT` statement that aren’t output by the second `SELECT` statement.

### Conditional Aggregates

- **Conditional aggregates** are aggregate functions the compute a result set based on a given set of conditions.

- `NULL` can be used to denote an empty field value.

- `CASE` statements allow for custom classification of data.

- `CASE` statements can be used inside aggregates (like `SUM()` and `COUNT()`) to provide filtered measures.

### Date, Number, and String Functions

Date functions:

- `DATETIME` returns the date and time of the column specified. This can be modified to return only the date or only the time.

- `DATETIME(time1, '+ X hours', 'Y minutes', 'Z days')` increments the specificed column by a given number of hours, minutes, or days.

Numeric functions:

- `CAST(number1 AS REAL) / number2` returns the result as a real number by casting one of numeric inputs as a real number.

- `ROUND(number, precision)` returns the numeric value rounded off to the next value specified.

String functions:

- `'string1' || ' ' || 'string2'` concatenates `string1` and `string 2`, with a space between.

- `REPLACE(string,from_string,to_string)` returns the string with all occurrences of the string `from_string` replaced by the string `to_string`.
