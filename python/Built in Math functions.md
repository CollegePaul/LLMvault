### Built-in Math Functions in Python

Python provides a variety of built-in math functions that can be used to perform mathematical operations. These functions are part of the `math` module, which must be imported before you can use them. Here are some commonly used math functions along with examples:

1. **math.sqrt(x)**: Returns the square root of x.
   ```python
   import math
   result = math.sqrt(16)
   print(result)  # Output: 4.0
   ```

2. **math.pow(x, y)**: Returns x raised to the power of y.
   ```python
   import math
   result = math.pow(2, 3)
   print(result)  # Output: 8.0
   ```

3. **math.ceil(x)**: Rounds a number up to the nearest integer.
   ```python
   import math
   result = math.ceil(4.1)
   print(result)  # Output: 5
   ```

4. **math.floor(x)**: Rounds a number down to the nearest integer.
   ```python
   import math
   result = math.floor(4.9)
   print(result)  # Output: 4
   ```

5. **math.log(x, base)**: Returns the logarithm of x to the specified base.
   ```python
   import math
   result = math.log(100, 10)
   print(result)  # Output: 2.0
   ```

6. **math.exp(x)**: Returns e raised to the power of x.
   ```python
   import math
   result = math.exp(1)
   print(result)  # Output: 2.718281828459045
   ```

7. **math.sin(x)**, **math.cos(x)**, **math.tan(x)**: Return the sine, cosine, and tangent of x radians.
   ```python
   import math
   angle = math.radians(30)  # Convert degrees to radians
   sin_value = math.sin(angle)
   cos_value = math.cos(angle)
   tan_value = math.tan(angle)
   print(sin_value, cos_value, tan_value)  # Output: 0.49999999999999994 0.8660254037844387 0.5773502691896257
   ```

8. **math.pi**: Provides the value of π (pi).
   ```python
   import math
   print(math.pi)  # Output: 3.141592653589793
   ```

These functions are very useful for various mathematical computations in Python.

#Built_in_Math_functions #Python