The `DROP TABLE` command is used to delete a table and its data from the PostgreSQL database. Here's the basic syntax:

```sql
DROP TABLE your_table_name;
```

This command will remove the specified table `your_table_name` and all of its data permanently. If you want to ensure that the command only executes if the table exists, you can use the `IF EXISTS` clause:

```sql
DROP TABLE IF EXISTS your_table_name;
```

This will prevent an error if the table does not exist. Be very careful with this command, as it will completely remove the table structure and data with no way to recover it unless you have a backup.

Make sure to replace `your_table_name` with your actual table name.
