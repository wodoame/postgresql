Performing mathematical operations on columns in PostgreSQL is straightforward. You can use standard arithmetic operators to perform calculations directly in your SQL queries.

### Basic Arithmetic Operations

1. **Addition**:
   ```sql
   SELECT column1 + column2 AS result
   FROM table_name;
   ```
   This query adds the values of `column1` and `column2`.

2. **Subtraction**:
   ```sql
   SELECT column1 - column2 AS result
   FROM table_name;
   ```
   This query subtracts the values of `column2` from `column1`.

3. **Multiplication**:
   ```sql
   SELECT column1 * column2 AS result
   FROM table_name;
   ```
   This query multiplies the values of `column1` and `column2`.

4. **Division**:
   ```sql
   SELECT column1 / column2 AS result
   FROM table_name;
   ```
   This query divides the values of `column1` by `column2`.

### Using Functions

1. **SUM**:
   ```sql
   SELECT SUM(column_name) AS total
   FROM table_name;
   ```
   This query calculates the sum of all values in `column_name`.

2. **AVG**:
   ```sql
   SELECT AVG(column_name) AS average
   FROM table_name;
   ```
   This query calculates the average of all values in `column_name`.

3. **MIN and MAX**:
   ```sql
   SELECT MIN(column_name) AS minimum, MAX(column_name) AS maximum
   FROM table_name;
   ```
   This query finds the minimum and maximum values in `column_name`.

4. **ROUND**:
   ```sql
   SELECT ROUND(column_name, 2) AS rounded_value
   FROM table_name;
   ```
   This query rounds the values in `column_name` to 2 decimal places.

### Combining Operations

You can also combine multiple operations in a single query:
```sql
SELECT (column1 + column2) * column3 / column4 AS result
FROM table_name;
```
This query performs addition, multiplication, and division in one go.

### Example

Let's say you have a table `sales` with columns `price` and `quantity`, and you want to calculate the total revenue for each row:
```sql
SELECT price * quantity AS total_revenue
FROM sales;
```
