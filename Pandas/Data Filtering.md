### Data Filtering in Pandas

Data filtering in Pandas involves selecting subsets of data based on specific conditions. This is crucial for analyzing and manipulating datasets efficiently. You can filter rows, columns, or entire DataFrame segments using boolean indexing.

#### Basic Filtering with Boolean Indexing:
You can use a condition to return a subset of your data that meets the criteria. For instance, if you have a DataFrame and want to filter rows where a column's value is greater than a certain threshold, you would do so like this:

```python
import pandas as pd

# Sample DataFrame
data = {'Name': ['John', 'Anna', 'James', 'Linda'],
        'Age': [28, 24, 35, 32],
        'City': ['New York', 'Paris', 'London', 'Berlin']}
df = pd.DataFrame(data)

# Filtering rows where Age > 30
filtered_df = df[df['Age'] > 30]
print(filtered_df)
```

**Output:**
```
    Name  Age    City
2  James   35  London
3  Linda   32  Berlin
```

#### Multiple Conditions:
You can also use multiple conditions to filter data. For example, if you want to find people older than 25 and living in 'London':

```python
# Filtering rows where Age > 25 AND City is 'London'
filtered_df = df[(df['Age'] > 25) & (df['City'] == 'London')]
print(filtered_df)
```

**Output:**
```
    Name  Age    City
2  James   35  London
```

#### Using the `.query()` Method:
Alternatively, you can use the `.query()` method for a more readable syntax:

```python
# Using .query() to filter rows where Age > 25 and City is 'London'
filtered_df = df.query('Age > 25 & City == "London"')
print(filtered_df)
```

**Output:**
```
    Name  Age    City
2  James   35  London
```

These examples demonstrate the basics of data filtering in Pandas, allowing you to manipulate and analyze data effectively. #Data Filtering #Pandas #Python