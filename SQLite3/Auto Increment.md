### Auto Increment in SQLite3

In SQLite3, there isn't a direct `AUTO_INCREMENT` keyword like in MySQL. Instead, SQLite uses the `INTEGER PRIMARY KEY` to automatically increment the primary key value of a table. When you define a column as `INTEGER PRIMARY KEY`, SQLite will automatically populate this column with an incrementing integer whenever a new row is inserted into the table.

If no rowid is specified on the insert statement, or if NULL is specified, then SQLite generates the rowid automatically using an algorithm that guarantees that the new rowid does not collide with any previously used rowid in the same table. This ensures that each row has a unique identifier.

### Example Using Python

Here’s how you can create a table with an auto-incrementing primary key in SQLite3 and insert data into it using Python:

```python
import sqlite3

# Connect to SQLite database (or create it if it doesn't exist)
connection = sqlite3.connect('example.db')

# Create a cursor object using the cursor method
cursor = connection.cursor()

# Create table with an auto-incrementing primary key
cursor.execute('''CREATE TABLE IF NOT EXISTS users (
                    id INTEGER PRIMARY KEY,
                    name TEXT NOT NULL)''')

# Insert data into the table
cursor.execute("INSERT INTO users (name) VALUES ('Alice')")
cursor.execute("INSERT INTO users (name) VALUES ('Bob')")

# Commit changes and close the connection
connection.commit()

# Query to see all rows in the table
cursor.execute("SELECT * FROM users")
rows = cursor.fetchall()
for row in rows:
    print(row)

# Close the connection
connection.close()
```

In this example, the `id` column is defined as an `INTEGER PRIMARY KEY`, which means it will automatically increment each time a new record is inserted into the `users` table. The output of the script will display all the records with their auto-generated IDs.

#Auto Increment #SQLite3 #Python