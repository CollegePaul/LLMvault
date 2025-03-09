### Introduction to Dynamical Systems in Mathematics

Dynamical systems are mathematical models that describe the time evolution of various physical, biological, or economic processes. At their core, they consist of equations representing how certain variables change over time based on initial conditions and system parameters.

The study of dynamical systems focuses on understanding long-term behavior, stability, bifurcations (sudden changes in behavior), and chaos. These systems can be categorized into discrete-time and continuous-time systems. Discrete-time systems evolve at distinct time intervals, often described by difference equations, whereas continuous-time systems change smoothly over time, modeled with differential equations.

#### Example of a Continuous-Time Dynamical System: The Simple Harmonic Oscillator

The simple harmonic oscillator is a classic example used to illustrate the behavior of continuous-time dynamical systems. It models a mass attached to a spring that oscillates back and forth under the influence of Hooke's Law. The system can be described by a second-order differential equation:

\[ \frac{d^2x}{dt^2} + \omega^2 x = 0 \]

where \( x(t) \) is the displacement from equilibrium, and \( \omega \) is the angular frequency.

In Python, we can solve this system numerically using libraries such as SciPy:

```python
import numpy as np
from scipy.integrate import odeint
import matplotlib.pyplot as plt

# Define the differential equation
def simple_harmonic_oscillator(x, t, omega):
    x1, v1 = x
    dxdt = [v1, -omega**2 * x1]
    return dxdt

# Initial conditions: initial position and velocity
x0 = [1.0, 0.0]

# Time points to solve for
t = np.linspace(0, 10, 100)

# Solve the differential equation
omega = 2*np.pi  # Angular frequency
solution = odeint(simple_harmonic_oscillator, x0, t, args=(omega,))

# Plot the results
plt.plot(t, solution[:, 0], label='Displacement')
plt.xlabel('Time')
plt.ylabel('Position (x)')
plt.title('Simple Harmonic Oscillator')
plt.legend()
plt.show()
```

In this example, `odeint` is used to solve the differential equation over a specified time interval. The resulting plot shows how the position of the mass varies with time, exhibiting periodic oscillatory behavior.

#### Example of a Discrete-Time Dynamical System: Logistic Map

The logistic map is a discrete-time dynamical system that models population growth under limited resources. It is defined by the recurrence relation:

\[ x_{n+1} = r x_n (1 - x_n) \]

where \( x_n \) represents the ratio of the current population to the maximum possible population, and \( r \) is a parameter controlling the growth rate.

Here's how you can simulate the logistic map in Python:

```python
import numpy as np
import matplotlib.pyplot as plt

# Define the logistic map function
def logistic_map(x, r):
    return r * x * (1 - x)

# Initial population ratio and number of iterations
x0 = 0.5
iterations = 100
r_values = [2.5, 3.5, 4]

for r in r_values:
    x = np.zeros(iterations)
    x[0] = x0
    for t in range(1, iterations):
        x[t] = logistic_map(x[t-1], r)
    
    plt.plot(range(iterations), x, label=f'r={r}')

plt.xlabel('Time')
plt.ylabel('Population Ratio (x)')
plt.title('Logistic Map Behavior')
plt.legend()
plt.show()
```

In this example, the logistic map is iterated over 100 steps for different values of \( r \). The resulting plots illustrate how the behavior changes from stable fixed points to periodic cycles and ultimately chaotic behavior as \( r \) increases.

### Conclusion

Dynamical systems provide a powerful framework for understanding the evolution of complex systems across various domains. Through examples like the simple harmonic oscillator and logistic map, we can explore fundamental concepts such as stability, periodicity, and chaos. #DynamicalSystems #Maths