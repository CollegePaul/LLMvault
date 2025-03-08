### Matrices Basics in Mathematics

A matrix is a rectangular array of numbers, symbols, or expressions, arranged in rows and columns. The individual items in a matrix are called its elements or entries. Matrices are used in various fields such as physics, engineering, computer science, and economics for solving systems of linear equations, transformations, and more.

A matrix can be described by its dimensions, which specify the number of rows and columns it contains. For example, a matrix with 3 rows and 2 columns is called a "3 by 2" matrix or a "3x2" matrix.

Matrices can be added, subtracted, multiplied, and manipulated in various ways to solve mathematical problems. One of the fundamental operations is matrix multiplication, which involves multiplying rows by columns from two matrices.

#### Example:
Consider a 2x2 matrix A and a 2x1 matrix B:

\[ 
A = \begin{bmatrix} 
1 & 2 \\
3 & 4 
\end{bmatrix}, \quad
B = \begin{bmatrix}
5 \\
6 
\end{bmatrix}
\]

To multiply matrix A by matrix B, you perform the following operations:

\[ 
AB = \begin{bmatrix} 
(1*5 + 2*6) \\
(3*5 + 4*6) 
\end{bmatrix} = \begin{bmatrix} 
17 \\
39 
\end{bmatrix}
\]

Here's a simple Python code example using the `numpy` library to perform matrix multiplication:

```python
import numpy as np

# Define matrices A and B
A = np.array([[1, 2], [3, 4]])
B = np.array([5, 6])

# Perform matrix multiplication
result = np.dot(A, B)

print("Matrix A:")
print(A)
print("\nMatrix B:")
print(B)
print("\nResult of AB:")
print(result)
```

This code snippet defines two matrices A and B, performs their multiplication using `np.dot()`, and prints the result. #Matrices Basics #Maths #python