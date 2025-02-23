### Min Function in SQLite3

The `MIN` function in SQLite3 is an aggregate function used to return the smallest value from a set of values. It's particularly useful when you need to find the minimum value in a specific column of a table.

#### Syntax:
```sql
SELECT MIN(column_name) FROM table_name;
```

#### Example:
Suppose you have a table named `products` with the following data:

| product_id | product_name | price |
|------------|--------------|-------|
| 1          | Product A    | 20.5  |
| 2          | Product B    | 30.7  |
| 3          | Product C    | 19.8  |

To find the minimum price in the `products` table, you can use the `MIN` function as follows:

```sql
SELECT MIN(price) FROM products;
```

This query would return:

| min(price) |
|------------|
| 19.8       |

#### Using Python with SQLite3:
Here is an example of how to use the `MIN` function in a Python script using the `sqlite3` module.

```python
import sqlite3

# Connect to the database (or create it if it doesn't exist)
conn = sqlite3.connect('example.db')
cursor = conn.cursor()

# Create a table and insert some data
cursor.execute('''
CREATE TABLE IF NOT EXISTS products (
    product_id INTEGER PRIMARY KEY,
    product_name TEXT,
    price REAL
);
''')

cursor.execute("INSERT INTO products (product_name, price) VALUES ('Product A', 20.5)")
cursor.execute("INSERT INTO products (product_name, price) VALUES ('Product B', 30.7)")
cursor.execute("INSERT INTO products (product_name, price) VALUES ('Product C', 19.8)")

# Commit the changes
conn.commit()

# Use the MIN function to find the minimum price
cursor.execute('SELECT MIN(price) FROM products')
min_price = cursor.fetchone()[0]

print(f"The minimum price is: {min_price}")

# Close the connection
conn.close()
```

This script creates a table, inserts some data, and then uses the `MIN` function to retrieve and print the minimum price from the `products` table. #Min Function #SQLite3 #Python