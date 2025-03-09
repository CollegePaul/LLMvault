### Introduction to Optimization in Math

Optimization is a branch of mathematics that focuses on finding the best solution from all feasible solutions. This process involves maximizing or minimizing an objective function, subject to certain constraints. In other words, optimization aims to find the optimal values of decision variables that will lead to the desired outcome, whether it's minimizing costs, maximizing profits, or achieving some other goal under given limitations.

The problems encountered in optimization can be broadly categorized into two types:

1. **Linear Optimization (Linear Programming):** Here, both the objective function and constraints are linear. Linear programming is widely used in various fields such as production planning, logistics, and resource allocation due to its simplicity and efficiency.
   
2. **Non-linear Optimization:** This involves optimizing a non-linear objective function or dealing with non-linear constraints. Non-linear optimization problems can be more complex and require advanced techniques to solve.

#### Example of Linear Programming using Python

To illustrate linear programming, let's consider a simple production planning problem where we need to determine the optimal number of two products (Product A and Product B) to manufacture to maximize profit, given limited resources such as labor and materials. Assume:

- Profit per unit: $10 for Product A and $20 for Product B
- Labor required: 3 hours/unit for Product A and 5 hours/unit for Product B; total available labor = 40 hours
- Material required: 2 units/unit for Product A and 6 units/unit for Product B; total material available = 18 units

We can solve this problem using Python's `scipy.optimize.linprog` function.

```python
from scipy.optimize import linprog

# Coefficients of the objective function (to be minimized, hence negative)
c = [-10, -20]

# Coefficients for inequality constraints
A = [
    [3, 5],  # labor constraint coefficients
    [2, 6]   # material constraint coefficients
]

# Right-hand side values of the inequality constraints
b = [40, 18]

# Bounds for each variable (non-negative)
x_bounds = (0, None)
y_bounds = (0, None)

# Solving the linear programming problem
result = linprog(c, A_ub=A, b_ub=b, bounds=[x_bounds, y_bounds], method='highs')

print("Optimal number of Product A:", result.x[0])
print("Optimal number of Product B:", result.x[1])
print("Maximum Profit:", -result.fun)  # Negate again to get the actual maximum profit
```

In this example, `linprog` is used to find the optimal production quantities for Product A and Product B that maximize the profit while respecting the constraints on labor and materials.

#Optimization #Maths