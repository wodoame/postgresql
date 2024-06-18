The `ADD COLUMN` command is used to add a new column to an existing table in your database. Here's an example of how to use it:

```sql
ALTER TABLE your_table_name
ADD COLUMN new_column_name data_type;
```

This will add a new column named `new_column_name` with the specified `data_type` to the table `your_table_name`. You can also specify additional attributes for the column, such as `NOT NULL` or a default value:

```sql
ALTER TABLE your_table_name
ADD COLUMN new_column_name data_type NOT NULL DEFAULT default_value;
```

Make sure to replace `your_table_name`, `new_column_name`, `data_type`, and `default_value` with your actual table name, new column name, data type, and the default value you want to set.
