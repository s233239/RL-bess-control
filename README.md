# Reinforcement Learning for Battery Energy Storage Control
This project applies **reinforcement learning** to optimize the operation of a battery energy storage system (BESS) in a **real-time electricity market**. The goal is to **maximize revenue** while considering electricity price fluctuations and battery constraints.

**Date:** November-December 2024

---

## 🛠️ Key Skills & Techniques

- **Reinforcement Learning:** Value Iteration, Policy Iteration  
- **Mathematical Modeling:** Markov Decision Processes (MDP), discrete optimization  
- **Programming:** Python, NumPy, pandas  
- **Data Analysis:** Historical electricity price data, state discretization, transition probability estimation  
- **Energy Systems:** Battery Energy Storage Systems (BESS), real-time market simulation

---

## 📄 Project Overview

This project models the sequential decision-making problem of operating a BESS using **value iteration** and **policy iteration** algorithms.  
The system is designed to determine optimal charging, discharging, or idle actions at each hourly timestep based on electricity prices, state of charge, and time.

The problem is framed as a **Markov Decision Process (MDP)**, where the battery can **charge, discharge, or remain idle** at each hourly timestep.  
The main steps include:  

1. **Problem Formulation:** Define state space (SOC, electricity price, time), action space, reward function, and objective (maximize cumulative revenue).  
2. **State Discretization & Transition Probabilities:** Approximate continuous variables into discrete intervals and estimate transition probabilities from historical price data.  
3. **Iteration Algorithms:** Implement **Value Iteration** and **Policy Iteration** to find the optimal policy.  
4. **Performance Evaluation:** Analyze the effects of discount factors and price discretization on revenue and battery behavior.

---

## ⚙️ Problem Formulation

The BESS operation is modeled as a **MDP** defined by the tuple ⟨S, A, P, R, γ⟩.  
- **State (S):** Battery state of charge (SOC), electricity price level, and time step.  
- **Action (A):** Discharge (−1), idle (0), or charge (1).  
- **Reward (R):** Positive for selling (discharge), negative for buying (charge), zero for idling.  
- **Transition (P):** Deterministic for SOC changes, stochastic for price evolution.  
- **Objective:** Maximize expected cumulative reward (total revenue) over the planning horizon.

---

## 📈 Key Results

- RL strategies successfully optimize BESS revenue.  
- Discount factor tuning is critical to balance short-term vs. long-term profit.  
- Price discretization granularity affects policy performance and revenue variability (> Higher price discretization improves profit potential but increases volatility).
- Both Value Iteration and Policy Iteration algorithms converge to identical optimal policies.

---

## 💡 Optional Improvements

- Use adaptive price discretization or continuous RL for more precise control.  
- Include battery degradation to model long-term costs.  
- Extend to multiple batteries or market competition scenarios.
- Explore continuous state/action spaces with advanced RL algorithms (e.g., Q-learning, DDPG).

---

## 📝 References
- Machine Learning for Energy Systems course materials.
- Assignment instructions are provided in Assignment 3.pdf.

---

## 👥 Contributors

- @ismufahmi
- [@strenchev](https://github.com/strenchev)  
- [@nic0lew0ng](https://github.com/nic0lew0ng)  
- [@raullabarthes](https://github.com/raullabarthes)  




