### Definite Integrals in Mathematics

Definite integrals are a fundamental concept in calculus used to calculate the area under a curve between two points. Unlike indefinite integrals, which yield an antiderivative (a function), definite integrals evaluate to a specific number representing the net signed area between the function and the x-axis over a defined interval [a, b].

The definite integral of a function \( f(x) \) from \( a \) to \( b \) is denoted as:

\[
\int_{a}^{b} f(x) \, dx
\]

This expression calculates the area under the curve \( y = f(x) \) from \( x = a \) to \( x = b \). The result of a definite integral can be positive, negative, or zero depending on whether the function is above, below, or crossing the x-axis within the interval.

### Example in Code

Here's a simple Python code example using the `scipy.integrate.quad` function to compute the definite integral of \( f(x) = x^2 \) from 0 to 1:

```python
from scipy.integrate import quad

# Define the function
def integrand(x):
    return x**2

# Compute the definite integral from 0 to 1
result, error = quad(integrand, 0, 1)

print(f"The definite integral of x^2 from 0 to 1 is: {result}")
```

In this example:
- The function `integrand` represents \( f(x) = x^2 \).
- The `quad` function computes the definite integral of `integrand` over the interval [0, 1].
- The result is printed out.

The output should be approximately 0.3333, which is the exact value of the integral of \( x^2 \) from 0 to 1.

#DefiniteIntegrals #Maths #python