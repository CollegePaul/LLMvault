### Understanding Index in Python

In Python, an index refers to the position of an element within a sequence-like data structure such as strings, lists, tuples, or other iterable objects. Indexing allows you to access individual elements or slices of these sequences. It's important to note that Python uses zero-based indexing, meaning that the first element of a sequence is at index 0.

Here are some examples demonstrating how indices work in different data structures:

#### Example with Strings
```python
my_string = "Hello"
print(my_string[0])   # Output: H
print(my_string[-1])  # Output: o (negative indexing starts from the end)
```

#### Example with Lists
```python
my_list = [10, 20, 30, 40, 50]
print(my_list[2])     # Output: 30
print(my_list[-2])    # Output: 40 (accessing second last element)
```

#### Example with Tuples
```python
my_tuple = (1, 2, 3, 4, 5)
print(my_tuple[1])    # Output: 2
print(my_tuple[-1])   # Output: 5
```

In the examples above:
- `my_string[0]` and `my_list[2]` access elements at their respective zero-based indices.
- Negative indices like `-1`, `-2`, etc., are used to count from the end of the sequence.

Indexing is a fundamental concept in Python that enables efficient manipulation and retrieval of data stored in sequences. #Index #Python