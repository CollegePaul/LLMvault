### Derivative Definition in Mathematics

The derivative of a function measures how the output of the function changes as its input changes. It can be thought of as the rate at which the value of a function is changing with respect to a change in the input values. Mathematically, the derivative of a function \( f \) at a point \( x \), denoted as \( f'(x) \), is defined using limits:

\[ f'(x) = \lim_{h \to 0} \frac{f(x + h) - f(x)}{h} \]

This limit represents the slope of the tangent line to the graph of the function at the point \( (x, f(x)) \).

### Example in Code

Let's consider a simple example where we compute the derivative of a function using the above definition. We'll use Python and the `sympy` library to calculate the derivative of \( f(x) = x^2 \).

```python
from sympy import symbols, diff

# Define the variable
x = symbols('x')

# Define the function
f = x**2

# Compute the derivative
derivative_of_f = diff(f, x)

print("The derivative of f(x) = x^2 is:", derivative_of_f)
```

When you run this code, it will output:

```
The derivative of f(x) = x^2 is: 2*x
```

This result confirms that the derivative of \( x^2 \) is \( 2x \), which aligns with the known mathematical result. #Derivative Definition #Maths #python