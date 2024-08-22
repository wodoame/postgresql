The `CASE` statement in PostgreSQL is used to add conditional logic to your queries, similar to `if/else` statements in programming languages. It allows you to execute different expressions based on certain conditions.

### Syntax
There are two forms of the `CASE` statement: **simple** and **searched**.

#### Simple CASE
```sql
CASE expression
    WHEN value1 THEN result1
    WHEN value2 THEN result2
    ...
    [ELSE else_result]
END
```

#### Searched CASE
```sql
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    ...
    [ELSE else_result]
END
```

### Examples

1. **Simple CASE**:
   ```sql
   SELECT product_name,
          CASE category_id
              WHEN 1 THEN 'Electronics'
              WHEN 2 THEN 'Clothing'
              WHEN 3 THEN 'Furniture'
              ELSE 'Other'
          END AS category
   FROM products;
   ```
   This query categorizes products based on their `category_id`.

2. **Searched CASE**:
   ```sql
   SELECT employee_name,
          CASE
              WHEN salary > 80000 THEN 'High'
              WHEN salary BETWEEN 50000 AND 80000 THEN 'Medium'
              ELSE 'Low'
          END AS salary_range
   FROM employees;
   ```
   This query classifies employees into salary ranges.

3. **Using CASE in WHERE Clause**:
   ```sql
   SELECT *
   FROM orders
   WHERE CASE
             WHEN order_status = 'Pending' THEN order_date > '2024-01-01'
             ELSE true
         END;
   ```
   This query filters orders based on their status and date.

4. **Using CASE with Aggregate Functions**:
   ```sql
   SELECT department,
          COUNT(employee_id) AS num_employees,
          CASE
              WHEN AVG(salary) > 70000 THEN 'High'
              ELSE 'Low'
          END AS avg_salary_level
   FROM employees
   GROUP BY department;
   ```
   This query groups employees by department and classifies the average salary level.

### Notes
- The `CASE` statement can be used in `SELECT`, `WHERE`, `GROUP BY`, and `HAVING` clauses.
- If no condition is met and there is no `ELSE` clause, the `CASE` statement returns `NULL`.
