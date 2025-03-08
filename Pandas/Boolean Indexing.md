### Boolean Indexing in Pandas

Boolean indexing in Pandas allows for filtering data based on conditions. This method involves creating a boolean condition that is applied to a DataFrame or Series, returning only the rows (or elements) where the condition evaluates to `True`. 

For example, consider a simple DataFrame containing information about students:

```python
import pandas as pd

# Create a sample DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Age': [25, 30, 35, 40],
    'Score': [88, 92, 78, 85]
}

df = pd.DataFrame(data)
```

To filter out students who are older than 30, you can use boolean indexing:

```python
# Boolean condition to filter rows where Age is greater than 30
condition = df['Age'] > 30

# Apply the condition to the DataFrame
filtered_df = df[condition]

print(filtered_df)
```

This will output:

```
      Name  Age  Score
2  Charlie   35     78
3    David   40     85
```

You can also combine multiple conditions using logical operators like `&` (and), `|` (or), and `~` (not). For example, to find students who are older than 28 and have a score greater than 90:

```python
# Combined boolean condition
condition = (df['Age'] > 28) & (df['Score'] > 90)

# Apply the combined condition
filtered_df = df[condition]

print(filtered_df)
```

This will output:

```
   Name  Age  Score
1   Bob   30     92
```

Boolean indexing is a powerful tool for data manipulation, enabling you to easily filter and analyze subsets of your data based on specific criteria. #BooleanIndexing #Pandas #Python