Meta commands in PostgreSQL are special commands used within the `psql` interactive terminal to perform various administrative and informational tasks. These commands are also known as "slash commands" because they start with a backslash (`\`). They allow you to interact with the database without writing SQL queries.

### Common Meta Commands

1. **Connecting to a Database**:
   ```sql
   \c [database_name]
   ```
   Connects to the specified database.

2. **Listing Databases**:
   ```sql
   \l
   ```
   Lists all databases.

3. **Listing Tables**:
   ```sql
   \dt
   ```
   Lists all tables in the current database.

4. **Listing Views**:
   ```sql
   \dv
   ```
   Lists all views in the current database.

5. **Listing Indexes**:
   ```sql
   \di
   ```
   Lists all indexes in the current database.

6. **Describing a Table**:
   ```sql
   \d [table_name]
   ```
   Describes the structure of the specified table.

7. **Listing Schemas**:
   ```sql
   \dn
   ```
   Lists all schemas in the current database.

8. **Executing a File**:
   ```sql
   \i [filename]
   ```
   Executes SQL commands from a file.

9. **Timing Queries**:
   ```sql
   \timing
   ```
   Toggles timing of queries on or off.

10. **Exiting `psql`**:
    ```sql
    \q
    ```
    Exits the `psql` terminal.

### Advanced Meta Commands

1. **Setting Variables**:
   ```sql
   \set [variable] [value]
   ```
   Sets an internal variable.

2. **Changing Directory**:
   ```sql
   \cd [directory]
   ```
   Changes the working directory.

3. **Executing Shell Commands**:
   ```sql
   \! [command]
   ```
   Executes a shell command.

4. **Copying Data**:
   ```sql
   \copy [table_name] TO '[file_path]' WITH (FORMAT csv);
   ```
   Copies data from a table to a file.

### Getting Help
To see a full list of meta commands, you can use:
```sql
\?
```
This command displays all available meta commands along with brief descriptions.
