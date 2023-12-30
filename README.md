# Deep Q-Network (DQN) Agent for CartPole

## Overview

This script implements a Deep Q-Network (DQN) agent to solve the CartPole problem using OpenAI's Gym environment. The agent learns to balance a pole on a cart by applying forces to the left or right. The DQN agent uses a neural network to approximate the Q-function, and it employs techniques like epsilon-greedy for exploration and experience replay for efficient learning.

## Key Components

### Environment

- **CartPole-v1**: A Gym environment where the goal is to keep the pole upright by applying forces to a cart moving along a frictionless track.

### DQNAgent

- **Neural Network**: A simple feedforward neural network with two hidden layers, taking the state as input and outputting Q-values for each action.
- **Epsilon-Greedy Strategy**: For action selection, balancing exploration (choosing a random action) and exploitation (choosing the best-known action).
- **Experience Replay**: Stores transitions in a memory buffer and samples minibatches to train the network, improving learning stability and efficiency.
- **Target Update**: The Q-value update during training accounts for future rewards discounted by a factor gamma, aiming to learn the optimal policy.

## How to Run

1. **Setup**: Ensure you have the required packages: `gym`, `numpy`, `keras`.
2. **Parameters**: Adjust parameters like the number of episodes, batch size, or learning rates as necessary.
3. **Execution**: Run the script to start training the agent. The script will print the total reward and epsilon value at the end of each episode.

## Outputs

- The script outputs the total reward the agent achieved and the current value of epsilon after each episode.
- With rendering enabled (`render = True`), you can visualize the cart and pole during the training process.

## Modifying the Script

- **n_episodes**: Change the number of episodes to run the training for longer or shorter periods.
- **batch_size**: Adjust the minibatch size used for training from the replay memory.
- **Network Architecture**: Modify the neural network layers or activation functions to experiment with different approximations of the Q-function.
- **render**: Set to `True` to watch the cart and pole in action as the agent trains.

## Conclusion

This script provides an implementation of a DQN agent for the CartPole environment, showcasing fundamental concepts of reinforcement learning such as Q-learning, neural function approximation, exploration vs. exploitation, and experience replay.

