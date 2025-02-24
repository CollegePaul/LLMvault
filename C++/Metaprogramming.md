### Metaprogramming in C++

Metaprogramming in C++ refers to the practice of writing code that can manipulate or "program" other programs. This concept allows developers to generate, modify, and analyze code at compile-time rather than run-time. C++ supports metaprogramming through features like templates, constexpr functions, and macros.

**Templates** are a fundamental part of C++ metaprogramming. They enable the creation of generic code that can operate on different data types without losing type safety. For instance, you can use templates to implement algorithms that work with various data structures or perform compile-time computations.

```cpp
// Example: Template for calculating factorial at compile time
template<int N>
struct Factorial {
    static const int value = N * Factorial<N - 1>::value;
};

template<>
struct Factorial<0> {
    static const int value = 1;
};

int main() {
    constexpr int result = Factorial<5>::value; // Computes at compile time
    return 0;
}
```

**Constexpr functions** allow for more flexible and readable compile-time computations compared to templates. They can be used to perform arithmetic operations, comparisons, and other tasks during compilation.

```cpp
// Example: Constexpr function for calculating factorial
constexpr int factorial(int n) {
    if (n <= 1)
        return 1;
    else
        return n * factorial(n - 1);
}

int main() {
    constexpr int result = factorial(5); // Computes at compile time
    return 0;
}
```

**Macros**, though not as powerful or type-safe as templates or constexpr, are another form of metaprogramming in C++. They allow for simple text substitution during the preprocessing stage.

```cpp
// Example: Macro for calculating square
#define SQUARE(x) ((x) * (x))

int main() {
    int result = SQUARE(5); // Expands to ((5) * (5)) at compile time
    return 0;
}
```

### Metaprogramming in Python

While C++ is known for its advanced metaprogramming capabilities, Python also supports a form of metaprogramming through features like decorators, metaclasses, and the `exec` function. However, Python's metaprogramming is generally simpler compared to C++.

**Decorators** are a common way to modify functions or methods at runtime. They can be used for logging, access control, memoization, and other purposes.

```python
# Example: Decorator for logging function calls
def log_function_call(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__} with arguments {args} and keyword arguments {kwargs}")
        result = func(*args, **kwargs)
        print(f"{func.__name__} returned {result}")
        return result
    return wrapper

@log_function_call
def add(a, b):
    return a + b

add(3, 4)  # Output: Calling add with arguments (3, 4) and keyword arguments {}
           #         add returned 7
```

**Metaclasses** are used to customize class creation. They can be thought of as "classes of classes" that define how a class behaves.

```python
# Example: Metaclass for automatically adding a 'greet' method to classes
class GreetingMeta(type):
    def __new__(cls, name, bases, dct):
        dct['greet'] = lambda self: f"Hello from {self.__class__.__name__}!"
        return super().__new__(cls, name, bases, dct)

class MyClass(metaclass=GreetingMeta):
    pass

obj = MyClass()
print(obj.greet())  # Output: Hello from MyClass!
```

**Exec Function** allows for dynamic execution of Python code. It can be used to execute strings containing Python statements.

```python
# Example: Using exec to create a function dynamically
code = """
def dynamic_function():
    print("Hello from the dynamically created function!")
"""

exec(code)
dynamic_function()  # Output: Hello from the dynamically created function!
```

#Metaprogramming #cpp