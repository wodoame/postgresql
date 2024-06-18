The `TRUNCATE TABLE` command is used to quickly remove all records from a table in PostgreSQL. It's similar to the `DELETE` command without a `WHERE` clause but is more efficient and doesn't generate individual row delete actions. Here's how you use it:

```sql
TRUNCATE TABLE your_table_name;
```

This will immediately delete all records from the table `your_table_name`. It's a very powerful command and should be used with caution, as it cannot be rolled back if you're not in a transaction block.

If you want to truncate multiple tables at once, you can list them separated by commas:

```sql
TRUNCATE TABLE table_name1, table_name2;
```

Make sure to replace `your_table_name`, `table_name1`, and `table_name2` with your actual table names.
