### Constructors and Destructors in C++

In C++, constructors and destructors are special member functions that manage the initialization and cleanup of objects. 

**Constructors** are called automatically when an object is created, used to initialize the data members of the class. There are several types of constructors:
- **Default Constructor**: Takes no parameters.
- **Parameterized Constructor**: Takes one or more parameters.
- **Copy Constructor**: Used to create a new object as a copy of an existing object.

**Destructors**, on the other hand, are called automatically when an object is destroyed (e.g., goes out of scope), used for cleaning up resources such as closing files or releasing memory.

Here’s a simple example in C++:

```cpp
class Rectangle {
public:
    int width, height;

    // Default Constructor
    Rectangle() : width(0), height(0) {}

    // Parameterized Constructor
    Rectangle(int w, int h) : width(w), height(h) {}

    // Copy Constructor
    Rectangle(const Rectangle &other) : width(other.width), height(other.height) {}

    ~Rectangle() {
        // Destructor code here (e.g., freeing resources)
        std::cout << "Destructor called" << std::endl;
    }
};

int main() {
    Rectangle rect1;          // Calls default constructor
    Rectangle rect2(5, 3);    // Calls parameterized constructor
    Rectangle rect3 = rect2;  // Calls copy constructor

    return 0;
}
```

### Python Equivalent Example

In Python, constructors and destructors are handled differently. Python uses `__init__` for initialization (similar to a constructor) and `__del__` for cleanup (similar to a destructor), but it’s less commonly used due to automatic garbage collection.

Here's how you might implement something similar in Python:

```python
class Rectangle:
    def __init__(self, width=0, height=0):
        self.width = width
        self.height = height
        print("Constructor called")

    def __del__(self):
        print("Destructor called")

rect1 = Rectangle()          # Calls default constructor (default values)
rect2 = Rectangle(5, 3)      # Calls parameterized constructor with values

# Python handles the cleanup automatically, but __del__ is still called
```

### Tags:
#Constructors and Destructors  
#cpp