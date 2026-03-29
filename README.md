# 🤖 Experiment 5: Monte Carlo, SARSA & Q-Learning in GridWorld

**Name:** Sanad Naqvi
**Roll No:** 221A023

---

## 🎯 Aim

To implement and compare **Monte Carlo Control**, **SARSA**, and **Q-Learning** algorithms in a custom GridWorld environment.

---

## 📌 Problem Statement

The objective is to train an agent to navigate a grid environment and reach a goal state efficiently using different reinforcement learning techniques.

---

## 📖 Theory

### 🔹 GridWorld Environment

* A 4×4 grid
* Start state: (0,0)
* Goal state: (3,3)
* Reward:

  * +1 for reaching goal
  * -0.1 for each step

---

### 🔹 Monte Carlo Control

* Learns from complete episodes
* Updates Q-values based on average returns
* Uses ε-greedy policy for exploration

---

### 🔹 SARSA (On-Policy TD Learning)

* Updates Q-values using:

  * Current state-action pair
  * Next state-action pair
* Formula:

  ```
  Q(s,a) ← Q(s,a) + α [r + γQ(s',a') − Q(s,a)]
  ```

---

### 🔹 Q-Learning (Off-Policy TD Learning)

* Learns optimal policy independent of current policy
* Uses maximum Q-value of next state
* Formula:

  ```
  Q(s,a) ← Q(s,a) + α [r + γ max Q(s',a') − Q(s,a)]
  ```

---

## 🛠️ Implementation

### 🔹 Libraries Used

* numpy
* random

### 🔹 Steps

1. Created custom GridWorld environment
2. Defined actions and reward system
3. Implemented:

   * Monte Carlo Control
   * SARSA
   * Q-Learning
4. Trained agent for multiple episodes (5000)
5. Stored Q-values for each method
6. Compared learning outcomes

---

## 📊 Results

### 🔹 Sample Q-values

* **Monte Carlo:**

  * Initial Q-values mostly near 0
  * Slower learning due to episodic updates

* **SARSA:**

  * Example: Q((0,0),1) ≈ 0.133
  * More stable and safe learning

* **Q-Learning:**

  * Example: Q((0,0),1) ≈ 0.180
  * Faster convergence and higher values

---

### 🔹 Observations

* Q-Learning performs better in finding optimal policy
* SARSA is safer (on-policy learning)
* Monte Carlo is slower but conceptually simple

---

## 📈 Analysis

* Exploration (ε-greedy) helps discover optimal paths
* Temporal Difference methods (SARSA, Q-Learning) learn faster than Monte Carlo
* Q-Learning shows highest Q-values indicating better policy

---

## ✅ Conclusion

* All three algorithms successfully learned policies in GridWorld
* Q-Learning achieved best performance
* SARSA provided stable and safer learning
* Monte Carlo was slower but effective
* This experiment highlights differences between episodic and TD learning methods

---

## 📚 References

* Reinforcement Learning Notes
* Sutton & Barto RL Concepts
* Python Documentation

---

## 📦 requirements.txt

```id="p3k9sd"
numpy
```
