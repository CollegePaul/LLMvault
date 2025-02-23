### Data Inspection in Pandas

Data inspection in Pandas involves examining the dataset to understand its structure, contents, and any issues that might need addressing before further analysis. This step is crucial as it helps in identifying missing values, data types, and other anomalies that could affect subsequent analyses.

Pandas provides several functions for inspecting data:

1. **`head()`**: Displays the first few rows of the DataFrame.
2. **`tail()`**: Displays the last few rows of the DataFrame.
3. **`info()`**: Provides a concise summary of the DataFrame, including the number of non-null entries and the data types of each column.
4. **`describe()`**: Generates descriptive statistics for numerical columns, such as mean, median, standard deviation, etc.
5. **`isnull().sum()`**: Counts the number of missing values in each column.

#### Examples

```python
import pandas as pd

# Create a sample DataFrame
data = {
    'Name': ['Alice', 'Bob', None, 'David'],
    'Age': [25, 30, 22, None],
    'City': ['New York', 'Los Angeles', 'Chicago', 'Houston']
}

df = pd.DataFrame(data)

# Display the first few rows
print("First few rows:")
print(df.head())

# Display the last few rows
print("\nLast few rows:")
print(df.tail())

# Get a concise summary of the DataFrame
print("\nDataFrame Info:")
print(df.info())

# Generate descriptive statistics
print("\nDescriptive Statistics:")
print(df.describe())

# Count missing values in each column
print("\nMissing Values:")
print(df.isnull().sum())
```

#### Output

```
First few rows:
     Name   Age         City
0   Alice  25.0     New York
1     Bob  30.0  Los Angeles
2    None  22.0      Chicago
3   David   NaN      Houston

Last few rows:
     Name   Age         City
0   Alice  25.0     New York
1     Bob  30.0  Los Angeles
2    None  22.0      Chicago
3   David   NaN      Houston

DataFrame Info:
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 4 entries, 0 to 3
Data columns (total 3 columns):
 #   Column  Non-Null Count  Dtype  
---  ------  --------------  -----  
 0   Name    3 non-null      object 
 1   Age     2 non-null      float64
 2   City    4 non-null      object 
dtypes: float64(1), object(2)
memory usage: 208.0+ bytes

Descriptive Statistics:
         Age
count  2.000000
mean  27.500000
std   3.535534
min  22.000000
25%  24.750000
50%  27.500000
75%  30.250000
max  30.000000

Missing Values:
Name    1
Age     2
City    0
dtype: int64
```

#Data Inspection #Pandas #Python