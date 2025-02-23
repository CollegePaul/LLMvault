### Array Creation in Numpy

Numpy provides several functions to create arrays efficiently. These functions allow you to generate arrays filled with zeros, ones, constants, or even random values. Here are some of the most commonly used methods:

1. **Using `numpy.array()`**:
   This function is used to create an array from a list or any other iterable.
   
   ```python
   import numpy as np

   # Create a 1D array
   arr_1d = np.array([1, 2, 3, 4])
   print(arr_1d)  # Output: [1 2 3 4]

   # Create a 2D array (matrix)
   arr_2d = np.array([[1, 2], [3, 4]])
   print(arr_2d)  
   # Output:
   # [[1 2]
   #  [3 4]]
   ```

2. **Using `numpy.zeros()`**:
   This function creates an array filled with zeros.
   
   ```python
   zeros_arr = np.zeros((2, 3))  # Creates a 2x3 matrix of zeros
   print(zeros_arr)  
   # Output:
   # [[0. 0. 0.]
   #  [0. 0. 0.]]
   ```

3. **Using `numpy.ones()`**:
   This function creates an array filled with ones.
   
   ```python
   ones_arr = np.ones((2, 3))  # Creates a 2x3 matrix of ones
   print(ones_arr)  
   # Output:
   # [[1. 1. 1.]
   #  [1. 1. 1.]]
   ```

4. **Using `numpy.full()`**:
   This function creates an array filled with a specified value.
   
   ```python
   full_arr = np.full((2, 3), 5)  # Creates a 2x3 matrix of fives
   print(full_arr)  
   # Output:
   # [[5 5 5]
   #  [5 5 5]]
   ```

5. **Using `numpy.arange()`**:
   This function returns evenly spaced values within a given interval.
   
   ```python
   arange_arr = np.arange(0, 10, 2)  # Creates an array of even numbers from 0 to 8
   print(arange_arr)  # Output: [0 2 4 6 8]
   ```

6. **Using `numpy.linspace()`**:
   This function returns evenly spaced values over a specified interval.
   
   ```python
   linspace_arr = np.linspace(0, 1, 5)  # Creates an array of 5 numbers from 0 to 1
   print(linspace_arr)  # Output: [0.   0.25 0.5  0.75 1.  ]
   ```

7. **Using `numpy.random.rand()`**:
   This function returns random samples from a uniform distribution over `[0, 1)`.

   ```python
   rand_arr = np.random.rand(3)  # Creates an array of 3 random numbers between 0 and 1
   print(rand_arr)  
   ```

8. **Using `numpy.eye()`**:
   This function returns a 2D array with ones on the diagonal and zeros elsewhere.
   
   ```python
   eye_arr = np.eye(3)  # Creates a 3x3 identity matrix
   print(eye_arr)  
   # Output:
   # [[1. 0. 0.]
   #  [0. 1. 0.]
   #  [0. 0. 1.]]
   ```

These functions provide a robust way to initialize arrays, which are fundamental in numerical computations and data manipulation.

#Array Creation
#Numpy