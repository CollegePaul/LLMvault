### Type Check in Python

Type checking in Python refers to the process of verifying that the variables, expressions, and function parameters used in a program conform to expected types. Python supports both dynamic type checking, which occurs at runtime, and static type checking using tools like `mypy`, which can be done before the code is executed.

Dynamic type checking involves checking types during runtime. This is typical for Python since it is a dynamically typed language. Here’s an example of how you might perform a type check at runtime:

```python
def print_length(obj):
    if isinstance(obj, (list, tuple, str)):
        print(f"The length of the object is: {len(obj)}")
    else:
        print("The provided object does not have a length.")

# Examples
print_length([1, 2, 3])  # Output: The length of the object is: 3
print_length("hello")    # Output: The length of the object is: 5
print_length(42)        # Output: The provided object does not have a length.
```

Static type checking involves annotating variables, function parameters, and return types with expected data types. This doesn’t change how your code runs but allows tools like `mypy` to check for type consistency before execution:

```python
def add_numbers(a: int, b: int) -> int:
    return a + b

# Example usage
result = add_numbers(3, 4)
print(result)  # Output: 7
```

In the static typing example above, we have specified that `add_numbers` should take two integers and return an integer. Tools like `mypy` can check these annotations for consistency.

Type checking is crucial for catching errors early in the development process and making your code more robust and maintainable. #Type check #Python