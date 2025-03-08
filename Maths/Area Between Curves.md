### Area Between Curves in Mathematics

The concept of the area between curves involves calculating the region enclosed between two or more functions over a given interval. This area can be found using definite integrals, where you subtract the integral of the lower function from the integral of the upper function over the interval of interest.

#### Basic Example:

Consider two functions \( f(x) = x^2 \) and \( g(x) = 4 - x^2 \). To find the area between these curves, we first need to determine where they intersect. Setting \( f(x) = g(x) \):

\[
x^2 = 4 - x^2
\]

Solving for \( x \):

\[
2x^2 = 4 \\
x^2 = 2 \\
x = \pm \sqrt{2}
\]

So, the curves intersect at \( x = \sqrt{2} \) and \( x = -\sqrt{2} \). Over this interval, we can see that \( g(x) \geq f(x) \).

The area between the curves from \( x = -\sqrt{2} \) to \( x = \sqrt{2} \) is given by:

\[
\text{Area} = \int_{-\sqrt{2}}^{\sqrt{2}} [g(x) - f(x)] \, dx \\
= \int_{-\sqrt{2}}^{\sqrt{2}} [(4 - x^2) - x^2] \, dx \\
= \int_{-\sqrt{2}}^{\sqrt{2}} (4 - 2x^2) \, dx
\]

Now we evaluate this integral:

\[
= \left[ 4x - \frac{2}{3}x^3 \right]_{-\sqrt{2}}^{\sqrt{2}}
\]

Substitute the limits of integration:

\[
= \left( 4(\sqrt{2}) - \frac{2}{3}(\sqrt{2})^3 \right) - \left( 4(-\sqrt{2}) - \frac{2}{3}(-\sqrt{2})^3 \right)
\]

Simplify:

\[
= \left( 4\sqrt{2} - \frac{4\sqrt{2}}{3} \right) - \left( -4\sqrt{2} + \frac{4\sqrt{2}}{3} \right) \\
= \left( 4\sqrt{2} - \frac{4\sqrt{2}}{3} \right) + \left( 4\sqrt{2} - \frac{4\sqrt{2}}{3} \right) \\
= 8\sqrt{2} - \frac{8\sqrt{2}}{3} \\
= \frac{24\sqrt{2}}{3} - \frac{8\sqrt{2}}{3} \\
= \frac{16\sqrt{2}}{3}
\]

So, the area between the curves \( f(x) = x^2 \) and \( g(x) = 4 - x^2 \) from \( x = -\sqrt{2} \) to \( x = \sqrt{2} \) is \( \frac{16\sqrt{2}}{3} \).

#AreaBetweenCurves #Maths