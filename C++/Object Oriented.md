### Object-Oriented Programming in C++

Object-Oriented Programming (OOP) is a programming paradigm that uses "objects" to design applications and computer programs. It emphasizes the use of data, or objects, rather than functions and logic. The main concepts of OOP are encapsulation, inheritance, polymorphism, and abstraction.

1. **Encapsulation**: Encapsulation is the mechanism of hiding the internal representation, or state, and requiring all interaction to be performed through an object's methods. In C++, this is achieved using classes where members can be declared as private, protected, or public. 

2. **Inheritance**: Inheritance allows a new class (derived class) to inherit properties and behaviors (methods) from an existing class (base class). This promotes code reusability.

3. **Polymorphism**: Polymorphism allows objects of different classes to be treated as objects of a common superclass. It can be achieved through method overriding and function overloading in C++.

4. **Abstraction**: Abstraction involves hiding the complex reality while exposing only the necessary parts. It is used to reduce programming complexity and effort by allowing programmers to focus on interactions at a higher level without needing to understand all the details.

### Example Using Python

While the examples will be in C++, we can illustrate similar concepts using Python, which also supports OOP.

#### Encapsulation in Python:
```python
class Account:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.__balance = balance  # Private attribute

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount
            return True
        else:
            return False

    def withdraw(self, amount):
        if 0 < amount <= self.__balance:
            self.__balance -= amount
            return True
        else:
            return False

    def get_balance(self):
        return self.__balance

# Usage
acc = Account("John")
acc.deposit(100)
print(acc.get_balance())  # Output: 100
```

#### Inheritance in Python:
```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        raise NotImplementedError("Subclasses must implement this method")

class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

# Usage
dog = Dog("Buddy")
print(dog.speak())  # Output: Buddy says Woof!
```

#### Polymorphism in Python:
```python
class Cat(Animal):
    def speak(self):
        return f"{self.name} says Meow!"

def animal_sound(animal):
    print(animal.speak())

# Usage
dog = Dog("Buddy")
cat = Cat("Whiskers")

animal_sound(dog)  # Output: Buddy says Woof!
animal_sound(cat)  # Output: Whiskers says Meow!
```

#### Abstraction in Python:
```python
from abc import ABC, abstractmethod

class Vehicle(ABC):
    @abstractmethod
    def start(self):
        pass

class Car(Vehicle):
    def start(self):
        print("Car is starting")

# Usage
car = Car()
car.start()  # Output: Car is starting
```

#Object Oriented #cpp