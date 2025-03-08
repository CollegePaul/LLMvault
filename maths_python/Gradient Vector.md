### Gradient Vector in Mathematics

The gradient vector is a fundamental concept in multivariable calculus that represents the direction and rate of maximum increase of a scalar-valued function. For a function \( f(x, y) \), the gradient vector is denoted as \( \nabla f \) and is defined as:

\[
\nabla f = \left( \frac{\partial f}{\partial x}, \frac{\partial f}{\partial y} \right)
\]

Here, \( \frac{\partial f}{\partial x} \) and \( \frac{\partial f}{\partial y} \) are the partial derivatives of \( f \) with respect to \( x \) and \( y \), respectively. The gradient vector points in the direction of the steepest ascent from any given point, and its magnitude indicates the rate of change.

#### Example

Consider the function \( f(x, y) = x^2 + 3y^2 \).

To find the gradient vector, we compute the partial derivatives:

\[
\frac{\partial f}{\partial x} = 2x
\]
\[
\frac{\partial f}{\partial y} = 6y
\]

Thus, the gradient vector is:

\[
\nabla f(x, y) = (2x, 6y)
\]

At a specific point, say \( (1, 2) \), the gradient vector would be:

\[
\nabla f(1, 2) = (2 \cdot 1, 6 \cdot 2) = (2, 12)
\]

This means that at the point \( (1, 2) \), the function increases most rapidly in the direction of the vector \( (2, 12) \).

### Python Code Example

Here's a simple Python code using NumPy to compute the gradient vector for the same function:

```python
import numpy as np

def f(x, y):
    return x**2 + 3*y**2

def gradient_f(x, y):
    df_dx = 2 * x
    df_dy = 6 * y
    return np.array([df_dx, df_dy])

# Point at which to evaluate the gradient
point = (1, 2)

# Compute the gradient vector at the given point
grad_vector = gradient_f(*point)
print(f"Gradient Vector at {point}: {grad_vector}")
```

This code defines a function `f` and its gradient `gradient_f`, computes the gradient at a specified point, and prints the result. The output will confirm our manual calculation:

```
Gradient Vector at (1, 2): [ 2 12]
```

#Gradient Vector #Maths #python