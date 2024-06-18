The `ALTER COLUMN` command is part of the `ALTER TABLE` statement and is used to change the definition of an existing column in a table. Here's how you can use it to change a column's data type:

```sql
ALTER TABLE your_table_name
ALTER COLUMN column_name TYPE new_data_type;
```

And here's how to set a default value for a column:

```sql
ALTER TABLE your_table_name
ALTER COLUMN column_name SET DEFAULT default_value;
```

To remove a default value from a column:

```sql
ALTER TABLE your_table_name
ALTER COLUMN column_name DROP DEFAULT;
```

Make sure to replace `your_table_name`, `column_name`, `new_data_type`, and `default_value` with your actual table name, column name, new data type, and default value.
