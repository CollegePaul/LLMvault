### Partial Derivatives

In mathematics, partial derivatives are used in calculus to find the rate at which a function changes as one of its variables changes while keeping all other variables constant. This concept is crucial when dealing with multivariable functions, where the function depends on more than one variable.

For example, consider a function \( f(x, y) = x^2 + 3xy + y^2 \). The partial derivative of this function with respect to \( x \), denoted as \( \frac{\partial f}{\partial x} \), is found by treating all other variables (in this case, \( y \)) as constants. Thus, the partial derivative with respect to \( x \) would be:

\[ \frac{\partial f}{\partial x} = 2x + 3y \]

Similarly, the partial derivative of \( f(x, y) \) with respect to \( y \), denoted as \( \frac{\partial f}{\partial y} \), treats \( x \) as a constant:

\[ \frac{\partial f}{\partial y} = 3x + 2y \]

### Python Code Example

Here is a simple example using Python and the `sympy` library to calculate partial derivatives of a function.

```python
import sympy as sp

# Define symbols for variables
x, y = sp.symbols('x y')

# Define the function f(x, y)
f = x**2 + 3*x*y + y**2

# Calculate the partial derivative with respect to x
df_dx = sp.diff(f, x)

# Calculate the partial derivative with respect to y
df_dy = sp.diff(f, y)

print("Partial Derivative of f with respect to x:", df_dx)
print("Partial Derivative of f with respect to y:", df_dy)
```

This code defines a function \( f(x, y) \) and calculates its partial derivatives with respect to both \( x \) and \( y \).

#PartialDerivatives #Maths #python