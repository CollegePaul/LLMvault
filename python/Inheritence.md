### Inheritance in Python

Inheritance is a fundamental concept in object-oriented programming that allows a class to inherit attributes and methods from another class. The class that inherits is called the derived or child class, while the class being inherited from is called the base or parent class. This mechanism promotes code reusability and establishes a hierarchical relationship between classes.

Here’s a simple example to illustrate inheritance in Python:

```python
# Base class
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        raise NotImplementedError("Subclasses must implement this method")

# Derived class
class Dog(Animal):
    def speak(self):
        return f"{self.name} says Woof!"

# Another derived class
class Cat(Animal):
    def speak(self):
        return f"{self.name} says Meow!"

# Creating instances of the derived classes
dog = Dog("Buddy")
cat = Cat("Whiskers")

print(dog.speak())  # Output: Buddy says Woof!
print(cat.speak())  # Output: Whiskers says Meow!
```

In this example, `Animal` is a base class with an initializer (`__init__`) and a method (`speak`). The `Dog` and `Cat` classes are derived from the `Animal` class. They inherit the `name` attribute and override the `speak` method to provide specific implementations for each type of animal.

This demonstrates how inheritance allows you to create specialized classes that share common functionality while also having unique behaviors. #Inheritence #Python