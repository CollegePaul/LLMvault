### Series (Rigorous)

In mathematics, a series is the sum of the terms of an infinite sequence of numbers. More formally, it is the limit of the sequence of partial sums, as the number of terms increases indefinitely. A series is considered convergent if this limit exists and is finite; otherwise, it is divergent.

For instance, consider the geometric series:

\[ S = \sum_{n=0}^{\infty} ar^n \]

where \(a\) is the first term and \(r\) is the common ratio. This series converges to a sum if \(|r| < 1\), and the sum can be calculated using the formula:

\[ S = \frac{a}{1 - r} \]

Here’s a simple Python code example that demonstrates how to calculate the partial sums of this geometric series and check for convergence:

```python
def geometric_series_sum(a, r, n_terms):
    # Calculate the nth partial sum of the geometric series
    if abs(r) >= 1:
        return None  # Series diverges
    current_term = a
    partial_sum = 0
    
    for _ in range(n_terms):
        partial_sum += current_term
        current_term *= r
    
    return partial_sum

# Example usage
a = 1  # First term
r = 0.5  # Common ratio
n_terms = 10  # Number of terms to consider

partial_sum = geometric_series_sum(a, r, n_terms)
print(f"The {n_terms}th partial sum of the series is: {partial_sum}")

# Check convergence by increasing number of terms
for n in [10, 50, 100]:
    print(f"Partial sum with {n} terms: {geometric_series_sum(a, r, n)}")

# Series (Rigorous) #Maths #python
```

This code defines a function to compute the partial sums of a geometric series and demonstrates how these sums approach a limit as the number of terms increases. The tags at the end indicate that this explanation pertains to rigorous series in mathematics and includes Python code.