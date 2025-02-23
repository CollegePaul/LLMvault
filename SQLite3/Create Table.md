### Create Table in SQLite3

In SQLite3, the `CREATE TABLE` statement is used to create a new table within a database. This statement allows you to define the structure of the table by specifying the column names and their data types. Here's a basic syntax:

```sql
CREATE TABLE table_name (
    column1 datatype PRIMARY KEY,
    column2 datatype NOT NULL,
    column3 datatype,
    ...
);
```

- `table_name` is the name of the new table.
- Each `column` represents a different attribute or field within the table.
- `datatype` specifies what kind of data can be stored in each column (e.g., INTEGER, TEXT, REAL).
- Constraints like `PRIMARY KEY`, `NOT NULL`, and others can be applied to define rules about how data is handled.

### Example Using Python

Here’s an example using Python to create a table in SQLite3:

```python
import sqlite3

# Connect to SQLite database (or create it if it doesn't exist)
conn = sqlite3.connect('example.db')

# Create a cursor object using the cursor method
cursor = conn.cursor()

# SQL command to create a table
create_table_command = """
CREATE TABLE IF NOT EXISTS employees (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    position TEXT,
    salary REAL
);
"""

# Execute the command
cursor.execute(create_table_command)

# Commit the changes
conn.commit()

# Close the connection
conn.close()
```

In this example, we first import the `sqlite3` module and establish a connection to a database file named `example.db`. We then create a cursor object to execute SQL commands. The `CREATE TABLE` statement defines a table called `employees` with four columns: `id`, `name`, `position`, and `salary`. The `id` column is set as the primary key, ensuring each record has a unique identifier. After executing the command, we commit our changes to the database and close the connection.

#Create Table #SQLite3 #Python