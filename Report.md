## Solution architecture
The agent uses the Double DQN approach with two duplicate neural networks consisting of three fully connected layers with 64 nodes each and RELU activation functions. The "local" networks' parameters are updated on every learning step while the "target" networks' parameters are softly nudged towards the "local" networks' parameter values with an adjustment factor of .001.

Batches of 64 next states chosen randomly from a buffer of 100,000 memorized experiences are passed through both networks and produce two sets of action values. While the local network's output is used to choose the preferred action based on maximum value, the target network's value for that action is discounted (gamma = .99) and added to memorized rewards to calculate current state values. These are compared against state values predicted by the local network and the loss is backpropagated through the local network. 

Local network parameters are then updated using Adam optimizer and a learning rate of .0005.  

## Results

![Training path](images/training.png)

The described approach achieved an average score of 13 points over the last 100 episodes after 513 episodes of training.

## Outlook

In order to improve the algorithm's performance, [prioritized experience replay](https://arxiv.org/abs/1511.05952) or [dueling DQN architecture](https://arxiv.org/abs/1511.06581) may be implemented.
