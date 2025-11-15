# Cartpole - Reinforcement Learning Results ⚖️
This experiment compares **PPO**, **DQN** and a **random baseline** on the **CartPole-v1** environment
## Environment Details 
- Action space: Discrete(2)
- Observation space: (4)
- Maximum steps per episode: 500
- Reward: +1 for every time-step the pole stays balanced

## Algorithms Tested 🤖
- **PPO** (Proxmial Policy Optimization)
- **DQN** (Deep Q-Network)

## Key Findings 
- **PPO** achieves faster learning, convergence and higher stability
- **DQN** performs well but requires much more timesteps to achieve similar outcomes
- **Baseline** fails to improve, maintaining a near 0 reward throughout
- Overall **PPO** is more efficient and achieves the same level of total reward in a third of the training time it takes **DQN**, confirming it is a superior algorothm for the cartpole envrionment

## Visual Results 📈
- **DQN v Baseline MA Comparison**
![DQN Baseline MA Comparison](/Results/Cartpole/DQN_Baseline_MA.png)
---
- **PPO v Baseline MA Comparison**
![PPO Baseline MA Comparison](/Results/Cartpole/PPO_Baseline_MA.png)
---
- **PPO v DQN MA Comparison**
![PPO DQN MA Comparison](/Results/Cartpole/PPO_DQN_MA.png)
---
- **PPO v DQN Metrics Comparison**
![PPO DQN Metrics Comparison](/Results/Cartpole/PPO_DQN_Metrics.png)
---

## **PPO**
### **Evaluation Curve**
![PPO Evaluation Graph](/Results/Cartpole/PPO_evaluation.png)
### **Training Curve**
![PPO Training  Graph](/Results/Cartpole/PPO_training.png)

---

## **DQN**
### **Evaluation Curve**
![DQN Evaluation Graph](/Results/Cartpole/DQN_evaluation.png)
### **Training Curve**
![DQN Training Graph](/Results/Cartpole/DQN_training.png)

---
***⚠️ NOTE: These are some sample images from runs, a full zip file of runs available on repository***