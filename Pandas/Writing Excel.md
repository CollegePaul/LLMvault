### Writing Excel in Pandas

When working with data analysis in Python, Pandas offers robust tools for handling data efficiently. One common task is writing data to an Excel file. This can be accomplished using the `pandas.ExcelWriter` class or the `DataFrame.to_excel()` method.

The `to_excel()` function allows you to export a DataFrame directly into an Excel spreadsheet. It's straightforward and provides several parameters to customize the output, such as sheet name, starting row/column, and formatting options.

Here are some examples of how to use these methods:

#### Example 1: Writing a DataFrame to a Single Sheet

```python
import pandas as pd

# Create a sample DataFrame
data = {'Name': ['Alice', 'Bob', 'Charlie'],
        'Age': [25, 30, 35]}
df = pd.DataFrame(data)

# Write the DataFrame to an Excel file
df.to_excel('output.xlsx', sheet_name='Sheet1', index=False)
```

In this example, a simple DataFrame is created and written to `output.xlsx` under the sheet named 'Sheet1'. The `index=False` parameter ensures that the row indices are not written into the Excel file.

#### Example 2: Writing Multiple DataFrames to Different Sheets

```python
import pandas as pd

# Create sample DataFrames
data1 = {'Fruit': ['Apple', 'Banana'],
         'Quantity': [10, 5]}
df1 = pd.DataFrame(data1)

data2 = {'Vegetable': ['Carrot', 'Broccoli'],
         'Quantity': [8, 4]}
df2 = pd.DataFrame(data2)

# Create an Excel writer object
with pd.ExcelWriter('output.xlsx') as writer:
    df1.to_excel(writer, sheet_name='Fruits', index=False)
    df2.to_excel(writer, sheet_name='Vegetables', index=False)
```

This example demonstrates how to write two different DataFrames into separate sheets within the same Excel file using `pandas.ExcelWriter`. The `with` statement ensures that the writer is properly closed after writing.

#### Example 3: Formatting the Output

Pandas can also apply basic formatting to your data in Excel. Here’s an example:

```python
import pandas as pd

# Create a sample DataFrame
data = {'Name': ['Alice', 'Bob', 'Charlie'],
        'Age': [25, 30, 35]}
df = pd.DataFrame(data)

# Write the DataFrame to an Excel file with some formatting
with pd.ExcelWriter('output.xlsx') as writer:
    df.to_excel(writer, sheet_name='Sheet1', index=False)
    worksheet = writer.sheets['Sheet1']
    
    # Apply basic formatting using openpyxl
    for idx, col in enumerate(df):  # loop through all columns
        series = df[col]
        max_len = max((
            series.astype(str).map(len).max(),  # len of largest item
            len(str(series.name))  # len of column name/header
        )) + 1  # adding a little extra space
        worksheet.set_column(idx, idx, max_len)  # set column width
```

This example shows how to adjust the column widths in Excel based on the length of the data using `openpyxl` (which Pandas uses under the hood for Excel writing).

#Writing Excel #Pandas #Python