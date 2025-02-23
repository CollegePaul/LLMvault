### Abstraction in Decomposition in Python

Decomposition is a fundamental concept in programming that involves breaking down complex problems into smaller, more manageable parts. Each part can then be solved individually or handled as a single unit within a larger system. Abstraction plays a crucial role in this process by hiding the complexity of these parts and providing a simplified interface for interacting with them.

In Python, abstraction is often achieved through functions, classes, and modules. Functions allow you to encapsulate a piece of code that performs a specific task, while classes encapsulate data and behavior related to an object. Modules help in organizing and managing code by grouping related functions and classes together.

#### Example using Functions

Consider the problem of calculating the area of different shapes (e.g., rectangle, circle). Instead of writing one large function that handles all cases, we can decompose the task into smaller functions for each shape:

```python
def calculate_rectangle_area(width, height):
    return width * height

def calculate_circle_area(radius):
    import math
    return math.pi * radius ** 2

# Using the abstracted functions
rectangle_area = calculate_rectangle_area(5, 10)
circle_area = calculate_circle_area(7)

print("Rectangle Area:", rectangle_area)
print("Circle Area:", circle_area)
```

In this example, `calculate_rectangle_area` and `calculate_circle_area` are functions that perform specific tasks. The user of these functions does not need to know the details of how the area is calculated; they just call the function with the required parameters.

#### Example using Classes

When dealing with more complex systems, classes can be used to encapsulate data and behavior related to an object. For instance, if we were modeling a bank account system, we could decompose it into different classes:

```python
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance

    def deposit(self, amount):
        if amount > 0:
            self.balance += amount
            return True
        return False

    def withdraw(self, amount):
        if 0 < amount <= self.balance:
            self.balance -= amount
            return True
        return False

# Using the BankAccount class
account = BankAccount("Alice", 100)
account.deposit(50)
account.withdraw(30)

print(f"{account.owner}'s balance is ${account.balance}")
```

Here, `BankAccount` is a class that encapsulates data (owner and balance) and methods (deposit and withdraw). The user of the class interacts with it through its public interface without needing to understand the internal implementation details.

#Abstraction in Decomposition #Python