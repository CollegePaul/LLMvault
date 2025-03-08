### Gradient Vector in Mathematics

The gradient vector is a fundamental concept in multivariable calculus that describes the direction of the steepest ascent or descent of a scalar field (a function of several variables). For a given function \( f(x, y) \), its gradient at a point \( (x_0, y_0) \) is denoted by \( \nabla f(x_0, y_0) \) and is defined as:

\[ \nabla f(x_0, y_0) = \left( \frac{\partial f}{\partial x} \Bigg|_{(x_0,y_0)}, \frac{\partial f}{\partial y} \Bigg|_{(x_0,y_0)} \right) \]

This means the gradient vector consists of the partial derivatives of \( f \) with respect to each variable, evaluated at a specific point. The direction of this vector indicates where the function increases most rapidly, and its magnitude represents the rate of change in that direction.

#### Example

Consider the function \( f(x, y) = x^2 + 2y^2 \). To find the gradient vector at the point \( (1, 1) \), we first compute the partial derivatives:

\[ \frac{\partial f}{\partial x} = 2x \]
\[ \frac{\partial f}{\partial y} = 4y \]

Evaluating these at \( (1, 1) \):

\[ \nabla f(1, 1) = \left( 2 \cdot 1, 4 \cdot 1 \right) = (2, 4) \]

Thus, the gradient vector at \( (1, 1) \) is \( (2, 4) \), indicating that moving in this direction from \( (1, 1) \) will cause \( f(x, y) \) to increase most rapidly. The magnitude of this vector, \( \sqrt{2^2 + 4^2} = \sqrt{20} = 2\sqrt{5} \), represents the rate of that increase.

#Gradient Vector #Maths