### Array Arithmetic in Numpy

Numpy provides efficient array operations that allow element-wise arithmetic between arrays, as well as between arrays and scalars. This means that you can perform operations like addition, subtraction, multiplication, and division directly on arrays without the need for explicit loops.

For example, consider two numpy arrays `a` and `b`:

```python
import numpy as np

a = np.array([1, 2, 3])
b = np.array([4, 5, 6])

# Element-wise addition
addition_result = a + b
print("Element-wise Addition:", addition_result)  # Output: [5 7 9]

# Element-wise subtraction
subtraction_result = a - b
print("Element-wise Subtraction:", subtraction_result)  # Output: [-3 -3 -3]

# Element-wise multiplication
multiplication_result = a * b
print("Element-wise Multiplication:", multiplication_result)  # Output: [4 10 18]

# Element-wise division
division_result = a / b
print("Element-wise Division:", division_result)  # Output: [0.25 0.4  0.5]
```

In these examples, each operation is applied element-wise across the arrays `a` and `b`. You can also perform arithmetic operations with scalars:

```python
scalar = 3

# Addition of a scalar to an array
add_scalar_result = a + scalar
print("Addition with Scalar:", add_scalar_result)  # Output: [4 5 6]

# Multiplication of an array with a scalar
mul_scalar_result = a * scalar
print("Multiplication with Scalar:", mul_scalar_result)  # Output: [3 6 9]
```

In the case of operations between arrays and scalars, the scalar is applied to each element in the array.

### Broadcasting

Numpy also supports broadcasting, which allows arithmetic operations between arrays of different shapes. The smaller array is "broadcast" across the larger array so that they have compatible shapes for element-wise operations:

```python
c = np.array([[1, 2], [3, 4]])

# Broadcasting a scalar to an array
broadcast_add_result = c + 5
print("Broadcast Addition:", broadcast_add_result)  
# Output: 
# [[6 7]
#  [8 9]]

# Broadcasting arrays with different shapes
d = np.array([10, 20])
broadcast_mul_result = c * d
print("Broadcast Multiplication:", broadcast_mul_result)
# Output:
# [[10 40]
#  [30 80]]
```

In this example, the scalar `5` is added to each element of array `c`, and array `d` with shape `(2,)` is multiplied against each row of array `c`.

#Array Arithmetic #Numpy