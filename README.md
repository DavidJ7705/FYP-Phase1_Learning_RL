# FYP Phase 1: Learning Reinforcement Learning 🤖

## Project Overview 📋

This repository documents Phase 1 of my Final Year Project, focused on learning and understanding the fundamentals of Reinforcement Learning (RL). The project explores various RL algorithms and compares their performance across different environments.

### What is This Project?

This is a hands-on learning project where I implemented and compared several popular reinforcement learning algorithms on classic OpenAI Gymnasium environments. The goal was to gain practical experience with RL concepts, understand how different algorithms perform, and establish a foundation for more advanced RL work in later project phases.

### Environments Explored

1. **CartPole-v1**: A classic control problem where the agent must balance a pole on a moving cart
2. **FrozenLake**: A grid-world navigation problem where the agent must reach a goal while avoiding holes on a slippery frozen lake

### Algorithms Implemented

- **PPO (Proximal Policy Optimization)**: A policy gradient method known for stability and efficiency
- **DQN (Deep Q-Network)**: A value-based method that uses deep learning to approximate Q-values
- **A2C (Advantage Actor-Critic)**: An actor-critic method that balances policy and value learning
- **Random Baseline**: A baseline agent that takes random actions for comparison

### Key Learnings

Through this project, I gained experience with:
- Implementing and training RL agents using Stable-Baselines3
- Working with OpenAI Gymnasium environments
- Comparing algorithm performance across different problem types
- Understanding the strengths and weaknesses of policy-based vs. value-based methods
- Analyzing training curves and convergence behavior

## Technologies Used 🛠️

- **Stable-Baselines3**: Industry-standard RL algorithm implementations
- **OpenAI Gymnasium**: Toolkit for developing and comparing RL algorithms
- **Python**: Primary programming language
- **NumPy**: Numerical computing
- **Matplotlib**: Visualization and monitoring

## Setup Instructions 🔧

### Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/DavidJ7705/FYP-Phase1_Learning_RL.git
   cd FYP-Phase1_Learning_RL
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install required packages**
   ```bash
   pip install -r requirements.txt
   ```

### Verify Installation

Test that everything is installed correctly:
```bash
python -c "import gymnasium; import stable_baselines3; print('Setup successful!')"
```

## Project Structure 📁

```
FYP-Phase1_Learning_RL/
│
├── .github/workflows
│   └── ci.yml
│
├── `documentation` 
│   ├── Cartpole/ 
│   │   ├── comparison
│   │   │   └── run_...
│   │   │       ├── graphs/
│   │   │       │   └── *graphs.png
│   │   │       └── summary.md 
│   │   │
│   │   ├── ppo-cartpole
│   │   │   └── run_...
│   │   │       ├── graphs/
│   │   │       │   └── *graphs.png
│   │   │       ├── model/
│   │   │       │   └── ppo_cartpole.zip
│   │   │       ├── monitor/
│   │   │       │   └── monitor.csv
│   │   │       ├── videos/
│   │   │       │   └── *videos.mp4
│   │   │       └── summary.md 
│   │   │
│   │   ├── dqn-cartpole
│   │   │   └── run_...
│   │   │       └── ... (same structure as above)
│   │   │
│   │   └── random-baseline
│   │       └── run_...
│   │           └── ... (same structure as above)
│   │               
│   └── Frozenlake/
│       ├── comparison
│       │   └── run_...
│       │       └── ... (same structure as above)
│       │
│       ├── ppo-frozenlake
│       │   └── run_...
│       │       └── ... (same structure as above)
│       │
│       ├── dqn-frozenlake
│       │   └── run_...
│       │       └── ... (same structure as above)
│       ├── a2c-frozenlake
│       │   └── run_...
│       │       └── ... (same structure as above)
│       │
│       └── random-baseline
│           └── run_...
│               └── ... (same structure as above)
│               
├── notebooks
│   ├── Cartpole/ 
│   │   ├── 01_random_baseline.ipynb
│   │   ├── 02_ppo_model.ipynb
│   │   ├── 03_compare_ppo_baseline.ipynb
│   │   ├── 04_dqn_model.ipynb
│   │   ├── 05_compare_dqn_baseline.ipynb
│   │   └── 06_compare_dqn_ppo.ipynb
│   │
│   └── Frozenlake/
│       ├── 01_random_baseline.ipynb
│       ├── 02_ppo_model.ipynb
│       ├── 03_dqn_model.ipynb
│       ├── 04_a2c_model.ipynb
│       └── 05_compare_dqn_ppo.ipynb
│
├── Results/
│   ├── Cartpole/ 
│   │   ├── *graphs.png
│   │   └── README.md
│   │
│   └── Frozenlake/
│       ├── *graphs.png
│       └── README.md
│
├── .gitignore
├── README.md   
└── requirements.txt  
```

