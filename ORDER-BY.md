In PostgreSQL, the `ORDER BY` clause allows you to sort the result set of a query based on one or more columns. Here's how it works:

1. **Sorting by One Column:**
   - To sort rows by a single column, use the following syntax:
     ```sql
     SELECT column1, column2, ...
     FROM table_name
     ORDER BY column1 [ASC | DESC];
     ```
   - Replace `column1` with the column you want to sort by. By default, it sorts in ascending order (ASC), but you can specify descending order (DESC) explicitly.

2. **Example - Sorting by First Name (Ascending):**
   ```sql
   SELECT first_name, last_name
   FROM customer
   ORDER BY first_name ASC;
   ```
   This query sorts customers by their first names in ascending order.

3. **Example - Sorting by Last Name (Descending):**
   ```sql
   SELECT first_name, last_name
   FROM customer
   ORDER BY last_name DESC;
   ```
   This query sorts customers by their last names in descending order.

4. **Sorting by Multiple Columns:**
   - To sort by multiple columns, separate them with commas:
     ```sql
     SELECT first_name, last_name
     FROM customer
     ORDER BY first_name ASC, last_name DESC;
     ```
   - This query sorts by first name (ascending) and then by last name (descending).

Remember that the `ORDER BY` clause is handy for arranging query results in a specific order.
