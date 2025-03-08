### Introduction to Number Theory

Number Theory is a branch of pure mathematics primarily concerned with the properties and relationships of numbers, especially integers. It encompasses various topics such as prime numbers, divisibility, modular arithmetic, Diophantine equations, and more. Number theory has deep implications in cryptography, coding theory, and computer science.

#### Example: Prime Numbers

One fundamental concept in number theory is the identification of prime numbers—numbers greater than 1 that have no divisors other than 1 and themselves. For instance, 2, 3, 5, 7, 11, and 13 are prime numbers.

Here's a simple Python code example to determine if a given number is prime:

```python
def is_prime(n):
    """Check if a number is prime."""
    if n <= 1:
        return False
    if n == 2:
        return True
    if n % 2 == 0:
        return False
    for i in range(3, int(n**0.5) + 1, 2):
        if n % i == 0:
            return False
    return True

# Example usage
number = 29
if is_prime(number):
    print(f"{number} is a prime number.")
else:
    print(f"{number} is not a prime number.")
```

In this code, the `is_prime` function checks if a number is prime by testing divisibility. It first handles edge cases for numbers less than or equal to 1 and even numbers greater than 2. Then, it checks divisibility from 3 up to the square root of the number, skipping even numbers.

#NumberTheory #Maths #python