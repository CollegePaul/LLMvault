### Understanding Limits in Mathematics

In mathematics, limits are used to describe the behavior of functions as they approach certain values. The concept of a limit is fundamental in calculus and analysis. A limit tells us what value a function approaches as its input gets closer and closer to some specified value.

For example, consider the function \( f(x) = \frac{x^2 - 1}{x - 1} \). This function is undefined at \( x = 1 \), but we can find the limit of this function as \( x \) approaches 1. By simplifying the expression, we get \( f(x) = x + 1 \) for all \( x \neq 1 \). Therefore, the limit of \( f(x) \) as \( x \) approaches 1 is 2.

### Python Code Example

Here's a simple Python code example using the `sympy` library to calculate the limit of the function mentioned above:

```python
from sympy import symbols, limit

# Define the variable and function
x = symbols('x')
f = (x**2 - 1) / (x - 1)

# Calculate the limit as x approaches 1
limit_value = limit(f, x, 1)
print("The limit of f(x) as x approaches 1 is:", limit_value)
```

When you run this code, it will output:

```
The limit of f(x) as x approaches 1 is: 2
```

This confirms that the limit of \( f(x) = \frac{x^2 - 1}{x - 1} \) as \( x \) approaches 1 is indeed 2.

#Limits #Maths #python