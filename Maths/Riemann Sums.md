### Understanding Riemann Sums in Mathematics

Riemann sums are a method used in calculus to approximate the area under a curve, or more formally, the definite integral of a function over a specified interval. The basic idea is to divide the area under the curve into several rectangles and then sum up their areas. By increasing the number of rectangles (or decreasing their width), the approximation becomes more accurate.

#### Types of Riemann Sums

1. **Left Riemann Sum**: Here, the height of each rectangle is determined by the function value at the left endpoint of each subinterval.
2. **Right Riemann Sum**: In this case, the height of each rectangle corresponds to the function value at the right endpoint of each subinterval.
3. **Midpoint Riemann Sum**: The height of each rectangle is based on the function value at the midpoint of each subinterval.

#### Example

Consider a simple function \( f(x) = x^2 \) over the interval [0, 4]. We want to approximate the area under this curve using Riemann sums with four rectangles.

- **Left Riemann Sum**:
  - Divide the interval into four parts: [0,1], [1,2], [2,3], and [3,4].
  - The heights of the rectangles are \( f(0) = 0^2 \), \( f(1) = 1^2 \), \( f(2) = 2^2 \), and \( f(3) = 3^2 \).
  - The sum is: \( (0 \times 1) + (1 \times 1) + (4 \times 1) + (9 \times 1) = 14 \).

- **Right Riemann Sum**:
  - Heights are determined by the right endpoints: \( f(1) = 1^2 \), \( f(2) = 2^2 \), \( f(3) = 3^2 \), and \( f(4) = 4^2 \).
  - The sum is: \( (1 \times 1) + (4 \times 1) + (9 \times 1) + (16 \times 1) = 30 \).

- **Midpoint Riemann Sum**:
  - Heights are based on the midpoints of each interval: \( f(0.5) = 0.5^2 \), \( f(1.5) = 1.5^2 \), \( f(2.5) = 2.5^2 \), and \( f(3.5) = 3.5^2 \).
  - The sum is: \( (0.25 \times 1) + (2.25 \times 1) + (6.25 \times 1) + (12.25 \times 1) = 21 \).

Each of these sums provides an approximation of the area under the curve \( f(x) = x^2 \) from 0 to 4, and increasing the number of rectangles would yield a more precise estimate.

#Riemann Sums #Maths