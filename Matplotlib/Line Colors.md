### Line Colors in Matplotlib

In Matplotlib, line colors can be specified in several ways to enhance the visual appeal and readability of plots. You can use color names (like 'red', 'blue'), hexadecimal color codes (like '#FF5733'), RGB tuples (like (1, 0, 0) for red), or even predefined colormaps.

Here's a brief overview along with examples:

#### Using Color Names
```python
import matplotlib.pyplot as plt

# Data
x = [0, 1, 2, 3, 4]
y1 = [0, 1, 4, 9, 16]
y2 = [0, 2, 8, 18, 32]

plt.plot(x, y1, color='blue', label='Square')
plt.plot(x, y2, color='green', label='Double Square')

# Adding legend
plt.legend()

# Display plot
plt.show()
```

#### Using Hexadecimal Color Codes
```python
import matplotlib.pyplot as plt

# Data
x = [0, 1, 2, 3, 4]
y1 = [0, 1, 4, 9, 16]
y2 = [0, 2, 8, 18, 32]

plt.plot(x, y1, color='#FF5733', label='Square')  # Coral color
plt.plot(x, y2, color='#33FF57', label='Double Square')  # Lime green

# Adding legend
plt.legend()

# Display plot
plt.show()
```

#### Using RGB Tuples
```python
import matplotlib.pyplot as plt

# Data
x = [0, 1, 2, 3, 4]
y1 = [0, 1, 4, 9, 16]
y2 = [0, 2, 8, 18, 32]

plt.plot(x, y1, color=(1, 0.5, 0), label='Square')  # Orange
plt.plot(x, y2, color=(0, 1, 0.5), label='Double Square')  # Teal

# Adding legend
plt.legend()

# Display plot
plt.show()
```

By using these different methods, you can customize the line colors in your Matplotlib plots to suit your needs.

#Line Colors #matplotlib