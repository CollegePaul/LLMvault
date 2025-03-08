### Introduction to Linear Transformations

In mathematics, a linear transformation (also known as a linear map) is a function between two vector spaces that preserves the operations of vector addition and scalar multiplication. Essentially, if you apply a linear transformation to a sum of vectors, it is equivalent to applying the transformation to each vector individually and then summing the results. Similarly, multiplying a vector by a scalar before applying the transformation yields the same result as applying the transformation first and then multiplying.

To put it more formally, let \( V \) and \( W \) be two vector spaces over the same field (like real numbers or complex numbers). A function \( T: V \rightarrow W \) is called a linear transformation if it satisfies the following properties:
1. **Additivity**: \( T(u + v) = T(u) + T(v) \) for all vectors \( u, v \) in \( V \).
2. **Homogeneity of degree 1**: \( T(cu) = cT(u) \) for all vectors \( u \) in \( V \) and all scalars \( c \).

### Basic Examples

**Example 1: Scaling**
Consider the function \( T(x, y) = (3x, 3y) \). This is a linear transformation from \( \mathbb{R}^2 \) to \( \mathbb{R}^2 \). It scales every vector by a factor of 3. You can verify that it satisfies both properties:
- Additivity: \( T((x_1, y_1) + (x_2, y_2)) = T(x_1 + x_2, y_1 + y_2) = (3(x_1 + x_2), 3(y_1 + y_2)) = (3x_1 + 3x_2, 3y_1 + 3y_2) = (3x_1, 3y_1) + (3x_2, 3y_2) = T(x_1, y_1) + T(x_2, y_2) \).
- Homogeneity: \( T(c(x, y)) = T(cx, cy) = (3cx, 3cy) = c(3x, 3y) = cT(x, y) \).

**Example 2: Rotation**
Let's take a function that rotates every vector in the plane by 90 degrees counterclockwise. This transformation can be defined as \( T(x, y) = (-y, x) \). It also satisfies both properties:
- Additivity: \( T((x_1, y_1) + (x_2, y_2)) = T(x_1 + x_2, y_1 + y_2) = (-(y_1 + y_2), x_1 + x_2) = (-y_1 - y_2, x_1 + x_2) = (-y_1, x_1) + (-y_2, x_2) = T(x_1, y_1) + T(x_2, y_2) \).
- Homogeneity: \( T(c(x, y)) = T(cx, cy) = (-cy, cx) = c(-y, x) = cT(x, y) \).

### Conclusion

Linear transformations are fundamental in linear algebra and have applications in various fields such as physics, engineering, computer science, and more. They provide a way to understand how geometric shapes and spaces change under specific operations.

#LinearTransformations #Maths