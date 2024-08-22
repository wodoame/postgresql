The `LIMIT` keyword in SQL is used to specify the maximum number of rows that the query should return. It's particularly useful when dealing with large datasets, as it allows you to retrieve only a subset of records.

### Syntax
```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition
LIMIT number_of_rows OFFSET offset_value;
```
- **number_of_rows**: The maximum number of rows to return.
- **offset_value**: The number of rows to skip before starting to return rows (optional).

### Examples

1. **Basic Usage**:
   ```sql
   SELECT * FROM employees LIMIT 5;
   ```
   This query retrieves the first 5 rows from the `employees` table.

2. **Using `LIMIT` with `OFFSET`**:
   ```sql
   SELECT * FROM employees LIMIT 5 OFFSET 10;
   ```
   This query skips the first 10 rows and then retrieves the next 5 rows from the `employees` table.

3. **Ordering Results**:
   ```sql
   SELECT * FROM employees ORDER BY salary DESC LIMIT 3;
   ```
   This query retrieves the top 3 highest-paid employees.

### Notes
- The `LIMIT` clause is supported by most SQL databases, including MySQL and PostgreSQL.
- In some databases like SQL Server, you might use `TOP` instead of `LIMIT`.
- The `OFFSET` clause is optional and can be used to skip a specified number of rows before returning the result set.
