### Encapsulation in Python

Encapsulation is one of the fundamental concepts in object-oriented programming that involves bundling the data (attributes) and methods (functions) that operate on the data into a single unit or class. It also restricts direct access to some of an object's components, which can prevent the accidental modification of data. In Python, encapsulation is primarily achieved through the use of private and protected attributes and methods.

In Python, the convention for indicating that an attribute or method should not be accessed directly from outside the class is by prefixing its name with an underscore (`_`) for protected members and double underscores (`__`) for private members. While these do not enforce strict access control like in some other languages (e.g., C++), they serve as a strong hint to developers that these components should be treated as non-public.

#### Example of Encapsulation

```python
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner  # Public attribute
        self.__balance = balance  # Private attribute

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount
            print(f"Added {amount} to the balance")
        else:
            print("Deposit amount must be positive")

    def withdraw(self, amount):
        if 0 < amount <= self.__balance:
            self.__balance -= amount
            print(f"Withdrew {amount} from the balance")
        elif amount > self.__balance:
            print("Insufficient funds")
        else:
            print("Withdrawal amount must be positive")

    def get_balance(self):
        return self.__balance

# Creating an instance of BankAccount
account = BankAccount("John Doe", 100)

# Accessing public attribute
print(account.owner)  # Output: John Doe

# Trying to access private attribute (not recommended)
# print(account.__balance)  # This will raise an AttributeError

# Using methods to interact with the private data
account.deposit(50)
print(account.get_balance())  # Output: 150

account.withdraw(30)
print(account.get_balance())  # Output: 120
```

In this example, `__balance` is a private attribute that should not be accessed directly from outside the `BankAccount` class. The methods `deposit`, `withdraw`, and `get_balance` provide controlled access to modify and retrieve the balance.

#Encapsulation #Python