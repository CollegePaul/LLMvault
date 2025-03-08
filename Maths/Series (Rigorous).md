### Series (Rigorous)

In mathematics, particularly in analysis, a series refers to an infinite sum of terms that are successively added together. Formally, a series can be defined as the limit of the sequence of partial sums of a given infinite sequence of numbers. If these partial sums converge to a limit, the series is said to converge to that limit; otherwise, it diverges.

To understand this rigorously, consider an infinite sequence \((a_n)\) where \(n\) ranges over all natural numbers (i.e., \(a_1, a_2, a_3, \ldots\)). The \(n\)-th partial sum \(S_n\) of the series is defined as:
\[ S_n = a_1 + a_2 + \cdots + a_n. \]
The series itself is then defined as:
\[ \sum_{n=1}^{\infty} a_n, \]
and it converges if and only if the sequence of partial sums \((S_n)\) converges to some limit \(L\). That is,
\[ \lim_{n \to \infty} S_n = L. \]

#### Example:
Consider the geometric series with the first term 1 and common ratio \(r\) where \(|r| < 1\):
\[ \sum_{n=0}^{\infty} r^n = 1 + r + r^2 + r^3 + \cdots. \]
The partial sums of this series are:
\[ S_n = 1 + r + r^2 + \cdots + r^n. \]
Using the formula for the sum of a finite geometric series, we get:
\[ S_n = \frac{1 - r^{n+1}}{1 - r}. \]
As \(n\) approaches infinity and \(|r| < 1\), \(r^{n+1}\) approaches 0, so the sequence of partial sums converges to:
\[ \lim_{n \to \infty} S_n = \frac{1}{1 - r}. \]
Thus, the series converges to \(\frac{1}{1 - r}\).

#Series (Rigorous) #Maths