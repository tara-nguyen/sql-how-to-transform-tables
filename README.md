##### From Codecademy course

# How to Transform Tables with SQL

### Subqueries

- Subqueries are used to complete an SQL transformation by nesting one query within another query.

- A non-correlated subquery is a subquery that can be run independently of the outer query and can be used to complete a multi-step transformation.

- A correlated subquery is a subquery that cannot be run independently of the outer query. The order of operations in a correlated subquery is as follows:

  - A row is processed in the outer query.
  - Then, for that particular row in the outer query, the subquery is executed.
