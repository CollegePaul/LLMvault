### L'Hôpital's Rule in Mathematics

L'Hôpital's Rule is a theorem used to evaluate limits of indeterminate forms, typically involving fractions where both the numerator and the denominator approach zero (0/0) or infinity (∞/∞). According to this rule, if the limit of a function as x approaches some value results in an indeterminate form, then the limit of that function is equal to the limit of the derivatives of the numerator and denominator, provided these limits exist.

#### Basic Examples:

1. **Example 1: Indeterminate Form 0/0**

   Consider the limit:
   
   \[
   \lim_{{x \to 0}} \frac{\sin(x)}{x}
   \]
   
   As \( x \) approaches 0, both \(\sin(x)\) and \(x\) approach 0, leading to an indeterminate form of 0/0. Applying L'Hôpital's Rule:
   
   - Derivative of the numerator \(\sin(x)\): \(\cos(x)\)
   - Derivative of the denominator \(x\): \(1\)

   Thus,
   
   \[
   \lim_{{x \to 0}} \frac{\cos(x)}{1} = \cos(0) = 1
   \]

2. **Example 2: Indeterminate Form ∞/∞**

   Consider the limit:
   
   \[
   \lim_{{x \to \infty}} \frac{x^2}{e^x}
   \]
   
   As \( x \) approaches infinity, both \(x^2\) and \(e^x\) approach infinity, leading to an indeterminate form of ∞/∞. Applying L'Hôpital's Rule:
   
   - Derivative of the numerator \(x^2\): \(2x\)
   - Derivative of the denominator \(e^x\): \(e^x\)

   Thus,
   
   \[
   \lim_{{x \to \infty}} \frac{2x}{e^x}
   \]
   
   This is still indeterminate, so we apply L'Hôpital's Rule again:
   
   - Derivative of the numerator \(2x\): \(2\)
   - Derivative of the denominator \(e^x\): \(e^x\)

   Thus,
   
   \[
   \lim_{{x \to \infty}} \frac{2}{e^x} = 0
   \]

#L'Hôpital's Rule #Maths