### Array Indexing in Numpy

Array indexing in NumPy allows you to access specific elements or subarrays within a NumPy array using index positions. Similar to Python lists, indexing starts at 0. However, NumPy provides more advanced capabilities for multidimensional arrays.

#### Basic Indexing:

For one-dimensional arrays, you can access individual elements by specifying their index position:

```python
import numpy as np

# Creating a 1D numpy array
arr_1d = np.array([10, 20, 30, 40, 50])

# Accessing the third element (index 2)
print(arr_1d[2])  # Output: 30
```

For multidimensional arrays, you can use tuples to specify indices for each dimension:

```python
# Creating a 2D numpy array
arr_2d = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Accessing the element at second row and third column (index (1, 2))
print(arr_2d[1, 2])  # Output: 6
```

#### Slicing:

You can also use slicing to extract subarrays. The general syntax is `start:end:step` where `end` is non-inclusive.

```python
# Slicing a 1D array to get elements from index 1 to 3 (non-inclusive)
print(arr_1d[1:4])  # Output: [20 30 40]

# Slicing a 2D array to get the first two rows and all columns
print(arr_2d[:2, :])  
# Output:
# [[1 2 3]
#  [4 5 6]]
```

#### Boolean Indexing:

Boolean indexing allows you to filter elements based on conditions.

```python
# Using boolean indexing to get all elements greater than 20
bool_mask = arr_1d > 20
print(arr_1d[bool_mask])  # Output: [30 40 50]
```

#### Fancy Indexing:

Fancy indexing involves using integer arrays or lists to specify which indices to access.

```python
# Using fancy indexing with a list of indices
indices = [0, 2, 4]
print(arr_1d[indices])  # Output: [10 30 50]

# Using fancy indexing on a 2D array
rows = np.array([0, 2])
cols = np.array([0, 2])
print(arr_2d[rows, cols])  
# Output:
# [1 9]
```

Array Indexing in NumPy is a powerful feature that provides various methods to access and manipulate elements efficiently. #ArrayIndexing #Numpy