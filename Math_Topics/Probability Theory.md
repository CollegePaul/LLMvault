### Introduction to Probability Theory in Math

Probability theory is a branch of mathematics that deals with quantifying the likelihood of events occurring. It provides a framework for understanding uncertainty and randomness. At its core, probability theory involves calculating probabilities, which are numerical values between 0 and 1 that represent the chance of an event happening. An event with a probability of 0 is impossible, while an event with a probability of 1 is certain.

#### Key Concepts:
- **Sample Space (Ω):** This is the set of all possible outcomes of an experiment.
- **Event (E):** An event is a subset of the sample space, representing one or more outcomes that we are interested in.
- **Probability Measure (P):** A function that assigns probabilities to events. It satisfies three main properties:
  1. \(0 \leq P(E) \leq 1\) for any event E.
  2. \(P(\Omega) = 1\), meaning the probability of at least one outcome in the sample space is certain.
  3. For mutually exclusive events (events that cannot happen simultaneously), the probability of their union is the sum of their individual probabilities: \(P(A \cup B) = P(A) + P(B)\).

#### Basic Probability Rules:
- **Addition Rule:** The probability of either event A or event B occurring is given by \(P(A \cup B) = P(A) + P(B) - P(A \cap B)\), where \(A \cap B\) represents the intersection of events A and B.
- **Multiplication Rule:** The probability of both event A and event B occurring is given by \(P(A \cap B) = P(A) \times P(B|A)\), where \(P(B|A)\) is the conditional probability of event B occurring given that event A has already occurred.

#### Example in Python:
Let's consider a simple example involving rolling a fair six-sided die. We want to calculate the probability of rolling an even number.

```python
# Define the sample space for rolling a six-sided die
sample_space = [1, 2, 3, 4, 5, 6]

# Define the event of interest: rolling an even number
event_even = [x for x in sample_space if x % 2 == 0]

# Calculate the probability of the event
probability_even = len(event_even) / len(sample_space)

print(f"Probability of rolling an even number: {probability_even}")
```

In this example, the sample space consists of six outcomes, and the event of interest (rolling an even number) includes three outcomes: 2, 4, and 6. The probability is calculated as the ratio of favorable outcomes to total possible outcomes, which is \(3/6 = 0.5\).

#Probability Theory #Maths