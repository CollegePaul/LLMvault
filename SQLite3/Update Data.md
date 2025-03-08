### Updating Data in SQLite3

Updating data in SQLite3 involves modifying existing records within a database table. This process typically uses the `UPDATE` SQL statement, which allows you to change the values of one or more columns based on specified conditions.

In Python, you can perform updates using the `sqlite3` module, which provides a lightweight disk-based database that doesn’t require a separate server process. Here’s how you can update data in an SQLite3 database with Python:

1. **Connect to the Database**: First, establish a connection to your SQLite3 database.
2. **Create a Cursor Object**: Use this object to execute SQL commands.
3. **Write and Execute the UPDATE Statement**: Specify which table and columns to update along with the conditions.
4. **Commit Changes**: Save the changes made by the `UPDATE` statement.
5. **Close the Connection**: Properly close the connection to free up resources.

#### Example

Let's assume we have a simple table named `employees` with the following schema:

- `id`: INTEGER PRIMARY KEY
- `name`: TEXT NOT NULL
- `age`: INTEGER
- `department`: TEXT

Here’s how you can update the age of an employee whose name is 'John Doe':

```python
import sqlite3

# Connect to SQLite database (or create it if it doesn't exist)
conn = sqlite3.connect('example.db')

# Create a cursor object using the cursor method
cursor = conn.cursor()

# SQL query to UPDATE data
update_query = """
UPDATE employees
SET age = ?
WHERE name = ?;
"""

# Data to be updated
new_age = 35
employee_name = 'John Doe'

# Execute the update statement
cursor.execute(update_query, (new_age, employee_name))

# Commit the changes
conn.commit()

# Check if the update was successful
cursor.execute("SELECT * FROM employees WHERE name = ?", (employee_name,))
updated_employee = cursor.fetchone()
print(updated_employee)

# Close the connection
conn.close()
```

In this example:
- We connect to a database file named `example.db`.
- An `UPDATE` SQL statement is prepared and executed with new age and employee name.
- Changes are committed to the database.
- The updated record is fetched and printed to verify the update.
- Finally, the connection is closed.

#Update Data #SQLite3 #Python