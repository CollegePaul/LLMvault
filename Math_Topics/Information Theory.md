### Introduction to Information Theory in Math

Information Theory, developed by Claude Shannon in the 1940s, provides a framework to quantify information. At its core, it deals with the measurement of information content, the compression of information, and the reliability of communication over noisy channels.

#### Key Concepts:

- **Entropy**: A measure of uncertainty or randomness in a set of data. It quantifies how much "information" is contained in a message.
  
  Mathematically, for a discrete random variable \( X \) with possible outcomes \( x_1, x_2, ..., x_n \) and probabilities \( p(x_i) \), the entropy \( H(X) \) is given by:
  \[
  H(X) = -\sum_{i=1}^{n} p(x_i) \log_2(p(x_i))
  \]

- **Mutual Information**: Measures how much one random variable reduces uncertainty about another. It quantifies the amount of information obtained about one random variable through observing another.

#### Example in Python:

Let's calculate the entropy of a simple probability distribution using Python.

```python
import numpy as np

# Define probabilities for an event with three possible outcomes
probabilities = np.array([0.2, 0.5, 0.3])

# Calculate the entropy
entropy = -np.sum(probabilities * np.log2(probabilities))
print(f"Entropy: {entropy} bits")
```

In this example:
- We have a discrete event with three outcomes.
- The probabilities of these outcomes are given as `[0.2, 0.5, 0.3]`.
- The entropy is calculated using the formula provided and gives us an idea of how much information is contained in these probabilities.

#Information Theory #Maths