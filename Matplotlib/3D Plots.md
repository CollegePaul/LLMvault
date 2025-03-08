### 3D Plots in Matplotlib

Matplotlib provides extensive support for creating three-dimensional plots through its `mpl_toolkits.mplot3d` module. These plots are useful for visualizing data that has three dimensions, such as height over a geographic area or depth of an object in space.

To create a 3D plot in Matplotlib, you first need to import the necessary modules and set up a figure with a 3D subplot using `add_subplot(projection='3d')`. Once the subplot is created, you can use various functions like `plot_surface`, `plot_wireframe`, and `scatter` to add different types of plots.

Here's an example that demonstrates how to create a simple 3D surface plot:

```python
import matplotlib.pyplot as plt
from mpl_toolkits.mplot3d import Axes3D
import numpy as np

# Create a new figure for plotting
fig = plt.figure()

# Add a subplot with a 3D projection
ax = fig.add_subplot(111, projection='3d')

# Generate sample data
x = np.linspace(-5, 5, 100)
y = np.linspace(-5, 5, 100)
X, Y = np.meshgrid(x, y)
Z = np.sin(np.sqrt(X**2 + Y**2))

# Plot the surface
ax.plot_surface(X, Y, Z, cmap='viridis')

# Set labels for axes
ax.set_xlabel('X axis')
ax.set_ylabel('Y axis')
ax.set_zlabel('Z axis')

# Display the plot
plt.show()
```

In this example:
- A 3D subplot is created.
- Sample data `X`, `Y`, and `Z` are generated using NumPy. The `Z` values represent the height of the surface at each point `(x, y)`.
- `plot_surface` is used to create a colored surface plot based on the provided `X`, `Y`, and `Z` data.
- Labels for the axes are set to help understand the plot.

3D plots can also be customized with different color maps (`cmap`), line styles, and more to suit specific visualization needs. #3D Plots #matplotlib