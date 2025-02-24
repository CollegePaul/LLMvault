### Exception Handling in C++

Exception handling in C++ is a mechanism that allows a program to handle runtime errors or exceptional conditions gracefully. It provides a way to transfer control from one part of a program to another in response to an exception being thrown and caught. The primary components of exception handling in C++ are:

1. **try block**: A section of code where exceptions may occur. This is the place where you wrap your risky operations that might throw an exception.
2. **catch block**: Code that handles the exception thrown by the try block. You can have multiple catch blocks to handle different types of exceptions.
3. **throw statement**: Used to generate an exception within a program. When a throw statement is executed, it causes control to jump to the first matching catch handler.

Here is a simple example in C++:

```cpp
#include <iostream>

int divide(int numerator, int denominator) {
    if (denominator == 0) {
        throw std::runtime_error("Division by zero error");
    }
    return numerator / denominator;
}

int main() {
    try {
        int result = divide(10, 0);
        std::cout << "Result: " << result << std::endl;
    } catch (const std::exception& e) {
        std::cerr << "Exception caught: " << e.what() << std::endl;
    }
    return 0;
}
```

In this example, the `divide` function checks if the denominator is zero and throws a `std::runtime_error` if it is. The `main` function includes a try block that calls `divide`. If an exception is thrown, control is transferred to the catch block where the error message is printed.

### Equivalent Example in Python

In Python, exception handling is done using `try`, `except`, `else`, and `finally` blocks. Here’s how you can handle exceptions in a similar scenario:

```python
def divide(numerator, denominator):
    if denominator == 0:
        raise ValueError("Division by zero error")
    return numerator / denominator

try:
    result = divide(10, 0)
    print(f"Result: {result}")
except ValueError as e:
    print(f"Exception caught: {e}")
```

In this Python example, the `divide` function raises a `ValueError` if the denominator is zero. The `try` block calls `divide`, and any exceptions raised are caught in the `except` block where they are printed.

#Exception Handling #cpp