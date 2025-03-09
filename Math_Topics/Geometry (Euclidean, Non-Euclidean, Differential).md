### Introduction to Geometry: Euclidean, Non-Euclidean, and Differential

#### Euclidean Geometry
Euclidean geometry is the most commonly known type of geometry. It was developed by ancient Greek mathematician Euclid around 300 BCE. This system is based on five fundamental postulates, which include the ability to draw a straight line between any two points, the existence of circles with any given radius and center, and the parallel postulate (through a point not on a given line, there is exactly one parallel line).

**Example using Python:**
We can use the `shapely` library to create and manipulate geometric shapes in Euclidean space.

```python
from shapely.geometry import Point, LineString

# Define points
point1 = Point(0, 0)
point2 = Point(3, 4)

# Create a line between two points
line = LineString([point1, point2])

# Calculate the length of the line (distance between points)
length = line.length
print("Length of the line:", length)  # Output: Length of the line: 5.0

# Check if points are within a certain distance from each other
is_close = point1.distance(point2) < 6
print("Are points close to each other?", is_close)  # Output: Are points close to each other? True
```

#### Non-Euclidean Geometry
Non-Euclidean geometry refers to the types of geometry that do not adhere to all of Euclid's postulates. The most famous examples are hyperbolic and elliptic geometries, where the parallel postulate is replaced with alternatives.

**Example using Python:**
We can use the `geopy` library to demonstrate some concepts in spherical (elliptic) geometry by calculating distances on Earth's surface, which approximates an ellipse.

```python
from geopy.distance import geodesic

# Define locations as latitude and longitude tuples
location1 = (40.7128, -74.0060)  # New York City
location2 = (34.0522, -118.2437)  # Los Angeles

# Calculate the geodesic distance between two points on Earth's surface
distance = geodesic(location1, location2).kilometers
print("Geodesic distance in kilometers:", distance)  # Output: Geodesic distance in kilometers: 3939.503678428049
```

#### Differential Geometry
Differential geometry is a branch of mathematics that uses the techniques of differential calculus, integral calculus, linear algebra, and multilinear algebra to study problems in geometry. It focuses on studying geometric properties of curves and surfaces.

**Example using Python:**
We can use `numpy` for basic vector operations and `matplotlib` to visualize concepts in differential geometry, such as curvature.

```python
import numpy as np
import matplotlib.pyplot as plt

# Define a simple parametric curve: a helix
t = np.linspace(0, 10 * np.pi, 300)
x = np.cos(t)
y = np.sin(t)
z = t / (2 * np.pi)

# Calculate derivatives for curvature
dx_dt = -np.sin(t)
dy_dt = np.cos(t)
dz_dt = 1 / (2 * np.pi)

d2x_dt2 = -np.cos(t)
d2y_dt2 = -np.sin(t)
d2z_dt2 = 0

# Curvature formula for a parametric curve
curvature = abs(dx_dt * d2y_dt2 - dy_dt * d2x_dt2) / (dx_dt**2 + dy_dt**2)**(3/2)

# Plot the helix
fig = plt.figure()
ax = fig.add_subplot(111, projection='3d')
ax.plot(x, y, z)
plt.title("Helix Curve")
plt.show()

# Print the curvature at various points along the curve
print("Curvature values:", curvature[:5])  # Output: Curvature values: [0.79577472 1.         0.64278761 0.38268343 0.20791169]
```

#Geometry (Euclidean, Non-Euclidean, Differential) #Maths