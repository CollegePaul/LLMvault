### Explanation of Eigenvalues in Mathematics

In linear algebra, eigenvalues are scalar values associated with a system of linear equations represented by a square matrix. Specifically, an eigenvalue \(\lambda\) of a matrix \(A\) is a value such that there exists a non-zero vector \(v\) (called the eigenvector) satisfying the equation:

\[ A v = \lambda v \]

This equation can be rewritten as:

\[ (A - \lambda I) v = 0 \]

where \(I\) is the identity matrix. The determinant of the matrix \((A - \lambda I)\) must be zero for non-zero vectors \(v\) to exist, leading to the characteristic polynomial of the matrix. Solving this polynomial gives the eigenvalues.

### Example in Code

Here's a simple Python code example using the `numpy` library to calculate the eigenvalues and eigenvectors of a square matrix:

```python
import numpy as np

# Define a 2x2 matrix
A = np.array([[4, 2], [1, 3]])

# Calculate eigenvalues and eigenvectors
eigenvalues, eigenvectors = np.linalg.eig(A)

print("Eigenvalues:")
print(eigenvalues)
print("\nEigenvectors:")
print(eigenvectors)
```

In this example, the matrix \(A\) is a 2x2 matrix. The `np.linalg.eig` function computes the eigenvalues and eigenvectors of \(A\). The output will show the eigenvalues and corresponding columns of the eigenvector matrix.

#Eigenvalues #Maths #python