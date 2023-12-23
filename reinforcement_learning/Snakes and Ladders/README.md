# Snakes and Ladders Reinforcement Learning

## Overview

This repository contains the implementation of a Q-learning algorithm for playing the Snakes and Ladders game. The code includes functions for rendering the game board, defining game dynamics, and implementing the Q-learning algorithm.

## Game Board Rendering

The `render_game_board` function uses Matplotlib to visualize the game board. It displays the board image, the current position of the player (robot), and a caption indicating the current state, action, and reward.

## Game Dynamics

The `get_next_position_reward` function defines the game dynamics. It calculates the new position based on the chosen action and assigns a reward according to the game rules, incorporating features such as ladders and snakes.

## Random Agent Play

The code includes a loop where a random agent plays the game for a specified number of steps. The agent randomly selects actions, observes the next position and reward, and accumulates the total reward. It looks something like the video below:

https://github.com/tanmy-sharma/AI/assets/98535797/1c3d03eb-5cb5-4fd4-a755-35cc12cfe4d0

## Q-learning Algorithm

The Q-learning algorithm is implemented in the loop where the agent plays the game and updates the Q-table. The algorithm follows these key steps:
- Choose an action using a greedy policy.
- Perform the action, observe the next position, and receive the reward.
- Update the Q-value for the current state-action pair using the Bellman equation.

## Q-table Initialization

The Q-table (`Q`) is initialized to store Q-values for each state-action pair. States represent grid positions, and actions are the four possible moves (left, right, up, down).

## Training

To train the Q-learning algorithm and improve its performance:

1. **Run the Random Agent Play:**
   - Execute the code to observe a random agent playing the game.
   - Note the total reward achieved by the random agent.

2. **Modify Hyperparameters:**
   - Adjust hyperparameters such as learning rate, discount factor, and exploration-exploitation balance in the Q-learning algorithm.

3. **Increase Training Episodes:**
   - Increase the number of training episodes to allow the agent to explore and learn from more experiences.

4. **Evaluate and Iterate:**
   - After training, evaluate the agent's performance using the `print_optimal_trajectory` function.
   - If the performance is not satisfactory, iterate by adjusting hyperparameters and repeating the training process.
  
The training process will look something like the video below:

https://github.com/tanmy-sharma/AI/assets/98535797/cec195fc-7628-470d-a2df-6f6827f0853d

## Optimal Path Printing

The `print_optimal_trajectory` function traces the optimal path using the learned Q-table. It starts from the initial position and chooses the action with the highest Q-value at each step until reaching the goal. Optimal Path for this problem can be seen below:

## Usage

1. Run the code to observe a random agent playing the game.
2. Implement and run additional experiments to improve the Q-learning algorithm.
3. Since this is a relatively smaller example of Q-learning, we can achieve our desired state very easily. As we increase the hurdles, our parameters will increase and so will the training time and iterations.
