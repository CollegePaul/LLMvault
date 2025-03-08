### Understanding Unit Testing in Python

Unit testing is a software development process where individual components or units of source code are tested to ensure they work correctly. In Python, unit tests are typically written using the `unittest` framework, which provides a rich set of tools for constructing and running tests.

#### Key Concepts:
- **Test Case**: A test case is the smallest unit of testing that can be performed on an individual component or function.
- **Test Suite**: A collection of test cases and/or test suites. It’s used to aggregate tests that should be executed together.
- **Test Runner**: A tool for executing a set of tests and producing a report.

#### Writing a Unit Test:
To write a unit test in Python, follow these steps:

1. Import the `unittest` module.
2. Create a class that inherits from `unittest.TestCase`.
3. Define methods within this class to test specific functionality. Each method should start with the word `test`.
4. Use various assertion methods provided by the `unittest.TestCase` class to check for expected outcomes.

#### Example:
Let’s consider a simple function `add(a, b)` which adds two numbers and write unit tests for it.

```python
# Function to be tested
def add(a, b):
    return a + b

# Importing unittest module
import unittest

# Creating a class that inherits from unittest.TestCase
class TestAddFunction(unittest.TestCase):

    # Method to test the add function with positive numbers
    def test_add_positive_numbers(self):
        self.assertEqual(add(1, 2), 3)

    # Method to test the add function with negative numbers
    def test_add_negative_numbers(self):
        self.assertEqual(add(-1, -2), -3)

    # Method to test the add function with a positive and negative number
    def test_add_mixed_numbers(self):
        self.assertEqual(add(1, -2), -1)

# This allows running tests from the command line using 'python script_name.py'
if __name__ == '__main__':
    unittest.main()
```

In this example:
- We define a function `add` that adds two numbers.
- We create a test class `TestAddFunction` inheriting from `unittest.TestCase`.
- We write three test methods to check if the `add` function works correctly for different sets of inputs (positive, negative, and mixed).
- The `assertEqual` method is used to check if the output of `add` matches the expected result.
- Finally, we call `unittest.main()` to run all the tests when the script is executed.

#Unit test #Python