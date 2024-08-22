The `HAVING` keyword in PostgreSQL is used to filter groups of rows created by the `GROUP BY` clause. It allows you to specify conditions on aggregate functions, which the `WHERE` clause cannot do.

### Syntax
```sql
SELECT column1, aggregate_function(column2)
FROM table_name
WHERE condition
GROUP BY column1
HAVING condition;
```

### Examples

1. **Basic Usage**:
   ```sql
   SELECT department, COUNT(employee_id) AS num_employees
   FROM employees
   GROUP BY department
   HAVING COUNT(employee_id) > 10;
   ```
   This query selects departments with more than 10 employees.

2. **Using Aggregate Functions**:
   ```sql
   SELECT department, AVG(salary) AS avg_salary
   FROM employees
   GROUP BY department
   HAVING AVG(salary) > 50000;
   ```
   This query selects departments where the average salary is greater than 50,000.

3. **Combining with `WHERE`**:
   ```sql
   SELECT department, SUM(salary) AS total_salary
   FROM employees
   WHERE hire_date >= '2020-01-01'
   GROUP BY department
   HAVING SUM(salary) > 100000;
   ```
   This query selects departments where the total salary of employees hired after January 1, 2020, is greater than 100,000.

### Notes
- The `HAVING` clause is used after the `GROUP BY` clause.
- It is particularly useful for filtering groups based on aggregate function results.
