### Understanding Limits in Mathematics

In mathematics, limits are used to describe the behavior of functions as they approach certain values. The concept of limits is fundamental to calculus and helps define continuity, derivatives, and integrals.

#### Basic Examples:

1. **Simple Function Limit:**
   Consider the function $$ f(x) = x + 2 $$. To find the limit of this function as $$ x $$ approaches 3, we evaluate what happens when $$ x $$ gets closer and closer to 3.
   
   $$
   \lim_{x \to 3} (x + 2) = 5
   $$
   
   Here, as $$ x $$ approaches 3, the value of $$ f(x) $$ approaches 5.

2. **Piecewise Function Limit:**
   Let's look at a piecewise function:
   
   $$
   f(x) = 
   \begin{cases} 
   x^2 & \text{if } x < 1 \\
   2x + 1 & \text{if } x \geq 1
   \end{cases}
   $$
   
   To find the limit of $$ f(x) $$ as $$ x $$ approaches 1, we need to check if both one-sided limits are equal.
   
   - As $$ x $$ approaches 1 from the left ($$ x < 1 $$):
     
     $$
     \lim_{x \to 1^-} (x^2) = 1
     $$
     
   - As $$ x $$ approaches 1 from the right ($$ x \geq 1 $$):
     
     $$
     \lim_{x \to 1^+} (2x + 1) = 3
     $$
   
   Since these two limits are not equal, we say that the limit of $$ f(x) $$ as $$ x $$ approaches 1 does not exist.

3. **Limit Involving Infinity:**
   Consider the function $$ g(x) = \frac{1}{x} $$. To find the limit as $$ x $$ approaches infinity:
   
   $$
   \lim_{x \to \infty} \left( \frac{1}{x} \right) = 0
   $$
   
   As $$ x $$ becomes very large, the value of $$ \frac{1}{x} $$ becomes closer and closer to 0.

Limits are essential for understanding the behavior of functions in various scenarios, especially when dealing with discontinuities or asymptotic behaviors. #Limits #Maths