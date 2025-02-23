### Histogram in Matplotlib

A histogram in Matplotlib is a graphical representation that organizes a group of data points into user-specified ranges. This method provides a visual interpretation of numerical data by indicating the number of occurrences (frequency) of values within specified ranges or bins.

To create a histogram in Matplotlib, you can use the `hist()` function from the `pyplot` module. Here’s how you can do it:

```python
import matplotlib.pyplot as plt

# Sample data: heights of students in cm
heights = [160, 162, 165, 170, 172, 173, 180, 185, 190, 195, 170, 175, 168, 172, 174, 176, 178]

# Create a histogram
plt.hist(heights, bins=5, edgecolor='black')

# Adding titles and labels
plt.title('Histogram of Student Heights')
plt.xlabel('Height (cm)')
plt.ylabel('Number of Students')

# Show the plot
plt.show()
```

In this example:
- `heights` is a list containing sample data.
- The `hist()` function creates the histogram. The `bins` parameter specifies the number of bins to use in the histogram, and `edgecolor` gives color to the edges of each bin for better visualization.

The resulting plot will show how many students fall into each specified height range (bin).

#Histogram #matplotlib