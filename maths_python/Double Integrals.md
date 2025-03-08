### Double Integrals in Mathematics

Double integrals are a means of integration over a two-dimensional region in the plane. They can be thought of as an extension of single-variable integration, where instead of summing up infinitely many rectangles to find the area under a curve, we sum up infinitely many "prisms" or volumes under a surface.

To evaluate a double integral over a rectangular region defined by \(a \leq x \leq b\) and \(c \leq y \leq d\), you can think of it as integrating with respect to one variable while treating the other as constant, then repeating the process for the second variable. Mathematically, this is written as:

\[ \int_{c}^{d} \int_{a}^{b} f(x,y) \, dx \, dy \]

This represents the volume under the surface \(z = f(x,y)\) over the rectangle in the \(xy\)-plane.

### Example of Double Integral

Suppose we want to evaluate the double integral of the function \(f(x, y) = x + y\) over the rectangle defined by \(0 \leq x \leq 1\) and \(0 \leq y \leq 2\).

The double integral is:

\[ \int_{0}^{2} \int_{0}^{1} (x + y) \, dx \, dy \]

First, we integrate with respect to \(x\):

\[ \int_{0}^{1} (x + y) \, dx = \left[ \frac{x^2}{2} + xy \right]_0^1 = \frac{1}{2} + y \]

Next, we integrate the result with respect to \(y\):

\[ \int_{0}^{2} \left( \frac{1}{2} + y \right) \, dy = \left[ \frac{y}{2} + \frac{y^2}{2} \right]_0^2 = 1 + 2 = 3 \]

So, the value of the double integral is 3.

### Python Code Example

Here's a simple Python code example using `scipy.integrate` to compute the same double integral:

```python
from scipy import integrate

# Define the function f(x, y)
def integrand(y, x):
    return x + y

# Perform the double integral
result, error = integrate.dblquad(integrand, 0, 1, lambda x: 0, lambda x: 2)

print("The result of the double integral is:", result) # The result should be close to 3
```

This code defines the function \(f(x, y)\), and uses `dblquad` from `scipy.integrate` to compute the double integral over the specified region. The order of integration in `dblquad` is with respect to the inner variable first (y in this case), then the outer variable (x). #DoubleIntegrals #Maths #python