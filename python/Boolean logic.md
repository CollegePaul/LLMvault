### Boolean Logic in Python

Boolean logic in Python deals with operations that result in either `True` or `False`. These values are used to make decisions and control the flow of programs. The primary operators used in boolean logic are:

- **AND (`and`)**: Returns `True` if both operands (conditions) are true.
- **OR (`or`)**: Returns `True` if at least one operand is true.
- **NOT (`not`)**: Inverts the truth value of its operand.

Additionally, Python provides comparison operators to compare values:

- Equal to (`==`)
- Not equal to (`!=`)
- Greater than (`>`)
- Less than (`<`)
- Greater than or equal to (`>=`)
- Less than or equal to (`<=`)

Here are some examples to illustrate these concepts in Python:

```python
# Example of AND operator
x = 5
y = 10
result_and = (x > 0) and (y < 20)  # True because both conditions are true
print("AND Result:", result_and)

# Example of OR operator
a = 3
b = 8
result_or = (a == 4) or (b > 7)    # True because the second condition is true
print("OR Result:", result_or)

# Example of NOT operator
c = 15
result_not = not(c < 10)           # True because c is not less than 10
print("NOT Result:", result_not)

# Comparison operators
d = 20
e = 30
is_equal = (d == e)                # False, because d is not equal to e
is_greater = (e > d)               # True, because e is greater than d
print("Is Equal:", is_equal)
print("Is Greater:", is_greater)
```

In these examples:
- The `and` operator checks if both conditions are true.
- The `or` operator checks if at least one of the conditions is true.
- The `not` operator negates the truth value of a condition.

Comparison operators are used to evaluate whether values meet certain criteria, which are essential for making decisions in code. #Boolean logic #Python