### Trig Identities in Mathematics

Trigonometric identities are equations involving trigonometric functions that are true for every value of the variables occurring in them, where both sides of the equation are defined. These identities are useful for simplifying expressions and solving equations. Common trigonometric identities include Pythagorean identities, reciprocal identities, quotient identities, and sum and difference identities.

For example, one of the most basic and important trigonometric identities is the Pythagorean identity:
\[ \sin^2(\theta) + \cos^2(\theta) = 1 \]

This identity holds true for any angle \(\theta\).

### Example in Code

Let's demonstrate this identity with a simple Python code snippet. We'll calculate \(\sin^2(\theta) + \cos^2(\theta)\) for a few different angles to verify that the result is always 1.

```python
import math

def verify_pythagorean_identity(angle_degrees):
    angle_radians = math.radians(angle_degrees)
    sin_squared = math.sin(angle_radians) ** 2
    cos_squared = math.cos(angle_radians) ** 2
    identity_result = sin_squared + cos_squared
    return identity_result

# Testing the identity for different angles
angles_to_test = [0, 30, 45, 60, 90]
results = {angle: verify_pythagorean_identity(angle) for angle in angles_to_test}

for angle, result in results.items():
    print(f"For angle {angle} degrees, sin^2({angle}) + cos^2({angle}) = {result}")

# Expected output should be very close to 1 for each angle
```

This code converts an angle from degrees to radians (since the `math.sin` and `math.cos` functions in Python use radians), calculates \(\sin^2(\theta) + \cos^2(\theta)\), and prints the result. The output should be very close to 1 for all tested angles, confirming the Pythagorean identity.

#Trig Identities #Maths #python