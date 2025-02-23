### Execute Query in SQLite3

Executing queries in SQLite3 involves using SQL commands to interact with an SQLite database. This can be done through various operations such as SELECT, INSERT, UPDATE, DELETE, etc. In Python, you typically use the `sqlite3` module to perform these operations. The process generally includes connecting to a database (or creating one if it doesn't exist), executing your SQL commands, and then closing the connection.

Here's a step-by-step explanation with examples using Python:

1. **Import the sqlite3 module**:
   ```python
   import sqlite3
   ```

2. **Connect to an SQLite database**:
   This will create a new database if it doesn't already exist.
   ```python
   conn = sqlite3.connect('example.db')
   ```

3. **Create a cursor object**:
   The cursor is used to execute SQL commands.
   ```python
   cursor = conn.cursor()
   ```

4. **Execute an SQL command using the cursor**:
   For example, creating a new table:
   ```python
   cursor.execute('''CREATE TABLE IF NOT EXISTS users (
                     id INTEGER PRIMARY KEY,
                     name TEXT NOT NULL,
                     age INTEGER)''')
   ```

5. **Insert data into the table**:
   You can use placeholders (`?`) in your SQL commands to safely insert values.
   ```python
   cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ('Alice', 30))
   conn.commit()  # Committing changes to the database
   ```

6. **Query data from the table**:
   Use the `SELECT` statement to fetch data.
   ```python
   cursor.execute("SELECT * FROM users")
   rows = cursor.fetchall()
   for row in rows:
       print(row)
   ```

7. **Close the connection**:
   It's important to close the database connection when you're done.
   ```python
   conn.close()
   ```

### Example Code

Here is a complete example that puts all these steps together:

```python
import sqlite3

# Connect to SQLite database (or create it)
conn = sqlite3.connect('example.db')

# Create a cursor object using the connection
cursor = conn.cursor()

# Create table if it doesn't exist
cursor.execute('''CREATE TABLE IF NOT EXISTS users (
                  id INTEGER PRIMARY KEY,
                  name TEXT NOT NULL,
                  age INTEGER)''')

# Insert a new row into the 'users' table
cursor.execute("INSERT INTO users (name, age) VALUES (?, ?)", ('Alice', 30))
conn.commit()

# Query all rows from the 'users' table
cursor.execute("SELECT * FROM users")
rows = cursor.fetchall()
for row in rows:
    print(row)

# Close the connection to the database
conn.close()
```

This script will create a new SQLite database named `example.db`, create a `users` table if it doesn't exist, insert a new user into the table, query all users from the table, and then close the connection.

#Execute Query #SQLite3 #Python