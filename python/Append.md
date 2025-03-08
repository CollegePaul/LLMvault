### Explanation of Append in Python

In Python, the `append()` method is used to add an element to the end of a list. This method modifies the original list by adding the new element at the last position. It takes one argument, which is the item you want to add to the list.

Here's how it works:

```python
# Create a list
my_list = [1, 2, 3]

# Use append() to add an element to the end of the list
my_list.append(4)

# Print the updated list
print(my_list)  # Output: [1, 2, 3, 4]
```

In this example, we start with a list `my_list` containing three elements. By using the `append()` method and passing `4` as an argument, we add `4` to the end of the list.

Another example demonstrating appending different data types:

```python
# Create a list with mixed data types
mixed_list = ['apple', 3.14, True]

# Append a string
mixed_list.append('banana')

# Append an integer
mixed_list.append(42)

# Print the updated list
print(mixed_list)  # Output: ['apple', 3.14, True, 'banana', 42]
```

In this case, `mixed_list` initially contains a string, a float, and a boolean value. We use the `append()` method to add a string `'banana'` and an integer `42` to the list.

#Append #Python