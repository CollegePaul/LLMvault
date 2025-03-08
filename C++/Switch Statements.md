### Switch Statements in C++

In C++, switch statements provide a way to execute one block of code among many alternatives. It is often used as a cleaner alternative to multiple if-else statements, especially when dealing with integer or character types. The syntax involves a control expression that is evaluated once and compared against several constant values (known as cases). If a match is found, the corresponding block of code is executed.

Here’s a basic structure:

```cpp
switch (expression) {
    case value1:
        // Code to be executed if expression == value1
        break;
    case value2:
        // Code to be executed if expression == value2
        break;
    default:
        // Code to be executed if expression does not match any of the above cases
}
```

The `break` statement is crucial as it prevents fall-through, which would cause execution to continue into subsequent cases. The `default` case is optional and acts as a catch-all for values that do not match any specified cases.

#### Example in C++

```cpp
#include <iostream>
using namespace std;

int main() {
    int number = 2;
    switch (number) {
        case 1:
            cout << "Number is 1" << endl;
            break;
        case 2:
            cout << "Number is 2" << endl;
            break;
        case 3:
            cout << "Number is 3" << endl;
            break;
        default:
            cout << "Number is not 1, 2, or 3" << endl;
    }
    return 0;
}
```

### Example in Python

Python does not have a built-in switch statement, but similar functionality can be achieved using dictionaries to map cases to functions or values.

#### Example in Python Using Dictionary

```python
def case_1():
    return "Number is 1"

def case_2():
    return "Number is 2"

def case_3():
    return "Number is 3"

def default_case():
    return "Number is not 1, 2, or 3"

switch_dict = {
    1: case_1,
    2: case_2,
    3: case_3
}

number = 2

# Get the function from switch_dict and call it
result = switch_dict.get(number, default_case)()
print(result)
```

This Python example mimics a switch statement by using a dictionary to map `number` values to corresponding functions. The `get` method is used to retrieve the appropriate function, with `default_case` as the fallback if the key is not found.

#Switch Statements #cpp