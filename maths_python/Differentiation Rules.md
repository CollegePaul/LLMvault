### Differentiation Rules in Mathematics

Differentiation rules are a set of formulas used to compute the derivatives of various functions. These rules simplify the process of finding derivatives, which are essential in calculus for understanding rates of change and slopes of curves. Some fundamental differentiation rules include:

1. **Power Rule**: If \( f(x) = x^n \), then \( f'(x) = nx^{n-1} \).
2. **Sum Rule**: The derivative of a sum is the sum of the derivatives, i.e., if \( f(x) = g(x) + h(x) \), then \( f'(x) = g'(x) + h'(x) \).
3. **Constant Multiple Rule**: If \( f(x) = c \cdot g(x) \), where \( c \) is a constant, then \( f'(x) = c \cdot g'(x) \).
4. **Product Rule**: For two functions \( f(x) \) and \( g(x) \), the derivative of their product is given by \( (f \cdot g)'(x) = f'(x)g(x) + f(x)g'(x) \).
5. **Quotient Rule**: For two functions \( f(x) \) and \( g(x) \), the derivative of their quotient is given by \( \left(\frac{f}{g}\right)'(x) = \frac{f'(x)g(x) - f(x)g'(x)}{(g(x))^2} \).

### Example in Python

Let's use these rules to compute the derivative of a function using Python. Suppose we have the function \( f(x) = 3x^2 + 5x + 7 \). We will find its derivative step by step.

```python
# Define a class for polynomial functions and their derivatives
class Polynomial:
    def __init__(self, coefficients):
        # Coefficients are in ascending order of power, e.g., [c0, c1, c2] represents c0 + c1*x + c2*x^2
        self.coefficients = coefficients
    
    def derivative(self):
        new_coeffs = []
        for power, coeff in enumerate(self.coefficients[1:], start=1):
            new_coeffs.append(coeff * power)
        return Polynomial(new_coeffs)
    
    def __str__(self):
        terms = [f"{coeff}x^{power}" if power > 0 else f"{coeff}"
                 for power, coeff in enumerate(reversed(self.coefficients))]
        return " + ".join(terms)

# Example function: 3x^2 + 5x + 7
f = Polynomial([7, 5, 3])

# Compute the derivative of the function
f_prime = f.derivative()

# Print the original and derived functions
print("Original Function:", f)
print("Derived Function:", f_prime)
```

In this example:
- We define a `Polynomial` class to represent polynomial functions.
- The `derivative` method computes the derivative using the power rule for each term.
- We create an instance of `Polynomial` with coefficients `[7, 5, 3]`, representing \( 7 + 5x + 3x^2 \).
- We call the `derivative` method to compute and print the derived function, which is \( 5 + 6x \).

#Differentiation Rules #Maths #python