### Linear Differential Equations in Mathematics

Linear differential equations are equations that involve an unknown function and its derivatives, where each term can be a constant or a multiple of the unknown function or any derivative of it. They are called "linear" because each term is either a constant or a product of a constant and a single variable (or its derivative), raised to the power one.

A general form of a linear differential equation of order \( n \) can be written as:

\[ a_n(x)y^{(n)} + a_{n-1}(x)y^{(n-1)} + \cdots + a_1(x)y' + a_0(x)y = g(x) \]

where \( y^{(n)}, y^{(n-1)}, \ldots, y' \) denote the \( n \)-th, \( (n-1) \)-th, ..., first derivatives of the function \( y \), and \( a_n(x), a_{n-1}(x), \ldots, a_0(x), g(x) \) are functions of \( x \).

#### Example: First-order Linear Differential Equation

Consider the first-order linear differential equation:

\[ y' + 2y = e^{3t} \]

To solve this equation using Python, we can use the `solve_ivp` function from the `scipy.integrate` module. Here's a simple example code to solve and plot the solution of the given differential equation.

```python
import numpy as np
from scipy.integrate import solve_ivp
import matplotlib.pyplot as plt

# Define the differential equation
def dY_dt(t, Y):
    return -2 * Y + np.exp(3 * t)

# Initial condition
Y0 = [1]  # y(0) = 1

# Time points where we want to solve
t_eval = np.linspace(0, 5, 100)

# Solve the differential equation
sol = solve_ivp(fun=dY_dt, t_span=[0, 5], y0=Y0, t_eval=t_eval)

# Plot the solution
plt.plot(sol.t, sol.y[0])
plt.xlabel('t')
plt.ylabel('y(t)')
plt.title('Solution of the Linear Differential Equation y\' + 2y = e^(3t)')
plt.grid(True)
plt.show()
```

This code defines the differential equation \( y' + 2y = e^{3t} \), sets an initial condition, solves it over a specified range of time points, and then plots the solution.

#Linear DEs #Maths #python