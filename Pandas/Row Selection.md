### Row Selection in Pandas

Row selection in Pandas allows you to choose specific rows from a DataFrame based on certain criteria or conditions. This can be accomplished using methods like `.loc[]`, `.iloc[]`, boolean indexing, or the `query()` method. Each method has its own use case and syntax.

1. **Using .loc[]:**
   - The `.loc[]` method is primarily label-based, but it may also be used with a boolean array.
   
   ```python
   import pandas as pd

   data = {
       'Name': ['Alice', 'Bob', 'Charlie'],
       'Age': [25, 30, 35],
       'Occupation': ['Engineer', 'Doctor', 'Artist']
   }

   df = pd.DataFrame(data)

   # Select rows with index labels
   selected_rows = df.loc[[0, 2]]
   print(selected_rows)
   ```

2. **Using .iloc[]:**
   - The `.iloc[]` method is integer-location based indexing for selection by position.
   
   ```python
   # Select rows by their integer location
   selected_rows = df.iloc[0:2]  # Rows from index 0 to 1 (exclusive of 2)
   print(selected_rows)
   ```

3. **Using Boolean Indexing:**
   - This method involves creating a boolean condition to filter the DataFrame.
   
   ```python
   # Select rows where Age is greater than 28
   selected_rows = df[df['Age'] > 28]
   print(selected_rows)
   ```

4. **Using query() Method:**
   - The `query()` method allows you to write queries in a string format.
   
   ```python
   # Select rows where Occupation is 'Doctor'
   selected_rows = df.query("Occupation == 'Doctor'")
   print(selected_rows)
   ```

These methods provide flexibility and power for selecting specific rows based on various conditions, making data manipulation and analysis more efficient.

#Row Selection #Pandas #Python