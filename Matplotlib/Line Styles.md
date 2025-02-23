### Line Styles in Matplotlib

Matplotlib provides a variety of line styles that can be used to customize the appearance of lines in plots. These styles help in distinguishing between different datasets or emphasizing certain features of the data. The following are some common line styles available in Matplotlib:

- `'-'` : Solid line
- `'--'`: Dashed line
- `'-.'`: Dash-dot line
- `':'`: Dotted line

These line styles can be specified when creating a plot using functions like `plot()`. Here is an example demonstrating the use of different line styles in a plot:

```python
import matplotlib.pyplot as plt
import numpy as np

# Generate some data
x = np.linspace(0, 10, 100)
y1 = np.sin(x)
y2 = np.cos(x)

# Create a plot with different line styles
plt.figure(figsize=(8, 4))
plt.plot(x, y1, linestyle='-', label='Sine Wave (Solid Line)')
plt.plot(x, y2, linestyle='--', label='Cosine Wave (Dashed Line)')

# Adding more lines with other styles for demonstration
y3 = np.sin(x + np.pi / 2)
y4 = np.cos(x - np.pi / 4)

plt.plot(x, y3, linestyle='-.', label='Shifted Sine (Dash-Dot Line)')
plt.plot(x, y4, linestyle=':', label='Shifted Cosine (Dotted Line)')

# Adding labels and title
plt.title('Different Line Styles in Matplotlib')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.legend()

# Show the plot
plt.show()
```

In this example, four different sine and cosine waves are plotted with various line styles: solid, dashed, dash-dot, and dotted. This visualization helps in understanding how each style can be used to distinguish between different datasets in a single plot.

#Line Styles #matplotlib