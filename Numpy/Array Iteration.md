### Array Iteration in Numpy

Array iteration in NumPy refers to the process of accessing each element of an array one by one. While iterating over a multi-dimensional array, the elements are accessed row-wise (i.e., along the last axis). However, it's worth noting that for large arrays, using explicit loops can be inefficient, and vectorized operations are generally preferred for performance reasons.

Here’s how you can iterate through an array in NumPy:

**Example 1: Iterating over a one-dimensional array**

```python
import numpy as np

# Creating a 1D array
arr_1d = np.array([1, 2, 3, 4, 5])

# Iterating over the array
for element in arr_1d:
    print(element)
```

**Output:**
```
1
2
3
4
5
```

**Example 2: Iterating over a two-dimensional array**

```python
import numpy as np

# Creating a 2D array
arr_2d = np.array([[1, 2, 3], [4, 5, 6]])

# Iterating over the array (rows)
for row in arr_2d:
    print(row)
```

**Output:**
```
[1 2 3]
[4 5 6]
```

To iterate through each element of a multi-dimensional array, you can use `numpy.nditer`, which is more efficient and flexible.

**Example 3: Using numpy.nditer to iterate over elements**

```python
import numpy as np

# Creating a 2D array
arr_2d = np.array([[1, 2, 3], [4, 5, 6]])

# Iterating over each element using nditer
for element in np.nditer(arr_2d):
    print(element)
```

**Output:**
```
1
2
3
4
5
6
```

### Conclusion

While array iteration is straightforward in NumPy, it's important to leverage vectorized operations whenever possible for better performance. #Array Iteration #Numpy