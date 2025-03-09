### Introduction to Number Theory

Number Theory is a branch of pure mathematics devoted primarily to the study of integers and integer-valued functions. It encompasses a wide range of topics, including prime numbers, divisibility, congruences, Diophantine equations, quadratic residues, and more. The field has both theoretical and practical applications, with links to cryptography, coding theory, and computer science.

#### Key Concepts

1. **Divisibility**: This is the basic concept where one number can divide another without leaving a remainder. For example, 4 divides 8 (written as \(4|8\)) because there's no remainder when 8 is divided by 4.

2. **Prime Numbers**: A prime number is a natural number greater than 1 that has no positive divisors other than 1 and itself. The first few primes are 2, 3, 5, 7, 11, etc.

3. **Congruences**: This concept deals with the remainder of division operations. Two numbers \(a\) and \(b\) are congruent modulo \(m\) (written as \(a \equiv b \mod m\)) if they have the same remainder when divided by \(m\).

4. **Diophantine Equations**: These are polynomial equations whose solutions are sought among integers. An example is \(x^2 + y^2 = z^2\), which represents Pythagorean triples.

#### Python Examples

Here are a few examples demonstrating some of these concepts in Python:

1. **Checking Divisibility**:
    ```python
    def is_divisible(a, b):
        return a % b == 0

    print(is_divisible(8, 4))  # Output: True
    ```

2. **Finding Prime Numbers** (using the Sieve of Eratosthenes):
    ```python
    def sieve_of_eratosthenes(n):
        primes = [True] * (n+1)
        p = 2
        while (p * p <= n):
            if (primes[p] == True):
                for i in range(p * p, n+1, p):
                    primes[i] = False
            p += 1
        prime_numbers = [p for p in range(2, n) if primes[p]]
        return prime_numbers

    print(sieve_of_eratosthenes(30))  # Output: [2, 3, 5, 7, 11, 13, 17, 19, 23, 29]
    ```

3. **Solving Congruences**:
    ```python
    def solve_congruence(a, b, m):
        for x in range(m):
            if (a * x) % m == b:
                return x
        return None

    print(solve_congruence(2, 3, 5))  # Output: 4 because (2*4)%5 = 8%5 = 3
    ```

Number Theory and Maths