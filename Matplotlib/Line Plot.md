### Line Plot in Matplotlib

A line plot in Matplotlib is a type of chart that displays information as a series of data points connected by straight line segments. It is particularly useful for visualizing trends over time or ordered categories. Each point on the plot represents the intersection of x and y coordinates, with lines connecting these points to form a continuous curve.

To create a line plot in Matplotlib, you can use the `plot()` function from the `pyplot` module. This function takes at least two arguments: the data for the x-coordinates and the data for the y-coordinates.

#### Example

Here is a simple example of how to create a line plot using Matplotlib:

```python
import matplotlib.pyplot as plt

# Sample data
x = [0, 1, 2, 3, 4, 5]
y = [0, 1, 4, 9, 16, 25]

# Create a line plot
plt.plot(x, y, marker='o')

# Adding title and labels
plt.title('Simple Line Plot')
plt.xlabel('X Axis Label')
plt.ylabel('Y Axis Label')

# Display the plot
plt.show()
```

In this example:
- We import `pyplot` from `matplotlib`.
- Define two lists `x` and `y` which represent the coordinates of the points.
- Use `plt.plot()` to create a line plot, with `marker='o'` adding circular markers at each data point.
- Add a title and labels for both axes using `plt.title()`, `plt.xlabel()`, and `plt.ylabel()`.
- Finally, call `plt.show()` to display the plot.

#Line Plot #matplotlib