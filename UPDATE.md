The `UPDATE` command is used to modify existing records in a table. Here's a basic example of how to use it:

```sql
UPDATE your_table_name
SET column1 = value1, column2 = value2
WHERE condition;
```

This will update `column1` to `value1` and `column2` to `value2` for all rows that meet the specified condition. Make sure to replace `your_table_name`, `column1`, `column2`, `value1`, `value2`, and the `condition` with your actual table name, column names, values you want to set, and the condition for selecting rows.

## Example
Let's say you have a table named `employees` with columns `id`, `name`, and `salary`. If you want to give a raise to an employee with a specific ID, you would use the following command:

```sql
UPDATE employees
SET salary = salary + 5000
WHERE id = 4;
```

This command increases the salary by 5000 for the employee whose ID is 4.

If you want to update the name of an employee based on their current name, you could use:

```sql
UPDATE employees
SET name = 'John Doe'
WHERE name = 'John Smith';
```

This command changes the name from 'John Smith' to 'John Doe'.

Remember to replace `employees`, `id`, `name`, and `salary` with your actual table and column names, and adjust the values and conditions according to your needs.
