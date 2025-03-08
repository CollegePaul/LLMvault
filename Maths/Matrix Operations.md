### Introduction to Matrix Operations

Matrix operations are fundamental in mathematics, particularly in fields such as linear algebra, computer graphics, physics, and engineering. Matrices are rectangular arrays of numbers, symbols, or expressions arranged in rows and columns. The primary matrix operations include addition, subtraction, scalar multiplication, matrix multiplication, and the transpose.

#### 1. Matrix Addition and Subtraction
Matrix addition and subtraction can only be performed between matrices of the same dimensions (same number of rows and columns). To add or subtract two matrices, you simply add or subtract corresponding elements.

**Example:**

Let \( A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \) and \( B = \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix} \)

- **Addition:** \( A + B = \begin{bmatrix} 1+5 & 2+6 \\ 3+7 & 4+8 \end{bmatrix} = \begin{bmatrix} 6 & 8 \\ 10 & 12 \end{bmatrix} \)

- **Subtraction:** \( A - B = \begin{bmatrix} 1-5 & 2-6 \\ 3-7 & 4-8 \end{bmatrix} = \begin{bmatrix} -4 & -4 \\ -4 & -4 \end{bmatrix} \)

#### 2. Scalar Multiplication
Scalar multiplication involves multiplying every element of a matrix by a scalar (a single number).

**Example:**

Let \( A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \) and the scalar \( k = 3 \)

- **Scalar Multiplication:** \( 3A = 3 \times \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} = \begin{bmatrix} 3 & 6 \\ 9 & 12 \end{bmatrix} \)

#### 3. Matrix Multiplication
Matrix multiplication is a bit more complex than addition and subtraction. It requires that the number of columns in the first matrix be equal to the number of rows in the second matrix. The resulting matrix has dimensions equal to the number of rows of the first matrix by the number of columns of the second matrix.

**Example:**

Let \( A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \) and \( B = \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix} \)

- **Matrix Multiplication:** \( AB = \begin{bmatrix} (1*5 + 2*7) & (1*6 + 2*8) \\ (3*5 + 4*7) & (3*6 + 4*8) \end{bmatrix} = \begin{bmatrix} 19 & 22 \\ 43 & 50 \end{bmatrix} \)

#### 4. Transpose of a Matrix
The transpose of a matrix is an operator that flips the matrix over its diagonal, switching the row and column indices of the elements.

**Example:**

Let \( A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \)

- **Transpose:** \( A^T = \begin{bmatrix} 1 & 3 \\ 2 & 4 \end{bmatrix} \)

These operations form the basis of more advanced linear algebra concepts and are crucial for solving systems of linear equations, among other applications. #Matrix Operations #Maths