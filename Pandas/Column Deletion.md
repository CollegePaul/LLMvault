### Column Deletion in Pandas

In Pandas, deleting columns from a DataFrame can be accomplished using the `drop()` method or by directly using the `del` statement. The `drop()` method is more flexible as it allows you to specify which axis (rows or columns) you are dropping and whether or not to modify the DataFrame in place.

#### Using the `drop()` Method

The `drop()` method can be used to remove one or more columns by specifying their names along with setting the `axis` parameter to 1 (since we want to drop a column, not a row).

```python
import pandas as pd

# Create a sample DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35],
    'City': ['New York', 'Los Angeles', 'Chicago']
}
df = pd.DataFrame(data)

# Drop the 'Age' column using drop()
df_dropped_age = df.drop('Age', axis=1)
print(df_dropped_age)
```

In this example, the 'Age' column is removed from `df`, and a new DataFrame `df_dropped_age` is created without the 'Age' column.

#### Using the `del` Statement

The `del` statement can be used to delete columns directly by referencing them. This method modifies the original DataFrame.

```python
# Delete the 'City' column using del
del df['City']
print(df)
```

After this code is executed, the 'City' column will be removed from the original DataFrame `df`.

#### In-Place Deletion

Both methods can be used to modify the DataFrame in place by setting the `inplace` parameter of the `drop()` method to `True`, or by using the `del` statement which inherently modifies the DataFrame.

```python
# Drop the 'Name' column in place using drop()
df.drop('Name', axis=1, inplace=True)
print(df)
```

After running this code, the original DataFrame `df` will no longer contain the 'Name' column.

#Column Deletion #Pandas #Python