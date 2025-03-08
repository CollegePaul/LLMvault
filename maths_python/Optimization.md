### Optimization in Mathematics

Optimization in mathematics involves finding the best solution to a problem from a set of possible solutions. This process often entails maximizing or minimizing an objective function, subject to certain constraints. The goal could be as varied as finding the shortest path, minimizing costs, maximizing profits, or optimizing resource allocation.

#### Example: Linear Programming - Minimizing Cost

Suppose you run a factory that produces two types of products, Product A and Product B. Each product requires resources like labor and materials to produce. You want to minimize the total cost of production while meeting certain demands and respecting the constraints on resources.

Let's define:
- \( x_1 \): number of units of Product A
- \( x_2 \): number of units of Product B

Objective function (cost to minimize):
\[ C = 4x_1 + 3x_2 \]

Constraints:
- Labor constraint: \( 2x_1 + x_2 \geq 100 \)
- Material constraint: \( x_1 + 2x_2 \geq 80 \)
- Non-negativity: \( x_1, x_2 \geq 0 \)

To solve this problem using Python, we can use the `scipy.optimize.linprog` function from the SciPy library.

#### Python Code Example

```python
from scipy.optimize import linprog

# Coefficients of the objective function to minimize (cost)
c = [4, 3]

# Coefficients of the inequality constraints (left-hand side)
A = [[-2, -1], [-1, -2]]

# Right-hand side of the inequality constraints
b = [-100, -80]

# Bounds for each variable (x1 and x2 must be non-negative)
x_bounds = (0, None)
y_bounds = (0, None)

# Solve the linear programming problem
result = linprog(c, A_ub=A, b_ub=b, bounds=[x_bounds, y_bounds], method='highs')

print("Optimal value of x1:", result.x[0])
print("Optimal value of x2:", result.x[1])
print("Minimum cost:", result.fun)
```

In this code:
- We define the objective function coefficients (`c`).
- We set up the inequality constraints using `A` and `b`.
- We specify that \(x_1\) and \(x_2\) must be non-negative.
- We use the `linprog` function to solve the problem, specifying the method as 'highs'.
- Finally, we print the optimal values of \(x_1\), \(x_2\), and the minimum cost.

#Optimization #Maths #python