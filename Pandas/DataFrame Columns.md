### Understanding DataFrame Columns in Pandas

DataFrame Columns in Pandas represent the different variables or attributes in your dataset. Each column can be thought of as a single feature or variable, containing data of the same type across its entries. You can perform various operations on DataFrame columns such as selecting, modifying, deleting, and analyzing them.

Here are some basic examples to demonstrate how you can work with DataFrame Columns using Python:

1. **Creating a DataFrame:**

   ```python
   import pandas as pd

   data = {
       'Name': ['Alice', 'Bob', 'Charlie'],
       'Age': [25, 30, 35],
       'City': ['New York', 'Los Angeles', 'Chicago']
   }

   df = pd.DataFrame(data)
   print(df)
   ```

   Output:
   ```
     Name  Age         City
   0  Alice   25     New York
   1    Bob   30  Los Angeles
   2  Charlie   35      Chicago
   ```

2. **Selecting Columns:**

   You can select a single column or multiple columns from the DataFrame.

   ```python
   # Selecting a single column
   print(df['Name'])

   # Selecting multiple columns
   print(df[['Name', 'City']])
   ```

3. **Adding a New Column:**

   You can add new data to your DataFrame by creating a new column.

   ```python
   df['Employed'] = [True, False, True]
   print(df)
   ```

4. **Modifying an Existing Column:**

   Existing columns can be modified or transformed.

   ```python
   # Doubling the age
   df['Age'] = df['Age'] * 2
   print(df)
   ```

5. **Deleting a Column:**

   Columns can be deleted using the `drop` method.

   ```python
   df.drop('Employed', axis=1, inplace=True)
   print(df)
   ```

These examples illustrate some of the common operations you can perform on DataFrame columns in Pandas. #DataFrame Columns #Pandas #Python