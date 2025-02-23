### Explanation of Sort Values in Pandas

The `sort_values` method in Pandas is used to sort DataFrame or Series data by one or more columns. It allows you to specify whether the sorting should be in ascending or descending order, and it can handle missing values during the sorting process.

#### Basic Usage:
- **axis**: Specifies the axis along which to sort. `axis=0` (default) sorts rows, and `axis=1` sorts columns.
- **by**: The column name(s) by which to sort the DataFrame.
- **ascending**: Boolean or list of booleans indicating whether each column should be sorted in ascending order. If a single boolean value is used, it applies to all specified columns.
- **na_position**: Controls where NaNs are placed in the sort result. Valid options are 'first' and 'last'.

#### Example Usage:

```python
import pandas as pd

# Create a sample DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David'],
    'Age': [25, 30, None, 22],
    'Salary': [70000, 80000, 65000, 90000]
}

df = pd.DataFrame(data)

# Sort the DataFrame by Age in ascending order
sorted_df_asc = df.sort_values(by='Age', ascending=True)
print("Sorted by Age (Ascending):")
print(sorted_df_asc)

# Sort the DataFrame by Salary in descending order and place NaNs at the end
sorted_df_desc = df.sort_values(by='Salary', ascending=False, na_position='last')
print("\nSorted by Salary (Descending) with NaNs last:")
print(sorted_df_desc)
```

#### Output:
```
Sorted by Age (Ascending):
      Name   Age  Salary
3    David  22.0   90000
0    Alice  25.0   70000
1      Bob  30.0   80000
2  Charlie   NaN   65000

Sorted by Salary (Descending) with NaNs last:
      Name   Age  Salary
3    David  22.0   90000
1      Bob  30.0   80000
0    Alice  25.0   70000
2  Charlie   NaN   65000
```

#Sort Values #Pandas #Python