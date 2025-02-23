### Describe Method in Pandas

The `describe()` method in Pandas is used to generate descriptive statistics that summarize the central tendency, dispersion, and shape of a dataset’s distribution, excluding NaN values. By default, it provides information about numerical columns such as count, mean, standard deviation, minimum value, 25th percentile (Q1), median (50th percentile or Q2), 75th percentile (Q3), and maximum value.

The `describe()` method can also be customized to include statistics for non-numeric data by using the `include` parameter. Setting `include='all'` will provide statistics for all columns, including objects and categorical types, while `exclude` can be used to exclude specific column types.

#### Examples

```python
import pandas as pd

# Creating a sample DataFrame
data = {
    'Age': [25, 30, 35, 40, 45],
    'Salary': [50000, 60000, 70000, 80000, 90000],
    'Department': ['HR', 'Engineering', 'Marketing', 'Finance', 'Sales']
}

df = pd.DataFrame(data)

# Using describe() on the DataFrame
print(df.describe())
```

Output:
```
           Age     Salary
count   5.000000   5.000000
mean   35.000000  70000.000000
std    11.180340  15811.388301
min    25.000000  50000.000000
25%    30.000000  60000.000000
50%    35.000000  70000.000000
75%    40.000000  80000.000000
max    45.000000  90000.000000
```

In this example, `describe()` provides statistics for the numerical columns 'Age' and 'Salary'. The 'Department' column is ignored because it contains non-numeric data.

To include all columns in the description:

```python
# Using describe() with include='all'
print(df.describe(include='all'))
```

Output:
```
         Age     Salary Department
count   5.00      5.00        5.0
mean   35.00  70000.00       NaN
std    11.18  15811.39       NaN
min    25.00   50000.00      Finance
25%    30.00   60000.00     HR
50%    35.00   70000.00 Marketing
75%    40.00   80000.00       Sales
max    45.00   90000.00      Engineering
unique     NaN        NaN        5.0
top      NaN        NaN      Finance
freq       NaN        NaN        1.0
```

In this second example, `describe()` includes statistics for all columns, including the 'Department' column, which is of object type.

#Describe Method #Pandas #Python