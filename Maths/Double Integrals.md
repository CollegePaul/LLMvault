### Understanding Double Integrals in Mathematics

Double integrals are an extension of single-variable integration to functions of two variables over regions in the plane. They allow us to integrate over areas, volumes, or other quantities that depend on two variables.

#### Basic Concept:
In one-dimensional calculus, a single integral calculates the area under a curve. Similarly, a double integral computes the volume under a surface defined by a function \( f(x, y) \) over a region in the \( xy \)-plane.

#### Notation and Setup:
The notation for a double integral is as follows:

\[ \iint_R f(x,y) \, dA \]

where \( R \) is the region of integration in the \( xy \)-plane. The differential \( dA \) represents an infinitesimal area element within this region.

#### Iterated Integrals:
Evaluating a double integral often involves breaking it down into iterated integrals (integrating first with respect to one variable, then the other). For instance:

\[ \iint_R f(x,y) \, dA = \int_a^b \left( \int_{g_1(x)}^{g_2(x)} f(x,y) \, dy \right) dx \]

or

\[ \iint_R f(x,y) \, dA = \int_c^d \left( \int_{h_1(y)}^{h_2(y)} f(x,y) \, dx \right) dy \]

The limits of integration depend on the shape and orientation of the region \( R \).

#### Example:
Consider the function \( f(x, y) = xy \) over the rectangular region defined by \( 0 \leq x \leq 2 \) and \( 0 \leq y \leq 1 \). The double integral to evaluate is:

\[ \iint_R xy \, dA = \int_0^2 \left( \int_0^1 xy \, dy \right) dx \]

First, integrate with respect to \( y \):

\[ \int_0^1 xy \, dy = x \left[ \frac{y^2}{2} \right]_0^1 = \frac{x}{2} \]

Then, integrate the result with respect to \( x \):

\[ \int_0^2 \frac{x}{2} \, dx = \frac{1}{2} \left[ \frac{x^2}{2} \right]_0^2 = \frac{1}{2} \cdot 2 = 1 \]

Thus, the value of the double integral is \( 1 \).

#Double Integrals #Maths