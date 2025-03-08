### Understanding Loops in Python

In Python, loops are used to execute a block of code repeatedly until a certain condition is met. There are two primary types of loops in Python: `for` loops and `while` loops.

#### For Loop
A `for` loop iterates over a sequence (such as a list, tuple, dictionary, set, or string) allowing you to execute a block of code for each item in the sequence.

**Example:**
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```
In this example, `fruit` takes on the value of each item in the list `fruits`, one at a time, and prints it.

#### While Loop
A `while` loop continues to execute as long as a specified condition is `True`. If the condition becomes `False`, the loop terminates.

**Example:**
```python
count = 0
while count < 5:
    print(count)
    count += 1
```
Here, the loop prints the value of `count` and then increments it by one each time through the loop. The loop stops when `count` is no longer less than 5.

#### Additional Loop Control Statements
- **Break:** Exits a loop prematurely.
- **Continue:** Skips the current iteration and moves to the next.
- **Else with Loops:** Executes after a loop finishes, but only if it wasn't terminated by a `break`.

**Example of Break:**
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    if fruit == "banana":
        break
    print(fruit)
```
In this example, the loop stops when it reaches `"banana"` and does not print it.

**Example of Continue:**
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    if fruit == "banana":
        continue
    print(fruit)
```
Here, `"banana"` is skipped over, and the loop continues with the next item.

**Example of Else with For Loop:**
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    if fruit == "orange":
        break
else:
    print("No orange found")
```
In this example, since `"orange"` is not found in the list, the `else` block executes.

Loops are fundamental to programming as they allow for efficient automation of repetitive tasks. #Python #Loops