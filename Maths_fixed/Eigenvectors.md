### Understanding Eigenvectors in Mathematics

In linear algebra, an eigenvector of a matrix is a non-zero vector that changes by only a scalar factor when that linear transformation (matrix multiplication) is applied to it. More formally, if $$ A $$ is a square matrix and $$ v $$ is a non-zero vector, then $$ v $$ is an eigenvector of $$ A $$ if there exists a scalar $$ \lambda $$, known as the eigenvalue, such that:

$$ Av = \lambda v $$

This equation states that when the matrix $$ A $$ is multiplied by the vector $$ v $$, the result is simply the vector $$ v $$ scaled by some factor $$ \lambda $$.

#### Example

Consider a simple 2x2 matrix $$ A $$:

$$ A = \begin{bmatrix} 2 & 0 \\ 0 & 3 \end{bmatrix} $$

We want to find an eigenvector and the corresponding eigenvalue. Let’s assume the eigenvector is:

$$ v = \begin{bmatrix} x \\ y \end{bmatrix} $$

According to the definition, $$ Av = \lambda v $$:

$$ \begin{bmatrix} 2 & 0 \\ 0 & 3 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = \lambda \begin{bmatrix} x \\ y \end{bmatrix} $$

This results in:

$$ \begin{bmatrix} 2x \\ 3y \end{bmatrix} = \begin{bmatrix} \lambda x \\ \lambda y \end{bmatrix} $$

From this, we can derive two equations:

1. $$ 2x = \lambda x $$
2. $$ 3y = \lambda y $$

If $$ x \neq 0 $$, from the first equation, we get $$ \lambda = 2 $$. If $$ y \neq 0 $$, from the second equation, we get $$ \lambda = 3 $$.

This shows that there are two eigenvalues for this matrix: $$ \lambda_1 = 2 $$ and $$ \lambda_2 = 3 $$.

For $$ \lambda_1 = 2 $$:

$$ Av = 2v \Rightarrow \begin{bmatrix} 2 & 0 \\ 0 & 3 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 2x \\ 6y \end{bmatrix} = \begin{bmatrix} 2x \\ 2y \end{bmatrix} $$

This implies $$ y = 0 $$, so any vector of the form $$ \begin{bmatrix} x \\ 0 \end{bmatrix} $$ is an eigenvector for $$ \lambda_1 = 2 $$.

For $$ \lambda_2 = 3 $$:

$$ Av = 3v \Rightarrow \begin{bmatrix} 2 & 0 \\ 0 & 3 \end{bmatrix} \begin{bmatrix} x \\ y \end{bmatrix} = \begin{bmatrix} 2x \\ 3y \end{bmatrix} = \begin{bmatrix} 3x \\ 3y \end{bmatrix} $$

This implies $$ x = 0 $$, so any vector of the form $$ \begin{bmatrix} 0 \\ y \end{bmatrix} $$ is an eigenvector for $$ \lambda_2 = 3 $$.