### Exponential Functions in Mathematics

Exponential functions are mathematical functions that have the form \( f(x) = a \cdot b^x \), where \( a \) and \( b \) are constants, \( a \neq 0 \), \( b > 0 \), and \( b \neq 1 \). The variable \( x \) is in the exponent. Exponential functions are characterized by their rapid growth or decay, depending on the value of the base \( b \).

- If \( b > 1 \), the function represents exponential growth.
- If \( 0 < b < 1 \), the function represents exponential decay.

### Example in Code

Here's a simple Python code example that demonstrates an exponential growth function:

```python
import matplotlib.pyplot as plt
import numpy as np

# Define the exponential function
def exponential_growth(x, a=1, b=2):
    return a * (b ** x)

# Generate x values from 0 to 5
x_values = np.linspace(0, 5, 400)
y_values = [exponential_growth(x) for x in x_values]

# Plot the function
plt.plot(x_values, y_values, label='Exponential Growth (b=2)')
plt.title('Example of Exponential Function')
plt.xlabel('x')
plt.ylabel('f(x)')
plt.legend()
plt.grid(True)
plt.show()
```

This code defines an exponential growth function with \( a = 1 \) and \( b = 2 \), generates x values from 0 to 5, computes the corresponding y values using the function, and plots these values. The plot visually represents the rapid growth characteristic of exponential functions.

#Exponential Functions #Maths #python