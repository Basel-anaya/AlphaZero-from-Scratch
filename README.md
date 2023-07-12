# AlphaZero from Scratch
Out of the box implementation on the Reinforcement Learning algorithm **`AlphaZero`**, And using the algorithm on 2 games which are:
### **Tic Tac Toe Game**
![tictactoe](https://raw.githubusercontent.com/foersterrobert/AlphaZero/master/assets/tictactoe.gif)
### **Connect Four Game**
![connectfour](https://raw.githubusercontent.com/foersterrobert/AlphaZero/master/assets/connectfour.gif)

The AlphaZero project is an implementation of the AlphaZero algorithm for training an AI agent to play the Connect Four game. The algorithm combines self-play, Monte Carlo Tree Search (MCTS), and deep neural networks to achieve strong gameplay without relying on human expertise.

The project consists of several components:

1. Game Implementation:

- The ConnectFour class represents the Connect Four game, providing methods for game state manipulation, move validation, and win conditions.

2. Neural Network Model:

- The ResNet class is a deep neural network model implemented using PyTorch.
- It serves as both a policy network, estimating the probabilities of each action, and a value network, providing a value estimation for the current game state.
- The model is trained through self-play and updated using a combination of policy and value losses.

3. Monte Carlo Tree Search (MCTS):

- The MCTS class performs the Monte Carlo Tree Search algorithm, which combines tree traversal, node selection, and simulation to search for the best moves.
- It uses the ResNet model to guide the search by estimating action probabilities and state values.
- MCTS iteratively builds a search tree and explores possible moves to determine the most promising actions.

4. Training Process:

- The AlphaZero class orchestrates the training process, combining self-play and model updates.
- Self-play generates training examples by playing games against itself using the current model.
- The MCTS algorithm is used to select moves during self-play and generate training examples.
- The model is then trained using the generated examples through a combination of policy and value losses.

5. Game Interface:

- The code includes a game loop where a human player can play against the trained AI agent.
- The AI agent selects moves using MCTS, while the human player provides input through the console.
- The game continues until there is a win or draw.

The AlphaZero project demonstrates the application of deep reinforcement learning techniques to train an AI agent to play Connect Four. It showcases the effectiveness of the AlphaZero algorithm in achieving strong gameplay without relying on human knowledge or heuristics.

### Some Helpful Resources
* AlphaZero-Paper: https://arxiv.org/pdf/1712.01815.pdf
* Paper-Walkthrough: https://youtu.be/0slFo1rV0EM
* MCTS-Explained: https://youtu.be/UXW2yZndl7U
* AlphaZero-Explained: https://youtu.be/62nq4Zsn8vc
