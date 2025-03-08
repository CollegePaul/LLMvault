### Separable Differential Equations

In mathematics, separable differential equations are a type of first-order ordinary differential equation that can be solved by "separating" the variables. This means rearranging the equation so that all terms involving one variable appear on one side and all terms involving the other variable appear on the other side. The general form of a separable differential equation is:

\[ \frac{dy}{dx} = g(x)h(y) \]

To solve this, we separate the variables to get:

\[ \frac{1}{h(y)} dy = g(x) dx \]

Then, integrate both sides:

\[ \int \frac{1}{h(y)} dy = \int g(x) dx + C \]

Where \(C\) is the constant of integration.

#### Basic Example

Consider the differential equation:

\[ y' = xy \]

This can be written as:

\[ \frac{dy}{dx} = xy \]

To separate the variables, divide both sides by \(y\) (assuming \(y \neq 0\)) and multiply both sides by \(dx\):

\[ \frac{1}{y} dy = x dx \]

Now, integrate both sides:

\[ \int \frac{1}{y} dy = \int x dx + C \]

This simplifies to:

\[ \ln|y| = \frac{x^2}{2} + C \]

Exponentiating both sides to solve for \(y\) gives:

\[ y = e^{x^2/2 + C} = Ce^{x^2/2} \]

Where \(C\) is an arbitrary constant.

#Separable DEs #Maths