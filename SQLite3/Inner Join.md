### Inner Join in SQLite3

An Inner Join in SQLite3 is used to combine rows from two or more tables based on a related column between them. The result set will only include rows where there is a match in both tables. Essentially, it returns records that have matching values in the specified columns of both tables.

For example, consider two tables: `employees` and `departments`. Each employee belongs to a department, and this relationship can be established through a common column such as `department_id`.

#### employees table
| employee_id | name     | department_id |
|-------------|----------|---------------|
| 1           | Alice    | 1             |
| 2           | Bob      | 2             |
| 3           | Charlie  | 1             |

#### departments table
| department_id | department_name |
|---------------|-----------------|
| 1             | HR              |
| 2             | Engineering     |

Using an Inner Join, you can combine these tables to get a list of employees along with their respective department names:

```sql
SELECT 
    employees.name, 
    departments.department_name 
FROM 
    employees 
INNER JOIN 
    departments 
ON 
    employees.department_id = departments.department_id;
```

This SQL query will produce the following result set:
| name     | department_name |
|----------|-----------------|
| Alice    | HR              |
| Bob      | Engineering     |
| Charlie  | HR              |

#### Example in Python

Here is how you can perform an Inner Join using SQLite3 in a Python script:

```python
import sqlite3

# Connect to the SQLite database (or create it if it doesn't exist)
conn = sqlite3.connect('example.db')
cursor = conn.cursor()

# Create tables
cursor.execute('''
CREATE TABLE IF NOT EXISTS employees (
    employee_id INTEGER PRIMARY KEY,
    name TEXT,
    department_id INTEGER
)
''')

cursor.execute('''
CREATE TABLE IF NOT EXISTS departments (
    department_id INTEGER PRIMARY KEY,
    department_name TEXT
)
''')

# Insert data into the tables
cursor.execute("INSERT INTO employees (name, department_id) VALUES ('Alice', 1)")
cursor.execute("INSERT INTO employees (name, department_id) VALUES ('Bob', 2)")
cursor.execute("INSERT INTO employees (name, department_id) VALUES ('Charlie', 1)")

cursor.execute("INSERT INTO departments (department_name) VALUES ('HR')")
cursor.execute("INSERT INTO departments (department_name) VALUES ('Engineering')")

# Perform an Inner Join
cursor.execute('''
SELECT 
    employees.name, 
    departments.department_name 
FROM 
    employees 
INNER JOIN 
    departments 
ON 
    employees.department_id = departments.department_id
''')

# Fetch and print the results
results = cursor.fetchall()
for row in results:
    print(row)

# Close the connection
conn.close()
```

Running this Python script will output:
```
('Alice', 'HR')
('Bob', 'Engineering')
('Charlie', 'HR')
```

This example demonstrates how to set up tables, insert data, and perform an Inner Join using SQLite3 in Python. #InnerJoin #SQLite3 #Python