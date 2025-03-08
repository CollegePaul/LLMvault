### Explanation of Chain Rule in Mathematics

The Chain Rule is a fundamental concept in calculus used to find the derivative of composite functions. A composite function is formed when one function is nested inside another. If you have a function \( y = f(g(x)) \), then the derivative of \( y \) with respect to \( x \) is given by:

\[ \frac{dy}{dx} = f'(g(x)) \cdot g'(x) \]

This means that you first find the derivative of the outer function evaluated at the inner function, and then multiply it by the derivative of the inner function.

### Example

Consider the function \( y = (3x + 2)^4 \). Here, the outer function is \( f(u) = u^4 \) where \( u = g(x) = 3x + 2 \).

1. Find the derivative of the outer function with respect to \( u \):
   \[ \frac{df}{du} = 4u^3 \]

2. Substitute \( u = 3x + 2 \) into the derivative:
   \[ \frac{df}{du} = 4(3x + 2)^3 \]

3. Find the derivative of the inner function with respect to \( x \):
   \[ \frac{dg}{dx} = 3 \]

4. Apply the Chain Rule:
   \[ \frac{dy}{dx} = \frac{df}{du} \cdot \frac{dg}{dx} = 4(3x + 2)^3 \cdot 3 = 12(3x + 2)^3 \]

### Python Code Example

Here's a simple Python code example using the sympy library to compute the derivative of \( y = (3x + 2)^4 \) using the Chain Rule.

```python
import sympy as sp

# Define the variable and function
x = sp.symbols('x')
y = (3*x + 2)**4

# Compute the derivative using sympy
dy_dx = sp.diff(y, x)

# Print the result
print("The derivative of y with respect to x is:", dy_dx)
```

This code will output:
```
The derivative of y with respect to x is: 12*(3*x + 2)**3
```

#Chain Rule #Maths #python