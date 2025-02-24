### Lambda Expressions in C++

Lambda expressions provide a convenient way to define anonymous functions directly within code, especially useful for short snippets that are used only once. Introduced in C++11, lambda expressions allow the creation of inline functions without having to explicitly declare and name them.

A basic lambda expression consists of three parts:
- **Capture list**: Specifies which variables from the enclosing scope can be used inside the lambda.
- **Parameter list**: Similar to a regular function, it defines the parameters that the lambda takes.
- **Body**: Contains the code that executes when the lambda is called.

The general syntax for a lambda expression in C++ is:
```cpp
[capture_list](parameters) -> return_type { body }
```

#### Example in C++
Here’s an example of using a lambda expression to sort a vector of integers based on their absolute values:

```cpp
#include <iostream>
#include <vector>
#include <algorithm>

int main() {
    std::vector<int> numbers = {-1, 2, -3, 4, -5};

    // Using lambda expression to sort by absolute value
    std::sort(numbers.begin(), numbers.end(), [](int a, int b) {
        return abs(a) < abs(b);
    });

    for (int num : numbers) {
        std::cout << num << " ";
    }
    // Output: -1 2 -3 4 -5

    return 0;
}
```

#### Similar Example in Python
Python does not have lambda expressions in the same form as C++, but it does support anonymous functions using the `lambda` keyword. Here’s how you could achieve a similar result to the above example in Python:

```python
numbers = [-1, 2, -3, 4, -5]

# Using lambda function to sort by absolute value
sorted_numbers = sorted(numbers, key=lambda x: abs(x))

print(sorted_numbers)  # Output: [-1, 2, -3, 4, -5]
```

In this Python example, the `lambda` keyword is used to create a small anonymous function that takes one argument `x` and returns its absolute value. This lambda function is then passed as the `key` argument to the `sorted()` function.

#Lambda_Expressions #cpp