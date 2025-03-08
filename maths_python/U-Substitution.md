### U-Substitution in Mathematics

U-Substitution, also known as integration by substitution, is a method used to simplify integrals. The technique involves substituting a part of the integral with another variable (commonly denoted as 'u') to transform the integral into a form that is easier to solve.

Here's a step-by-step explanation:
1. **Identify the Substitution**: Choose a part of the integral to replace with 'u'. Typically, this should be something whose derivative appears in the integrand.
2. **Differentiate**: Find the differential (du) of your substitution.
3. **Rewrite the Integral**: Replace the chosen part and its differential in the original integral with 'u' and 'du'.
4. **Integrate**: Integrate with respect to 'u'.
5. **Substitute Back**: Replace 'u' with the original expression in terms of the variable.

### Example

Consider the integral:  
\[ \int (3x^2 + 2) \cdot e^{x^3 + 2x} \, dx \]

**Step-by-step solution using U-Substitution:**

1. **Identify the Substitution**: Let \( u = x^3 + 2x \).
2. **Differentiate**: Compute \( du = (3x^2 + 2) \, dx \).
3. **Rewrite the Integral**: The integral becomes \( \int e^u \, du \).
4. **Integrate**: The integral of \( e^u \) is \( e^u + C \).
5. **Substitute Back**: Replace \( u \) with \( x^3 + 2x \):  
\[ \int (3x^2 + 2) \cdot e^{x^3 + 2x} \, dx = e^{x^3 + 2x} + C \]

### Python Code Example

Here is a simple Python code example using SymPy to perform U-Substitution and integration:

```python
from sympy import symbols, integrate, exp

# Define the variable
x = symbols('x')

# Define the integrand: (3*x**2 + 2) * exp(x**3 + 2*x)
integrand = (3*x**2 + 2) * exp(x**3 + 2*x)

# Perform the integration
result = integrate(integrand, x)

# Print the result
print(result)
```

This code will output:
\[ e^{x^3 + 2x} \]

#U-Substitution #Maths #python