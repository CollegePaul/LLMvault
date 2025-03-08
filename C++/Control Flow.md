### Control Flow in C++

Control flow in C++ refers to the order in which statements are executed within a program. It allows the programmer to control the flow of execution based on certain conditions or repeated actions. The primary mechanisms for controlling flow in C++ include conditional statements (like `if`, `else if`, and `switch`), loops (`for`, `while`, and `do-while`), and jump statements (`break`, `continue`, and `return`).

#### Conditional Statements

**If Statement:**
```cpp
int x = 10;
if (x > 5) {
    std::cout << "x is greater than 5" << std::endl;
}
```

**Else If Statement:**
```cpp
int x = 3;
if (x > 5) {
    std::cout << "x is greater than 5" << std::endl;
} else if (x == 5) {
    std::cout << "x is equal to 5" << std::endl;
} else {
    std::cout << "x is less than 5" << std::endl;
}
```

**Switch Statement:**
```cpp
int day = 3;
switch (day) {
case 1:
    std::cout << "Monday" << std::endl;
    break;
case 2:
    std::cout << "Tuesday" << std::endl;
    break;
case 3:
    std::cout << "Wednesday" << std::endl;
    break;
default:
    std::cout << "Another day" << std::endl;
}
```

#### Loops

**For Loop:**
```cpp
for (int i = 0; i < 5; ++i) {
    std::cout << "Iteration " << i << std::endl;
}
```

**While Loop:**
```cpp
int i = 0;
while (i < 5) {
    std::cout << "Iteration " << i << std::endl;
    ++i;
}
```

**Do-While Loop:**
```cpp
int i = 0;
do {
    std::cout << "Iteration " << i << std::endl;
    ++i;
} while (i < 5);
```

#### Jump Statements

**Break Statement:**
```cpp
for (int i = 0; i < 10; ++i) {
    if (i == 5) break;
    std::cout << "Iteration " << i << std::endl;
}
```

**Continue Statement:**
```cpp
for (int i = 0; i < 10; ++i) {
    if (i % 2 == 0) continue;
    std::cout << "Odd number: " << i << std::endl;
}
```

**Return Statement:**
```cpp
int add(int a, int b) {
    return a + b;
}
```

### Equivalent Examples in Python

**If Statement:**
```python
x = 10
if x > 5:
    print("x is greater than 5")
```

**Else If Statement:**
```python
x = 3
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is equal to 5")
else:
    print("x is less than 5")
```

**Switch-like Statement using Dictionary (Python doesn't have a switch statement):**
```python
day = 3
switcher = {
    1: "Monday",
    2: "Tuesday",
    3: "Wednesday"
}
print(switcher.get(day, "Another day"))
```

**For Loop:**
```python
for i in range(5):
    print("Iteration", i)
```

**While Loop:**
```python
i = 0
while i < 5:
    print("Iteration", i)
    i += 1
```

**Do-While-like Loop (Python doesn't have a do-while loop):**
```python
i = 0
while True:
    print("Iteration", i)
    i += 1
    if not (i < 5):
        break
```

**Break Statement:**
```python
for i in range(10):
    if i == 5:
        break
    print("Iteration", i)
```

**Continue Statement:**
```python
for i in range(10):
    if i % 2 == 0:
        continue
    print("Odd number:", i)
```

**Return Statement:**
```python
def add(a, b):
    return a + b
```

#Control Flow #cpp