### Data Transformation in Pandas

Data transformation in Pandas refers to the process of converting or altering data from one format or structure to another. This can involve operations such as changing data types, normalizing values, handling missing data, filtering rows based on conditions, aggregating data, and reshaping datasets. These transformations are crucial for preparing data for analysis, machine learning, or visualization.

Here are some common data transformation techniques in Pandas along with examples:

1. **Changing Data Types**:
   You can change the data type of a column using `astype()`.

   ```python
   import pandas as pd

   df = pd.DataFrame({
       'Age': ['25', '30', '45']
   })
   df['Age'] = df['Age'].astype(int)
   ```

2. **Handling Missing Data**:
   Use methods like `fillna()`, `dropna()` to handle missing data.

   ```python
   df = pd.DataFrame({
       'Salary': [50000, None, 60000]
   })
   df['Salary'].fillna(55000, inplace=True)
   ```

3. **Filtering Rows**:
   Filter rows based on a condition using boolean indexing.

   ```python
   df = pd.DataFrame({
       'Score': [82, 91, 74]
   })
   filtered_df = df[df['Score'] > 80]
   ```

4. **Aggregating Data**:
   Use aggregation functions like `sum()`, `mean()`, `groupby()` to summarize data.

   ```python
   df = pd.DataFrame({
       'Department': ['HR', 'Tech', 'HR'],
       'Salary': [50000, 60000, 55000]
   })
   average_salary_by_dept = df.groupby('Department')['Salary'].mean()
   ```

5. **Reshaping Data**:
   Use `pivot()`, `melt()` to reshape data for better analysis.

   ```python
   df = pd.DataFrame({
       'Year': [2021, 2021, 2022],
       'Quarter': ['Q1', 'Q4', 'Q1'],
       'Revenue': [150, 300, 180]
   })
   pivot_df = df.pivot(index='Year', columns='Quarter', values='Revenue')
   ```

6. **Applying Functions**:
   Use `apply()` to apply a function along an axis of the DataFrame.

   ```python
   def increment(value):
       return value + 10

   df = pd.DataFrame({
       'Price': [100, 200, 300]
   })
   df['Updated Price'] = df['Price'].apply(increment)
   ```

Data transformation is a fundamental aspect of data manipulation in Pandas, enabling users to clean and prepare their datasets effectively for further analysis. #Data Transformation #Pandas #Python