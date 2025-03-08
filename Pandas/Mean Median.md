### Mean and Median in Pandas

In Pandas, mean and median are statistical measures that can be easily calculated using the built-in functions `mean()` and `median()`. These functions help summarize data by providing central tendencies of a dataset.

- **Mean**: The average value of a dataset. It is calculated by summing up all the values in the dataset and then dividing by the number of values.
  
- **Median**: The middle value when the data points are arranged in ascending order. If there is an even number of observations, the median is the average of the two middle numbers.

Here’s how you can calculate these measures using Pandas with Python:

```python
import pandas as pd

# Creating a simple DataFrame
data = {'Values': [10, 20, 30, 40, 50]}
df = pd.DataFrame(data)

# Calculating the mean
mean_value = df['Values'].mean()
print(f"Mean: {mean_value}")

# Calculating the median
median_value = df['Values'].median()
print(f"Median: {median_value}")
```

In this example:
- We first create a DataFrame `df` with a single column 'Values'.
- We then use the `.mean()` function to calculate the mean of the values in the 'Values' column.
- Similarly, we use the `.median()` function to find the median.

This simple example illustrates how straightforward it is to compute these statistical measures using Pandas. #MeanMedian #Pandas #Python