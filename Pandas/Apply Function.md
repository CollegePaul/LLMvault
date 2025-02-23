### Apply Function in Pandas

The `apply` function in Pandas is a versatile tool that allows users to apply a specific function along an axis of a DataFrame or to individual elements of a Series. It's particularly useful when you need to perform operations that aren't directly supported by built-in Pandas functions.

#### Key Points:

- **Function Application**: You can use `apply` to apply a custom function to the rows or columns of a DataFrame, or to each element of a Series.
- **Axis Parameter**: The `axis` parameter determines whether the function is applied row-wise (`axis=0`) or column-wise (`axis=1`). By default, it applies column-wise.
- **Return Type**: The return type of the `apply` function depends on the function you use and how it processes the data.

#### Examples:

**Example 1: Applying a Function to a Series**

```python
import pandas as pd

# Create a simple DataFrame
data = {'A': [1, 2, 3], 'B': [4, 5, 6]}
df = pd.DataFrame(data)

# Define a custom function
def square(x):
    return x ** 2

# Apply the function to each element in column 'A'
squared_A = df['A'].apply(square)
print(squared_A)
```

Output:
```
0     1
1     4
2     9
Name: A, dtype: int64
```

**Example 2: Applying a Function to Rows of a DataFrame**

```python
# Define a function that sums the elements in each row
def sum_row(row):
    return row['A'] + row['B']

# Apply the function to each row
df['Sum'] = df.apply(sum_row, axis=1)
print(df)
```

Output:
```
   A  B  Sum
0  1  4    5
1  2  5    7
2  3  6    9
```

**Example 3: Using a Lambda Function**

```python
# Use a lambda function to multiply each element in column 'B' by 10
df['B'] = df['B'].apply(lambda x: x * 10)
print(df)
```

Output:
```
   A   B  Sum
0  1  40    5
1  2  50    7
2  3  60    9
```

### Conclusion

The `apply` function is a powerful feature in Pandas that allows for flexible data manipulation. Whether you're working with Series or DataFrames, it provides the means to apply custom logic efficiently.

#Apply Function #Pandas #Python