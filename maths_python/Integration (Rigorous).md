### Explanation of Integration (Rigorous) in Mathematics

Integration is a fundamental concept in calculus that allows us to compute areas, volumes, and other quantities. In rigorous terms, integration involves finding the limit of a sum of infinitesimally small quantities. This process can be understood through the Riemann integral, which defines the area under a curve as the limit of sums of rectangular approximations (Riemann sums) as their width approaches zero.

The rigorous definition of the Riemann integral for a function \( f \) over an interval \([a, b]\) is given by:
\[ \int_{a}^{b} f(x) \, dx = \lim_{{\Delta x \to 0}} \sum_{i=1}^{n} f(x_i^*) \Delta x \]
where \( \Delta x = \frac{b-a}{n} \), and \( x_i^* \) is a point in the i-th subinterval.

### Simple Python Code Example for Numerical Integration

To illustrate this concept numerically, we can use the trapezoidal rule, which is a simple method for approximating definite integrals. The trapezoidal rule improves upon the Riemann sum by using trapezoids instead of rectangles, providing better accuracy.

Here’s a Python code example that demonstrates numerical integration using the trapezoidal rule:

```python
import numpy as np

def trapezoidal_rule(f, a, b, n):
    """
    Approximates the integral of f from a to b using the trapezoidal rule with n subintervals.
    
    :param f: The function to integrate
    :param a: The lower limit of integration
    :param b: The upper limit of integration
    :param n: The number of subintervals
    :return: The approximate integral
    """
    h = (b - a) / n
    x = np.linspace(a, b, n+1)
    y = f(x)
    
    # Trapezoidal rule formula: 
    # Integral ≈ (h/2) * [f(a) + 2*sum(f(x_i)) + f(b)]
    integral = h * (0.5*y[0] + np.sum(y[1:-1]) + 0.5*y[-1])
    
    return integral

# Example usage: Integrate the function f(x) = x^2 from 0 to 1
def f(x):
    return x**2

a, b = 0, 1
n = 1000  # Number of subintervals

approx_integral = trapezoidal_rule(f, a, b, n)
print(f"Approximate integral of x^2 from {a} to {b} using {n} subintervals: {approx_integral}")

# The exact integral of x^2 from 0 to 1 is 1/3
exact_integral = 1/3
print(f"Exact integral: {exact_integral}")
```

This code defines a function `trapezoidal_rule` that approximates the integral of a given function \( f \) over an interval \([a, b]\) using the trapezoidal rule with \( n \) subintervals. The example usage demonstrates integrating the function \( f(x) = x^2 \) from 0 to 1.

#Integration (Rigorous) #Maths #python