## Running the Project ▶️
### CartPole Experiments

The CartPole experiments are organized in Jupyter notebooks in the `notebooks/Cartpole/` directory. Run them in order:

1. **Random Baseline** - `01_random_baseline.ipynb`
2. **PPO Model** - `02_ppo_model.ipynb`
3. **Compare PPO vs Baseline** - `03_compare_ppo_baseline.ipynb`
4. **DQN Model** - `04_dqn_model.ipynb`
5. **Compare DQN vs Baseline** - `05_compare_dqn_baseline.ipynb`
6. **Compare DQN vs PPO** - `06_compare_dqn_ppo.ipynb`

### FrozenLake Experiments

The FrozenLake experiments are in the `notebooks/Frozenlake/` directory. Run them in order:

1. **Random Baseline** - `01_random_baseline.ipynb`
2. **PPO Model** - `02_ppo_model.ipynb`
3. **DQN Model** - `03_dqn_model.ipynb`
4. **A2C Model** - `04_a2c_model.ipynb`
5. **Compare DQN vs PPO** - `05_compare_dqn_ppo.ipynb`

### How to Run
Navigate to the `notebooks/` directory and open the desired notebook. Run cells sequentially from top to bottom.


### Viewing Results

Training results and performance metrics are organized in the `documentation/` directory:

- **Models**: Trained model files (`.zip`) in `documentation/{Environment}/{algorithm}/run_.../model/`
- **Graphs**: Training and evaluation visualizations in `documentation/{Environment}/{algorithm}/run_.../graphs/`
- **Videos**: Recorded agent gameplay in `documentation/{Environment}/{algorithm}/run_.../videos/`
- **Monitors**: Episode statistics (CSV format) in `documentation/{Environment}/{algorithm}/run_.../monitor/`
- **Summaries**: Markdown summaries of results in `documentation/{Environment}/{algorithm}/run_.../summary.md`
- **Comparisons**: Algorithm comparison results in `documentation/{Environment}/comparison/run_.../`

Each experiment run is timestamped and stored in its own `run_...` directory for easy tracking and comparison.

## Results 📊

Detailed results, performance comparisons, and visualizations for each environment can be found in the `Results/` directory:

- **CartPole Results**: See `Results/Cartpole/README.md` for performance analysis and comparison graphs
- **FrozenLake Results**: See `Results/Frozenlake/README.md` for performance analysis and comparison graphs

Each results directory contains comparison graphs and brief summaries of algorithm performance.

**Note**: Full documentation including trained models, videos, and monitoring logs are stored locally in the `documentation/` directory (not pushed to GitHub due to size constraints).

## References 📚

- [Stable-Baselines3 Documentation](https://stable-baselines3.readthedocs.io/)
- [OpenAI Gymnasium Documentation](https://gymnasium.farama.org/)


## Author 👤 

**David Jayakumar**  
Final Year Project 2024/2025

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://www.linkedin.com/in/your-profile) [![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com/DavidJ7705)