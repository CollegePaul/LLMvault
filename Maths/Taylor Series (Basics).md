### Taylor Series (Basics)

In mathematics, the Taylor series is a powerful tool used to represent functions as an infinite sum of terms that are calculated from the values of the function's derivatives at a single point. It provides a way to approximate complex functions using polynomials.

The general form of a Taylor series centered around a point \(a\) for a function \(f(x)\) is given by:

\[ f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!} (x-a)^n \]

Where:
- \(f^{(n)}(a)\) represents the \(n\)-th derivative of \(f\) evaluated at point \(a\).
- \(n!\) denotes factorial, which is the product of all positive integers up to \(n\).

#### Example

Let's consider a simple example: finding the Taylor series for the exponential function \(e^x\) around \(a=0\), also known as the Maclaurin series.

The derivatives of \(e^x\) are:
- \(f(x) = e^x \implies f(0) = 1\)
- \(f'(x) = e^x \implies f'(0) = 1\)
- \(f''(x) = e^x \implies f''(0) = 1\)

And so on, every derivative of \(e^x\) is \(e^x\), evaluated at \(0\), is always 1.

So the Taylor series expansion for \(e^x\) around 0 becomes:

\[ e^x = \sum_{n=0}^{\infty} \frac{x^n}{n!} = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots \]

This series converges to \(e^x\) for all values of \(x\).

#### Another Example

Consider the function \(f(x) = \cos(x)\) around \(a=0\).

The derivatives are:
- \(f(x) = \cos(x) \implies f(0) = 1\)
- \(f'(x) = -\sin(x) \implies f'(0) = 0\)
- \(f''(x) = -\cos(x) \implies f''(0) = -1\)
- \(f'''(x) = \sin(x) \implies f'''(0) = 0\)

Continuing this pattern, we get:

\[ \cos(x) = \sum_{n=0}^{\infty} (-1)^n \frac{x^{2n}}{(2n)!} = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots \]

This series converges to \(\cos(x)\) for all values of \(x\).

#Taylor Series (Basics) #Maths