### Understanding Limits (Rigorous)

In mathematics, the concept of limits is fundamental to calculus and analysis. It provides a way to describe the behavior of functions as they approach certain values or as they tend towards infinity. The rigorous definition of a limit involves formalizing what it means for a function \( f(x) \) to get arbitrarily close to some number \( L \) as \( x \) approaches a point \( c \).

The **formal epsilon-delta definition** states: 

For every real number \( \epsilon > 0 \), there exists a real number \( \delta > 0 \) such that for all \( x \neq c \), if the distance between \( x \) and \( c \) is less than \( \delta \) (i.e., \( |x - c| < \delta \)), then the distance between \( f(x) \) and \( L \) is less than \( \epsilon \) (i.e., \( |f(x) - L| < \epsilon \)).

This definition ensures that we can make \( f(x) \) as close to \( L \) as we want by choosing \( x \) sufficiently close to \( c \).

### Example in Code

To illustrate the concept of limits, let's consider a simple example where we approximate the limit of the function \( f(x) = (x^2 - 1) / (x - 1) \) as \( x \) approaches 1. This function simplifies to \( f(x) = x + 1 \) for \( x \neq 1 \), and it is undefined at \( x = 1 \). However, the limit as \( x \) approaches 1 is clearly 2.

We can write a Python code snippet that approximates this limit by evaluating \( f(x) \) for values of \( x \) increasingly close to 1:

```python
def f(x):
    return (x**2 - 1) / (x - 1)

# Values of x approaching 1 from both sides
approach_values = [0.9, 0.99, 0.999, 0.9999, 1.0001, 1.001, 1.01, 1.1]

for x in approach_values:
    print(f"f({x}) = {f(x)}")

# The values should get closer and closer to 2 as x approaches 1
```

In this code, we define the function \( f(x) \) and evaluate it at several points approaching 1 from both sides. As \( x \) gets closer to 1, \( f(x) \) gets closer to 2, demonstrating the limit.

#Limits (Rigorous) #Maths #python