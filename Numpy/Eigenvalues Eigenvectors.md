### Eigenvalues and Eigenvectors in Numpy

In linear algebra, eigenvalues and eigenvectors are fundamental concepts that provide insights into the properties of matrices. An eigenvector of a matrix \( A \) is a non-zero vector that changes by only a scalar factor when that linear transformation is applied to it. Mathematically, if \( v \) is an eigenvector of \( A \), then:

\[ A v = \lambda v \]

where \( \lambda \) is the corresponding eigenvalue.

In Numpy, we can compute the eigenvalues and eigenvectors of a matrix using the `numpy.linalg.eig` function. This function returns a tuple consisting of an array of eigenvalues and a 2D array where each column is an eigenvector associated with the corresponding eigenvalue.

#### Example

Let's consider a simple example to illustrate this:

```python
import numpy as np

# Define a matrix A
A = np.array([[4, 2], [1, 3]])

# Compute the eigenvalues and eigenvectors
eigenvalues, eigenvectors = np.linalg.eig(A)

print("Eigenvalues:", eigenvalues)
print("Eigenvectors:\n", eigenvectors)
```

In this example, matrix \( A \) is defined as:

\[ A = \begin{bmatrix} 4 & 2 \\ 1 & 3 \end{bmatrix} \]

The `np.linalg.eig` function computes the eigenvalues and eigenvectors. The output will be something like:

```
Eigenvalues: [5. 2.]
Eigenvectors:
 [[0.89442719 0.70710678]
 [0.4472136  -0.70710678]]
```

Here, the eigenvalues are \(5\) and \(2\), and the corresponding eigenvectors are approximately \([0.894, 0.447]^T\) and \([0.707, -0.707]^T\).

This means that:

\[ A \begin{bmatrix} 0.894 \\ 0.447 \end{bmatrix} = 5 \begin{bmatrix} 0.894 \\ 0.447 \end{bmatrix} \]

and

\[ A \begin{bmatrix} 0.707 \\ -0.707 \end{bmatrix} = 2 \begin{bmatrix} 0.707 \\ -0.707 \end{bmatrix} \]

#Eigenvalues Eigenvectors #Numpy