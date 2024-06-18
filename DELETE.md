The `DELETE` command is used to remove records from a table in PostgreSQL. Here's a basic example:

```sql
DELETE FROM your_table_name WHERE condition;
```

This command will delete all records that meet the specified condition from the table `your_table_name`. For example, if you want to delete all records where the `age` column is less than 18, you would use:

```sql
DELETE FROM your_table_name WHERE age < 18;
```

Be careful with the `DELETE` command, especially if you omit the `WHERE` clause, as it will remove all records from the table:

```sql
DELETE FROM your_table_name;
```

Always make sure to replace `your_table_name` with your actual table name and specify the appropriate condition for selecting the records to delete.
