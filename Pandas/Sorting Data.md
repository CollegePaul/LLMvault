### Sorting Data in Pandas

Sorting data is a common task in data analysis and manipulation using Pandas. It allows you to order your DataFrame or Series based on one or more columns, which can make it easier to analyze and visualize the data.

In Pandas, you can sort data using two main functions: `sort_values()` for sorting by column values and `sort_index()` for sorting by index labels.

#### Using `sort_values()`

The `sort_values()` function is used to sort a DataFrame or Series based on its values. You need to specify the column(s) by which you want to sort using the `by` parameter. The `ascending` parameter determines whether the data should be sorted in ascending (default) or descending order.

**Example:**

```python
import pandas as pd

# Creating a sample DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 20],
    'Score': [88.5, 91.0, 78.5]
}
df = pd.DataFrame(data)

# Sorting the DataFrame by 'Age' in ascending order
sorted_df = df.sort_values(by='Age')
print("Sorted by Age (ascending):")
print(sorted_df)
```

Output:
```
      Name  Age  Score
2  Charlie   20   78.5
0    Alice   25   88.5
1      Bob   30   91.0
```

You can also sort by multiple columns:

```python
# Sorting the DataFrame by 'Score' in descending order and then by 'Age' in ascending order
sorted_df = df.sort_values(by=['Score', 'Age'], ascending=[False, True])
print("\nSorted by Score (descending) and Age (ascending):")
print(sorted_df)
```

Output:
```
      Name  Age  Score
1      Bob   30   91.0
0    Alice   25   88.5
2  Charlie   20   78.5
```

#### Using `sort_index()`

The `sort_index()` function is used to sort a DataFrame or Series based on its index labels. The `ascending` parameter works the same way as in `sort_values()`.

**Example:**

```python
# Creating a sample DataFrame with a non-sequential index
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 20],
    'Score': [88.5, 91.0, 78.5]
}
df_indexed = pd.DataFrame(data, index=[2, 1, 3])

# Sorting the DataFrame by its index
sorted_df_indexed = df_indexed.sort_index()
print("\nSorted by Index:")
print(sorted_df_indexed)
```

Output:
```
   Name  Age  Score
1   Bob   30   91.0
2 Alice   25   88.5
3 Charlie   20   78.5
```

These functions provide powerful tools for organizing your data in Pandas, making it easier to perform further analysis and visualization tasks.

#Sorting Data #Pandas #Python