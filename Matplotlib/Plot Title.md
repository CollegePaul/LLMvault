### Plot Title in Matplotlib

The title of a plot in Matplotlib serves as a brief description or caption that helps viewers understand what the plot represents. It can provide context about the data being visualized, such as the subject matter, variables involved, or the main findings. Adding a title to your plots is generally a good practice as it enhances readability and comprehension.

In Matplotlib, you can set the title of a plot using the `title()` function. This function takes a string argument that becomes the title of the plot. You can also customize the appearance of the title by specifying additional parameters such as font size, color, and style.

### Example

Here is an example of how to add a title to a simple line plot in Matplotlib:

```python
import matplotlib.pyplot as plt

# Sample data
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

# Create a plot
plt.plot(x, y)

# Add a title to the plot
plt.title('Sample Line Plot', fontsize=16, color='blue')

# Show the plot
plt.show()
```

In this example, we create a line plot of `y` versus `x` and add a title "Sample Line Plot" with a font size of 16 and blue color.

#Plot Title #matplotlib