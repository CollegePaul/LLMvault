### Introduction to Combinatorics in Math

Combinatorics is a branch of mathematics that focuses on the study of discrete structures, including counting, arrangement, and combination of objects. It deals with questions such as: How many ways can we arrange a set of items? In how many ways can we select a subset from a set? These questions often arise in fields like probability theory, computer science, and statistics.

#### Basic Concepts:

1. **Permutations**: This is the arrangement of all or part of a set of objects in a specific order. The number of permutations of n distinct objects taken r at a time is given by the formula \( P(n, r) = \frac{n!}{(n-r)!} \).

2. **Combinations**: This involves selecting items from a collection where the order does not matter. The number of combinations of n distinct objects taken r at a time is given by the formula \( C(n, r) = \frac{n!}{r!(n-r)!} \).

3. **Factorial**: The factorial of a non-negative integer n, denoted as \( n! \), is the product of all positive integers less than or equal to n.

#### Example in Python:

Let's look at an example using Python to calculate permutations and combinations.

```python
# Importing the math library for factorial function
import math

def permutations(n, r):
    return math.factorial(n) // math.factorial(n - r)

def combinations(n, r):
    return math.factorial(n) // (math.factorial(r) * math.factorial(n - r))

# Example usage:
n = 5  # Total items
r = 3  # Items to be chosen

perm = permutations(n, r)
comb = combinations(n, r)

print(f"Permutations of {n} objects taken {r} at a time: {perm}")
print(f"Combinations of {n} objects taken {r} at a time: {comb}")
```

In this example:
- We define two functions `permutations` and `combinations` that use the factorial function from Python's math library to compute permutations and combinations.
- We then calculate the number of ways to arrange 5 items taken 3 at a time, and the number of ways to select 3 items from 5 without regard to order.

#Combinatorics #Maths