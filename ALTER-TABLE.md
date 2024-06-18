The `ALTER TABLE` command is used to modify the existing structure of a table in your database. You can use it to add, delete, or modify columns as well as change the data type of a column. Here's an example of how to add a new column to a table:

```sql
ALTER TABLE your_table_name ADD COLUMN new_column_name data_type;
```

And here's how to modify an existing column's data type:

```sql
ALTER TABLE your_table_name ALTER COLUMN column_name TYPE new_data_type;
```

Remember to replace `your_table_name`, `new_column_name`, `column_name`, `data_type`, and `new_data_type` with your actual table and column names and the respective data types.
