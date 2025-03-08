### Legend Creation in Matplotlib

In Matplotlib, a legend provides a way to label different data series plotted on a graph. Legends are essential for making your plots more understandable, especially when multiple datasets are visualized on the same axes.

To add a legend to a plot, you typically use the `plt.legend()` function after plotting your data. You can specify labels for each dataset using the `label` parameter in the plotting functions like `plt.plot()`, `plt.scatter()`, etc. When you call `plt.legend()`, Matplotlib automatically uses these labels to create the legend.

Here are some examples of how to create legends with different types of plots:

#### Example 1: Line Plot

```python
import matplotlib.pyplot as plt

# Data for plotting
x = [1, 2, 3, 4, 5]
y1 = [2, 3, 5, 7, 11]
y2 = [1, 4, 6, 8, 10]

# Plotting the data
plt.plot(x, y1, label='Prime Numbers')
plt.plot(x, y2, label='Even Numbers')

# Adding a legend
plt.legend()

# Displaying the plot
plt.title('Line Plot with Legend')
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.show()
```

#### Example 2: Scatter Plot

```python
import matplotlib.pyplot as plt

# Data for plotting
x = [1, 2, 3, 4, 5]
y1 = [2, 3, 5, 7, 11]
y2 = [1, 4, 6, 8, 10]

# Plotting the data
plt.scatter(x, y1, label='Prime Numbers')
plt.scatter(x, y2, label='Even Numbers')

# Adding a legend
plt.legend()

# Displaying the plot
plt.title('Scatter Plot with Legend')
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.show()
```

#### Example 3: Bar Chart

```python
import matplotlib.pyplot as plt

# Data for plotting
categories = ['A', 'B', 'C', 'D']
values1 = [23, 45, 67, 89]
values2 = [12, 34, 56, 78]

# Plotting the data
plt.bar(categories, values1, label='Category A')
plt.bar(categories, values2, bottom=values1, label='Category B')

# Adding a legend
plt.legend()

# Displaying the plot
plt.title('Stacked Bar Chart with Legend')
plt.xlabel('Categories')
plt.ylabel('Values')
plt.show()
```

In each of these examples, the `label` parameter is used to provide a name for each dataset. The `plt.legend()` function then creates a legend that associates these names with the corresponding data series in the plot.

#Legend Creation #matplotlib