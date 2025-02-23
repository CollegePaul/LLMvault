### Basic Plot in Matplotlib

Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python. A basic plot in Matplotlib typically involves plotting data points on a two-dimensional graph using the `plot` function from the `pyplot` module.

Here's how you can create a simple line plot:

```python
import matplotlib.pyplot as plt

# Data for plotting
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

# Create a figure and an axes.
fig, ax = plt.subplots()

# Plot data on the axes.
ax.plot(x, y)

# Set labels for x and y axes
ax.set_xlabel('X Axis Label')
ax.set_ylabel('Y Axis Label')

# Set a title for the plot
ax.set_title('Simple Line Plot')

# Display the plot
plt.show()
```

In this example:
- We import `pyplot` from Matplotlib, which is commonly used for plotting.
- We define two lists, `x` and `y`, representing the data points to be plotted.
- Using `plt.subplots()`, we create a figure and a set of subplots (in this case, just one).
- The `plot` method on the axes object (`ax`) is used to plot the data. Here, it creates a line graph of `y` over `x`.
- We use `set_xlabel`, `set_ylabel`, and `set_title` methods to label the axes and title the plot.
- Finally, `plt.show()` displays the plot.

#Basic Plot #matplotlib