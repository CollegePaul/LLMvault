### Trigonometric Functions in Mathematics

Trigonometric functions are essential mathematical tools used to describe the relationships between angles and sides of triangles. The primary trigonometric functions are sine, cosine, and tangent, which can be defined using a right-angled triangle:

1. **Sine (sin)**: For an angle θ in a right triangle, sin(θ) is the ratio of the length of the side opposite to the angle to the length of the hypotenuse.
2. **Cosine (cos)**: cos(θ) is the ratio of the length of the adjacent side to the length of the hypotenuse.
3. **Tangent (tan)**: tan(θ) is the ratio of the length of the opposite side to the length of the adjacent side.

These functions are also used in various fields such as physics, engineering, and computer science for solving problems related to angles and waves.

#### Example Code in Python

Here's a simple Python code example that demonstrates how to use these trigonometric functions using the `math` module:

```python
import math

# Define an angle in degrees
angle_degrees = 30

# Convert the angle to radians
angle_radians = math.radians(angle_degrees)

# Calculate sine, cosine, and tangent of the angle
sin_value = math.sin(angle_radians)
cos_value = math.cos(angle_radians)
tan_value = math.tan(angle_radians)

print(f"Sine of {angle_degrees} degrees: {sin_value}")
print(f"Cosine of {angle_degrees} degrees: {cos_value}")
print(f"Tangent of {angle_degrees} degrees: {tan_value}")
```

In this code:
- We import the `math` module, which provides access to mathematical functions.
- We define an angle in degrees and convert it to radians since trigonometric functions in Python's `math` module expect angles in radians.
- We then calculate the sine, cosine, and tangent of the given angle using `math.sin()`, `math.cos()`, and `math.tan()` respectively.

#TrigonometricFunctions #Maths #python