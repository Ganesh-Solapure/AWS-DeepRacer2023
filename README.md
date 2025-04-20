# 🏎️ AWS DeepRacer Student League 2023 – Reinforcement Learning Project

Welcome to my AWS DeepRacer project repository! This project showcases my journey in autonomous racing using reinforcement learning (RL), where I trained, optimized, and competed in the **AWS DeepRacer Student League 2023**. The car learns to drive in a simulated environment using AWS SageMaker and reinforcement learning algorithms.

## 🎯 Objective
To build a reinforcement learning model that autonomously navigates a racetrack with minimum lap time and maximum stability, and compete in the official AWS DeepRacer League.

## 📅 Competition Participation
| Month     | Event                       | World Rank | India Rank | Asia Pacific Rank | Lap Time   | Off-tracks |
|-----------|-----------------------------|------------|------------|-------------------|------------|------------|
| July 2023 | BreadCentric Speedway       | 324 / 2362 | 108 / 819  | 187 / 1330        | 03:23.884  | 2          |
| August 2023 | Rogue Raceway             | 607 / 2645 | 244 / 876  | 339 / 1293        | 04:21.846  | 0          |

## 🧠 Key Features
- 🧪 Trained reinforcement learning models using AWS SageMaker and RoboMaker simulation.
- 🧩 Custom reward functions for different track conditions.
- 🎯 Hyperparameter tuning to balance speed and track stability.
- 📊 Analyzed logs to minimize off-track penalties and improve performance.

## 🚀 Technologies Used
- Python
- AWS DeepRacer
- SageMaker (for training models)
- RoboMaker (simulation)
- CloudWatch (monitoring and logs)
- Jupyter Notebook (reward function coding)

## 🧾 Reward Function Snippet
```python
def reward_function(params):
    if params['all_wheels_on_track'] and params['speed'] > 2.0:
        return 1.0
    else:
        return 1e-3
