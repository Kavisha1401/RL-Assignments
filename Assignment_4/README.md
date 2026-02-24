# Reinforcement Learning – Assignment 4  
## Multi-Armed Bandits: UCB and Naive Algorithm

---

## 📌 Questions

### 1. UCB Comparison
- Compare **UCB** for:
  - Stationary reward distributions
  - Non-stationary reward distributions  
- Include performance plots.
- Also compare:
  - **Constant α (step-size)**
  - **Sample Average method**

---

### 2. Naive Algorithm
- Implement the Naive algorithm with:
  - ε = 0.1  
  - δ = 0.05  

---

### 3. Effect of ε and δ
- Vary:
  - ε from 0.01 to 0.1
  - δ from 0.01 to 0.1
- Create performance plots to analyze the effect of different values.

---

## 🧠 Algorithms

### UCB
UCB selects actions using:

$$
A_t = \arg\max_a \left[ Q_t(a) + c \sqrt{\frac{\ln t}{N_t(a)}} \right]
$$

- Works well in stationary environments.
- In non-stationary settings:
  - Sample Average adapts slowly.
  - Constant α performs better.

### Naive Algorithm
Uses empirical means and confidence bounds based on ε and δ to guide action selection.

---

## 📊 Analysis
- UCB performs well for stationary rewards.
- Constant step-size is better for non-stationary environments.
- Smaller ε and δ increase confidence but require more samples.

---

## 🚀 How to Run
1. Open `RL_Assignment_4.ipynb`
2. Run all cells
3. Observe generated performance plots.
