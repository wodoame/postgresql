The `BETWEEN` operator in PostgreSQL is used to filter the result set within a specific range. It can be applied to numbers, text, or dates. Here's a quick overview:

### Syntax
```sql
expression BETWEEN low_value AND high_value;
```
- **expression**: The column or value to be checked.
- **low_value**: The start of the range.
- **high_value**: The end of the range.

### Examples

1. **Numbers**:
   ```sql
   SELECT * FROM products WHERE price BETWEEN 10 AND 20;
   ```
   This query selects all products with a price between 10 and 20.

2. **Dates**:
   ```sql
   SELECT * FROM orders WHERE order_date BETWEEN '2023-01-01' AND '2023-12-31';
   ```
   This query selects all orders placed in the year 2023.

3. **Text**:
   ```sql
   SELECT * FROM employees WHERE last_name BETWEEN 'A' AND 'M';
   ```
   This query selects all employees whose last names fall alphabetically between 'A' and 'M'.

### Notes
- The `BETWEEN` operator is inclusive, meaning it includes the boundary values (`low_value` and `high_value`).
- You can also use `NOT BETWEEN` to exclude a range of values.
