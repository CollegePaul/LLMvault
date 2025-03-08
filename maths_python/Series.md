### Series in Mathematics

A series in mathematics is the sum of the terms of an infinite sequence of numbers. It can be finite or infinite, but the term "series" often refers to an infinite sum. A series can converge to a specific number (a convergent series) or diverge (a divergent series).

For example, consider the geometric series:  
\[ S = 1 + \frac{1}{2} + \frac{1}{4} + \frac{1}{8} + \cdots \]

This series can be written as:
\[ S = \sum_{n=0}^{\infty} \left(\frac{1}{2}\right)^n \]

The sum of this infinite geometric series is known to converge to 2. 

### Python Code Example

Here's a simple Python code example that calculates the partial sum of the above geometric series up to `n` terms:

```python
# Function to calculate the sum of the first n terms of a geometric series with ratio r
def geometric_series_sum(n, r):
    total = 0
    for i in range(n):
        total += r**i
    return total

# Example usage: Calculate the sum of the first 10 terms of the series 1 + 1/2 + 1/4 + ...
n_terms = 10
ratio = 0.5
result = geometric_series_sum(n_terms, ratio)
print(f"The sum of the first {n_terms} terms is: {result}")
```

This code defines a function `geometric_series_sum` that computes the sum of the first `n` terms of a geometric series with a given ratio `r`. It then calculates and prints the sum of the first 10 terms of the series \(1 + \frac{1}{2} + \frac{1}{4} + \cdots\).

#Series #Maths #python