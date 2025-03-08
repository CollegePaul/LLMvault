### Function Overloading in C++

Function overloading in C++ allows multiple functions to have the same name but different parameters. This means that you can create several functions with the same name, as long as their parameter lists are different. The compiler decides which function to call based on the arguments passed to it during a function call.

For example, consider the following code snippet where we overload a function named `print`:

```cpp
#include <iostream>

void print(int i) {
    std::cout << "Printing int: " << i << std::endl;
}

void print(double f) {
    std::cout << "Printing float: " << f << std::endl;
}

void print(char* c) {
    std::cout << "Printing character: " << c << std::endl;
}

int main() {
    print(10);
    print(3.14);
    print("Hello, World!");

    return 0;
}
```

In this example, the `print` function is overloaded to handle different data types—integer, double, and character array.

### Function Overloading in Python

Python does not support traditional function overloading as seen in C++. However, you can achieve similar functionality using default arguments or variable-length argument lists.

Here's an example using default arguments:

```python
def print_item(item=None):
    if isinstance(item, int):
        print(f"Printing integer: {item}")
    elif isinstance(item, float):
        print(f"Printing float: {item}")
    elif isinstance(item, str):
        print(f"Printing string: {item}")

print_item(10)
print_item(3.14)
print_item("Hello, World!")
```

And here's an example using variable-length argument lists:

```python
def print_items(*args):
    for item in args:
        if isinstance(item, int):
            print(f"Printing integer: {item}")
        elif isinstance(item, float):
            print(f"Printing float: {item}")
        elif isinstance(item, str):
            print(f"Printing string: {item}")

print_items(10, 3.14, "Hello, World!")
```

In both Python examples, we achieve similar behavior to function overloading in C++ by using different techniques.

#Function_Overloading #cpp