### Explanation of Differentiation (Rigorous)

In mathematics, differentiation is a fundamental concept in calculus that deals with finding the rate at which a function's output changes as its input changes. More rigorously, it involves computing the limit of the ratio of the change in the function's value to the change in the input value as the latter approaches zero.

Formally, if \( f \) is a real-valued function defined on an open interval around a point \( x_0 \), and the limit

\[
f'(x_0) = \lim_{h \to 0} \frac{f(x_0 + h) - f(x_0)}{h}
\]

exists, then \( f \) is said to be differentiable at \( x_0 \), and the value of this limit is called the derivative of \( f \) at \( x_0 \).

### Example in Code

Here's a simple Python code example that demonstrates numerical differentiation using the definition above. We'll compute the derivative of a function \( f(x) = x^2 \) at a specific point, say \( x = 3 \), using a small value for \( h \).

```python
def differentiate(f, x, h=1e-5):
    """Numerical differentiation using the definition of the derivative."""
    return (f(x + h) - f(x)) / h

# Define the function f(x) = x^2
def f(x):
    return x ** 2

# Compute the derivative of f at x = 3
x_value = 3
derivative_at_x_value = differentiate(f, x_value)

print(f"The derivative of f(x) = x^2 at x = {x_value} is approximately: {derivative_at_x_value}")
```

### Output
When you run the above code, it will output an approximation of the derivative of \( f(x) = x^2 \) at \( x = 3 \), which should be close to 6 (since the exact derivative of \( f(x) = x^2 \) is \( f'(x) = 2x \)).

#Differentiation (Rigorous) #Maths #python