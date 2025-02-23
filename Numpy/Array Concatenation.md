### Array Concatenation in Numpy

Array concatenation in NumPy allows you to join arrays along an existing axis. This operation can be performed using several functions, but the most commonly used ones are `numpy.concatenate`, `numpy.vstack`, and `numpy.hstack`.

1. **`numpy.concatenate((a1, a2, ...), axis=0)`**:
   - Joins arrays along the specified axis.
   - If `axis=0`, it stacks them vertically (row-wise).
   - If `axis=1`, it stacks them horizontally (column-wise).

2. **`numpy.vstack(tup)`**:
   - Stacks arrays in sequence vertically (row-wise).
   - It is equivalent to `numpy.concatenate((a1, a2, ...), axis=0)`.

3. **`numpy.hstack(tup)`**:
   - Stacks arrays in sequence horizontally (column-wise).
   - It is equivalent to `numpy.concatenate((a1, a2, ...), axis=1)` for 2D arrays.

#### Examples

```python
import numpy as np

# Example 1: Using numpy.concatenate with axis=0
array1 = np.array([[1, 2], [3, 4]])
array2 = np.array([[5, 6], [7, 8]])
result_concat_axis0 = np.concatenate((array1, array2), axis=0)
print("Concatenated along axis=0:\n", result_concat_axis0)

# Example 2: Using numpy.concatenate with axis=1
result_concat_axis1 = np.concatenate((array1, array2), axis=1)
print("\nConcatenated along axis=1:\n", result_concat_axis1)

# Example 3: Using numpy.vstack
result_vstack = np.vstack((array1, array2))
print("\nStacked vertically using vstack:\n", result_vstack)

# Example 4: Using numpy.hstack
result_hstack = np.hstack((array1, array2))
print("\nStacked horizontally using hstack:\n", result_hstack)
```

**Output**:
```
Concatenated along axis=0:
 [[1 2]
 [3 4]
 [5 6]
 [7 8]]

Concatenated along axis=1:
 [[1 2 5 6]
 [3 4 7 8]]

Stacked vertically using vstack:
 [[1 2]
 [3 4]
 [5 6]
 [7 8]]

Stacked horizontally using hstack:
 [[1 2 5 6]
 [3 4 7 8]]
```

#Array Concatenation #Numpy