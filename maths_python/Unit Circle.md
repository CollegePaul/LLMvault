### Unit Circle in Mathematics

The Unit Circle is a circle with a radius of 1 centered at the origin (0,0) on the coordinate plane. It plays a crucial role in trigonometry as it helps in defining the sine, cosine, and tangent of an angle. Any point on the unit circle can be represented as (cos(θ), sin(θ)), where θ is the angle formed from the positive x-axis to the line segment connecting the origin to that point.

For example, consider a 90-degree angle (or π/2 radians) in the unit circle. The coordinates of the point on the unit circle at this angle are (cos(π/2), sin(π/2)) which simplifies to (0, 1).

### Python Code Example

Here is a simple Python code that demonstrates how to use trigonometric functions from the `math` module to find points on the Unit Circle for different angles:

```python
import math

def point_on_unit_circle(angle_degrees):
    angle_radians = math.radians(angle_degrees)
    x = math.cos(angle_radians)
    y = math.sin(angle_radians)
    return (x, y)

# Example usage: Find the point on the unit circle for a 90-degree angle
angle = 90
point = point_on_unit_circle(angle)
print(f"The point on the unit circle at {angle} degrees is: {point}")

# Additional example: Iterate through angles from 0 to 360 degrees and print points
angles = range(0, 361, 30)  # Angles from 0 to 360 in steps of 30 degrees
for angle in angles:
    point = point_on_unit_circle(angle)
    print(f"The point on the unit circle at {angle} degrees is: {point}")
```

#Unit Circle #Maths #python