### Error Handling in C++

Error handling in C++ is crucial for writing robust programs that can deal with unexpected situations gracefully. C++ provides several mechanisms for error handling, primarily through the use of exceptions. Exceptions allow a program to transfer control from one part of the code to another when an error occurs, making it easier to manage errors and maintain clean code.

#### Basic Concepts

1. **Try Block**: Code that might throw an exception is placed inside a `try` block.
2. **Catch Block**: This block catches exceptions thrown by code in the try block. You can have multiple catch blocks for different types of exceptions.
3. **Throw Statement**: Used to throw an exception from a function or any part of the program.
4. **Exception Class**: Exceptions are typically objects, and C++ provides a standard hierarchy of exception classes.

#### Example

Here is a simple example demonstrating error handling using try, catch, and throw in C++:

```cpp
#include <iostream>
using namespace std;

double divide(double x, double y) {
    if (y == 0.0) {
        throw "Division by zero!";
    }
    return x / y;
}

int main() {
    try {
        cout << "Result: " << divide(10.0, 2.0) << endl;
        cout << "Result: " << divide(10.0, 0.0) << endl; // This will throw an exception
    } catch (const char* msg) {
        cerr << "Error: " << msg << endl;
    }
    return 0;
}
```

In this example, the `divide` function throws a string as an exception if it is asked to divide by zero. The main function catches this exception and prints an error message.

#### Custom Exceptions

C++ allows you to define your own exceptions by creating classes that inherit from the standard `std::exception`.

```cpp
#include <iostream>
#include <stdexcept> // for std::runtime_error
using namespace std;

class DivideByZeroException : public runtime_error {
public:
    DivideByZeroException() : runtime_error("Attempted division by zero") {}
};

double divide(double x, double y) {
    if (y == 0.0) {
        throw DivideByZeroException();
    }
    return x / y;
}

int main() {
    try {
        cout << "Result: " << divide(10.0, 2.0) << endl;
        cout << "Result: " << divide(10.0, 0.0) << endl; // This will throw an exception
    } catch (const DivideByZeroException& e) {
        cerr << "Error: " << e.what() << endl;
    }
    return 0;
}
```

In this enhanced example, a custom exception class `DivideByZeroException` is used. The `divide` function throws an instance of this exception when it encounters a division by zero.

### Python Equivalent

While C++ uses exceptions for error handling, Python also employs similar mechanisms. Here’s how you can achieve similar functionality in Python:

```python
class DivideByZeroException(Exception):
    def __init__(self, message="Attempted division by zero"):
        super().__init__(message)

def divide(x, y):
    if y == 0:
        raise DivideByZeroException()
    return x / y

try:
    print("Result:", divide(10.0, 2.0))
    print("Result:", divide(10.0, 0.0))  # This will throw an exception
except DivideByZeroException as e:
    print(f"Error: {e}")
```

In this Python example, a custom exception class `DivideByZeroException` is defined and raised when a division by zero is attempted. The `try` block attempts to perform the division, and if a `DivideByZeroException` is raised, it is caught in the `except` block.

#Error Handling #cpp