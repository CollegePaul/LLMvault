### Integration by Parts

Integration by parts is a method used in calculus to integrate the product of two functions. This technique is derived from the product rule of differentiation. The formula for integration by parts is given by:

\[ \int u \, dv = uv - \int v \, du \]

Where:
- \( u \) and \( v \) are functions of the variable being integrated.
- \( du \) and \( dv \) are their respective differentials.

To apply this method effectively, you need to choose which part of the integrand will be \( u \) and which will be \( dv \). A common mnemonic for choosing \( u \) is "LIATE," standing for:
1. Logarithmic functions
2. Inverse trigonometric functions
3. Algebraic functions
4. Trigonometric functions
5. Exponential functions

This suggests that logarithmic and inverse trigonometric functions should be chosen as \( u \) first, followed by algebraic functions, then trigonometric functions, and finally exponential functions.

### Example in Code

Here's a simple Python code example using the `sympy` library to perform integration by parts. We will integrate the function \( x \cdot e^x \).

```python
from sympy import symbols, exp, integrate

# Define the variable
x = symbols('x')

# Define the functions u and dv
u = x
dv = exp(x)

# Compute du and v
du = u.diff(x)
v = integrate(dv, x)

# Apply integration by parts formula: ∫u dv = uv - ∫v du
result = u*v - integrate(v*du, x)

print("The result of the integration is:", result)
```

In this example:
- \( u = x \)
- \( dv = e^x \, dx \)
- Therefore, \( du = dx \) and \( v = \int e^x \, dx = e^x \).

Using the formula, we find that:

\[ \int x \cdot e^x \, dx = x \cdot e^x - \int e^x \, dx = x \cdot e^x - e^x + C \]

Where \( C \) is the constant of integration.

#Integration by Parts #Maths #python