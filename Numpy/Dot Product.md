### Dot Product in Numpy

The dot product, often referred to as the scalar product or inner product, is an algebraic operation that takes two equal-length sequences of numbers (usually coordinate vectors) and returns a single number. In the context of NumPy, the dot product can be computed using the `numpy.dot()` function or the `@` operator for arrays.

When applied to 1-dimensional arrays (vectors), the dot product is calculated as the sum of the products of their corresponding elements. For example, given two vectors \( \mathbf{a} = [a_1, a_2, ..., a_n] \) and \( \mathbf{b} = [b_1, b_2, ..., b_n] \), the dot product is defined as:

\[ \mathbf{a} \cdot \mathbf{b} = a_1b_1 + a_2b_2 + ... + a_nb_n \]

When applied to 2-dimensional arrays (matrices), the dot product involves matrix multiplication, where each element of the resulting matrix is computed as the dot product of the corresponding row from the first matrix and column from the second matrix.

Here are some examples using Python:

```python
import numpy as np

# Example with 1D arrays (vectors)
vector_a = np.array([1, 2, 3])
vector_b = np.array([4, 5, 6])

dot_product = np.dot(vector_a, vector_b)  # or vector_a @ vector_b
print("Dot product of vectors:", dot_product)

# Example with 2D arrays (matrices)
matrix_a = np.array([[1, 2], [3, 4]])
matrix_b = np.array([[5, 6], [7, 8]])

dot_product_matrix = np.dot(matrix_a, matrix_b)  # or matrix_a @ matrix_b
print("Dot product of matrices:\n", dot_product_matrix)
```

In the first example, the dot product of vectors \([1, 2, 3]\) and \([4, 5, 6]\) is calculated as \(1*4 + 2*5 + 3*6 = 32\).

In the second example, the dot product (matrix multiplication) of two 2x2 matrices results in a new 2x2 matrix. The element at position (0, 0) of the result is calculated as \(1*5 + 2*7 = 19\), and so on for other elements.

#Dot Product #Numpy