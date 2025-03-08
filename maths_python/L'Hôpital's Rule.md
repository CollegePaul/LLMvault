### L'Hôpital's Rule Explanation

L'Hôpital's Rule is a theorem in calculus used to evaluate limits of indeterminate forms, typically those that take the form 0/0 or ∞/∞. The rule states that if the limit of the ratio of two functions results in an indeterminate form, then the limit of that ratio is equal to the limit of the ratio of their derivatives, provided these limits exist.

For example, consider evaluating:

\[ \lim_{x \to a} \frac{f(x)}{g(x)} \]

If this limit evaluates to 0/0 or ∞/∞, L'Hôpital's Rule allows us to compute it as:

\[ \lim_{x \to a} \frac{f'(x)}{g'(x)} \]

provided the latter limit exists.

### Example in Code

Here is a simple Python code example using SymPy to demonstrate L'Hôpital's Rule:

```python
import sympy as sp

# Define the variable and functions
x = sp.symbols('x')
f = x**2 - 4
g = x - 2

# Calculate the limit of f(x)/g(x) as x approaches 2 directly
limit_direct = sp.limit(f/g, x, 2)

# Apply L'Hôpital's Rule by taking the derivatives of f and g
f_prime = sp.diff(f, x)
g_prime = sp.diff(g, x)

# Calculate the limit of f'(x)/g'(x) as x approaches 2
limit_lhopital = sp.limit(f_prime/g_prime, x, 2)

print("Direct Limit (0/0 indeterminate form):", limit_direct)
print("L'Hôpital's Rule Applied:", limit_lhopital)
```

In this example, the direct evaluation of \(\lim_{x \to 2} \frac{x^2 - 4}{x - 2}\) results in an indeterminate form 0/0. By applying L'Hôpital's Rule and taking the derivatives of the numerator and denominator, we find that the limit is 4.

#L'Hôpital's Rule #Maths #python