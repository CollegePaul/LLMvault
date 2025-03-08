### Integration Techniques in Mathematics

Integration techniques are methods used to find antiderivatives or definite integrals of functions. These techniques can be broadly categorized into:

1. **Substitution (u-substitution):** This method involves substituting a part of the function with a new variable, usually 'u', to simplify the integral.
2. **Integration by Parts:** This technique is used when integrating products of two functions and relies on the formula: \(\int u \, dv = uv - \int v \, du\).
3. **Partial Fraction Decomposition:** Used for integrating rational functions (fractions where both the numerator and denominator are polynomials) by breaking them into simpler fractions.
4. **Trigonometric Substitution:** Involves substituting trigonometric functions to simplify integrals of expressions involving square roots.

#### Example: Integration by Parts

Let's consider an example using integration by parts:

\[
\int x \cdot e^x \, dx
\]

Using the formula for integration by parts, let:
- \(u = x\) → \(du = dx\)
- \(dv = e^x \, dx\) → \(v = e^x\)

Thus,
\[
\int x \cdot e^x \, dx = x \cdot e^x - \int e^x \, dx = x \cdot e^x - e^x + C
\]

### Python Code Example

Here is a simple example of using the sympy library in Python to perform integration by parts:

```python
from sympy import symbols, integrate, exp

# Define the variable
x = symbols('x')

# Define the function
f = x * exp(x)

# Compute the integral
integral_result = integrate(f, x)

print("The integral of x*e^x is:", integral_result)
```

This code will output:

```
The integral of x*e^x is: (x - 1)*exp(x)
```

This confirms our manual calculation. #Integration Techniques #Maths #python