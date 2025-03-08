## Distributions in Mathematics

In mathematics and statistics, distributions describe the possible values and likelihoods that a random variable can take. One of the most well-known distributions is the **Normal Distribution** or Gaussian Distribution. It is characterized by its bell-shaped curve, which is symmetric around the mean (μ) and has a spread determined by the standard deviation (σ). The normal distribution is defined by the probability density function:

\[ f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}} \]

This equation describes how the values of the random variable are distributed around the mean. The key properties of a normal distribution include:
- The mean, median, and mode are all equal.
- Approximately 68% of the data falls within one standard deviation of the mean.
- About 95% of the data falls within two standard deviations.
- Around 99.7% of the data falls within three standard deviations.

### Example in Code

Here is a simple Python code example that demonstrates how to generate and plot a normal distribution using `numpy` for generating random numbers and `matplotlib` for plotting:

```python
import numpy as np
import matplotlib.pyplot as plt

# Parameters for the normal distribution
mu = 0        # mean
sigma = 1     # standard deviation

# Generate random samples from the normal distribution
samples = np.random.normal(mu, sigma, 1000)

# Plot a histogram of the generated samples
plt.hist(samples, bins=30, density=True, alpha=0.6, color='g')

# Plot the probability density function (PDF) for comparison
xmin, xmax = plt.xlim()
x = np.linspace(xmin, xmax, 100)
p = np.exp(-((x - mu)**2) / (2 * sigma**2)) / (sigma * np.sqrt(2 * np.pi))
plt.plot(x, p, 'k', linewidth=2)

# Labels and title
plt.title('Normal Distribution')
plt.xlabel('Value')
plt.ylabel('Density')

# Show the plot
plt.show()
```

This code snippet generates 1000 random samples from a normal distribution with mean `mu = 0` and standard deviation `sigma = 1`. It then plots these samples as a histogram and overlays the theoretical probability density function for visual comparison.

#Distributions (Normal, etc.) #Maths #python