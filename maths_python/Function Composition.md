### Function Composition in Mathematics

Function composition involves applying one function to the results of another. If you have two functions \( f \) and \( g \), their composition, denoted as \( (f \circ g)(x) \) or simply \( f(g(x)) \), means that you first apply \( g \) to \( x \), and then apply \( f \) to the result of \( g(x) \).

For example, if \( f(x) = 2x + 3 \) and \( g(x) = x^2 \), then the composition \( (f \circ g)(x) \) is calculated as follows:

1. Apply \( g \) to \( x \): \( g(x) = x^2 \)
2. Take the result from step 1 and apply \( f \): \( f(g(x)) = f(x^2) = 2(x^2) + 3 = 2x^2 + 3 \)

### Python Code Example

Here's a simple Python code example demonstrating function composition:

```python
def f(x):
    return 2 * x + 3

def g(x):
    return x ** 2

# Function to compose two functions
def compose_functions(f, g):
    def composed_function(x):
        return f(g(x))
    return composed_function

# Create the composed function (f ∘ g)
composed = compose_functions(f, g)

# Test the composed function
x_value = 5
result = composed(x_value)
print(f"The result of (f ∘ g)({x_value}) is {result}")
# Output should be 2 * (5^2) + 3 = 53
```

# Tags
#Function #Maths #python
