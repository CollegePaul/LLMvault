### Understanding Unique Values in Numpy

In NumPy, unique values refer to the distinct elements present in an array. The function `numpy.unique()` is used to find these unique elements. This function can be very useful when you need to identify all the different types of data in your dataset or when you want to check for duplicates.

#### Basic Usage
The simplest way to use `numpy.unique()` is by passing it an array, and it returns a sorted array of unique values.

```python
import numpy as np

array = np.array([1, 2, 2, 3, 4, 4, 5])
unique_values = np.unique(array)
print(unique_values)  # Output: [1 2 3 4 5]
```

#### Additional Parameters
`numpy.unique()` also supports additional parameters that can provide more information about the unique elements.

- `return_index`: If True, it returns the indices of the first occurrences of the unique values in the original array.
- `return_inverse`: If True, it returns an array of integers representing the index of each element in the unique array.
- `return_counts`: If True, it returns the counts of each unique value.

```python
array = np.array([1, 2, 2, 3, 4, 4, 5])
unique_values, indices, inverse, counts = np.unique(array, return_index=True, return_inverse=True, return_counts=True)
print("Unique values:", unique_values)        # Output: [1 2 3 4 5]
print("Indices:", indices)                    # Output: [0 1 3 4 6]
print("Inverse:", inverse)                    # Output: [0 1 1 2 3 3 4]
print("Counts:", counts)                      # Output: [1 2 1 2 1]
```

#### Using with Multidimensional Arrays
`numpy.unique()` can also be used with multidimensional arrays, but by default, it flattens the array before finding unique values.

```python
array = np.array([[1, 2], [3, 4], [1, 2]])
unique_values = np.unique(array)
print(unique_values)  # Output: [1 2 3 4]
```

To find unique rows or columns, you can use the `axis` parameter.

```python
array = np.array([[1, 2], [3, 4], [1, 2]])
unique_rows = np.unique(array, axis=0)
print(unique_rows)  # Output: [[1 2] [3 4]]
```

### Conclusion
The `numpy.unique()` function is a powerful tool for data manipulation and analysis, allowing you to easily identify unique elements in an array and gather additional information about their distribution.

#Unique Values #Numpy