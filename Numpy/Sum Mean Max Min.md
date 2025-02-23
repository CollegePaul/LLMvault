### Sum, Mean, Max, Min in Numpy

In NumPy, `sum`, `mean`, `max`, and `min` are functions used to perform basic statistical computations on arrays. Here's how each of these functions works:

- **Sum (`np.sum`)**: This function calculates the sum of all elements in an array or along a specified axis.
  
  Example:
  ```python
  import numpy as np

  arr = np.array([1, 2, 3, 4, 5])
  total_sum = np.sum(arr)
  print(total_sum)  # Output: 15
  ```

- **Mean (`np.mean`)**: This function computes the arithmetic mean (average) of elements in an array or along a specified axis.
  
  Example:
  ```python
  import numpy as np

  arr = np.array([1, 2, 3, 4, 5])
  average = np.mean(arr)
  print(average)  # Output: 3.0
  ```

- **Max (`np.max`)**: This function returns the maximum value from an array or along a specified axis.
  
  Example:
  ```python
  import numpy as np

  arr = np.array([1, 2, 3, 4, 5])
  max_value = np.max(arr)
  print(max_value)  # Output: 5
  ```

- **Min (`np.min`)**: This function returns the minimum value from an array or along a specified axis.
  
  Example:
  ```python
  import numpy as np

  arr = np.array([1, 2, 3, 4, 5])
  min_value = np.min(arr)
  print(min_value)  # Output: 1
  ```

These functions are incredibly useful for performing quick statistical analysis on data stored in NumPy arrays. They can be applied to multi-dimensional arrays as well, with the `axis` parameter allowing computations along specific dimensions.

#Sum Mean Max Min #Numpy