### Introduction to Topology in Mathematics

Topology is a branch of mathematics that studies properties of space that are preserved under continuous deformations, such as stretching and bending, but not tearing or gluing. Unlike geometry, which focuses on distances and angles, topology examines the more fundamental aspects of shape, such as connectivity and compactness.

**Key Concepts:**

1. **Topological Spaces:** A topological space is a set equipped with a collection of subsets, called open sets, that satisfy certain axioms. These axioms ensure that the union of any number of open sets and the intersection of a finite number of open sets are also open.

2. **Continuous Functions:** In topology, a function between two topological spaces is continuous if the preimage of every open set in the codomain is open in the domain.

3. **Homeomorphisms:** A homeomorphism is a bijective (one-to-one and onto) continuous function with a continuous inverse. Two topological spaces are said to be homeomorphic if there exists a homeomorphism between them. Homeomorphic spaces have identical topological properties.

4. **Connectedness:** A space is connected if it cannot be divided into two disjoint non-empty open sets. Intuitively, a connected space is one that is all in one piece and has no holes separating its parts.

5. **Compactness:** A space is compact if every open cover (a collection of open sets whose union contains the entire space) has a finite subcover (a smaller collection of those open sets whose union still covers the space).

**Examples:**

- The real line \(\mathbb{R}\) with its usual topology, where open sets are unions of intervals.
- A circle is homeomorphic to any other simple closed curve in 2D space but not to a figure eight (which has a different number of connected components when points are removed).

**Python Example:**

Here's a simple example using Python and the `sympy` library to illustrate the concept of open sets and continuous functions. We will check if a function is continuous at a point by examining its behavior around that point.

```python
import sympy as sp

# Define a variable and a function
x = sp.symbols('x')
f = x**2 - 3*x + 2

# Define a point to check continuity
point = 1

# Calculate the limit of the function as x approaches the point from both sides
limit_left = sp.limit(f, x, point, dir='-')
limit_right = sp.limit(f, x, point, dir='+')

# Evaluate the function at the point
value_at_point = f.subs(x, point)

# Check if the limits are equal to the function value at the point
is_continuous = (limit_left == limit_right) and (limit_left == value_at_point)
print("Is the function continuous at x =", point, "?", is_continuous)
```

In this example, we check if the quadratic function \( f(x) = x^2 - 3x + 2 \) is continuous at \( x = 1 \). The function is continuous at a point if the limit from both sides equals the function's value at that point. 

#Topology #Maths