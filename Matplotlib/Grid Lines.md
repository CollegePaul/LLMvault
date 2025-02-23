### Grid Lines in Matplotlib

In Matplotlib, grid lines are used to enhance the readability of plots by providing a background reference that helps viewers align data points more easily. These lines can be customized in terms of their appearance, including color, style (solid, dashed, etc.), and line width.

To add grid lines to a plot in Matplotlib, you can use the `grid()` function from the `pyplot` module. This function enables or disables the grid lines on the current axes. You can also specify additional parameters such as `axis`, `which`, `color`, `linestyle`, and `linewidth` to further customize the grid.

Here is a simple example demonstrating how to add grid lines to a plot:

```python
import matplotlib.pyplot as plt

# Sample data
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

# Create a figure and an axes
fig, ax = plt.subplots()

# Plot the data
ax.plot(x, y, marker='o')

# Add grid lines to the plot
ax.grid(True)

# Optionally, customize the grid appearance
ax.grid(which='both', axis='both', linestyle='--', linewidth=0.5, color='gray')

# Set labels and title
ax.set_xlabel('X-axis')
ax.set_ylabel('Y-axis')
ax.set_title('Plot with Grid Lines')

# Display the plot
plt.show()
```

In this example:
- A simple line plot is created using `ax.plot()`.
- The `ax.grid(True)` function call enables grid lines on both axes.
- Additional customization is applied using `ax.grid(which='both', axis='both', linestyle='--', linewidth=0.5, color='gray')` to set the grid style to dashed lines with a gray color.

#Grid Lines #matplotlib