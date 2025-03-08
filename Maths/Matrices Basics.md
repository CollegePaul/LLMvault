### Matrices Basics

Matrices are fundamental structures in mathematics used to organize numbers or other elements into rows and columns. A matrix is essentially a rectangular array of numbers, symbols, or expressions, arranged in rows and columns.

#### Basic Terminology:
- **Element**: Each number inside the matrix is called an element.
- **Row**: Numbers aligned horizontally within the matrix form a row.
- **Column**: Numbers aligned vertically within the matrix form a column.
- **Order/Dimension**: The order of a matrix is defined by the number of rows and columns it contains, written as m x n (m rows and n columns).

#### Types of Matrices:
1. **Row Matrix**: A matrix with only one row.
2. **Column Matrix**: A matrix with only one column.
3. **Square Matrix**: A matrix where the number of rows is equal to the number of columns.
4. **Diagonal Matrix**: A square matrix in which all off-diagonal elements are zero.
5. **Identity Matrix**: A diagonal matrix with ones on the main diagonal and zeros elsewhere.

#### Basic Operations:
1. **Addition/Subtraction**: Two matrices can be added or subtracted if they have the same dimensions. The operation is performed element-wise.
2. **Scalar Multiplication**: Each element of a matrix is multiplied by a scalar (a single number).
3. **Matrix Multiplication**: Two matrices can be multiplied if the number of columns in the first matrix is equal to the number of rows in the second matrix.

#### Example:
Consider two matrices:

\[ A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}, \quad B = \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix} \]

**Addition**: 
\[ A + B = \begin{bmatrix} 1+5 & 2+6 \\ 3+7 & 4+8 \end{bmatrix} = \begin{bmatrix} 6 & 8 \\ 10 & 12 \end{bmatrix} \]

**Scalar Multiplication**: 
\[ 2A = 2 \times \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} = \begin{bmatrix} 2 & 4 \\ 6 & 8 \end{bmatrix} \]

**Matrix Multiplication** (if C is a matrix with compatible dimensions):
\[ C = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}, \quad AC = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \times \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} = \begin{bmatrix} 1\cdot1+2\cdot0 & 1\cdot0+2\cdot1 \\ 3\cdot1+4\cdot0 & 3\cdot0+4\cdot1 \end{bmatrix} = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix} \]

Matrices are used extensively in various fields, including physics, engineering, computer science, and economics, to solve systems of linear equations, among other applications.

#Matrices Basics #Maths