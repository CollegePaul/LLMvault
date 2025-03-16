
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

---

> [!tip]
> This is a tip


$$ \frac{dy}{dx} = f'(g(x)) \cdot g'(x) $$

