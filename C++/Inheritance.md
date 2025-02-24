### Inheritance in C++

Inheritance is a fundamental concept in object-oriented programming that allows one class, known as a derived class or subclass, to inherit attributes and methods from another class, referred to as the base class or superclass. This mechanism promotes code reusability and establishes a hierarchical relationship between classes.

In C++, inheritance is implemented using access specifiers like `public`, `protected`, and `private`. The syntax for defining a derived class in C++ involves specifying the name of the base class after a colon (`:`) and an access specifier. For example:

```cpp
class Base {
public:
    void display() {
        std::cout << "Base Class" << std::endl;
    }
};

class Derived : public Base {
public:
    void show() {
        std::cout << "Derived Class" << std::endl;
    }
};

int main() {
    Derived d;
    d.display();  // Accessing base class method
    d.show();     // Accessing derived class method
    return 0;
}
```

In this example, `Derived` is a subclass of `Base`. The `public` access specifier means that the public members of `Base` are accessible as public members in `Derived`.

### Example Using Python

Python also supports inheritance. Here's how you can implement a similar scenario using Python:

```python
class Base:
    def display(self):
        print("Base Class")

class Derived(Base):
    def show(self):
        print("Derived Class")

d = Derived()
d.display()  # Accessing base class method
d.show()     # Accessing derived class method
```

In this Python example, `Derived` inherits from `Base`. The `display` method of `Base` is accessible through an instance of `Derived`.

#Inheritance #cpp