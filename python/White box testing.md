### White Box Testing in Python

White box testing, also known as structural or glass box testing, involves examining the internal structure of an application or its code. The focus is on ensuring that all paths through the program are tested to verify that each part of the source code works correctly. This type of testing requires a deep understanding of the system's architecture and implementation details.

In Python, white box testing can be performed using various techniques such as:

1. **Statement Coverage:** Ensuring that every line of code is executed at least once.
2. **Decision Coverage:** Testing all possible paths through conditional statements (if-else).
3. **Path Coverage:** Executing all possible paths in a program.
4. **Loop Coverage:** Verifying the execution of loops with different iterations.

To demonstrate white box testing, let's consider a simple Python function that calculates the factorial of a number:

```python
def factorial(n):
    if n < 0:
        raise ValueError("Factorial is not defined for negative numbers")
    elif n == 0 or n == 1:
        return 1
    else:
        result = 1
        for i in range(2, n + 1):
            result *= i
        return result

# Test cases for white box testing
def test_factorial():
    # Statement coverage: test each line of code
    assert factorial(0) == 1  # Tests the base case (n == 0)
    assert factorial(1) == 1  # Tests the base case (n == 1)
    
    try:
        factorial(-1)  # Tests the error handling for negative input
    except ValueError as e:
        assert str(e) == "Factorial is not defined for negative numbers"
    
    # Decision coverage: test both branches of if-else
    assert factorial(5) == 120  # Tests the else branch (n > 1)

# Run tests
test_factorial()
```

In this example:
- We ensure that all lines in the `factorial` function are executed by various test cases.
- We handle both branches of the if-else statements to achieve decision coverage.
- We include a test for the error handling mechanism.

By performing white box testing, developers can identify and fix bugs early in the development process, leading to more robust and reliable software. #White_box_testing #Python