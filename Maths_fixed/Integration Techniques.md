### Integration Techniques in Mathematics

Integration techniques are methods used to find antiderivatives or definite integrals of functions. These techniques are essential in calculus and are applied across various fields such as physics, engineering, and economics.

#### Basic Examples:

1. **Basic Power Rule**:
   The simplest integration technique involves the power rule for basic polynomial functions.
   
   $$ \int x^n \, dx = \frac{x^{n+1}}{n+1} + C \quad \text{(for } n \neq -1\text{)} $$
   
   Example:
   $$ \int x^3 \, dx = \frac{x^4}{4} + C $$

2. **Substitution** (u-substitution):
   This technique involves substituting a part of the function with another variable to simplify the integral.
   
   Example:
   $$ \int 2x(x^2+1)^3 \, dx $$
   Let \( u = x^2 + 1 \), then \( du = 2x \, dx \).
   The integral becomes:
   $$ \int u^3 \, du = \frac{u^4}{4} + C = \frac{(x^2+1)^4}{4} + C $$

3. **Integration by Parts**:
   This technique is used when the integral involves a product of two functions. The formula is:
   
   $$ \int u \, dv = uv - \int v \, du $$
   
   Example:
   $$ \int x e^x \, dx $$
   Let \( u = x \) and \( dv = e^x \, dx \), then \( du = dx \) and \( v = e^x \).
   Using the formula:
   $$ \int x e^x \, dx = x e^x - \int e^x \, dx = x e^x - e^x + C $$

4. **Partial Fractions**:
   This technique is used to integrate rational functions by breaking them into simpler fractions.
   
   Example:
   $$ \int \frac{1}{x^2 - 1} \, dx = \int \left( \frac{1/2}{x-1} - \frac{1/2}{x+1} \right) \, dx $$
   Which simplifies to:
   $$ \frac{1}{2} \ln|x-1| - \frac{1}{2} \ln|x+1| + C = \frac{1}{2} \ln\left|\frac{x-1}{x+1}\right| + C $$

5. **Trigonometric Substitutions**:
   This technique involves substituting trigonometric functions for other expressions to simplify the integral.
   
   Example:
   $$ \int \sqrt{4 - x^2} \, dx $$
   Let \( x = 2\sin\theta \), then \( dx = 2\cos\theta \, d\theta \).
   The integral becomes:
   $$ \int \sqrt{4 - (2\sin\theta)^2} \cdot 2\cos\theta \, d\theta = \int \sqrt{4(1-\sin^2\theta)} \cdot 2\cos\theta \, d\theta $$
   Which simplifies to:
   $$ \int \sqrt{4\cos^2\theta} \cdot 2\cos\theta \, d\theta = \int 4\cos^2\theta \, d\theta $$

### Tags:
#Integration Techniques #Maths