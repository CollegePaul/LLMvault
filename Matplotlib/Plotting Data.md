### Plotting Data in Matplotlib

Matplotlib is a comprehensive library for creating static, animated, and interactive visualizations in Python. It provides an object-oriented API for embedding plots into applications using general-purpose GUI toolkits like Tkinter, wxPython, Qt, or GTK. The most basic plot in Matplotlib is the line plot.

To get started with plotting data, you first need to import the necessary module from Matplotlib, typically `pyplot`. Here’s a simple example of how to create a line plot:

```python
import matplotlib.pyplot as plt

# Sample data
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

# Create a line plot
plt.plot(x, y)

# Adding title and labels
plt.title('Simple Line Plot')
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')

# Display the plot
plt.show()
```

In this example:
- `import matplotlib.pyplot as plt` imports the plotting library.
- `x` and `y` are lists of data points that will be plotted.
- `plt.plot(x, y)` creates a line plot using these data points.
- `plt.title()`, `plt.xlabel()`, and `plt.ylabel()` add a title to the plot and labels to the x and y axes, respectively.
- `plt.show()` displays the plot.

Matplotlib also supports other types of plots such as scatter plots, bar charts, histograms, etc. Here’s an example of creating a scatter plot:

```python
import matplotlib.pyplot as plt

# Sample data
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

# Create a scatter plot
plt.scatter(x, y)

# Adding title and labels
plt.title('Simple Scatter Plot')
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')

# Display the plot
plt.show()
```

In this example, `plt.scatter(x, y)` creates a scatter plot of the data points in `x` and `y`.

Matplotlib is highly customizable, allowing you to modify almost every aspect of the plots, including colors, line styles, markers, labels, etc. This makes it a powerful tool for data visualization.

#Plotting Data #matplotlib