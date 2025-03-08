### Continuity in Mathematics

Continuity is a fundamental concept in calculus that describes functions whose graphs can be drawn without lifting the pen from the paper. A function \( f(x) \) is continuous at a point \( c \) if three conditions are met:
1. The function \( f(c) \) is defined.
2. The limit of \( f(x) \) as \( x \) approaches \( c \) exists.
3. The limit of \( f(x) \) as \( x \) approaches \( c \) equals \( f(c) \).

In simpler terms, a function is continuous if small changes in the input result in only small changes in the output.

### Example

Consider the function \( f(x) = x^2 \). This function is continuous everywhere because it meets the three conditions of continuity at every point \( c \):
- \( f(c) = c^2 \) is defined for all real numbers.
- The limit as \( x \) approaches \( c \) of \( x^2 \) is \( c^2 \).
- Since the limit equals the function value, \( f(x) \) is continuous.

### Python Code Example

Here's a simple Python code that demonstrates continuity by evaluating a function and its limit at a point:

```python
import numpy as np

def f(x):
    return x**2

def limit_at_point(func, point, epsilon=1e-6):
    x_values = np.linspace(point - epsilon, point + epsilon, 1000)
    y_values = [func(x) for x in x_values]
    return np.mean(y_values)

point = 3
function_value = f(point)
limit_value = limit_at_point(f, point)

print("Function value at", point, ":", function_value)
print("Limit of the function as x approaches", point, ":", limit_value)
```

In this code:
- We define a simple quadratic function \( f(x) = x^2 \).
- We create a `limit_at_point` function that approximates the limit of \( f(x) \) as \( x \) approaches a given point.
- We then check if the function value at \( x = 3 \) matches the limit, which it should for a continuous function.

#Continuity #Maths #python