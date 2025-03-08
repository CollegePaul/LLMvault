### Array Shapes in Numpy

In NumPy, the shape of an array refers to the dimensions or size of each dimension of the array. The shape is represented as a tuple where each element in the tuple corresponds to the number of elements along that particular axis. For example, a two-dimensional array with 3 rows and 4 columns would have a shape of `(3, 4)`.

Here are some examples using Python:

1. **One-Dimensional Array:**
   ```python
   import numpy as np

   arr = np.array([1, 2, 3, 4])
   print("Array:", arr)
   print("Shape:", arr.shape)  # Output will be (4,)
   ```

2. **Two-Dimensional Array:**
   ```python
   arr_2d = np.array([[1, 2], [3, 4], [5, 6]])
   print("Array:\n", arr_2d)
   print("Shape:", arr_2d.shape)  # Output will be (3, 2)
   ```

3. **Three-Dimensional Array:**
   ```python
   arr_3d = np.array([[[1, 2], [3, 4]], [[5, 6], [7, 8]]])
   print("Array:\n", arr_3d)
   print("Shape:", arr_3d.shape)  # Output will be (2, 2, 2)
   ```

The shape attribute is very useful when you need to know how many elements are in each dimension of an array or when reshaping the array.

#Array Shapes #Numpy