### Count Function in SQLite3

The `COUNT()` function in SQLite3 is an aggregate function used to count the number of rows that match a specified condition. It can be used with or without a `WHERE` clause. The basic syntax is:

```sql
SELECT COUNT(column_name) FROM table_name WHERE condition;
```

If you omit the column name and use an asterisk (`*`), it counts all rows, including those with NULL values.

#### Examples Using Python

Here are some examples demonstrating how to use the `COUNT()` function in SQLite3 using Python:

1. **Counting All Rows**

   ```python
   import sqlite3

   # Connect to a database or create one if it doesn't exist
   conn = sqlite3.connect('example.db')
   cursor = conn.cursor()

   # Create a table
   cursor.execute('''CREATE TABLE IF NOT EXISTS employees (
                       id INTEGER PRIMARY KEY,
                       name TEXT NOT NULL,
                       department TEXT NOT NULL
                   )''')

   # Insert some data
   cursor.executemany('INSERT INTO employees (name, department) VALUES (?, ?)', [
       ('Alice', 'HR'),
       ('Bob', 'Engineering'),
       ('Charlie', 'Marketing'),
       ('David', 'HR')
   ])

   # Commit the changes
   conn.commit()

   # Count all rows in the table
   cursor.execute('SELECT COUNT(*) FROM employees')
   row_count = cursor.fetchone()[0]
   print(f'Total number of employees: {row_count}')

   # Close the connection
   conn.close()
   ```

2. **Counting Rows with a Condition**

   ```python
   import sqlite3

   # Connect to the database
   conn = sqlite3.connect('example.db')
   cursor = conn.cursor()

   # Count rows in a specific department
   cursor.execute("SELECT COUNT(*) FROM employees WHERE department = 'HR'")
   hr_count = cursor.fetchone()[0]
   print(f'Number of HR employees: {hr_count}')

   # Close the connection
   conn.close()
   ```

3. **Counting Non-NULL Values**

   ```python
   import sqlite3

   # Connect to the database
   conn = sqlite3.connect('example.db')
   cursor = conn.cursor()

   # Insert a row with NULL department
   cursor.execute("INSERT INTO employees (name, department) VALUES ('Eve', NULL)")
   conn.commit()

   # Count non-NULL departments
   cursor.execute("SELECT COUNT(department) FROM employees")
   non_null_department_count = cursor.fetchone()[0]
   print(f'Number of employees with a specified department: {non_null_department_count}')

   # Close the connection
   conn.close()
   ```

#Count Function #SQLite3 #Python