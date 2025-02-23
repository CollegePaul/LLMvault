### Title: Understanding Common Libraries in Python

Python, being a versatile programming language, has a rich ecosystem of libraries that cater to various needs. These libraries, whether part of the standard library or third-party packages, provide pre-written code for common tasks, making development faster and more efficient.

#### Standard Library:
- **os**: This module provides a way of using operating system-dependent functionality like reading or writing to the file system.
    ```python
    import os

    # Get current working directory
    print(os.getcwd())
    ```
  
- **sys**: It allows you to interact with the Python runtime environment. For example, you can use it to access command line arguments or terminate a program.
    ```python
    import sys

    # Print command line arguments
    for arg in sys.argv:
        print(arg)
    ```

- **datetime**: This module supplies classes for manipulating dates and times.
    ```python
    from datetime import datetime

    # Get the current date and time
    now = datetime.now()
    print("Current date and time:", now.strftime("%Y-%m-%d %H:%M:%S"))
    ```

- **math**: Offers mathematical functions like logarithms, square roots, trigonometric functions, etc.
    ```python
    import math

    # Calculate the square root of a number
    print(math.sqrt(16))  # Output: 4.0
    ```

#### Third-party Libraries:
- **NumPy**: Essential for scientific computing in Python, it provides support for large, multi-dimensional arrays and matrices.
    ```python
    import numpy as np

    # Create a NumPy array
    arr = np.array([1, 2, 3, 4])
    print(arr)
    ```

- **Pandas**: Great for data manipulation and analysis, it provides data structures like DataFrames which are similar to tables in SQL.
    ```python
    import pandas as pd

    # Create a DataFrame
    df = pd.DataFrame({
        'Name': ['Alice', 'Bob'],
        'Age': [25, 30]
    })
    print(df)
    ```

- **Matplotlib**: Used for plotting graphs and visualizations in Python.
    ```python
    import matplotlib.pyplot as plt

    # Plot a simple line graph
    plt.plot([1, 2, 3], [4, 5, 6])
    plt.show()
    ```

These libraries are just the tip of the iceberg. Python's extensive library support ensures that you can find or create a solution for almost any problem.

#Common Libraries #Python