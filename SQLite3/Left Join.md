### Left Join in SQLite3

A Left Join in SQLite3 is used to combine rows from two or more tables based on a related column between them. The result set includes all records from the left table, and the matched records from the right table. If there is no match, the result is NULL on the side of the right table.

#### Syntax:
```sql
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.common_column = table2.common_column;
```

### Example Using Python

Let's consider two tables: `employees` and `departments`. The `employees` table has an `employee_id` that is also a foreign key in the `departments` table.

```python
import sqlite3

# Create connection to SQLite database (or create it if it doesn't exist)
conn = sqlite3.connect('example.db')
cursor = conn.cursor()

# Create tables
cursor.execute('''
CREATE TABLE IF NOT EXISTS employees (
    employee_id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    department_id INTEGER,
    FOREIGN KEY(department_id) REFERENCES departments(department_id)
)
''')

cursor.execute('''
CREATE TABLE IF NOT EXISTS departments (
    department_id INTEGER PRIMARY KEY,
    department_name TEXT NOT NULL
)
''')

# Insert some data into the tables
employees_data = [
    (1, 'Alice', 1),
    (2, 'Bob', 2),
    (3, 'Charlie', None)  # Charlie does not belong to any department
]

departments_data = [
    (1, 'HR'),
    (2, 'Engineering')
]

cursor.executemany('INSERT INTO employees VALUES (?, ?, ?)', employees_data)
cursor.executemany('INSERT INTO departments VALUES (?, ?)', departments_data)

# Perform a Left Join query
cursor.execute('''
SELECT employees.name, departments.department_name
FROM employees
LEFT JOIN departments ON employees.department_id = departments.department_id
''')

# Fetch and print the results
results = cursor.fetchall()
for row in results:
    print(row)

# Close connection
conn.close()
```

#### Output:
```
('Alice', 'HR')
('Bob', 'Engineering')
('Charlie', None)
```

In this example, the query returns all employees along with their department names. Charlie, who does not belong to any department, has `None` in the `department_name` column.

#Left Join #SQLite3 #Python