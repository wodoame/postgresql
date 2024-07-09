To list all databases in PostgreSQL, you have a couple of options:

1. **Using psql (PostgreSQL command-line tool):**
   - Open your terminal or command prompt.
   - Log in to PostgreSQL using `psql` with the appropriate credentials (e.g., `psql --username=postgres`).
   - To list all databases, type either of the following commands:
     - `\list` or `\l`
     - These commands display the names of all databases available.
   - To switch to a specific database, use:
     - `\connect database_name` or `\c database_name`

2. **Using SQL query directly:**
   - Execute the following SQL query within your PostgreSQL environment:
     ```sql
     SELECT datname FROM pg_database;
     ```
   - This concise query fetches the names of all databases on your PostgreSQL server.

Remember that you won't see tables from other databases unless you connect to the correct database.
