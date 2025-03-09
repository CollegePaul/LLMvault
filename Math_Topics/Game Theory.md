### Introduction to Game Theory in Math

Game theory is a branch of mathematics that studies strategic decision-making among rational individuals in situations where the outcome for each participant depends on the choices of all participants. It provides tools to understand and predict behavior in competitive as well as cooperative scenarios.

At its core, game theory involves players who choose strategies from a set of available options. Each player's payoff or utility is determined by the combination of strategies chosen by all players involved. The goal is often to identify the optimal strategy for each player that maximizes their payoff, given the strategies of others.

#### Key Concepts in Game Theory:
1. **Players**: Individuals or entities making decisions.
2. **Strategies**: Choices available to a player.
3. **Payoffs**: Outcomes received by players based on the combination of strategies chosen.
4. **Nash Equilibrium**: A stable state where no player can improve their payoff by unilaterally changing their strategy, given the strategies of others.

#### Types of Games:
- **Cooperative vs Non-Cooperative**: In cooperative games, players can form binding agreements; in non-cooperative games, they cannot.
- **Simultaneous vs Sequential**: Simultaneous games involve players making decisions at the same time, while sequential games have a clear order to decision-making.

#### Example: The Prisoner's Dilemma
The Prisoner's Dilemma is one of the most famous examples in game theory. It involves two suspects who are arrested and held separately. They are given the following choices:

- If both remain silent (cooperate), they each receive a small punishment.
- If one confesses (defects) while the other remains silent, the confessor goes free, and the silent partner receives a large punishment.
- If both confess, they both receive moderate punishments.

The payoff matrix can be represented as:

|                | Suspect B: Silent | Suspect B: Confess |
|----------------|-------------------|--------------------|
| **Suspect A:**<br>Silent         | -1, -1            | -3, 0              |
| **Suspect A:**<br>Confess       | 0, -3             | -2, -2             |

In this game, the Nash Equilibrium is for both to confess, even though mutual silence results in a better overall outcome.

#### Python Example: Implementing the Prisoner's Dilemma

```python
# Define payoffs
payoffs = {
    ('Silent', 'Silent'): (-1, -1),
    ('Silent', 'Confess'): (-3, 0),
    ('Confess', 'Silent'): (0, -3),
    ('Confess', 'Confess'): (-2, -2)
}

# Function to determine payoffs based on choices
def get_payoff(strategy_a, strategy_b):
    return payoffs[(strategy_a, strategy_b)]

# Example strategies chosen by each suspect
strategy_A = 'Confess'
strategy_B = 'Confess'

# Calculate and print the payoff for each suspect
payoff_A, payoff_B = get_payoff(strategy_A, strategy_B)
print(f"Suspect A's Payoff: {payoff_A}")
print(f"Suspect B's Payoff: {payoff_B}")

```

In this example, both suspects choose to confess, leading to a Nash Equilibrium where they both receive a payoff of -2. This demonstrates the core concept of strategic interaction and how outcomes can be influenced by the choices made by all parties involved.

#Game Theory #Maths