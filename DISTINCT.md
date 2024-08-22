The `DISTINCT` keyword in SQL is used to return only unique (distinct) values from a column or a combination of columns. It's often used to eliminate duplicate rows in the result set.

### Syntax
```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```

### Examples

1. **Single Column**:
   ```sql
   SELECT DISTINCT country
   FROM customers;
   ```
   This query retrieves a list of unique countries from the `customers` table.

2. **Multiple Columns**:
   ```sql
   SELECT DISTINCT first_name, last_name
   FROM employees;
   ```
   This query retrieves unique combinations of first and last names from the `employees` table.

3. **Using `DISTINCT` with `COUNT`**:
   ```sql
   SELECT COUNT(DISTINCT country)
   FROM customers;
   ```
   This query counts the number of unique countries in the `customers` table.

### Notes
- The `DISTINCT` keyword applies to all columns listed in the `SELECT` statement.
- It can be used with aggregate functions like `COUNT` to get the count of unique values.
