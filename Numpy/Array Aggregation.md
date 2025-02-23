### Array Aggregation in Numpy

Array aggregation in NumPy refers to performing operations that summarize or reduce an array's data into a single scalar value. These operations are useful for statistical analysis, data processing, and more. Common aggregation functions include summing all elements, calculating the mean, finding the minimum or maximum values, and computing variances.

Here are some examples of how you can perform these operations in Python using NumPy:

#### Summation
The `np.sum()` function computes the sum of array elements over a given axis.
```python
import numpy as np

# Create a 2D array
arr = np.array([[1, 2, 3], [4, 5, 6]])

# Compute the total sum of all elements
total_sum = np.sum(arr)
print("Total Sum:", total_sum)  # Output: Total Sum: 21

# Compute the sum along axis 0 (column-wise)
col_sums = np.sum(arr, axis=0)
print("Column Sums:", col_sums)  # Output: Column Sums: [5 7 9]

# Compute the sum along axis 1 (row-wise)
row_sums = np.sum(arr, axis=1)
print("Row Sums:", row_sums)  # Output: Row Sums: [ 6 15]
```

#### Mean
The `np.mean()` function calculates the average of array elements.
```python
# Compute the mean of all elements
mean_all = np.mean(arr)
print("Mean (All Elements):", mean_all)  # Output: Mean (All Elements): 3.5

# Compute the mean along axis 0 (column-wise)
mean_col = np.mean(arr, axis=0)
print("Column Means:", mean_col)  # Output: Column Means: [2.5 3.5 4.5]

# Compute the mean along axis 1 (row-wise)
mean_row = np.mean(arr, axis=1)
print("Row Means:", mean_row)  # Output: Row Means: [2. 5.]
```

#### Minimum and Maximum
The `np.min()` and `np.max()` functions find the smallest and largest elements in an array, respectively.
```python
# Find the minimum value in the entire array
min_val = np.min(arr)
print("Minimum Value:", min_val)  # Output: Minimum Value: 1

# Find the maximum value along axis 0 (column-wise)
max_col = np.max(arr, axis=0)
print("Column Maximums:", max_col)  # Output: Column Maximums: [4 5 6]

# Find the minimum value along axis 1 (row-wise)
min_row = np.min(arr, axis=1)
print("Row Minimums:", min_row)  # Output: Row Minimums: [1 4]
```

#### Variance
The `np.var()` function computes the variance of array elements.
```python
# Compute the variance of all elements
variance_all = np.var(arr)
print("Variance (All Elements):", variance_all)  # Output: Variance (All Elements): 2.916666666666667

# Compute the variance along axis 0 (column-wise)
variance_col = np.var(arr, axis=0)
print("Column Variances:", variance_col)  # Output: Column Variances: [2.25 2.25 2.25]

# Compute the variance along axis 1 (row-wise)
variance_row = np.var(arr, axis=1)
print("Row Variances:", variance_row)  # Output: Row Variances: [0.66666667 0.66666667]
```

These examples illustrate how NumPy can efficiently handle aggregation tasks on arrays. The flexibility of specifying axes allows for detailed analysis along different dimensions of the data.

#Array Aggregation #Numpy