### Curve Sketching in Mathematics

Curve sketching involves analyzing a function to determine its graph's general shape and key features without plotting every point. This process uses calculus, algebra, and other mathematical tools to identify important characteristics such as intercepts, asymptotes, intervals of increase or decrease, local maxima and minima, concavity, and points of inflection.

#### Steps in Curve Sketching:

1. **Domain**: Determine the domain of the function where it is defined.
2. **Intercepts**:
   - **x-intercepts**: Find values of $$ x $$ for which $$ f(x) = 0 $$.
   - **y-intercept**: Find $$ f(0) $$ if in the domain.
3. **Symmetry**: Check if the function is even, odd, or neither to simplify the sketching process.
4. **Asymptotes**:
   - **Vertical Asymptotes**: Occur where the function approaches infinity (or negative infinity), typically at values of $$ x $$ that make a denominator zero in rational functions.
   - **Horizontal Asymptotes**: Determine behavior as $$ x \to \pm\infty $$.
5. **Critical Points and Intervals**:
   - Find derivatives to determine where the function increases or decreases.
   - Set the first derivative equal to zero or undefined to find critical points.
6. **Local Maxima and Minima**: Use the First Derivative Test around critical points.
7. **Concavity and Inflection Points**:
   - Determine concavity (upward or downward) using the second derivative.
   - Find inflection points where the second derivative changes sign.

#### Example:

Consider the function $$ f(x) = x^3 - 3x^2 + 2 $$.

1. **Domain**: The domain is all real numbers, as there are no restrictions on $$ x $$.
2. **Intercepts**:
   - **x-intercepts**: Solve $$ x^3 - 3x^2 + 2 = 0 $$. Factoring gives $$ (x-1)^2(x+2) = 0 $$, so the x-intercepts are $$ x = 1, -2 $$.
   - **y-intercept**: Evaluate at $$ x = 0 $$: $$ f(0) = 2 $$.
3. **Symmetry**: The function is neither even nor odd.
4. **Asymptotes**: No vertical or horizontal asymptotes as the polynomial degree is finite and positive.
5. **Critical Points**:
   - First derivative: $$ f'(x) = 3x^2 - 6x $$.
   - Set $$ f'(x) = 0 $$: $$ 3x(x-2) = 0 $$, so critical points are $$ x = 0, 2 $$.
6. **Local Maxima and Minima**:
   - Use the First Derivative Test: Test intervals around critical points.
     - For $$ x < 0 $$, choose $$ x = -1 $$: $$ f'(-1) > 0 $$ (increasing).
     - For $$ 0 < x < 2 $$, choose $$ x = 1 $$: $$ f'(1) < 0 $$ (decreasing).
     - For $$ x > 2 $$, choose $$ x = 3 $$: $$ f'(3) > 0 $$ (increasing).
   - Thus, $$ x = 0 $$ is a local maximum and $$ x = 2 $$ is a local minimum.
7. **Concavity and Inflection Points**:
   - Second derivative: $$ f''(x) = 6x - 6 $$.
   - Set $$ f''(x) = 0 $$: $$ 6(x-1) = 0 $$, so inflection point at $$ x = 1 $$.
   - Test intervals around $$ x = 1 $$:
     - For $$ x < 1 $$, choose $$ x = 0 $$: $$ f''(0) < 0 $$ (concave down).
     - For $$ x > 1 $$, choose $$ x = 2 $$: $$ f''(2) > 0 $$ (concave up).

By combining these observations, you can sketch the graph of $$ f(x) = x^3 - 3x^2 + 2 $$.