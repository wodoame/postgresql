The `DROP COLUMN` command is used to delete a column from an existing table. Here's how you can use it:

```sql
ALTER TABLE your_table_name
DROP COLUMN column_name;
```

This will remove the column named `column_name` from the table `your_table_name`. Be cautious when using this command, as it will permanently delete the column and all the data contained within it.

If you want to delete a column but ensure that the command only executes if the column exists, you can use the `IF EXISTS` clause:

```sql
ALTER TABLE your_table_name
DROP COLUMN IF EXISTS column_name;
```

Make sure to replace `your_table_name` and `column_name` with your actual table name and column name.
