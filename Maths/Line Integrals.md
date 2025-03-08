### Introduction to Line Integrals in Mathematics

A line integral is a type of definite integral that can be thought of as an extension of the concept of integration over curves. It is used to integrate scalar or vector fields along a curve in space. Essentially, it allows us to calculate the work done by a force acting on an object moving along a specific path.

#### Scalar Line Integrals
A scalar line integral calculates the total effect of a scalar field on a given curve. Suppose we have a scalar function \( f(x, y) \) and a smooth curve \( C \) defined by a parameterization \( \mathbf{r}(t) = (x(t), y(t)) \) for \( t \) in the interval \([a, b]\). The scalar line integral of \( f \) over \( C \) is given by:
\[
\int_C f(x, y) \, ds
\]
where \( ds \) represents a small segment along the curve. In terms of the parameterization, this can be written as:
\[
\int_a^b f(\mathbf{r}(t)) \|\mathbf{r}'(t)\| \, dt
\]

**Example:**
Consider a straight line segment \( C \) from point (0, 0) to (1, 1). We want to evaluate the scalar line integral of \( f(x, y) = x + y \) along this curve. The parameterization of the line segment can be given by:
\[
\mathbf{r}(t) = (t, t), \quad 0 \leq t \leq 1
\]
Then,
\[
f(\mathbf{r}(t)) = f(t, t) = t + t = 2t
\]
and the derivative of \( \mathbf{r}(t) \) is:
\[
\mathbf{r}'(t) = (1, 1)
\]
so,
\[
\|\mathbf{r}'(t)\| = \sqrt{1^2 + 1^2} = \sqrt{2}
\]
Thus, the line integral becomes:
\[
\int_C f(x, y) \, ds = \int_0^1 2t \cdot \sqrt{2} \, dt = 2\sqrt{2} \left[ \frac{t^2}{2} \right]_0^1 = \sqrt{2}
\]

#### Vector Line Integrals
A vector line integral calculates the total effect of a vector field on a given curve. Suppose we have a vector field \( \mathbf{F}(x, y) = (P(x, y), Q(x, y)) \) and a smooth curve \( C \) defined by a parameterization \( \mathbf{r}(t) = (x(t), y(t)) \) for \( t \) in the interval \([a, b]\). The vector line integral of \( \mathbf{F} \) over \( C \) is given by:
\[
\int_C \mathbf{F} \cdot d\mathbf{r}
\]
In terms of the parameterization, this can be written as:
\[
\int_a^b \mathbf{F}(\mathbf{r}(t)) \cdot \mathbf{r}'(t) \, dt
\]

**Example:**
Consider a vector field \( \mathbf{F}(x, y) = (y, x) \) and the same line segment \( C \) from point (0, 0) to (1, 1). The parameterization of the line segment is:
\[
\mathbf{r}(t) = (t, t), \quad 0 \leq t \leq 1
\]
Then,
\[
\mathbf{F}(\mathbf{r}(t)) = \mathbf{F}(t, t) = (t, t)
\]
and the derivative of \( \mathbf{r}(t) \) is:
\[
\mathbf{r}'(t) = (1, 1)
\]
Thus, the line integral becomes:
\[
\int_C \mathbf{F} \cdot d\mathbf{r} = \int_0^1 (t, t) \cdot (1, 1) \, dt = \int_0^1 (t + t) \, dt = \int_0^1 2t \, dt = \left[ t^2 \right]_0^1 = 1
\]

#LineIntegrals #Maths