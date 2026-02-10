# Assignment 2 – Nonstationary Multi-Armed Bandit Problem

## Problem Statement

The goal of this assignment is to study the limitations of sample-average action-value methods in **nonstationary environments**.

Design and conduct an experiment to demonstrate the difficulties that sample-average methods face when the underlying reward distributions change over time.

You must use a modified version of the **10-armed bandit testbed** with the following characteristics:

- All true action values \( q_*(a) \) start out equal.
- At every time step, each \( q_*(a) \) undergoes an **independent random walk**, implemented by adding a normally distributed increment with:
  - Mean = 0  
  - Standard deviation = 0.01  

This setup makes the problem **nonstationary**, as the optimal action may change over time.

## Objectives

1. Implement the nonstationary 10-armed bandit environment.
2. Compare the performance of two action-value methods:
   - **Sample-average method** (incremental implementation)
   - **Constant step-size method** with \( \alpha = 0.1 \)
3. Use an **ε-greedy policy** with:
   - \( \epsilon = 0.1 \)
4. Run experiments for a sufficiently long horizon (e.g., **10,000 time steps**).
5. Generate performance plots similar to **Figure 2.2** from Sutton & Barto:
   - Average reward over time
   - (Optional) Percentage of optimal action selected

## Expected Outcome

The experiment should clearly show that:
- The **sample-average method** performs poorly in nonstationary settings because it gives equal weight to outdated rewards.
- The **constant step-size method** adapts better to changes in action values and achieves higher average rewards over time.

## References

- Sutton, R. S., & Barto, A. G. (2018). *Reinforcement Learning: An Introduction* (2nd Edition), Exercise 2.5.
