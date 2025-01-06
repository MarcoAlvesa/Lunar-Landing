# Lunar-Landing
Deep Q-Learning for Lunar Landing (gymnasium)

Gymnasium is a great API for creating environments to train AIs. In this case, I used the 'LunarLander-v3' environment to apply Q-Learning techniques.

### Libraries:
- **os**: for operational system
- **random**: for random parameteres
- **numpy**: for matriz and math
- **torch**: to build and train AIs using pyTorch
- **torch.nn**: for neural network
- **torch.optim**: for train and otimize AIs
- **tortch.nn.funcitional**: to use some funcition in training
- **torch.autograd**: another module for training
     - **Variable**: to create variable from Torch
- **collections (deque and namedtuple)**: used indeed during the training

There are several parameters for the AI, the first one is:  

- **state_size**: this parameter represents the observation space, a 8-dimensional vector: the coordinates of the lander in x & y, linear velocities in x & y, angle, angular velocity, and two booleans that represent wether each leg is in contact with the ground or not.  
- **action_size**: there are four discrete actions available: 0 - do nothing, 1 - fire left orientation engine, 2 - fire main engine, 3 - fire right orientation engine.
