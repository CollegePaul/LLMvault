### Pie Chart in Matplotlib

A pie chart is a circular statistical graphic that is divided into slices to illustrate numerical proportion. In Matplotlib, a popular plotting library in Python, you can create pie charts using the `pie()` function from the `pyplot` module. This function allows you to represent data as proportions of a whole.

To create a simple pie chart, you need to provide at least one list of values representing the sizes of each slice. Optionally, you can also provide labels for each slice to make the chart more informative.

Here is an example of how to create a basic pie chart using Matplotlib:

```python
import matplotlib.pyplot as plt

# Data to plot
labels = ['Python', 'Java', 'C++', 'JavaScript']
sizes = [215, 130, 245, 210]

# Create a pie chart
plt.figure(figsize=(8, 6))
plt.pie(sizes, labels=labels, autopct='%1.1f%%', startangle=140)

# Equal aspect ratio ensures that pie is drawn as a circle.
plt.axis('equal')

# Display the plot
plt.title('Programming Language Usage')
plt.show()
```

In this example:
- `sizes` represents the data values for each slice of the pie chart.
- `labels` provides the names for each slice, corresponding to the data in `sizes`.
- `autopct='%1.1f%%'` adds percentage labels to each slice, rounded to one decimal place.
- `startangle=140` rotates the start of the pie chart by 140 degrees to make it more visually appealing.
- `plt.axis('equal')` ensures that the pie chart is a circle.

This simple example illustrates how to create a basic pie chart in Matplotlib. You can further customize your pie charts with additional parameters such as colors, explode (to highlight slices), and shadow effects.

#Pie Chart #matplotlib