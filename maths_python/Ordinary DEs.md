### Introduction to Ordinary Differential Equations (ODEs) in Mathematics

Ordinary Differential Equations (ODEs) are equations that contain one or more functions of one independent variable and their derivatives. They are used extensively in various fields such as physics, engineering, biology, and economics to model dynamic systems where the rate of change of a system is known.

For example, consider the motion of a falling object under gravity without air resistance. The position \( y(t) \) of the object at time \( t \) can be described by the second-order ODE:

\[ \frac{d^2y}{dt^2} = g \]

where \( g \) is the acceleration due to gravity.

To solve this, we often reduce it to a system of first-order ODEs. Let's define \( v(t) \) as the velocity of the object at time \( t \). Then we have:

\[ \frac{dy}{dt} = v \]
\[ \frac{dv}{dt} = g \]

This system can be solved given initial conditions, such as the initial position and velocity.

### Example in Python

To solve this system of ODEs using Python, we can use libraries like `scipy.integrate`. Here is a simple code example that solves the above problem:

```python
import numpy as np
from scipy.integrate import odeint
import matplotlib.pyplot as plt

# Define the system of differential equations
def system(y, t):
    ydot = np.zeros(2)
    ydot[0] = y[1]  # dy/dt = v
    ydot[1] = 9.8   # dv/dt = g (assuming g = 9.8 m/s^2)
    return ydot

# Initial conditions: initial position and velocity
y0 = [0, 0]

# Time points where we want the solution
t = np.linspace(0, 10, 101)  # from t=0 to t=10 seconds with 101 points

# Solve ODE
solution = odeint(system, y0, t)

# Extracting position and velocity from the solution
position = solution[:, 0]
velocity = solution[:, 1]

# Plotting the results
plt.figure(figsize=(12, 6))

plt.subplot(2, 1, 1)
plt.plot(t, position, label='Position (y)')
plt.title('Motion of a Falling Object')
plt.xlabel('Time [s]')
plt.ylabel('Position [m]')
plt.legend()

plt.subplot(2, 1, 2)
plt.plot(t, velocity, label='Velocity (v)', color='orange')
plt.xlabel('Time [s]')
plt.ylabel('Velocity [m/s]')
plt.legend()

plt.tight_layout()
plt.show()
```

In this example, we define a system of ODEs that describes the motion of a falling object. We use `odeint` from `scipy.integrate` to solve these equations over a specified time range and plot the results for both position and velocity.

#Ordinary DEs #Maths #python