### Taylor Series Basics

The Taylor series is a representation of a function as an infinite sum of terms that are calculated from the values of the function's derivatives at a single point. The formula for the Taylor series around a point \( a \) is:

\[ f(x) = f(a) + \frac{f'(a)}{1!}(x-a) + \frac{f''(a)}{2!}(x-a)^2 + \frac{f'''(a)}{3!}(x-a)^3 + \ldots \]

or more compactly,

\[ f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!} (x-a)^n \]

where \( f^{(n)}(a) \) is the nth derivative of \( f \) evaluated at \( a \), and \( n! \) denotes factorial of \( n \).

For example, the Taylor series for the exponential function \( e^x \) around \( x = 0 \) (also known as the Maclaurin series) is:

\[ e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \ldots \]

This series converges for all \( x \).

### Simple Python Code Example

Here's a simple Python code example to compute the Taylor series approximation of \( e^x \) around \( x = 0 \):

```python
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)

def taylor_series_exponential(x, terms=10):
    result = 0.0
    for n in range(terms):
        result += (x ** n) / factorial(n)
    return result

# Example usage
x_value = 2
approximation = taylor_series_exponential(x_value, terms=5)
print(f"Approximation of e^{x_value} using Taylor series with 5 terms: {approximation}")
```

In this code:
- The `factorial` function computes the factorial of a given number.
- The `taylor_series_exponential` function calculates the approximation of \( e^x \) using the first `terms` number of terms in the Taylor series expansion.

#Taylor Series (Basics) #Maths #python