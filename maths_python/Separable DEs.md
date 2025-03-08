### Separable Differential Equations

Separable differential equations are a type of first-order ordinary differential equation (ODE) that can be written in the form:

\[ \frac{dy}{dx} = f(x)g(y) \]

where \( f(x) \) is a function of \( x \) only, and \( g(y) \) is a function of \( y \) only. The key idea behind solving separable differential equations is to rearrange the equation so that all terms involving \( y \) are on one side and all terms involving \( x \) are on the other side. This allows us to integrate both sides separately.

The general solution can be found by integrating:

\[ \int \frac{1}{g(y)} dy = \int f(x) dx + C \]

where \( C \) is the constant of integration.

### Example

Consider the differential equation:

\[ \frac{dy}{dx} = 2x y \]

Here, we can identify that \( f(x) = 2x \) and \( g(y) = y \). Rearranging, we get:

\[ \frac{1}{y} dy = 2x dx \]

Integrating both sides, we obtain:

\[ \int \frac{1}{y} dy = \int 2x dx + C \]

This simplifies to:

\[ \ln|y| = x^2 + C \]

Exponentiating both sides gives us the solution:

\[ y = Ce^{x^2} \]

### Python Code Example

Here's a simple Python code example using `sympy` to solve this separable differential equation.

```python
import sympy as sp

# Define symbols
x, y = sp.symbols('x y')

# Define the differential equation dy/dx = 2*x*y
dy_dx = 2*x*y

# Solve the separable differential equation
solution = sp.dsolve(sp.Derivative(y, x) - dy_dx, y)

print(solution)
```

This code will output the general solution to the separable differential equation.

#Separable DEs #Maths #python