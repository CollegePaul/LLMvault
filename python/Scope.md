### Scope in Python

In Python, scope refers to the region of a program where a particular variable or function is accessible. There are primarily four types of scopes in Python:

1. **Local Scope**: Variables defined within a function are local to that function and cannot be accessed outside it.
2. **Enclosing Scope**: This occurs when you have nested functions, and the inner function has access to variables from the outer (enclosing) function's scope.
3. **Global Scope**: Variables defined at the top level of a script or module are global in nature and can be accessed anywhere within the module.
4. **Built-in Scope**: This is the widest scope containing all built-in names available to a Python program, such as `print`, `len`, etc.

Understanding these scopes helps manage variable lifetimes and access, preventing unintended interactions between different parts of a program.

#### Example Code

```python
# Global Scope
x = 10

def outer_function():
    # Enclosing Scope
    y = 20
    
    def inner_function():
        # Local Scope
        z = 30
        print(f"Inner function: x={x}, y={y}, z={z}")
    
    inner_function()
    print(f"Outer function: x={x}, y={y}")

outer_function()

# Trying to access local variable 'z' outside its scope will raise an error
# print(z)  # Uncommenting this line will cause a NameError

print(f"Global scope: x={x}")
```

In the example above:
- `x` is accessible everywhere because it's in the global scope.
- `y` can be accessed within both `outer_function()` and `inner_function()` due to the enclosing scope.
- `z` is only accessible within `inner_function()` as it is defined locally there.

#Scope #Python