### Loops in C++

In C++, loops are used to execute a block of code repeatedly as long as a specified condition is true. There are two primary types of loops: `for` and `while`.

#### For Loop

The `for` loop is ideal for situations where the number of iterations is known before entering the loop. It consists of three main components: initialization, condition, and increment/decrement statement.

**Syntax:**
```cpp
for (initialization; condition; increment/decrement) {
    // Code to be executed
}
```

**Example in C++:**
```cpp
#include <iostream>
using namespace std;

int main() {
    for (int i = 0; i < 5; i++) {
        cout << "Iteration number: " << i << endl;
    }
    return 0;
}
```
In this example, the loop will iterate five times, printing the iteration number each time.

**Equivalent Example in Python:**
```python
for i in range(5):
    print(f"Iteration number: {i}")
```

#### While Loop

The `while` loop is used when the exact number of iterations is not known beforehand and depends on a condition that is evaluated before each iteration.

**Syntax:**
```cpp
while (condition) {
    // Code to be executed
}
```

**Example in C++:**
```cpp
#include <iostream>
using namespace std;

int main() {
    int i = 0;
    while (i < 5) {
        cout << "Iteration number: " << i << endl;
        i++;
    }
    return 0;
}
```
This loop will also iterate five times, printing the iteration number each time.

**Equivalent Example in Python:**
```python
i = 0
while i < 5:
    print(f"Iteration number: {i}")
    i += 1
```

### #Loops (For, While) #cpp