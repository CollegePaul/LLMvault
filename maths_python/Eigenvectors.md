### Understanding Eigenvectors in Mathematics

In linear algebra, eigenvectors are special vectors associated with a linear transformation represented by a matrix. When such a matrix multiplies an eigenvector, the result is a scalar multiple of the same eigenvector. This scalar is known as the eigenvalue corresponding to that eigenvector.

Mathematically, if \( A \) is a square matrix and \( v \) is a vector, then \( v \) is an eigenvector of \( A \) if there exists a scalar \( \lambda \) (the eigenvalue) such that:

\[ Av = \lambda v \]

This equation means that the direction of the vector \( v \) does not change under the transformation by matrix \( A \), only its magnitude may scale.

### Example in Code

Let's use Python and the NumPy library to find the eigenvectors and eigenvalues of a given 2x2 matrix. Consider the matrix:

\[ A = \begin{bmatrix} 4 & 2 \\ 1 & 3 \end{bmatrix} \]

We will use NumPy's `linalg.eig` function to compute its eigenvectors and eigenvalues.

```python
import numpy as np

# Define the matrix A
A = np.array([[4, 2],
              [1, 3]])

# Compute the eigenvalues and eigenvectors of A
eigenvalues, eigenvectors = np.linalg.eig(A)

print("Eigenvalues:", eigenvalues)
print("Eigenvectors:\n", eigenvectors)
```

### Output Explanation

Running this code will output two main pieces of information:
- The eigenvalues of the matrix \( A \).
- The corresponding eigenvectors.

The output might look something like:

```
Eigenvalues: [5. 2.]
Eigenvectors:
 [[0.89442719 0.70710678]
 [0.4472136   0.70710678]]
```

This means that the matrix \( A \) has two eigenvalues, 5 and 2, with corresponding eigenvectors \(\begin{bmatrix} 0.894 \\ 0.447 \end{bmatrix}\) and \(\begin{bmatrix} 0.707 \\ 0.707 \end{bmatrix}\), respectively.

#Eigenvectors #Maths #python