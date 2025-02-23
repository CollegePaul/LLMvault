### Multiple Plots in Matplotlib

Matplotlib allows users to create multiple plots within a single figure or across several figures. This feature is useful for comparing different datasets, visualizing trends over time, or showcasing various aspects of the same data set in different ways.

To create multiple plots in a single figure, you can use the `subplot` function from Matplotlib's `pyplot` module. The `subplot` function divides the figure into a grid and selects which subplot is active for plotting by specifying the number of rows, columns, and the index of the current plot. Alternatively, you can use the `add_subplot` method on a `Figure` object to achieve similar results.

Here’s an example demonstrating how to create multiple subplots within a single figure using both methods:

```python
import matplotlib.pyplot as plt
import numpy as np

# Generate some data
x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)
y3 = np.tan(x)

# Method 1: Using subplot function
plt.figure(figsize=(12, 8))

# First plot: Sine wave
plt.subplot(2, 2, 1)  # 2 rows, 2 columns, first subplot
plt.plot(x, y1)
plt.title('Sine Wave')
plt.grid(True)

# Second plot: Cosine wave
plt.subplot(2, 2, 2)  # 2 rows, 2 columns, second subplot
plt.plot(x, y2)
plt.title('Cosine Wave')
plt.grid(True)

# Third plot: Tangent wave
plt.subplot(2, 2, 3)  # 2 rows, 2 columns, third subplot
plt.plot(x, y3)
plt.title('Tangent Wave')
plt.grid(True)

# Fourth plot (left blank as an example of empty space)

# Method 2: Using add_subplot method
fig = plt.figure(figsize=(12, 8))

# First plot: Sine wave using add_subplot
ax1 = fig.add_subplot(221)  # 2 rows, 2 columns, first subplot (can also use 2, 2, 1)
ax1.plot(x, y1)
ax1.set_title('Sine Wave using add_subplot')
ax1.grid(True)

# Second plot: Cosine wave using add_subplot
ax2 = fig.add_subplot(222)  # 2 rows, 2 columns, second subplot (can also use 2, 2, 2)
ax2.plot(x, y2)
ax2.set_title('Cosine Wave using add_subplot')
ax2.grid(True)

# Third plot: Tangent wave using add_subplot
ax3 = fig.add_subplot(223)  # 2 rows, 2 columns, third subplot (can also use 2, 2, 3)
ax3.plot(x, y3)
ax3.set_title('Tangent Wave using add_subplot')
ax3.grid(True)

# Fourth plot (left blank as an example of empty space)

plt.tight_layout()
plt.show()
```

In this example, two methods are shown for creating multiple subplots within a single figure. The first method uses the `subplot` function directly to specify the grid and position of each subplot. The second method uses the `add_subplot` method on a `Figure` object to achieve similar results.

Additionally, you can create multiple figures by calling `plt.figure()` multiple times. Each call to `plt.figure()` generates a new figure window.

#Multiple Plots #matplotlib