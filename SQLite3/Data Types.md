### Data Types in SQLite3

SQLite uses a dynamic type system that allows flexibility in storing data types. However, it primarily supports the following storage classes:

- **NULL**: Represents a NULL value.
- **INTEGER**: Used for integer values. SQLite can store integers up to 8 bytes (64-bit).
- **REAL**: Stores real numbers or floating-point numbers.
- **TEXT**: Used for text strings. SQLite encodes TEXT as either UTF-8, UTF-16BE, or UTF-16LE.
- **BLOB**: Binary large object, used for storing binary data.

SQLite's flexibility means that you can store a value of any type in any column, and the database will attempt to convert the data to the appropriate type based on context. However, when declaring columns, you can specify an affinity (type hint) for the column:

- **INTEGER**: Forces integer storage.
- **REAL**: Forces real or floating-point storage.
- **TEXT**: Forces string storage in UTF-8.
- **BLOB**: Forces binary data storage.
- **NUMERIC**: Forces numeric storage. SQLite will attempt to convert it to an INTEGER, REAL, or TEXT depending on the content.

### Example Using Python

Here is a simple example of creating a table with different data types and inserting some data using Python:

```python
import sqlite3

# Connect to SQLite database (or create if it doesn't exist)
conn = sqlite3.connect('example.db')
c = conn.cursor()

# Create table with various data type affinities
c.execute('''CREATE TABLE IF NOT EXISTS users (
             id INTEGER PRIMARY KEY,
             username TEXT NOT NULL,
             age INTEGER,
             height REAL,
             is_active BOOLEAN,
             profile_picture BLOB
           )''')

# Insert a row of data into the table
c.execute("INSERT INTO users (username, age, height, is_active) VALUES (?, ?, ?, ?)",
          ('john_doe', 30, 5.9, True))

# Save (commit) the changes
conn.commit()

# Close the connection to the database
conn.close()
```

In this example:
- `id` is an INTEGER and serves as a primary key.
- `username` is TEXT.
- `age` is an INTEGER.
- `height` is REAL.
- `is_active` is BOOLEAN, but SQLite does not have a dedicated BOOLEAN type. It stores TRUE or FALSE as 1 or 0.
- `profile_picture` is BLOB for storing binary data.

#Data_Types #SQLite3 #Python