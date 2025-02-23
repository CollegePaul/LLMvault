### Procedures in Python

In Python, procedures are generally referred to as functions. A function is a block of organized, reusable code that performs a single, related action. Functions provide better modularity for your application and a high degree of code reusing.

Functions in Python can take parameters (arguments), which are values passed into the function, and they can also return data as a result. The `def` keyword is used to declare a new function in Python.

Here's a simple example of a function that takes two arguments and returns their sum:

```python
# Define a function named 'add'
def add(a, b):
    """Return the sum of two numbers."""
    return a + b

# Call the function with two arguments
result = add(3, 5)

# Print the result
print(result)  # Output: 8
```

In this example:
- `def add(a, b):` defines a new function called `add` that takes two parameters `a` and `b`.
- The line `return a + b` computes the sum of `a` and `b`, and returns it.
- `result = add(3, 5)` calls the `add` function with arguments `3` and `5`, and stores the returned value in the variable `result`.

Functions can also have default parameters, which allows them to be called with fewer arguments than defined. Here's an example:

```python
# Define a function with a default parameter
def greet(name, greeting="Hello"):
    """Print a greeting message."""
    print(f"{greeting}, {name}!")

# Call the function with both arguments
greet("Alice", "Hi")  # Output: Hi, Alice!

# Call the function with only one argument
greet("Bob")          # Output: Hello, Bob!
```

In this example:
- The `greet` function is defined with two parameters: `name` and `greeting`. The `greeting` parameter has a default value of `"Hello"`.
- When calling the function with both arguments (`greet("Alice", "Hi")`), it overrides the default greeting.
- When calling the function with only one argument (`greet("Bob")`), it uses the default greeting.

Procedures (functions) are fundamental building blocks in Python programming, enabling you to write clear and maintainable code. #Procedure #Python