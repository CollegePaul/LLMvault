### Sum and Count in Pandas

In Pandas, `sum()` and `count()` are methods used to perform aggregation on DataFrame or Series objects. These functions help in computing numerical data efficiently.

- **`sum()`**: This method calculates the sum of the values for each column or row. By default, it operates along the index (axis=0), meaning it sums up all the rows for each column.
  
- **`count()`**: This method counts the number of non-null entries in each column or row. Like `sum()`, it also works along the index by default.

### Example

Let's consider a simple DataFrame to demonstrate how these methods work:

```python
import pandas as pd

# Creating a sample DataFrame
data = {
    'A': [1, 2, 3],
    'B': [4, None, 6],
    'C': [7, 8, 9]
}

df = pd.DataFrame(data)

print("Original DataFrame:")
print(df)
print("\nSum of each column (default behavior):")
print(df.sum())
print("\nCount of non-null values in each column (default behavior):")
print(df.count())
```

**Output:**

```
Original DataFrame:
     A    B  C
0  1.0  4.0  7
1  2.0  NaN  8
2  3.0  6.0  9

Sum of each column (default behavior):
A     6.0
B    10.0
C    24.0
dtype: float64

Count of non-null values in each column (default behavior):
A    3
B    2
C    3
dtype: int64
```

In this example:
- `df.sum()` computes the sum for columns 'A', 'B', and 'C'.
- `df.count()` counts the non-null entries in each of these columns.

#Sum Count #Pandas #Python