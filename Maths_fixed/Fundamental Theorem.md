### Fundamental Theorem of Calculus

The Fundamental Theorem of Calculus (FTC) is a cornerstone in calculus that establishes the relationship between differentiation and integration. Essentially, it states that if you have a function $$ f $$ which is continuous on an interval [a, b], and another function $$ F $$ defined by 

$$ F(x) = \int_{a}^{x} f(t) \, dt, $$

then the derivative of $$ F $$ with respect to $$ x $$ is just the original function $$ f $$. This part is often referred to as the First Fundamental Theorem of Calculus.

In mathematical terms:

$$ \frac{d}{dx} \left[ \int_{a}^{x} f(t) \, dt \right] = f(x). $$

The Second Fundamental Theorem of Calculus provides a way to compute definite integrals without having to take the limit of Riemann sums. It states that if $$ F $$ is an antiderivative of $$ f $$, i.e., $$ F'(x) = f(x) $$, then

$$ \int_{a}^{b} f(x) \, dx = F(b) - F(a). $$

#### Basic Examples:

**Example 1 (First FTC):**

Consider the function $$ f(t) = t^2 $$. Define another function $$ F(x) $$ as the definite integral of $$ f $$:

$$ F(x) = \int_{0}^{x} t^2 \, dt. $$

According to the First Fundamental Theorem of Calculus,

$$ \frac{d}{dx} [F(x)] = x^2. $$

**Example 2 (Second FTC):**

Let's use the Second Fundamental Theorem of Calculus with $$ f(x) = x^3 $$. We know that an antiderivative of $$ f(x) $$ is

$$ F(x) = \frac{x^4}{4} + C. $$

To find the definite integral from 1 to 2,

$$ \int_{1}^{2} x^3 \, dx = \left[ \frac{x^4}{4} \right]_1^2 = \frac{2^4}{4} - \frac{1^4}{4} = 4 - \frac{1}{4} = \frac{15}{4}. $$

#Fundamental Theorem #Maths