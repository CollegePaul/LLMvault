### Modulus in Python

The modulus operator in Python, represented by the `%` symbol, returns the remainder of the division between two numbers. It is used to determine what remains after one number has been divided by another to as great an extent as possible. This operation is particularly useful in scenarios where you need to check for divisibility or cycle through a range periodically.

For example, determining if a number is even or odd can be done using the modulus operator:
- If `number % 2` equals 0, the number is even.
- If `number % 2` equals 1, the number is odd.

Here are some examples of how to use the modulus operator in Python:

**Example 1: Checking Even or Odd**
```python
def check_even_odd(number):
    if number % 2 == 0:
        return "Even"
    else:
        return "Odd"

print(check_even_odd(4))  # Output: Even
print(check_even_odd(7))  # Output: Odd
```

**Example 2: Finding the Remainder**
```python
def find_remainder(dividend, divisor):
    return dividend % divisor

remainder = find_remainder(10, 3)
print(f"The remainder of 10 divided by 3 is {remainder}")  # Output: The remainder of 10 divided by 3 is 1
```

**Example 3: Using Modulus in a Loop**
```python
for i in range(10):
    if i % 2 == 0:
        print(f"{i} is even")
    else:
        print(f"{i} is odd")
```
This loop will iterate through numbers from 0 to 9 and print whether each number is even or odd using the modulus operator.

#Modulus #Python