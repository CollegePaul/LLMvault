### Fillna Method in Pandas

The `fillna` method in Pandas is used to fill missing values (NaN) in a DataFrame or Series. It provides several options for filling these missing values, including specifying a value to use, using forward or backward filling methods, and more.

Here are some common ways to use the `fillna` method:

1. **Filling with a specific value:**

   ```python
   import pandas as pd

   # Create a sample DataFrame with NaN values
   data = {'A': [1, 2, None, 4],
           'B': [None, 2, 3, 4]}
   df = pd.DataFrame(data)

   # Fill all NaN values with 0
   filled_df = df.fillna(0)
   print(filled_df)
   ```

   Output:
   ```
       A    B
   0  1.0  0.0
   1  2.0  2.0
   2  0.0  3.0
   3  4.0  4.0
   ```

2. **Forward fill (using the previous value):**

   ```python
   # Forward fill NaN values
   forward_filled_df = df.fillna(method='ffill')
   print(forward_filled_df)
   ```

   Output:
   ```
       A    B
   0  1.0  NaN
   1  2.0  2.0
   2  2.0  3.0
   3  4.0  4.0
   ```

3. **Backward fill (using the next value):**

   ```python
   # Backward fill NaN values
   backward_filled_df = df.fillna(method='bfill')
   print(backward_filled_df)
   ```

   Output:
   ```
       A    B
   0  1.0  2.0
   1  2.0  2.0
   2  4.0  3.0
   3  4.0  4.0
   ```

The `fillna` method is versatile and can be customized to handle missing data in a way that makes sense for your specific dataset and analysis needs.

#Fillna Method #Pandas #Python