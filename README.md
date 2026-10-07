# Enduro ALE: Deep Q-Network Agent

## 📖 Introduction
This project implements a Deep Q-Network (DQN) agent using PyTorch to play the `ALE/Enduro-v5` Atari environment. The agent learns to steer and pass cars directly from raw game frames without access to the underlying game state.

## 🎯 Task
The objective is to maximize the game score by learning an optimal sequence of actions from visual observations.

### Main Challenges
- Understanding motion from consecutive frames.
- Handling changing conditions such as day/night, snow, and fog.
- Stabilizing training with experience replay and a target network.

## 🧠 Method
- **Preprocessing:** RGB → grayscale → 84×84 → stack 4 frames.
- **CNN:** 3 convolutional layers extract visual features.
- **DQN:** Predicts Q-values for each discrete action.
- **Training:** Epsilon-greedy exploration, replay buffer (50,000), and target network updated every 10,000 steps.
- **Loss:** Smooth L1 Loss.

## 📊 Results
Average reward: 746

### Gameplay

![Gameplay Result](Model/enduro_test.gif)

**Video:** [Watch the full gameplay](https://github.com/bachPN73/Enduro_Ale/blob/main/Model/enduro_test_ep1000.mp4)

### Model Outputs
```text
Model/
├── dqn_enduro_final.pth
├── model_enduro_ep1000.pth
├── enduro_test.mp4
└── enduro_test_ep1000.mp4
```
