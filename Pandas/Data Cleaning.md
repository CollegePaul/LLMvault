### Data Cleaning in Pandas

Data cleaning in Pandas involves preparing raw data for analysis by identifying and correcting (or removing) errors and inconsistencies. This process typically includes handling missing values, filtering out irrelevant information, correcting inconsistent data formats, and dealing with outliers. Pandas provides a variety of functions that make these tasks straightforward.

#### Handling Missing Values
Missing data can be handled using methods like `dropna()` to remove rows or columns with missing values, or `fillna()` to fill them with specific values.

```python
import pandas as pd

# Create a sample DataFrame with missing values
data = {'Name': ['Alice', 'Bob', None, 'David'],
        'Age': [25, 30, 22, None],
        'City': ['New York', 'Los Angeles', 'Chicago', 'Houston']}
df = pd.DataFrame(data)

# Display the DataFrame with missing values
print("Original DataFrame:")
print(df)

# Drop rows with any missing values
df_cleaned = df.dropna()
print("\nDataFrame after dropping rows with missing values:")
print(df_cleaned)

# Fill missing values with a specific value
df_filled = df.fillna({'Name': 'Unknown', 'Age': 0})
print("\nDataFrame after filling missing values:")
print(df_filled)
```

#### Filtering and Removing Duplicates
Duplicate rows can be removed using the `drop_duplicates()` method. Additionally, data can be filtered based on conditions.

```python
# Create a sample DataFrame with duplicate entries
data = {'Name': ['Alice', 'Bob', 'Bob', 'David'],
        'Age': [25, 30, 30, 22],
        'City': ['New York', 'Los Angeles', 'Los Angeles', 'Chicago']}
df = pd.DataFrame(data)

# Display the DataFrame with duplicates
print("\nOriginal DataFrame:")
print(df)

# Remove duplicate rows based on all columns
df_no_duplicates = df.drop_duplicates()
print("\nDataFrame after removing duplicates:")
print(df_no_duplicates)

# Filter data for ages greater than 25
filtered_df = df[df['Age'] > 25]
print("\nFiltered DataFrame (age > 25):")
print(filtered_df)
```

#### Correcting Data Formats and Types
Data types can be converted using `astype()`, and string operations can be used to clean text data.

```python
# Create a sample DataFrame with inconsistent formats
data = {'Name': ['Alice', 'Bob', 'CHARLIE'],
        'Age': [25, 30, 22],
        'Salary': ['25000', '30000.5', '$40,000']}
df = pd.DataFrame(data)

# Display the original DataFrame
print("\nOriginal DataFrame:")
print(df)

# Convert the 'Name' column to lowercase
df['Name'] = df['Name'].str.lower()
print("\nDataFrame after converting 'Name' to lowercase:")
print(df)

# Remove dollar signs and commas from 'Salary', then convert to float
df['Salary'] = df['Salary'].str.replace('[\$,]', '', regex=True).astype(float)
print("\nDataFrame after cleaning 'Salary':")
print(df)

# Change data type of the 'Age' column
df['Age'] = df['Age'].astype(int)
print("\nDataFrame with corrected data types:")
print(df.dtypes)
```

#### Dealing with Outliers
Outliers can be detected and handled using statistical methods. For example, values outside 1.5 times the interquartile range (IQR) from the first or third quartiles can be considered outliers.

```python
# Create a sample DataFrame with potential outliers
data = {'Name': ['Alice', 'Bob', 'Charlie', 'David'],
        'Age': [25, 30, 100, 22],
        'Salary': [25000, 30000.5, 90000, 40000]}
df = pd.DataFrame(data)

# Display the original DataFrame
print("\nOriginal DataFrame:")
print(df)

# Calculate IQR for 'Age' and filter out outliers
Q1 = df['Age'].quantile(0.25)
Q3 = df['Age'].quantile(0.75)
IQR = Q3 - Q1
age_outliers = (df['Age'] < (Q1 - 1.5 * IQR)) | (df['Age'] > (Q3 + 1.5 * IQR))
filtered_df = df[~age_outliers]
print("\nDataFrame after removing age outliers:")
print(filtered_df)
```

This overview covers some of the essential techniques for data cleaning in Pandas, leveraging its powerful tools to prepare datasets efficiently and effectively. #Data Cleaning #Pandas #Python