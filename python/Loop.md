### Understanding Loops in Python

Loops in Python are used to execute a block of code repeatedly until a certain condition is met. There are two main types of loops in Python: `for` loops and `while` loops.

#### For Loop
A `for` loop is used for iterating over a sequence (such as a list, tuple, dictionary, set, or string). Here’s an example of a `for` loop that prints each fruit in a list:

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

In this example, the loop iterates over each element in the `fruits` list and prints it.

#### While Loop
A `while` loop executes as long as a specified condition is true. Here’s an example of a `while` loop that counts from 1 to 5:

```python
count = 1
while count <= 5:
    print(count)
    count += 1
```

In this example, the loop will continue running until the value of `count` exceeds 5.

#### Nested Loops
You can also have nested loops in Python, where one loop is inside another. Here’s an example of a nested `for` loop:

```python
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for a in adj:
    for f in fruits:
        print(a, f)
```

In this example, the inner loop will run through all its iterations for each iteration of the outer loop.

#### Loop Control Statements
- `break`: Exits the loop immediately when encountered.
- `continue`: Skips the current iteration and moves to the next one.
- `pass`: Acts as a placeholder and does nothing; it’s used when no action is required syntactically but syntactically some code is required.

Example using `break`:

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    if fruit == "banana":
        break
    print(fruit)
```

In this example, the loop will stop executing as soon as it encounters "banana".

#Loop #Python