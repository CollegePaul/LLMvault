### Sequences (Rigorous) in Mathematics

In mathematics, a sequence is an ordered collection of elements, typically indexed by natural numbers. Formally, a sequence can be defined as a function whose domain is the set of natural numbers or some subset thereof. Each element in the sequence is called a term. If we denote a sequence by \((a_n)\), then \(a_1, a_2, a_3, \ldots\) are the terms of the sequence.

Sequences can be finite or infinite. Finite sequences have a last term, whereas infinite sequences continue indefinitely. An example of a finite sequence is \((1, 3, 5, 7)\), and an example of an infinite sequence is \((1, \frac{1}{2}, \frac{1}{4}, \frac{1}{8}, \ldots)\).

The behavior of sequences, such as whether they converge to a limit or diverge, is often studied in mathematical analysis. A sequence \((a_n)\) is said to converge to a limit \(L\) if, for every positive number \(\epsilon\), there exists a natural number \(N\) such that for all \(n > N\), the absolute value of the difference between \(a_n\) and \(L\) is less than \(\epsilon\). Mathematically, this is written as:

\[ \lim_{n \to \infty} a_n = L \]

if and only if

\[ \forall \epsilon > 0, \exists N \in \mathbb{N}, \forall n > N, |a_n - L| < \epsilon. \]

### Example in Code

Here is a simple Python code example that demonstrates the concept of a sequence by generating the first few terms of the harmonic series, which is an infinite sequence defined as:

\[ H(n) = 1 + \frac{1}{2} + \frac{1}{3} + \ldots + \frac{1}{n} \]

```python
def harmonic_sequence(n):
    # Generate the first n terms of the harmonic sequence
    return [sum(1/i for i in range(1, k+1)) for k in range(1, n+1)]

# Example: Get the first 10 terms of the harmonic sequence
terms = harmonic_sequence(10)
print("The first 10 terms of the harmonic sequence are:", terms)
```

This code defines a function `harmonic_sequence` that calculates the first \(n\) terms of the harmonic series and prints them. #Sequences (Rigorous) #Maths #python