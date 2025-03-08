### Built-in Functions in Python

Python comes equipped with a set of built-in functions that are always available for use. These functions provide a wide range of capabilities, from basic operations like mathematical calculations to more complex tasks such as manipulating data structures and handling files. They are integral to writing efficient and effective Python code.

Some common examples of built-in functions include:

- **`print()`**: Used to output data to the standard output device (like the screen).
  ```python
  print("Hello, World!")
  ```

- **`len()`**: Returns the number of items in an object like a string, list, tuple, or dictionary.
  ```python
  my_list = [1, 2, 3, 4, 5]
  length_of_list = len(my_list)
  print(length_of_list)  # Output: 5
  ```

- **`type()`**: Returns the type of an object.
  ```python
  my_var = "Hello"
  var_type = type(my_var)
  print(var_type)  # Output: <class 'str'>
  ```

- **`int()`, `float()`, `str()`**: These functions are used to convert data types between integers, floating-point numbers, and strings.
  ```python
  num_str = "123"
  num_int = int(num_str)
  print(type(num_int))  # Output: <class 'int'>
  ```

- **`input()`**: Reads a line from input (e.g., the user or a file).
  ```python
  name = input("Enter your name: ")
  print(f"Hello, {name}!")
  ```

- **`max()`, `min()`**: These functions return the maximum and minimum values in an iterable.
  ```python
  numbers = [3, 1, 4, 1, 5, 9]
  max_num = max(numbers)
  min_num = min(numbers)
  print(f"Max: {max_num}, Min: {min_num}")  # Output: Max: 9, Min: 1
  ```

- **`sum()`**: Sums up all the elements in an iterable.
  ```python
  total = sum([10, 20, 30])
  print(total)  # Output: 60
  ```

These functions are just a small sample of what Python offers. They enhance productivity and simplify code by providing essential functionalities directly accessible without the need for additional libraries.

#Built in functions #Python