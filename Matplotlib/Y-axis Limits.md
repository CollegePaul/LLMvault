### Y-axis Limits in Matplotlib

In Matplotlib, setting y-axis limits allows you to control the range of values displayed on the vertical axis of a plot. This can be particularly useful for focusing on specific parts of your data or for ensuring that all plots have consistent scales. You can set these limits using the `set_ylim()` method on an Axes object or by passing the `ylim` parameter when creating a plot.

#### Example 1: Setting Y-axis Limits with `set_ylim()`

```python
import matplotlib.pyplot as plt

# Sample data
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

# Create a plot
fig, ax = plt.subplots()
ax.plot(x, y)

# Set y-axis limits
ax.set_ylim(0, 12)

plt.title('Plot with Y-axis Limits')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```

#### Example 2: Setting Y-axis Limits with `ylim` Parameter

```python
import matplotlib.pyplot as plt

# Sample data
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

# Create a plot and set y-axis limits directly
plt.plot(x, y)
plt.ylim(0, 12)

plt.title('Plot with Y-axis Limits')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```

In both examples, the y-axis is restricted to show values between 0 and 12. This helps in focusing on the data within this range.

#Y-axis Limits #matplotlib