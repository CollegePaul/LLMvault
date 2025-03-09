### Integration (Rigorous)

In mathematics, particularly in calculus, integration is a method to find the area under a curve, volumes, central points, and other quantities where the data are given by a continuous change. Rigorous integration involves defining integrals with precise mathematical definitions, often using limits of sums, such as Riemann sums or Lebesgue integrals.

To introduce rigorously, let's start with the concept of a definite integral using the Riemann sum approach:

Consider a function $$ f $$ defined on an interval [a, b]. We want to find the area under the curve $$ y = f(x) $$ from $$ x = a $$ to $$ x = b $$. The idea is to divide this interval into smaller subintervals and approximate the area of each segment using rectangles. 

Let's say we partition the interval [a, b] into n subintervals with endpoints $$ x_0, x_1, ..., x_n $$ where $$ a = x_0 < x_1 < ... < x_n = b $$. The length of the i-th subinterval is $$ \Delta x_i = x_i - x_{i-1} $$.

We choose an arbitrary point $$ c_i $$ in each interval [$$x_{i-1}$$, $$x_i$$] and construct rectangles with heights $$ f(c_i) $$ and widths $$ \Delta x_i $$. The sum of the areas of these rectangles is called a Riemann sum:
$$ S = \sum_{i=1}^{n} f(c_i) \Delta x_i. $$

The definite integral of $$ f $$ from $$ a $$ to $$ b $$, denoted as
$$ \int_a^b f(x) \, dx, $$
is defined as the limit of these Riemann sums as the largest subinterval length approaches zero:
$$ \int_a^b f(x) \, dx = \lim_{\max(\Delta x_i) \to 0} \sum_{i=1}^{n} f(c_i) \Delta x_i. $$

For example, let's compute a simple integral:
$$ \int_0^2 x \, dx. $$
We partition the interval [0, 2] into n subintervals of equal length $$ \Delta x = \frac{2}{n} $$. Choosing $$ c_i = x_{i-1} + \frac{\Delta x}{2} $$ as the midpoint of each subinterval, we have:
$$ f(c_i) = c_i = i\left(\frac{2}{n}\right) - \left(\frac{2}{n}\right) + \left(\frac{2}{n}\right)^2/2 = 2i/n - 1/n + 2/(2n^2). $$
The Riemann sum becomes:
$$ S = \sum_{i=1}^{n} f(c_i) \Delta x = \sum_{i=1}^{n} \left(2i/n - 1/n + 2/(2n^2)\right)(2/n) = \frac{4}{n^2}\sum_{i=1}^{n} i - \frac{2}{n^2}\sum_{i=1}^{n} 1 + \frac{2}{n^3}\sum_{i=1}^{n} 1. $$
Using the formulas for the sums of the first n natural numbers $$ \sum_{i=1}^{n} i = \frac{n(n+1)}{2} $$ and $$ \sum_{i=1}^{n} 1 = n $$:
$$ S = \frac{4}{n^2}\cdot\frac{n(n+1)}{2} - \frac{2}{n^2}\cdot n + \frac{2}{n^3}\cdot n = 2\left(1 + \frac{1}{n}\right) - \frac{2}{n} + \frac{2}{n^2}. $$
Taking the limit as $$ n \to \infty $$, all terms containing $$ n $$ in the denominator vanish, leaving:
$$ \lim_{n\to\infty} S = 2. $$

Thus,
$$ \int_0^2 x \, dx = 2. $$

#Integration (Rigorous) #Maths