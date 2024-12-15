# AI Snake Game Using Deep Q-Network (DQN)

This repository contains an implementation of an AI agent that plays the classic Snake game using a Deep Q-Network (DQN) algorithm. The DQN algorithm enables the agent to learn optimal strategies by interacting with the game environment and improving its decision-making over time.

## Features
- AI-controlled Snake using DQN.
- Dynamic game environment with rewards and penalties.
- Real-time visualization of the Snake gameplay.
- Replay memory and experience sampling for efficient learning.

## Requirements

To run this project, ensure you have the following installed:

- Python 3.7+
- `numpy`
- `pytorch`
- `matplotlib`
- `pygame`


Before installing packages it is crucial to create a virtual enviroment or conda enviroment to get rid of dependency issues.

You can install the required packages using:
```
pip install -r requirements.txt file
```
```
Then run command python3 agent.py
```


## Files in the Repository

- `snake_game.py`: Implements the Snake game environment.
- `model.py`: Defines the DQN algorithm, replay buffer, and model architecture.
- `agent.py`: Contains the training loop for the DQN agent.
- `README.md`: Documentation for the project.

## How It Works

1. **Environment**: The Snake game is implemented as a custom environment. The state includes the Snake's position, the direction it's moving in, and the position of the food.

2. **Deep Q-Network (DQN)**:
   - A neural network predicts Q-values for all possible actions (up, down, left, right) given the current state.
   - The agent chooses actions using an epsilon-greedy strategy to balance exploration and exploitation.
   - Rewards are assigned based on the agent's performance (e.g., eating food, hitting walls, or colliding with itself).

3. **Replay Memory**:
   - Transitions (state, action, reward, next state, done) are stored in a replay buffer.
   - Randomly sampled transitions are used to train the model, improving learning stability.

4. **Training**:
   - The model minimizes the mean squared error (MSE) between predicted Q-values and target Q-values using gradient descent.
   - The target Q-values are computed using the Bellman equation.

## Usage

### Training the AI
To train the DQN agent to play Snake:

```bash
python train.py
```

### Watching the AI Play
After training, you can run the trained agent to watch it play the game:

## Results

- The DQN agent gradually improves over episodes, learning strategies like moving toward food while avoiding collisions.
- You can visualize training progress using reward trends plotted with `matplotlib`.


## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

