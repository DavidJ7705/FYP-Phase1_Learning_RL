# FrozenLake - Reinforcement Learning Results 🧊
This experiment compares **PPO**, **DQN**, **A2C** and a **random baseline** on the **FrozenLake-v1** environment

## Environment Details
- Action space: Discrete(4)
- Observation space: Discrete(16) (4x4 grid)
- `is_slippery = False` = Deterministic, `is_slippery = True` = Stochastic

**Action Space (Discrete 4):**
- 0 → Left
- 1 → Down
- 2 → Right
- 3 → Up

## Observation Meaning
**Observation (Discrete integer):**
- A single integer (0–15) representing the agent’s position on the 4×4 grid.
- Each cell in the grid corresponds to a unique state:
  - `S` — Start position (state 0)
  - `F` — Frozen tile (safe)
  - `H` — Hole (episode ends with no reward)
  - `G` — Goal (episode ends with +1 reward)

## Algorithms Tested 🤖
- **PPO** (Proxmial Policy Optimization)
- **DQN** (Deep Q-Network)
- **A2C** (Advantage Actor Critic)

## a. Key Findings (`is_slippery = False`) ✅
- **PPO** & **A2C** achieves faster learning, convergence and higher stability, with around 98% success-rate
- **DQN** learns successfully but less consistently due to Q-Value variance
- **Baseline** fails to improve, maintaining a near 0 reward throughout
- Overall **PPO** is more efficient and achieves the same level of total reward in a third of the training time it takes **DQN**, confirming it is a superior algorothm for the FrozenLake envrionment

## b. Key Findings (`is_slippery = True`) ❌
- **PPO** performs the most consistently, maintaining steady learning across runs
- **A2C** occasionally matches **PPO** but has large fluctuations
- **DQN** struggles with unstable convergence due to randomness
- **Baseline** fails to improve, maintaining a near 0 reward throughout
- ***⚠️ NOTE: Not useful for our project as randomness alters it drastically, so will not be going into detail here***

## Visual Results (`is_slippery = False`) 📈
- **PPO v DQN v A2C v Random Baseline Cumulative Graph**
![PPO DQN A2C Cumulative Graph](/Results/FrozenLake/PPO_DQN_A2C_cumulative.png)
---
- **PPO v DQN v A2C v Random Baseline Cumulative Graph**
![PPO DQN A2C Metrics Graph](/Results/FrozenLake/PPO_DQN_A2C_metrics.png)
---
- **PPO v DQN v A2C v Random Baseline Cumulative Graph**
![PPO DQN A2C MA Graph](/Results/FrozenLake/PPO_DQN_A2C_MA.png)
---

## **PPO**
### **Evaluation Curve**
![PPO Evaluation Graph](/Results/FrozenLake/PPO_evaluation.png)
### **Training Curve**
![PPO Training  Graph](/Results/FrozenLake/PPO_training.png)

---

## **DQN**
### **Evaluation Curve**
![DQN Evaluation Graph](/Results/FrozenLake/DQN_evaluation.png)
### **Training Curve**
![DQN Training Graph](/Results/FrozenLake/DQN_training.png)

---

## **A2C**
### **Evaluation Curve**
![A2C Evaluation Graph](/Results/FrozenLake/A2C_evaluation.png)
### **Training Curve**
![A2C Training Graph](/Results/FrozenLake/A2C_training.png)

***⚠️ NOTE: These are some sample images from runs, a full zip file of runs available on repository***