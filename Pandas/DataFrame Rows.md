### DataFrame Rows in Pandas

In Pandas, a DataFrame is a two-dimensional labeled data structure with columns of potentially different types. Each row in a DataFrame represents an individual record or observation. Rows can be accessed using various methods such as `.iloc`, `.loc`, and by boolean indexing.

Here are some examples to illustrate how you can work with rows in a DataFrame:

#### Example 1: Accessing a Single Row Using `iloc`
```python
import pandas as pd

# Creating a sample DataFrame
data = {
    'Name': ['Alice', 'Bob', 'Charlie'],
    'Age': [25, 30, 35],
    'City': ['New York', 'Los Angeles', 'Chicago']
}
df = pd.DataFrame(data)

# Accessing the second row using iloc
second_row = df.iloc[1]
print(second_row)
```
**Output:**
```
Name         Bob
Age           30
City    Los Angeles
Name: 1, dtype: object
```

#### Example 2: Accessing Multiple Rows Using `iloc`
```python
# Accessing the first and third rows using iloc
first_and_third_rows = df.iloc[[0, 2]]
print(first_and_third_rows)
```
**Output:**
```
      Name  Age     City
0    Alice   25   New York
2  Charlie   35    Chicago
```

#### Example 3: Accessing Rows Using `loc` with Labels
First, let's set an index based on a column:
```python
# Setting 'Name' as the index
df.set_index('Name', inplace=True)

# Accessing rows using loc
alice_row = df.loc['Alice']
print(alice_row)
```
**Output:**
```
Age        25.0
City    New York
Name: Alice, dtype: object
```

#### Example 4: Filtering Rows Using Boolean Indexing
```python
# Resetting index for demonstration
df.reset_index(inplace=True)

# Accessing rows where Age is greater than 30 using boolean indexing
adults = df[df['Age'] > 30]
print(adults)
```
**Output:**
```
      Name  Age     City
2  Charlie   35    Chicago
```

These examples demonstrate various ways to access and manipulate DataFrame rows in Pandas, making it a powerful tool for data manipulation and analysis. #DataFrame Rows #Pandas #Python