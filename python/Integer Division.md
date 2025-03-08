### Integer Division in Python

In Python, integer division is an arithmetic operation that divides one number by another and returns the quotient without the remainder. This operation is performed using the `//` operator. When you use `//`, both operands are treated as integers, and the result is also an integer. If the division does not result in a whole number, the fractional part is discarded, and the result is rounded down towards negative infinity.

Here are some examples of integer division:

```python
# Example 1: Basic Integer Division
result = 10 // 3
print(result)  # Output will be 3

# Example 2: Negative Dividend
result = -10 // 3
print(result)  # Output will be -4 (not -3)

# Example 3: Zero Remainder
result = 15 // 3
print(result)  # Output will be 5

# Example 4: Division with Larger Divisor
result = 3 // 10
print(result)  # Output will be 0

# Example 5: Both Operands Negative
result = -10 // -3
print(result)  # Output will be 3
```

In the above examples, you can see how the `//` operator performs integer division and handles different scenarios such as positive and negative numbers, zero remainder, and when the divisor is larger than the dividend.

#Integer Division #Python