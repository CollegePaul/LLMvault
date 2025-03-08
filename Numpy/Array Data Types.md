### Array Data Types in NumPy

NumPy arrays are homogeneous sequences of fixed-size items. Each element in a NumPy array is of the same data type, which is specified by a special object called a `dtype`. The `dtype` describes how the bytes in each fixed-size block of memory corresponding to an array item should be interpreted.

Here are some common data types used in NumPy arrays:

- **int8**: Signed 8-bit integer (-128 to 127)
- **uint8**: Unsigned 8-bit integer (0 to 255)
- **int32**: Signed 32-bit integer
- **float32**: Single precision floating point number (sign bit, 8 bits for exponent, 23 bits for mantissa)
- **float64** or **double**: Double precision floating point number (sign bit, 11 bits for exponent, 52 bits for mantissa)

You can specify the data type when creating an array using the `dtype` parameter. Here are some examples:

```python
import numpy as np

# Creating an array with int8 data type
int_array = np.array([1, 2, 3], dtype=np.int8)
print("Integer Array:", int_array)
print("Data Type of Integer Array:", int_array.dtype)

# Creating an array with float64 data type
float_array = np.array([1.0, 2.5, 3.75], dtype=np.float64)
print("\nFloat Array:", float_array)
print("Data Type of Float Array:", float_array.dtype)

# Creating an array and letting NumPy infer the data type
auto_dtype_array = np.array([1, 2.0, 3])
print("\nArray with Auto Inferred Data Type:", auto_dtype_array)
print("Inferred Data Type:", auto_dtype_array.dtype)
```

This code will output:

```
Integer Array: [1 2 3]
Data Type of Integer Array: int8

Float Array: [1.   2.5  3.75]
Data Type of Float Array: float64

Array with Auto Inferred Data Type: [1.  2.  3.]
Inferred Data Type: float64
```

When creating an array, if you do not specify a `dtype`, NumPy will infer it from the data provided. For example, if you mix integers and floats in an array, NumPy will typically default to using the float data type.

#Array Data Types #Numpy