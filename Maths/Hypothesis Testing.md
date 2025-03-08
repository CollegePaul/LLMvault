### Hypothesis Testing in Mathematics

Hypothesis testing is a fundamental concept in statistics that involves making decisions about population parameters based on sample data. It helps us determine whether the observed differences between groups are significant or due to random chance.

The process begins with formulating two hypotheses:
- **Null Hypothesis (H₀):** This assumes no effect or no difference. For example, if you're testing a new drug, H₀ might be that the drug has no effect on the patient's condition.
- **Alternative Hypothesis (H₁):** This suggests an effect or a difference. In our example, H₁ could state that the drug does have an effect.

Here are the basic steps involved in hypothesis testing:
1. **State the hypotheses:** Clearly define both the null and alternative hypotheses.
2. **Choose a significance level (α):** This is a threshold to decide when you reject the null hypothesis. Common choices are 0.05 or 0.01.
3. **Collect data and compute the test statistic:** Use relevant statistical methods to gather sample data and calculate a value that will help in deciding between H₀ and H₁.
4. **Determine the p-value:** The p-value is the probability of observing your test statistic (or something more extreme) if the null hypothesis were true.
5. **Make a decision:** If the p-value is less than α, reject the null hypothesis in favor of the alternative. Otherwise, fail to reject the null hypothesis.

#### Example

Suppose you want to test whether a new teaching method improves students' test scores. The average score before implementing the new method was 75 out of 100. You randomly select 30 students and teach them using this new method. Their average score turns out to be 80 with a standard deviation of 5.

- **H₀:** μ = 75 (The new teaching method does not change the test scores)
- **H₁:** μ > 75 (The new teaching method increases the test scores)

You choose a significance level of α = 0.05 and calculate the z-score for your sample mean:
\[ Z = \frac{\bar{X} - \mu_0}{\sigma / \sqrt{n}} \]
Where,
- \( \bar{X} = 80 \) (sample mean)
- \( \mu_0 = 75 \) (population mean under H₀)
- \( \sigma = 5 \) (standard deviation of the sample)
- \( n = 30 \) (sample size)

\[ Z = \frac{80 - 75}{5 / \sqrt{30}} = \frac{5}{5 / 5.477} = \frac{5}{0.9129} \approx 5.48 \]

Using a standard normal distribution table or software, the p-value associated with this z-score is extremely small (less than 0.0001).

Since the p-value < α (0.0001 < 0.05), you reject H₀ in favor of H₁. There is strong evidence that the new teaching method increases students' test scores.

#Hypothesis Testing #Maths