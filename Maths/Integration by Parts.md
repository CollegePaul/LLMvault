### Integration by Parts in Mathematics

Integration by Parts is a method used to integrate the product of two functions. It is derived from the product rule of differentiation. The formula for integration by parts is given as:

\[ \int u \, dv = uv - \int v \, du \]

Here, \(u\) and \(v\) are functions of the variable being integrated (usually \(x\)), and \(du\) and \(dv\) represent their respective differentials.

To apply this method effectively, it's important to choose which part of the integrand will be \(u\) and which will be \(dv\). Typically, you want \(u\) to be a function that becomes simpler when differentiated, and \(dv\) to be something that can be easily integrated. A common mnemonic for choosing \(u\) is "LIATE" (Logarithmic, Inverse trigonometric, Algebraic, Trigonometric, Exponential), which suggests the order of preference.

**Example 1:**
Let's integrate \(\int x \cos(x) \, dx\).

- Let \(u = x\), then \(du = dx\).
- Let \(dv = \cos(x) \, dx\), then \(v = \sin(x)\).

Applying the formula:
\[ \int x \cos(x) \, dx = x \sin(x) - \int \sin(x) \, dx \]
\[ = x \sin(x) + \cos(x) + C \]

**Example 2:**
Now let's integrate \(\int e^x \sin(x) \, dx\).

- Let \(u = \sin(x)\), then \(du = \cos(x) \, dx\).
- Let \(dv = e^x \, dx\), then \(v = e^x\).

Applying the formula:
\[ \int e^x \sin(x) \, dx = e^x \sin(x) - \int e^x \cos(x) \, dx \]

Now, we need to apply integration by parts again on the remaining integral:

- Let \(u = \cos(x)\), then \(du = -\sin(x) \, dx\).
- Let \(dv = e^x \, dx\), then \(v = e^x\).

So,
\[ \int e^x \cos(x) \, dx = e^x \cos(x) + \int e^x \sin(x) \, dx \]

Substitute this back:
\[ \int e^x \sin(x) \, dx = e^x \sin(x) - (e^x \cos(x) + \int e^x \sin(x) \, dx) \]
\[ 2 \int e^x \sin(x) \, dx = e^x (\sin(x) - \cos(x)) \]
\[ \int e^x \sin(x) \, dx = \frac{e^x}{2} (\sin(x) - \cos(x)) + C \]

#Integration by Parts #Maths