### Method Overloading in Python

In Python, method overloading as seen in languages like Java or C++ does not exist in the same way. Python does not support traditional method overloading by default because it uses dynamic typing and allows functions to accept a variable number of arguments using default parameters and variable-length argument lists.

However, you can simulate method overloading in Python by using default arguments, `*args`, and `**kwargs` to handle different types of function calls. Here are some examples demonstrating these techniques:

#### Using Default Arguments

```python
def greet(name, greeting="Hello"):
    print(f"{greeting}, {name}!")

greet("Alice")        # Output: Hello, Alice!
greet("Bob", "Hi")    # Output: Hi, Bob!
```

#### Using *args (Variable-length arguments)

```python
def add(*numbers):
    return sum(numbers)

print(add(1, 2))       # Output: 3
print(add(1, 2, 3, 4)) # Output: 10
```

#### Using **kwargs (Keyword arguments)

```python
def display_info(**info):
    for key, value in info.items():
        print(f"{key}: {value}")

display_info(name="Alice", age=25)
# Output:
# name: Alice
# age: 25

display_info(city="Wonderland", country="Fantasia")
# Output:
# city: Wonderland
# country: Fantasia
```

These examples show how you can achieve similar functionality to method overloading in Python. While it's not the same as classical overloading, these techniques allow functions to handle different numbers and types of arguments flexibly.

#Overloading #Python