### Join Tables in SQLite3

In SQLite3, joining tables allows you to combine rows from two or more tables based on a related column between them. This operation is performed using SQL JOIN statements, which can be classified into several types such as INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL OUTER JOIN (though FULL OUTER JOIN is not directly supported in SQLite but can be simulated).

- **INNER JOIN**: Returns rows when there is at least one match in both tables.
- **LEFT JOIN** (or LEFT OUTER JOIN): Returns all rows from the left table, and matched rows from the right table. If no match is found, NULLs are returned for columns from the right table.
- **RIGHT JOIN** (or RIGHT OUTER JOIN): Returns all rows from the right table, and matched rows from the left table. If no match is found, NULLs are returned for columns from the left table. Note that SQLite does not support RIGHT JOIN directly but can be achieved using LEFT JOIN with tables swapped.
- **FULL OUTER JOIN**: Returns rows when there is a match in one of the tables. Since SQLite does not have a FULL OUTER JOIN, you would typically use a UNION of an INNER JOIN and two LEFT JOINs.

#### Example Using Python

Here’s how you can perform these joins using Python with SQLite3:

```python
import sqlite3

# Connect to SQLite database (or create it if it doesn't exist)
connection = sqlite3.connect('example.db')
cursor = connection.cursor()

# Create sample tables
cursor.execute('''
CREATE TABLE IF NOT EXISTS employees (
    id INTEGER PRIMARY KEY,
    name TEXT,
    department_id INTEGER
);
''')

cursor.execute('''
CREATE TABLE IF NOT EXISTS departments (
    id INTEGER PRIMARY KEY,
    name TEXT
);
''')

# Insert sample data into the tables
cursor.executemany('INSERT INTO employees (name, department_id) VALUES (?, ?)', [
    ('Alice', 1),
    ('Bob', 2),
    ('Charlie', NULL)
])

cursor.executemany('INSERT INTO departments (name) VALUES (?)', [
    ('HR'),
    ('Engineering')
])

# Commit changes
connection.commit()

# Perform an INNER JOIN
print("INNER JOIN:")
for row in cursor.execute('''
SELECT employees.name, departments.name 
FROM employees 
INNER JOIN departments ON employees.department_id = departments.id;
'''):
    print(row)

# Perform a LEFT JOIN
print("\nLEFT JOIN:")
for row in cursor.execute('''
SELECT employees.name, departments.name 
FROM employees 
LEFT JOIN departments ON employees.department_id = departments.id;
'''):
    print(row)

# Close the connection
connection.close()
```

This script sets up two tables: `employees` and `departments`. It then inserts some sample data into these tables and performs both an INNER JOIN and a LEFT JOIN to demonstrate how they work.

### Explanation Tags

#Join Tables #SQLite3 #Python