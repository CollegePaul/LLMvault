### Probability Basics in Mathematics

Probability is a measure of the likelihood that an event will occur. It is quantified as a number between 0 and 1, where 0 indicates impossibility and 1 indicates certainty. The probability of an event \( E \) is denoted as \( P(E) \).

The basic formula for probability is:
\[ P(E) = \frac{\text{Number of favorable outcomes}}{\text{Total number of possible outcomes}} \]

For example, if you roll a fair six-sided die, the probability of rolling a 4 is:
\[ P(\text{rolling a 4}) = \frac{1}{6} \]
This is because there is one favorable outcome (rolling a 4) and six possible outcomes (rolling a 1, 2, 3, 4, 5, or 6).

### Python Code Example

Here's a simple Python code example that simulates rolling a fair six-sided die and calculates the probability of rolling a specific number, say 4.

```python
import random

def roll_die():
    return random.randint(1, 6)

# Simulate rolling a die many times
num_trials = 10000
count_rolls_of_four = 0

for _ in range(num_trials):
    if roll_die() == 4:
        count_rolls_of_four += 1

probability_of_four = count_rolls_of_four / num_trials
print(f"Estimated probability of rolling a 4: {probability_of_four}")

# Theoretical probability
theoretical_probability_of_four = 1 / 6
print(f"Theoretical probability of rolling a 4: {theoretical_probability_of_four}")
```

In this code, we simulate rolling a die 10,000 times and count how many times a 4 is rolled. We then calculate the estimated probability by dividing the count of rolls of four by the total number of trials. The theoretical probability is calculated as \( \frac{1}{6} \).

#Probability Basics #Maths #python