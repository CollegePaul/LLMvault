### Introduction to Set Theory in Math

Set theory is a fundamental branch of mathematics that studies sets, which are collections of distinct objects considered as an object in their own right. The concept of sets provides a foundation for nearly all areas of mathematics, including algebra, analysis, topology, and probability.

**Key Concepts:**

- **Set:** A well-defined collection of distinct objects. For example, the set of natural numbers less than 5 is {1, 2, 3, 4}.
- **Element:** An object that belongs to a set. If an element \( x \) is in set \( A \), we write \( x \in A \).
- **Empty Set:** A set with no elements, denoted by \(\emptyset\) or {}.
- **Subset:** A set \( A \) is a subset of set \( B \) if every element of \( A \) is also an element of \( B \). This is written as \( A \subseteq B \).
- **Union:** The union of sets \( A \) and \( B \), denoted \( A \cup B \), is the set of elements which are in \( A \), in \( B \), or in both.
- **Intersection:** The intersection of sets \( A \) and \( B \), denoted \( A \cap B \), is the set of elements that are in both \( A \) and \( B \).
- **Complement:** The complement of a set \( A \), denoted \( A^c \) or \( \overline{A} \), is the set of elements not in \( A \). This concept requires specifying a universal set, which includes all possible elements under consideration.
- **Difference:** The difference between sets \( A \) and \( B \), denoted \( A - B \), is the set of elements that are in \( A \) but not in \( B \).
- **Cartesian Product:** The Cartesian product of two sets \( A \) and \( B \), denoted \( A \times B \), is the set of all ordered pairs (a, b) where \( a \in A \) and \( b \in B \).

**Examples in Python:**

```python
# Define some sets
A = {1, 2, 3}
B = {3, 4, 5}

# Union of sets
union_set = A.union(B)
print("Union:", union_set)  # Output: Union: {1, 2, 3, 4, 5}

# Intersection of sets
intersection_set = A.intersection(B)
print("Intersection:", intersection_set)  # Output: Intersection: {3}

# Difference of sets
difference_set = A - B
print("Difference (A-B):", difference_set)  # Output: Difference (A-B): {1, 2}

# Cartesian Product using list comprehension
cartesian_product = {(a, b) for a in A for b in B}
print("Cartesian Product:", cartesian_product)
# Output: Cartesian Product: {(1, 3), (1, 4), (1, 5), (2, 3), (2, 4), (2, 5), (3, 3), (3, 4), (3, 5)}

# Check if one set is a subset of another
is_subset = A.issubset(B)
print("Is A a subset of B?", is_subset)  # Output: Is A a subset of B? False

# Complement of a set requires defining the universal set
universal_set = {1, 2, 3, 4, 5, 6}
complement_set = universal_set - A
print("Complement of A:", complement_set)  # Output: Complement of A: {4, 5, 6}
```

#Set Theory #Maths