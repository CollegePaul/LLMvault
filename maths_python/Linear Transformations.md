### Linear Transformations in Mathematics

Linear transformations are functions between two vector spaces that preserve the operations of vector addition and scalar multiplication. In simpler terms, if you apply a linear transformation to a sum of vectors or a scaled vector, it is equivalent to applying the transformation individually and then performing the same operations on the results.

A key property of linear transformations is that they can be represented by matrices when the vector spaces are finite-dimensional. For example, in 2D space, a linear transformation can rotate, scale, shear, reflect, or any combination of these operations on points.

#### Example

Consider a simple example where we have a linear transformation that scales all vectors in 2D space by a factor of 2:

\[ T(x, y) = (2x, 2y) \]

Here, \(T\) is a linear transformation. To see why it is linear, consider two vectors \((x_1, y_1)\) and \((x_2, y_2)\):

- Scaling: \( T(k(x_1, y_1)) = (2kx_1, 2ky_1) = k(2x_1, 2y_1) = kT(x_1, y_1) \)
- Addition: \( T((x_1, y_1) + (x_2, y_2)) = T(x_1 + x_2, y_1 + y_2) = (2(x_1 + x_2), 2(y_1 + y_2)) \)
  Which equals: \( (2x_1 + 2x_2, 2y_1 + 2y_2) = (2x_1, 2y_1) + (2x_2, 2y_2) = T(x_1, y_1) + T(x_2, y_2) \)

Thus, the function \(T\) satisfies both conditions of linearity.

### Python Code Example

Here is a simple Python code example that demonstrates scaling a vector by a factor of 2 using a linear transformation:

```python
import numpy as np

def scale_vector(v, scale_factor):
    """
    Scales a vector v by a given scale_factor.
    
    :param v: numpy array representing the vector to be scaled
    :param scale_factor: scalar value representing the scaling factor
    :return: numpy array representing the scaled vector
    """
    # Define the transformation matrix for scaling
    transformation_matrix = np.array([[scale_factor, 0],
                                      [0, scale_factor]])
    
    # Apply the linear transformation to the vector v
    transformed_vector = np.dot(transformation_matrix, v)
    
    return transformed_vector

# Example usage:
original_vector = np.array([1, 2])
scaled_vector = scale_vector(original_vector, 2)

print("Original Vector:", original_vector)
print("Scaled Vector:", scaled_vector)  # Output should be [2, 4]
```

In this code, we define a function `scale_vector` that takes a vector and a scaling factor as inputs. It uses a transformation matrix to apply the linear transformation (scaling in this case) to the input vector. The result is then printed out.

#LinearTransformations #Maths #python