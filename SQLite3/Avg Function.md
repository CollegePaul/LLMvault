### Avg Function in SQLite3

The `AVG` function in SQLite3 is an aggregate function used to calculate the average value of a numeric column. It takes one argument, which is the name of the column whose values you want to average. The function returns the mean value of all non-NULL values in that column.

**Example:**

Suppose you have a table named `students` with columns `id`, `name`, and `score`. To find the average score of all students, you would use the following SQL query:

```sql
SELECT AVG(score) FROM students;
```

If you want to calculate the average score for a specific condition, such as students in a particular class or those above a certain age, you can add a `WHERE` clause. For example, to find the average score of students who scored more than 50:

```sql
SELECT AVG(score) FROM students WHERE score > 50;
```

**Example Using Python:**

Here’s how you can use the `AVG` function in SQLite3 with Python:

```python
import sqlite3

# Connect to SQLite database (or create it if it doesn't exist)
connection = sqlite3.connect('example.db')

# Create a cursor object using the cursor method
cursor = connection.cursor()

# Create table
cursor.execute('''CREATE TABLE IF NOT EXISTS students
             (id INTEGER PRIMARY KEY, name TEXT, score REAL)''')

# Insert data into table
students_data = [
    (1, 'Alice', 85.5),
    (2, 'Bob', 70.0),
    (3, 'Charlie', 90.5),
    (4, 'David', 65.0)
]

cursor.executemany('INSERT INTO students VALUES (?, ?, ?)', students_data)

# Commit the changes
connection.commit()

# Calculate average score using AVG function
cursor.execute('SELECT AVG(score) FROM students')
average_score = cursor.fetchone()[0]
print(f'Average Score: {average_score}')

# Close the connection
connection.close()
```

In this example, a SQLite database is created and connected to, a table named `students` is defined and populated with data. The average score of all students is then calculated using the `AVG` function, and the result is printed.

#Avg Function #SQLite3 #Python