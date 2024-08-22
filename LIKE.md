The `LIKE` operator in PostgreSQL is used to search for a specified pattern in a column. It's often used in the `WHERE` clause to filter rows based on partial matches. The `LIKE` operator supports two wildcards:

- **%**: Represents zero, one, or multiple characters.
- **_**: Represents a single character.

### Syntax
```sql
SELECT column1, column2, ...
FROM table_name
WHERE column_name LIKE pattern;
```

### Examples

1. **Basic Usage**:
   ```sql
   SELECT * FROM customers WHERE customer_name LIKE 'A%';
   ```
   This query selects all customers whose names start with 'A'.

2. **Using the `%` Wildcard**:
   ```sql
   SELECT * FROM products WHERE product_name LIKE '%phone%';
   ```
   This query selects all products that contain the word 'phone' anywhere in their name.

3. **Using the `_` Wildcard**:
   ```sql
   SELECT * FROM employees WHERE first_name LIKE 'J_n';
   ```
   This query selects all employees whose first names have 'J' as the first character and 'n' as the third character, with any character in between (e.g., 'Jan', 'Jon').

4. **Combining Wildcards**:
   ```sql
   SELECT * FROM addresses WHERE street LIKE '1_%_St';
   ```
   This query selects all addresses that start with '1', followed by any single character, followed by any number of characters, and ending with 'St'.

### Notes
- The `LIKE` operator is case-sensitive in PostgreSQL. For case-insensitive pattern matching, you can use the `ILIKE` operator.
- You can also use `NOT LIKE` to exclude patterns.
