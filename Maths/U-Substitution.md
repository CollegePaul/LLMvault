### U-Substitution in Mathematics

U-substitution, also known as integration by substitution, is a method used to simplify integrals that involve composite functions. The idea behind u-substitution is to replace a complex expression within the integral with a simpler variable \( u \), making it easier to integrate.

The process generally involves the following steps:
1. Identify a part of the integrand (the function inside the integral) to be substituted as \( u \).
2. Compute the derivative of \( u \) and solve for \( du \).
3. Substitute \( u \) and \( du \) into the integral, replacing the original expression.
4. Integrate with respect to \( u \).
5. Substitute back the original variable in place of \( u \).

#### Basic Example 1
Consider the integral:
\[
\int (2x + 3)^5 \, dx
\]
Let \( u = 2x + 3 \). Then, \( du = 2 \, dx \) or \( dx = \frac{du}{2} \).
Substitute into the integral:
\[
\int u^5 \cdot \frac{1}{2} \, du = \frac{1}{2} \int u^5 \, du
\]
Now integrate with respect to \( u \):
\[
\frac{1}{2} \cdot \frac{u^6}{6} + C = \frac{u^6}{12} + C
\]
Substitute back \( u = 2x + 3 \):
\[
\int (2x + 3)^5 \, dx = \frac{(2x + 3)^6}{12} + C
\]

#### Basic Example 2
Consider the integral:
\[
\int x \cos(x^2) \, dx
\]
Let \( u = x^2 \). Then, \( du = 2x \, dx \) or \( x \, dx = \frac{du}{2} \).
Substitute into the integral:
\[
\int \cos(u) \cdot \frac{1}{2} \, du = \frac{1}{2} \int \cos(u) \, du
\]
Now integrate with respect to \( u \):
\[
\frac{1}{2} \sin(u) + C
\]
Substitute back \( u = x^2 \):
\[
\int x \cos(x^2) \, dx = \frac{1}{2} \sin(x^2) + C
\]

#U-Substitution #Maths