### Continuity in Mathematics

In mathematics, particularly in calculus and real analysis, continuity of a function is a fundamental concept that describes how the function behaves around a point or across its domain. A function $$ f $$ is said to be continuous at a point $$ c $$ if three conditions are met:
1. The function value $$ f(c) $$ exists.
2. The limit of the function as $$ x $$ approaches $$ c $$ exists.
3. These two values are equal: $$ \lim_{{x \to c}} f(x) = f(c) $$.

In a more rigorous setting, continuity can be defined using the epsilon-delta definition:

A function $$ f $$ is continuous at a point $$ c $$ if for every $$ \epsilon > 0 $$. there exists a $$ \delta > 0 $$ such that whenever $$ |x - c| < \delta $$. it follows that $$ |f(x) - f(c)| < \epsilon $$.

This definition encapsulates the idea that small changes in the input of the function result in arbitrarily small changes in the output, which is a key property for many mathematical operations.

**Example:** Consider the function $$ f(x) = 2x + 3 $$. To show that this function is continuous at any point $$ c $$. we need to demonstrate that for every $$ \epsilon > 0 $$. there exists a $$ \delta > 0 $$ such that if $$ |x - c| < \delta $$. then $$ |f(x) - f(c)| < \epsilon $$.

Given $$ \epsilon > 0 $$. choose $$ \delta = \frac{\epsilon}{2} $$. If $$ |x - c| < \delta $$. then:
$$
|f(x) - f(c)| = |(2x + 3) - (2c + 3)| = |2(x - c)| = 2|x - c| < 2\left(\frac{\epsilon}{2}\right) = \epsilon.
$$
Thus, $$ f(x) = 2x + 3 $$ is continuous at any point $$ c $$.

#Continuity (Rigorous) #Maths