The `RENAME` keyword in SQL is used to change the name of a table or a column. Here's how you can use it:

### Renaming a Table
To rename a table, you use the `ALTER TABLE` statement followed by the `RENAME TO` clause.

#### Syntax
```sql
ALTER TABLE old_table_name RENAME TO new_table_name;
```

#### Example
```sql
ALTER TABLE students RENAME TO student_details;
```
This query renames the `students` table to `student_details`.

### Renaming a Column
To rename a column, you use the `ALTER TABLE` statement followed by the `RENAME COLUMN` clause.

#### Syntax
```sql
ALTER TABLE table_name RENAME COLUMN old_column_name TO new_column_name;
```

#### Example
```sql
ALTER TABLE student_details RENAME COLUMN name TO first_name;
```
This query renames the `name` column to `first_name` in the `student_details` table.

### Notes
- Renaming a table or column does not affect the data within the table.
- Make sure to update any queries or scripts that reference the old table or column name.
