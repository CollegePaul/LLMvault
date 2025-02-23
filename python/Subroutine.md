### Subroutines in Python

In Python, subroutines are primarily referred to as functions. Functions allow you to encapsulate code into reusable blocks, making your code more organized and modular. By defining a function once, you can call it multiple times throughout your program with different arguments if needed.

#### Key Characteristics of Functions in Python:

1. **Encapsulation:** Functions allow you to group related statements into a logical unit.
2. **Reusability:** Once a function is defined, it can be used (or called) multiple times without rewriting the code.
3. **Modularity:** Functions make your program more readable and manageable by breaking down complex problems into smaller parts.

#### Defining a Function:

To define a function in Python, you use the `def` keyword followed by the function name and parentheses which may include parameters. The statements that form the body of the function start with indentation and end when the indentation stops.

```python
# Example of defining a simple function to add two numbers

def add_numbers(a, b):
    """This function takes two numbers and returns their sum."""
    return a + b
```

#### Calling a Function:

Once you have defined a function, you can use it by calling its name followed by parentheses which may include arguments.

```python
# Example of calling the previously defined function

result = add_numbers(5, 3)
print("The sum is:", result)  # Output: The sum is: 8
```

#### Functions with Default Parameters:

Functions can also have default parameters. If a value is not provided for these parameters when the function is called, the default value will be used.

```python
# Example of a function with default parameter

def greet(name="World"):
    """This function greets to the person passed in as argument."""
    print(f"Hello, {name}!")

greet()          # Output: Hello, World!
greet("Alice")   # Output: Hello, Alice!
```

#### Functions Returning Multiple Values:

Functions can return multiple values by returning them as a tuple.

```python
# Example of a function that returns two values

def calculate_area_and_perimeter(length, width):
    area = length * width
    perimeter = 2 * (length + width)
    return area, perimeter

area, perimeter = calculate_area_and_perimeter(5, 3)
print("Area:", area)        # Output: Area: 15
print("Perimeter:", perimeter)  # Output: Perimeter: 16
```

Functions are a fundamental aspect of writing clean and efficient code in Python. They help in reducing redundancy, improving readability, and facilitating debugging.

#Subroutine #Python