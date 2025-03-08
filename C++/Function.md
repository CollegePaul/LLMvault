### Functions in C++

Functions in C++ are blocks of code that perform specific tasks. They help organize code into manageable sections, enhance reusability, and improve readability. A function can take inputs as parameters, execute a series of statements, and optionally return a value to the caller.

**Key Components of a Function:**
- **Function Declaration:** Specifies the function's name, return type, and parameter list.
  ```cpp
  int add(int a, int b);
  ```
- **Function Definition:** Contains the code that executes when the function is called. It includes the declaration and the body enclosed in curly braces `{}`.
  ```cpp
  int add(int a, int b) {
      return a + b;
  }
  ```
- **Function Call:** Invokes the function with specified arguments.
  ```cpp
  int result = add(3, 4); // Calls 'add' and stores the result (7) in 'result'
  ```

**Example of a Simple Function:**

```cpp
#include <iostream>
using namespace std;

// Function Declaration
int multiply(int x, int y);

int main() {
    int num1 = 5;
    int num2 = 6;
    
    // Function Call
    int product = multiply(num1, num2);
    
    cout << "The product of " << num1 << " and " << num2 << " is: " << product << endl;
    
    return 0;
}

// Function Definition
int multiply(int x, int y) {
    return x * y; // Returns the product of x and y
}
```

In this example:
- The function `multiply` is declared to take two integer parameters and return an integer.
- It is defined to return the product of its two parameters.
- Inside `main`, the function `multiply` is called with arguments `5` and `6`. The result, which is `30`, is stored in `product` and then printed.

#Function #cpp