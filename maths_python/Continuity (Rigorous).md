### Continuity (Rigorous)

In mathematics, particularly in calculus and real analysis, continuity of a function is defined rigorously using the concept of limits. A function \( f \) is said to be continuous at a point \( c \) if the following three conditions are met:

1. The function \( f(c) \) is defined.
2. The limit of \( f(x) \) as \( x \) approaches \( c \) exists.
3. The limit of \( f(x) \) as \( x \) approaches \( c \) equals \( f(c) \).

Formally, a function \( f \) is continuous at a point \( c \) if:

\[ \lim_{{x \to c}} f(x) = f(c) \]

A function is continuous on an interval if it is continuous at every point in the interval.

### Example in Code

To illustrate continuity using Python, we can define a simple function and check its behavior around a specific point. Let's consider the function \( f(x) = x^2 \), which is known to be continuous everywhere.

We'll write a Python script to evaluate the limit of this function as \( x \) approaches a given point and compare it with the value of the function at that point.

```python
import numpy as np

def f(x):
    return x**2

def check_continuity_at_point(f, c, epsilon=1e-6):
    # Calculate the function value at c
    f_c = f(c)
    
    # Calculate the limit of the function as x approaches c from both sides
    f_left_limit = f(c - epsilon)
    f_right_limit = f(c + epsilon)
    
    # Check if both limits are approximately equal to f(c)
    left_continuous = np.isclose(f_left_limit, f_c)
    right_continuous = np.isclose(f_right_limit, f_c)
    
    return left_continuous and right_continuous

# Point at which to check continuity
c = 2

if check_continuity_at_point(f, c):
    print(f"The function f(x) = x^2 is continuous at x = {c}.")
else:
    print(f"The function f(x) = x^2 is not continuous at x = {c}.")

# Continuity (Rigorous) #Maths #python
```

This code defines a simple quadratic function and checks its continuity at \( x = 2 \) by evaluating the function values from both sides of the point and comparing them to the value at the point. The `np.isclose` function is used to handle floating-point precision issues.

#Continuity (Rigorous) #Maths #python