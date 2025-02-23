### Value Counts in Pandas

The `value_counts()` function in Pandas is used to count the number of occurrences of each unique value in a Series or DataFrame column. It returns a new Series containing these counts, sorted by the frequency of values in descending order. This function is particularly useful for quick statistical analysis and data exploration, helping you understand the distribution of data within a dataset.

Here’s a simple example to illustrate how `value_counts()` works:

```python
import pandas as pd

# Creating a sample DataFrame
data = {'Fruit': ['Apple', 'Banana', 'Apple', 'Orange', 'Banana', 'Apple']}
df = pd.DataFrame(data)

# Using value_counts() on the 'Fruit' column
fruit_counts = df['Fruit'].value_counts()
print(fruit_counts)
```

Output:
```
Apple     3
Banana    2
Orange    1
Name: Fruit, dtype: int64
```

In this example, `value_counts()` is applied to the 'Fruit' column of a DataFrame. The result shows that "Apple" appears three times, "Banana" twice, and "Orange" once.

#Value Counts #Pandas #Python