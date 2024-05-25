To **insert new data into a PostgreSQL table**, you can use the `INSERT INTO` statement. Here's the basic syntax:

```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

In this syntax:
- Replace `table_name` with the name of the table where you want to insert data.
- Specify the column names in parentheses after `table_name`.
- Provide the corresponding values in parentheses after the `VALUES` keyword.

For example, let's say we have a table called `links` with columns `id`, `url`, `name`, `description`, and `last_update`. To insert a new row into this table, you can use the following example:

```sql
INSERT INTO links (url, name, description, last_update)
VALUES ('https://example.com', 'Example Website', 'A useful resource', '2024-05-25');
```

This query will insert a new row with the specified values for each column. If you want to return information about the inserted row, you can use the optional `RETURNING` clause.
