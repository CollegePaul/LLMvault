### Chain Rule in Mathematics

The Chain Rule is a fundamental concept in calculus used to find the derivative of composite functions. Essentially, it allows us to differentiate functions that are composed of other functions. The rule states that if you have a function $$ y = f(g(x)) $$. then the derivative of $$ y $$ with respect to $$ x $$ is given by:

$$ \frac{dy}{dx} = f'(g(x)) \cdot g'(x) $$

In simpler terms, you take the derivative of the outer function evaluated at the inner function and multiply it by the derivative of the inner function.

#### Basic Example

Let's consider a simple example to illustrate this. Suppose we have a composite function $$ y = (3x^2 + 1)^5 $$.

Here, the outer function is $$ f(u) = u^5 $$. where $$ u = g(x) = 3x^2 + 1 $$. To find $$ \frac{dy}{dx} $$:

1. Differentiate the outer function with respect to $$ u $$: 
   $$ f'(u) = 5u^4 $$
   
2. Evaluate this at the inner function:
   $$ f'(g(x)) = 5(3x^2 + 1)^4 $$

3. Differentiate the inner function with respect to $$ x $$:
   $$ g'(x) = 6x $$

4. Combine these results using the Chain Rule:
   $$ \frac{dy}{dx} = f'(g(x)) \cdot g'(x) = 5(3x^2 + 1)^4 \cdot 6x = 30x(3x^2 + 1)^4 $$

Thus, the derivative of $$ y = (3x^2 + 1)^5 $$ is $$ 30x(3x^2 + 1)^4 $$.