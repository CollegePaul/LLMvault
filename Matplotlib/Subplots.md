### Subplots in Matplotlib

Subplots in Matplotlib allow you to create multiple plots within a single figure. This feature is particularly useful when you want to compare different data sets or visualizations side by side. Subplots are organized in a grid system, where you can specify the number of rows and columns to define how many subplots you want.

To create subplots, you use the `plt.subplots()` function, which returns a figure object and an array of Axes objects (subplots). Each subplot is accessed through this array, allowing you to plot different data or styles on each one individually.

Here's a simple example to demonstrate creating a 2x2 grid of subplots:

```python
import matplotlib.pyplot as plt
import numpy as np

# Generate some data
x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)

# Create a figure and a set of subplots (2 rows, 2 columns)
fig, axs = plt.subplots(2, 2, figsize=(10, 8))

# Plot data on each subplot
axs[0, 0].plot(x, y1, 'r')
axs[0, 0].set_title('Sine Wave')

axs[0, 1].plot(x, y2, 'g')
axs[0, 1].set_title('Cosine Wave')

# You can also plot a combination of functions
axs[1, 0].plot(x, y1 + y2, 'b')
axs[1, 0].set_title('Sine + Cosine')

# Or another variation
axs[1, 1].plot(x, y1 * y2, 'm')
axs[1, 1].set_title('Sine * Cosine')

# Adjust layout to prevent overlap
plt.tight_layout()

# Display the figure with all subplots
plt.show()
```

In this example:
- We generate some data (`x`, `y1`, and `y2`).
- We create a figure with a 2x2 grid of subplots using `plt.subplots(2, 2)`.
- We plot different functions on each subplot.
- We use `set_title()` to add titles to each subplot for clarity.
- Finally, we use `plt.tight_layout()` to ensure that the subplots do not overlap.

This approach provides a flexible way to organize and visualize multiple datasets within a single figure. #Subplots #matplotlib