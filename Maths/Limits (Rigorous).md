### Introduction to Limits in Mathematics

In mathematics, limits are used to describe the behavior of functions as their inputs approach certain values. They are crucial in calculus and analysis because they help define continuity, derivatives, and integrals.

#### Rigorous Definition of a Limit

Formally, the limit of a function \( f(x) \) as \( x \) approaches a number \( a \) is said to be \( L \), denoted as:
\[
\lim_{{x \to a}} f(x) = L
\]
if for every positive real number \( \epsilon > 0 \), there exists a positive real number \( \delta > 0 \) such that whenever the distance from \( x \) to \( a \) is less than \( \delta \) (and \( x \neq a \)), the distance from \( f(x) \) to \( L \) is less than \( \epsilon \). Mathematically, this can be written as:
\[
0 < |x - a| < \delta \implies |f(x) - L| < \epsilon
\]

This formal definition captures the idea that values of \( f(x) \) get arbitrarily close to \( L \) when \( x \) is sufficiently close to \( a \).

#### Basic Example

Consider the function \( f(x) = 2x + 3 \). We want to find:
\[
\lim_{{x \to 1}} (2x + 3)
\]

Using the definition of a limit, we need to show that for any given \( \epsilon > 0 \), there is a \( \delta > 0 \) such that:
\[
|2x + 3 - 5| < \epsilon \quad \text{whenever} \quad 0 < |x - 1| < \delta
\]

Simplifying, we get:
\[
|2x - 2| = 2|x - 1| < \epsilon
\]
So, if we choose \( \delta = \frac{\epsilon}{2} \), then whenever \( 0 < |x - 1| < \delta \):
\[
2|x - 1| < 2\left(\frac{\epsilon}{2}\right) = \epsilon
\]

This shows that:
\[
\lim_{{x \to 1}} (2x + 3) = 5
\]

### Conclusion

Limits provide a way to understand the behavior of functions near specific points, which is essential for more advanced mathematical concepts. #Limits (Rigorous) #Maths