The `GROUP BY` command in PostgreSQL is used to arrange identical data into groups. This is particularly useful when you want to perform aggregate functions like `COUNT`, `SUM`, `AVG`, `MAX`, or `MIN` on each group.

### Syntax
```sql
SELECT column1, aggregate_function(column2)
FROM table_name
WHERE condition
GROUP BY column1;
```

### Examples

1. **Basic Usage**:
   ```sql
   SELECT department, COUNT(employee_id) AS num_employees
   FROM employees
   GROUP BY department;
   ```
   This query counts the number of employees in each department.

2. **Using Multiple Columns**:
   ```sql
   SELECT department, job_title, AVG(salary) AS avg_salary
   FROM employees
   GROUP BY department, job_title;
   ```
   This query calculates the average salary for each job title within each department.

3. **With `HAVING` Clause**:
   ```sql
   SELECT department, SUM(salary) AS total_salary
   FROM employees
   GROUP BY department
   HAVING SUM(salary) > 100000;
   ```
   This query calculates the total salary for each department but only includes departments where the total salary exceeds 100,000.

4. **Combining with `ORDER BY`**:
   ```sql
   SELECT department, COUNT(employee_id) AS num_employees
   FROM employees
   GROUP BY department
   ORDER BY num_employees DESC;
   ```
   This query counts the number of employees in each department and orders the results by the number of employees in descending order.

### Notes
- The `GROUP BY` clause must appear after the `WHERE` clause and before the `ORDER BY` clause.
- Columns that are not part of an aggregate function must be included in the `GROUP BY` clause.
