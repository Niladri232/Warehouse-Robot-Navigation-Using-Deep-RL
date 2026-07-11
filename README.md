# 🚚 Warehouse Pickup and Delivery using Deep Reinforcement Learning

A Deep Reinforcement Learning project that models a warehouse pickup-and-delivery task as a **Markov Decision Process (MDP)**. A custom **Gymnasium** environment was developed with directional wall constraints, and a **Deep Q-Network (DQN)** agent was trained to learn an optimal navigation policy for completing pickup and delivery tasks efficiently.

---

## 📌 Project Overview

Autonomous warehouse robots must navigate complex layouts while transporting goods between designated pickup and delivery locations. Traditional shortest-path algorithms require complete environment knowledge and often struggle in dynamic settings.

This project formulates the warehouse navigation problem as a **Markov Decision Process (MDP)** and trains a **Deep Q-Network (DQN)** agent capable of learning optimal navigation policies directly through interaction with the environment.

The implementation includes:

- A custom warehouse simulation environment built using **Gymnasium**
- Direction-specific wall constraints
- Reward shaping for efficient learning
- Deep Q-Network implemented in **PyTorch**
- ε-greedy exploration strategy
- Performance evaluation against baseline navigation

---

## 🏗️ Environment

The warehouse consists of

- Pickup locations
- Delivery locations
- Obstacles and directional walls
- Valid movement constraints
- Goal-oriented reward structure

The agent learns to:

1. Navigate to the pickup location.
2. Pick up the package.
3. Reach the destination.
4. Deliver the package while minimizing unnecessary movements.

---

## 🧠 Markov Decision Process Formulation

### State

The state consists of:

- Agent position
- Pickup status
- Pickup location
- Delivery destination

### Actions

- Move North
- Move South
- Move East
- Move West
- Pickup
- Dropoff

### Reward Function

Typical rewards include

| Action | Reward |
|---------|---------|
| Valid movement | Small negative reward |
| Successful pickup | Positive reward |
| Successful delivery | Large positive reward |
| Invalid action | Penalty |
| Collision/blocked movement | Penalty |

---

## 🤖 Deep Q-Network (DQN)

The agent is implemented using **PyTorch**.

Key features include:

- Experience Replay
- Target Network
- ε-greedy exploration
- Discounted future rewards
- Mini-batch gradient descent
- Stable policy learning

---

## ⚙️ Technologies Used

- Python
- PyTorch
- Gymnasium
- NumPy
- Matplotlib

---

## 📂 Repository Structure

```
.
├── custom warehouse.ipynb        # Custom warehouse environment
├── Gym_Taxi_Environment.ipynb    # Taxi baseline environment
├── README.md
└── images/                       # (Optional screenshots)
```

---

## 🚀 Getting Started

### Clone the repository

```bash
git clone https://github.com/yourusername/warehouse-dqn.git

cd warehouse-dqn
```

### Install dependencies

```bash
pip install gymnasium
pip install torch
pip install numpy
pip install matplotlib
```

or

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

Open either notebook:

```
custom warehouse.ipynb
```

or

```
Gym_Taxi_Environment.ipynb
```

Run all cells sequentially to:

- Create the environment
- Train the DQN agent
- Evaluate the learned policy
- Visualize training performance

---

## 📈 Results

The trained DQN agent successfully learned an efficient warehouse navigation policy.

Highlights include:

- Stable convergence during training
- High task completion rate
- Efficient pickup and delivery behavior
- Better performance than random navigation
- Improved policy quality through reward shaping

---

## 📚 Concepts Covered

- Reinforcement Learning
- Markov Decision Processes
- Deep Q-Learning
- Experience Replay
- Target Networks
- Exploration vs Exploitation
- Reward Engineering
- Custom Gymnasium Environments

---

## 🔮 Future Improvements

- Double DQN
- Dueling DQN
- Prioritized Experience Replay
- Multi-Agent Warehouse Coordination
- Dynamic Obstacles
- Curriculum Learning
- PPO and Actor-Critic implementations
- 3D warehouse simulation using Unity or Isaac Gym

---

## 📖 References

- Sutton, R. S., & Barto, A. G. *Reinforcement Learning: An Introduction.*
- OpenAI Gymnasium Documentation
- PyTorch Documentation
- Mnih et al. (2015), *Human-level Control through Deep Reinforcement Learning*

---

## 👤 Author

**Niladri Banerjee**

M.Sc. Data Science & Artificial Intelligence

Ramakrishna Mission Vivekananda Educational and Research Institute (RKMVERI)

GitHub: https://github.com/Niladri232

---
