### Where Function in Numpy

The `where` function in NumPy is used to select elements from two arrays based on a condition. It can also be used to find indices where a condition is true within an array. The basic syntax of the `where` function is:

```python
numpy.where(condition[, x, y])
```

- **condition**: This is the array-like input that represents the condition to test element-wise.
- **x**: Optional array-like input from which elements are chosen if the condition is true.
- **y**: Optional array-like input from which elements are chosen if the condition is false.

If both `x` and `y` are not specified, the function returns the indices of elements in an input array where the condition is True.

#### Examples

1. **Finding Indices Where Condition is True:**

```python
import numpy as np

arr = np.array([1, 3, 5, 7, 9])
indices = np.where(arr > 4)
print(indices)  # Output: (array([2, 3, 4]),)
```

In this example, `np.where(arr > 4)` returns the indices of elements in `arr` that are greater than 4.

2. **Selecting Elements Based on a Condition:**

```python
import numpy as np

x = np.array([10, 20, 30, 40, 50])
y = np.array([1, 2, 3, 4, 5])
result = np.where(x > 25, x, y)
print(result)  # Output: [ 1  2 30 40 50]
```

Here, `np.where(x > 25, x, y)` returns an array where elements from `x` are chosen if the condition is true; otherwise, elements from `y`.

#Where Function #Numpy