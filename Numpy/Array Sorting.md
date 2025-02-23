### Array Sorting in Numpy

Numpy provides several functions to sort arrays efficiently. These functions can be used to sort entire arrays or specific axes within multi-dimensional arrays. The primary function used for sorting is `numpy.sort()`, which returns a new array that is sorted, leaving the original array unchanged.

Another useful function is `numpy.argsort()`, which returns the indices that would sort an array. This can be particularly handy when you need to perform operations based on the order of elements but want to keep the original array intact.

Here are some examples demonstrating these functions:

#### Example 1: Using `numpy.sort()`

```python
import numpy as np

# Creating a simple array
arr = np.array([5, 2, 9, 1, 3])

# Sorting the array
sorted_arr = np.sort(arr)

print("Original array:", arr)
print("Sorted array:", sorted_arr)
```

#### Example 2: Using `numpy.argsort()`

```python
import numpy as np

# Creating a simple array
arr = np.array([5, 2, 9, 1, 3])

# Getting the indices that would sort the array
indices = np.argsort(arr)

print("Original array:", arr)
print("Indices that would sort the array:", indices)
```

#### Example 3: Sorting a multi-dimensional array

```python
import numpy as np

# Creating a 2D array
arr_2d = np.array([[10, 5], [2, 8]])

# Sorting each column (axis=0) of the array
sorted_by_col = np.sort(arr_2d, axis=0)

# Sorting each row (axis=1) of the array
sorted_by_row = np.sort(arr_2d, axis=1)

print("Original 2D array:\n", arr_2d)
print("Sorted by columns:\n", sorted_by_col)
print("Sorted by rows:\n", sorted_by_row)
```

#### Example 4: Using `numpy.ndarray.sort()`

This method sorts the array in place, modifying the original array.

```python
import numpy as np

# Creating a simple array
arr = np.array([5, 2, 9, 1, 3])

# Sorting the array in place
arr.sort()

print("Sorted array:", arr)
```

These examples illustrate different ways to sort arrays using Numpy. Whether you need to keep the original data intact or modify it, and whether you're working with one-dimensional or multi-dimensional arrays, Numpy provides flexible options to suit your needs.

#Array Sorting #Numpy