### Column Addition in Pandas

Column addition in Pandas refers to the process of creating a new column in a DataFrame by performing operations on existing columns or by assigning new data. This operation can involve simple arithmetic, complex calculations, or even conditional logic.

When you add a new column, it becomes part of the DataFrame and can be used for further analysis or transformations. Here's how you can perform column addition:

#### Example 1: Simple Arithmetic

```python
import pandas as pd

# Create a sample DataFrame
data = {'A': [1, 2, 3], 'B': [4, 5, 6]}
df = pd.DataFrame(data)

# Add a new column 'C' which is the sum of columns 'A' and 'B'
df['C'] = df['A'] + df['B']

print(df)
```

**Output:**
```
   A  B  C
0  1  4  5
1  2  5  7
2  3  6  9
```

In this example, column 'C' is created by adding the values of columns 'A' and 'B'.

#### Example 2: Using Conditional Logic

```python
# Add a new column 'D' which marks rows where the sum in 'C' is greater than 7 as 'High', otherwise 'Low'
df['D'] = df['C'].apply(lambda x: 'High' if x > 7 else 'Low')

print(df)
```

**Output:**
```
   A  B  C     D
0  1  4  5   Low
1  2  5  7   Low
2  3  6  9  High
```

Here, column 'D' is created based on a condition applied to the values in column 'C'.

#### Example 3: Using Vectorized Operations

```python
# Create another column 'E' which is the square of column 'A'
df['E'] = df['A'] ** 2

print(df)
```

**Output:**
```
   A  B  C     D  E
0  1  4  5   Low  1
1  2  5  7   Low  4
2  3  6  9  High  9
```

In this example, column 'E' is created using a vectorized operation to square each element in column 'A'.

Column addition in Pandas is a powerful feature that allows for dynamic data manipulation and analysis. #Column Addition #Pandas #Python