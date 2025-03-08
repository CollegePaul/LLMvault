### Explanation of Global in Python

In Python, the `global` keyword is used to declare that a variable inside a function is global (i.e., it exists outside of the local scope of the function and can be accessed or modified from anywhere within the module). By default, variables created inside a function are local to that function and cannot be accessed outside it. The `global` keyword allows you to modify these globally defined variables within a function.

Here’s an example:

```python
# Define a global variable
counter = 0

def increment():
    # Declare 'counter' as a global variable so we can modify it inside this function
    global counter
    counter += 1
    print("Inside function:", counter)

increment()
print("Outside function:", counter)
```

In this example, `counter` is defined outside the `increment` function and is therefore a global variable. Inside the function, `global counter` is used to indicate that we want to modify the global `counter` rather than creating a new local variable.

Output:
```
Inside function: 1
Outside function: 1
```

Without the `global` keyword, any attempt to modify `counter` inside the function would result in a `UnboundLocalError` because Python would treat it as a local variable that hasn't been initialized. #Global #Python