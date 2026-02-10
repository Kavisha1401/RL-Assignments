# 🎰 Multi-Armed Bandit Problem using ε-Greedy and UCB

##  Problem Statement

This assignment focuses on solving the **Multi-Armed Bandit (MAB)** problem using two action selection strategies: **ε-greedy** and **Upper Confidence Bound (UCB)**.  
The objective is to maximize the total reward 🎯 by selecting the best possible action while maintaining a balance between **exploration** 🔍 and **exploitation** 💡.

---

##  Algorithms Implemented

### ε-Greedy Algorithm
In the ε-greedy method, the agent selects a random action with probability ε (exploration 🔄) and selects the action with the highest estimated reward with probability (1 − ε) (exploitation ⭐).  
The value of ε is varied from **0.01 to 0.99** with a step size of **0.1** to analyze its effect on performance.

### Upper Confidence Bound (UCB) Algorithm
The UCB algorithm selects actions based on both estimated reward and uncertainty. The action selection formula used is:

\[
UCB(a) = Q(a) + \sqrt{\frac{2 \ln n}{n_a}}
\]

where \(Q(a)\) is the estimated action value and the second term represents the uncertainty 📊.

---

## 🔁 Reward Estimation

The estimated reward for each action is updated using **incremental sample averaging**, which allows efficient learning without storing all past rewards.

---

## ⚙️ Experimental Setup

- Number of arms: 5  
- Reward distribution: Bernoulli 🎲  
- Total iterations: 10,000  
- Each arm is selected at least once during initialization  

---

## 📈 Performance Evaluation

The performance of the algorithms is evaluated using:
- Average reward over time 📉  
- Percentage of optimal action selection ✅  

---

## 📊 Output and Analysis

- A plot of **Average Reward at 10,000 steps vs ε**  
- Learning curve comparison of **ε-greedy** and **UCB** based on average reward and optimal action percentage  

---

## 🏁 Conclusion

The results show how exploration strategies affect learning efficiency. UCB generally performs better in early stages due to systematic exploration, while ε-greedy performance depends on the choice of ε.
