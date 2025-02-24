### Polymorphism in C++

Polymorphism is a core concept in object-oriented programming that allows objects to be treated as instances of their parent class rather than their actual class. It enables one interface to be used for a general class of actions. The most common use of polymorphism is when a parent class reference is used to refer to a child class object.

In C++, polymorphism is primarily achieved through two mechanisms:
1. **Function Overloading**: This allows multiple functions to have the same name but different parameters.
2. **Virtual Functions and Function Overriding**: Virtual functions allow a base class function to be overridden in derived classes, enabling dynamic method binding.

Here's an example of polymorphism using virtual functions in C++:

```cpp
#include <iostream>
using namespace std;

class Animal {
public:
    virtual void speak() { // Virtual function
        cout << "Some sound" << endl;
    }
};

class Dog : public Animal {
public:
    void speak() override { // Overriding the base class function
        cout << "Bark" << endl;
    }
};

class Cat : public Animal {
public:
    void speak() override { // Overriding the base class function
        cout << "Meow" << endl;
    }
};

int main() {
    Animal* animal1 = new Dog();
    Animal* animal2 = new Cat();

    animal1->speak(); // Outputs: Bark
    animal2->speak(); // Outputs: Meow

    delete animal1;
    delete animal2;

    return 0;
}
```

In this example, the `Animal` class has a virtual function `speak()`. The `Dog` and `Cat` classes override this function. When we call `speak()` on pointers of type `Animal` that point to `Dog` and `Cat` objects, the overridden functions are called based on the actual object type.

### Example in Python

Python supports polymorphism through method overriding and duck typing. Here's how you can achieve similar functionality in Python:

```python
class Animal:
    def speak(self):
        print("Some sound")

class Dog(Animal):
    def speak(self):
        print("Bark")

class Cat(Animal):
    def speak(self):
        print("Meow")

def animal_sound(animal):
    animal.speak()

dog = Dog()
cat = Cat()

animal_sound(dog)  # Outputs: Bark
animal_sound(cat)  # Outputs: Meow
```

In this Python example, the `speak()` method is overridden in the `Dog` and `Cat` classes. The function `animal_sound()` takes an `Animal` object and calls its `speak()` method, demonstrating polymorphism.

#Polymorphism #cpp