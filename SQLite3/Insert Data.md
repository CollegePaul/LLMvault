### Inserting Data in SQLite3

Inserting data into an SQLite database involves using the `INSERT INTO` SQL statement. This statement allows you to add new rows of data to a specific table. In Python, this can be done using the `sqlite3` module, which provides a lightweight disk-based database that doesn’t require a separate server process.

Here’s how you can insert data into an SQLite database using Python:

1. **Connect to the Database:**
   First, establish a connection to your SQLite database file. If the file does not exist, SQLite will create it for you.
   
2. **Create a Cursor Object:**
   A cursor is used to execute SQL commands through Python code.

3. **Write an Insert Statement:**
   Use the `INSERT INTO` statement to specify which table and columns you want to insert data into, along with the values that should be inserted.

4. **Execute the Insert Statement:**
   Execute the SQL command using the cursor object.

5. **Commit the Changes:**
   After executing your commands, don’t forget to commit the changes to make them persistent in the database.

6. **Close the Connection:**
   Finally, close the connection when you are done with it to free up resources.

#### Example

Here is a step-by-step example using Python:

```python
import sqlite3

# Connect to SQLite database (or create it if it doesn't exist)
conn = sqlite3.connect('example.db')

# Create a cursor object to interact with the database
cursor = conn.cursor()

# Create a table named 'employees' if it doesn't already exist
cursor.execute('''
CREATE TABLE IF NOT EXISTS employees (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    age INTEGER,
    department TEXT
)
''')

# Insert data into the 'employees' table
cursor.execute("INSERT INTO employees (name, age, department) VALUES ('Alice', 30, 'HR')")
cursor.execute("INSERT INTO employees (name, age, department) VALUES ('Bob', 25, 'IT')")
cursor.execute("INSERT INTO employees (name, age, department) VALUES ('Charlie', 40, 'Finance')")

# Commit the changes to the database
conn.commit()

# Verify that the data has been inserted by querying it
cursor.execute('SELECT * FROM employees')
rows = cursor.fetchall()
for row in rows:
    print(row)

# Close the connection
conn.close()
```

This script does the following:

- Connects to an SQLite database named `example.db`.
- Creates a table called `employees` if it doesn’t exist.
- Inserts three new records into the `employees` table.
- Commits the changes to ensure they are saved in the database.
- Queries the table and prints out all records to verify that the data has been inserted correctly.
- Closes the connection to clean up.

#Insert Data #SQLite3 #Python