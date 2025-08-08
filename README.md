# Reinforcement Learning Agent for Battleship

## Overview

This project explores the application of reinforcement learning techniques—**SARSA**, **Expected SARSA**, and **Q-Learning**—to develop an intelligent agent that can efficiently play the game of Battleship. The core focus is on minimizing the number of moves required to sink all ships, thereby improving strategic decision-making over time.

## Objective

The objective is to create a reinforcement learning agent capable of mastering Battleship by learning from interactions within a custom-defined state space. Through iterative simulations, the agent optimizes its policy using temporal-difference learning methods to adapt its strategy dynamically.

## Key Features

- **Custom State Representation**:
  - States are specifically engineered to represent the Battleship grid in a way that maximizes learning efficiency.
  - Includes spatial awareness and historical tracking of hits/misses to form a compact, informative state.

- **Multiple Learning Algorithms**:
  - **SARSA**: Learns action values on-policy by updating from the action actually taken.
  - **Expected SARSA**: Uses expected value of next action instead of sampling, improving stability.
  - **Q-Learning**: An off-policy algorithm that learns from the maximum expected future reward.

- **Efficient Policy Learning**:
  - Balances exploration and exploitation through ε-greedy policies.
  - Adjusts strategy over episodes to converge on an optimal move sequence.

- **Battleship Game Simulation**:
  - Fully simulated environment for evaluating agent performance.
  - Tracks episode reward, number of moves, and win/loss statistics.

## Training Process

The agent is trained over thousands of simulated games. In each episode, it:
1. Receives the current board state.
2. Chooses an action based on its current Q-values.
3. Observes the result (hit, miss, sink).
4. Updates its Q-table according to the learning algorithm in use.

Each method evaluates:
- **Average number of moves to win**
- **Convergence rate**
- **Policy effectiveness**

## Requirements

- Python 3.x
- NumPy
- Matplotlib (optional, for visualization)


## How to Run

1. Open the Jupyter notebook:
   ```bash
   jupyter notebook Battleship_Simulator.ipynb
   ```
2. Execute each cell to run the environment setup, training loop, and evaluation metrics.
3. Select the desired learning algorithm by modifying the corresponding cell.

## Results and Evaluation

The notebook includes:
- Performance graphs (e.g., moves per episode)
- Q-table snapshots
- Comparative analysis across learning methods
- Visual feedback from gameplay simulations

---

