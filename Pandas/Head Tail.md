### Explanation of Head and Tail in Pandas

In Pandas, `head()` and `tail()` are methods used to preview the beginning and the end of a DataFrame or Series, respectively. These functions are particularly useful for quickly checking the structure and content of a dataset without having to display all of its data.

- **`head(n)`**: This method returns the first n rows of the DataFrame or Series. By default, `n` is set to 5, meaning it will return the first five rows if no argument is specified.
  
- **`tail(n)`**: Conversely, this method returns the last n rows of the DataFrame or Series, with a default value of 5 as well.

These functions are handy for initial data exploration and ensuring that your dataset has been loaded correctly.

#### Examples

```python
import pandas as pd

# Sample DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David', 'Eve', 'Frank'],
    'Age': [25, 30, 35, 40, 45, 50],
    'City': ['New York', 'Los Angeles', 'Chicago', 'Houston', 'Phoenix', 'Philadelphia']
}

df = pd.DataFrame(data)

# Using head() to see the first few rows
print("First 3 rows of DataFrame:")
print(df.head(3))

# Using tail() to see the last few rows
print("\nLast 2 rows of DataFrame:")
print(df.tail(2))
```

**Output:**
```
First 3 rows of DataFrame:
      Name  Age         City
0    Alice   25     New York
1      Bob   30  Los Angeles
2  Charlie   35      Chicago

Last 2 rows of DataFrame:
    Name  Age        City
4    Eve   45     Phoenix
5  Frank   50  Philadelphia
```

In the examples above, `head(3)` returns the first three rows of the DataFrame, while `tail(2)` returns the last two rows. This allows you to quickly inspect parts of your data without needing to view the entire dataset.

#Head Tail #Pandas #Python