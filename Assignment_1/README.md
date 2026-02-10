# Assignment 1 – Reinforcement Learning for Tic-Tac-Toe

## Problem Statement

The objective of this assignment is to implement a **Reinforcement Learning agent** for the game of **Tic-Tac-Toe** using **Q-learning**, and to analyze the learning behavior under different action-selection strategies.

The agent learns by interacting with the environment over multiple time steps and updates its action-value function based on observed rewards.

## Environment Description

- The environment is a standard **Tic-Tac-Toe game**.
- The agent plays by selecting actions (board positions) based on a learned Q-value table.
- Rewards are assigned based on game outcomes:
  - Win
  - Loss
  - Draw
  - Invalid or suboptimal actions (if applicable)

## Learning Algorithm

The agent uses **Q-learning**, an off-policy Temporal Difference (TD) control algorithm, defined by the update rule:

\[
Q(s,a) \leftarrow Q(s,a) + \alpha \left[ r + \gamma \max_a Q(s',a) - Q(s,a) \right]
\]

Where:
- \( s \) is the current state
- \( a \) is the selected action
- \( r \) is the received reward
- \( s' \) is the next state
- \( \alpha \) is the learning rate
- \( \gamma \) is the discount factor

## Action Selection Policies

The following policies are implemented and compared:

- **Greedy policy** (\( \epsilon = 0 \))
- **ε-greedy policy** with:
  - \( \epsilon = 0.1 \)
  - \( \epsilon = 0.01 \)

These strategies balance **exploration vs exploitation** during learning.

## Experimental Setup

- The agent is trained for different numbers of time steps:
  - **100 steps**
  - **300 steps**
  - **500 steps**
- For each configuration, learning performance is evaluated and averaged over runs.

## Performance Metrics

The following learning curves are generated:

1. **Average Reward vs Time-step**
2. **Percentage of Optimal Actions vs Time-step**

Each plot compares:
- Greedy policy
- ε-greedy (ε = 0.1)
- ε-greedy (ε = 0.01)

## Objectives

1. Implement a Q-learning agent for Tic-Tac-Toe.
2. Study how different exploration strategies affect learning.
3. Compare convergence behavior using learning curves.
4. Analyze the trade-off between exploration and exploitation.

## Expected Outcome

- Purely greedy agents learn slowly or get stuck in suboptimal behavior.
- ε-greedy agents achieve better long-term performance.
- Smaller ε values improve stability after sufficient exploration.

## References

- Sutton, R. S., & Barto, A. G. (2018). *Reinforcement Learning: An Introduction* (2nd Edition).
