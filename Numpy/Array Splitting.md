### Array Splitting in Numpy

Array splitting in NumPy involves dividing an array into multiple sub-arrays based on specified parameters or conditions. This can be achieved using various functions such as `numpy.split()`, `numpy.array_split()`, and `numpy.hsplit()`/`numpy.vsplit()`.

#### `numpy.split()`

The `numpy.split()` function divides an array into a list of sub-arrays by specifying the indices at which to split the array. The number of splits must be consistent with the shape of the array.

**Example:**

```python
import numpy as np

# Creating a 1D array
arr = np.array([1, 2, 3, 4, 5, 6])

# Splitting the array into three sub-arrays at indices 2 and 4
split_arr = np.split(arr, [2, 4])
print(split_arr)
```

Output:
```
[array([1, 2]), array([3, 4]), array([5, 6])]
```

#### `numpy.array_split()`

The `numpy.array_split()` function is similar to `numpy.split()`, but it allows for the splitting of an array into a specified number of sub-arrays. It can handle cases where the array cannot be split evenly by distributing the extra elements.

**Example:**

```python
import numpy as np

# Creating a 1D array with 9 elements
arr = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9])

# Splitting the array into 4 sub-arrays
split_arr = np.array_split(arr, 4)
print(split_arr)
```

Output:
```
[array([1, 2, 3]), array([4, 5, 6]), array([7, 8]), array([9])]
```

#### `numpy.hsplit()` and `numpy.vsplit()`

These functions are used to split arrays horizontally (`hsplit`) or vertically (`vsplit`). They are particularly useful for multi-dimensional arrays.

**Example:**

```python
import numpy as np

# Creating a 2D array
arr = np.array([[1, 2, 3], [4, 5, 6]])

# Splitting the array horizontally at index 2
h_split_arr = np.hsplit(arr, [2])
print("Horizontal split:\n", h_split_arr)

# Splitting the array vertically into two sub-arrays
v_split_arr = np.vsplit(arr, 2)
print("\nVertical split:\n", v_split_arr)
```

Output:
```
Horizontal split:
 [array([[1, 2],
       [4, 5]]), array([[3],
       [6]])]

Vertical split:
 [array([[1, 2, 3]]), array([[4, 5, 6]])]
```

### Tags

#Array Splitting #Numpy