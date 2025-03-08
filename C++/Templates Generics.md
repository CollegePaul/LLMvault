### Templates in C++

Templates in C++ are a powerful feature that allows you to write generic code, which can operate on different data types. They enable you to define functions or classes without specifying the exact type of the objects they will manipulate. Instead, placeholders for types (known as template parameters) are used, and these are replaced with actual types when the function or class is instantiated.

**Function Templates:**
A simple example of a function template in C++ could be a swap function that works for any data type:

```cpp
template <typename T>
void swap(T &a, T &b) {
    T temp = a;
    a = b;
    b = temp;
}
```

In this code, `typename T` is the template parameter. When you call `swap<int>(x, y);`, `T` gets replaced with `int`. Similarly, for other data types.

**Class Templates:**
Here's an example of a class template that defines a simple stack:

```cpp
template <typename T>
class Stack {
private:
    std::vector<T> elements;
public:
    void push(const T &element) { elements.push_back(element); }
    void pop() { elements.pop_back(); }
    const T& top() const { return elements.back(); }
};
```

In this example, `Stack<int>` would be a stack that holds integers, while `Stack<std::string>` would hold strings.

### Generics in Python

While C++ uses templates for generic programming, Python inherently supports generics through its dynamic typing system. However, Python 3.5 introduced type hints and the `typing` module to allow for more explicit and readable code when working with generic data types.

**Function Example:**
Here's a simple example of a function in Python that could be considered generic:

```python
def swap(a, b):
    return b, a

# Usage:
x, y = 10, 20
x, y = swap(x, y)  # Works with integers

x, y = "hello", "world"
x, y = swap(x, y)  # Works with strings
```

In Python, the `swap` function works for any type of arguments because Python is dynamically typed.

**Class Example:**
Python's list is a generic container that can hold elements of any type:

```python
class Stack:
    def __init__(self):
        self.elements = []
    
    def push(self, element):
        self.elements.append(element)
    
    def pop(self):
        return self.elements.pop()
    
    def top(self):
        return self.elements[-1]

# Usage:
int_stack = Stack()  # Works with integers
int_stack.push(10)
print(int_stack.top())

string_stack = Stack()  # Works with strings
string_stack.push("hello")
print(string_stack.top())
```

In this example, `Stack` can be used with any type of elements because Python's list is dynamic and can hold any type.

#Templates Generics #cpp