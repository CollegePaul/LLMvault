### Introduction to Set Theory in Mathematics

Set theory is a branch of mathematical logic that studies sets, which are collections of distinct objects. These objects can be anything: numbers, people, other sets, etc. In set theory, we define the relationship between sets using concepts such as union, intersection, difference, and complement.

- **Union**: The union of two sets \( A \) and \( B \), denoted \( A \cup B \), is the set of elements that are in \( A \), in \( B \), or in both.
- **Intersection**: The intersection of two sets \( A \) and \( B \), denoted \( A \cap B \), is the set of elements that are common to both \( A \) and \( B \).
- **Difference**: The difference between two sets \( A \) and \( B \), denoted \( A - B \), is the set of elements that are in \( A \) but not in \( B \).
- **Complement**: The complement of a set \( A \), denoted \( A' \) or \( A^c \), is the set of all elements not in \( A \).

### Example in Code

Here's a simple Python code example demonstrating these concepts:

```python
# Define two sets
set_a = {1, 2, 3, 4}
set_b = {3, 4, 5, 6}

# Union of set_a and set_b
union_ab = set_a.union(set_b)
print("Union:", union_ab)  # Output: Union: {1, 2, 3, 4, 5, 6}

# Intersection of set_a and set_b
intersection_ab = set_a.intersection(set_b)
print("Intersection:", intersection_ab)  # Output: Intersection: {3, 4}

# Difference between set_a and set_b
difference_ab = set_a - set_b
print("Difference (A-B):", difference_ab)  # Output: Difference (A-B): {1, 2}

# Complement of set_a (assuming the universal set is {1, 2, 3, 4, 5, 6})
universal_set = {1, 2, 3, 4, 5, 6}
complement_a = universal_set - set_a
print("Complement of A:", complement_a)  # Output: Complement of A: {5, 6}

```

This code snippet demonstrates how to create sets in Python and perform basic operations like union, intersection, difference, and finding the complement of a set. #Set Theory #Maths #python