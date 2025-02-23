### Order By in SQLite3

The `ORDER BY` clause in SQLite3 is used to sort the result-set returned by a `SELECT` statement. It allows you to specify one or more columns to determine the order of the rows in the output. The sorting can be done in ascending (ASC) or descending (DESC) order, with ascending being the default.

**Basic Syntax:**

```sql
SELECT column1, column2, ...
FROM table_name
ORDER BY column1 [ASC|DESC], column2 [ASC|DESC], ...;
```

- `column1`, `column2`: The columns you want to retrieve.
- `table_name`: The name of the table from which to retrieve data.
- `[ASC|DESC]`: Optional. Specifies whether the sorting should be in ascending or descending order. If not specified, ascending is assumed.

**Example:**

Suppose we have a table named `employees` with columns `id`, `name`, and `salary`. To retrieve all employees sorted by their salary in ascending order:

```sql
SELECT id, name, salary FROM employees ORDER BY salary;
```

To sort the employees by their salary in descending order:

```sql
SELECT id, name, salary FROM employees ORDER BY salary DESC;
```

**Using Python with SQLite3:**

Here's how you can use `ORDER BY` with a SQLite database in Python.

```python
import sqlite3

# Connect to an existing SQLite database (or create one if it doesn't exist)
conn = sqlite3.connect('example.db')

# Create a cursor object using the cursor() method
cursor = conn.cursor()

# Create table
cursor.execute('''CREATE TABLE IF NOT EXISTS employees 
                  (id INTEGER PRIMARY KEY, name TEXT, salary REAL)''')

# Insert some data into the table
employees_data = [(1, 'Alice', 50000),
                  (2, 'Bob', 45000),
                  (3, 'Charlie', 60000)]
cursor.executemany('INSERT INTO employees VALUES (?, ?, ?)', employees_data)

# Commit the changes
conn.commit()

# Fetch all rows from the table sorted by salary in ascending order
cursor.execute('SELECT id, name, salary FROM employees ORDER BY salary')
ascending_order = cursor.fetchall()
print("Ascending Order:", ascending_order)

# Fetch all rows from the table sorted by salary in descending order
cursor.execute('SELECT id, name, salary FROM employees ORDER BY salary DESC')
descending_order = cursor.fetchall()
print("Descending Order:", descending_order)

# Close the connection to the database
conn.close()
```

In this example, after creating and populating a table with employee data, we retrieve the data sorted by salary in both ascending and descending order using the `ORDER BY` clause. #Order By #SQLite3 #Python