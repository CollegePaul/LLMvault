### Group By in SQLite3

The `GROUP BY` clause in SQL, including SQLite3, is used to arrange identical data into groups. This clause comes in handy when combined with aggregate functions like COUNT(), SUM(), AVG(), MAX(), and MIN() to perform calculations on each group of rows.

For instance, if you have a table named `sales` containing columns `product_id`, `quantity`, and `price`, you can use the `GROUP BY` clause to find out the total quantity sold for each product.

Here’s an example using Python with SQLite3:

```python
import sqlite3

# Create a connection to a new or existing database
conn = sqlite3.connect('example.db')
cursor = conn.cursor()

# Create a table
cursor.execute('''
CREATE TABLE IF NOT EXISTS sales (
    id INTEGER PRIMARY KEY,
    product_id TEXT NOT NULL,
    quantity INTEGER NOT NULL,
    price REAL NOT NULL
)
''')

# Insert sample data into the table
cursor.executemany('INSERT INTO sales (product_id, quantity, price) VALUES (?, ?, ?)', [
    ('A', 20, 15.99),
    ('B', 10, 23.45),
    ('A', 15, 15.99),
    ('C', 5, 8.75),
    ('B', 20, 23.45)
])

# Commit the changes
conn.commit()

# Query to find total quantity sold for each product using GROUP BY
cursor.execute('''
SELECT product_id, SUM(quantity) AS total_quantity
FROM sales
GROUP BY product_id
''')

# Fetch and print the results
results = cursor.fetchall()
for row in results:
    print(f"Product ID: {row[0]}, Total Quantity Sold: {row[1]}")

# Close the connection
conn.close()
```

In this example, the `SELECT` statement along with `GROUP BY` groups the rows by `product_id` and calculates the sum of `quantity` for each group using the `SUM()` function.

### Output:
```
Product ID: A, Total Quantity Sold: 35
Product ID: B, Total Quantity Sold: 30
Product ID: C, Total Quantity Sold: 5
```

#Group By #SQLite3 #Python