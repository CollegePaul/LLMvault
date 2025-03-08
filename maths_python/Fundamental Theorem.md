### Fundamental Theorem of Calculus

The Fundamental Theorem of Calculus (FTC) establishes the connection between differentiation and integration, two central concepts in calculus. It has two parts:

1. **First Part**: If \( f \) is continuous on an interval \([a, b]\), then the function \( g(x) = \int_a^x f(t) \, dt\) defined on \([a, b]\) is uniformly continuous on \([a, b]\), differentiable on the open interval \((a, b)\), and its derivative is \( f(x) \). That is, \( g'(x) = f(x) \).

2. **Second Part**: If \( f \) is a continuous function on an interval \([a, b]\) and \( F \) is any antiderivative of \( f \) on \([a, b]\), then
\[ \int_a^b f(x) \, dx = F(b) - F(a). \]

In essence, the FTC provides a way to evaluate definite integrals by finding an antiderivative and evaluating it at the limits of integration.

### Example in Code

Let's consider the function \( f(x) = 2x \). We want to find the definite integral of this function from 1 to 3 using the Fundamental Theorem of Calculus. An antiderivative of \( f(x) = 2x \) is \( F(x) = x^2 \).

Using the second part of the FTC:
\[ \int_1^3 2x \, dx = F(3) - F(1) = 3^2 - 1^2 = 9 - 1 = 8. \]

Here's how you can implement this in Python:

```python
# Define the antiderivative function
def F(x):
    return x**2

# Calculate the definite integral using the Fundamental Theorem of Calculus
a, b = 1, 3
integral_value = F(b) - F(a)

print(f"The value of the integral from {a} to {b} is: {integral_value}")
```

This code snippet defines an antiderivative function \( F(x) \) and calculates the definite integral of \( f(x) = 2x \) from 1 to 3 by evaluating \( F(3) - F(1) \). The output will be `The value of the integral from 1 to 3 is: 8`.

#FundamentalTheorem #Maths #python