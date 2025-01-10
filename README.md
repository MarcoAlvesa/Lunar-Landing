# Lunar-Landing
Deep Q-Learning for Lunar Landing (gymnasium)  




https://github.com/user-attachments/assets/e2f75906-f4b5-4f8f-8fc4-4791ad740115



  
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

### Architecture of the Neural Network

There are several parameters for the AI, the first one is:  

- **state_size**: this parameter represents the observation space, a 8-dimensional vector: the coordinates of the lander in x & y, linear velocities in x & y, angle, angular velocity, and two booleans that represent wether each leg is in contact with the ground or not.  
- **action_size**: there are four discrete actions available: 0 - do nothing, 1 - fire left orientation engine, 2 - fire main engine, 3 - fire right orientation engine.
- **seed**: a seed with a value 42 for randomness.

  The archtecture are build with 3 conections layers using torch Linear function
- **fc1**: represents the first fully connection between the input layer and the first fully connected layer, the parameters is the state_size and the number of neurons, there is no rule of thumb to tell the optimal number of neurons but extensive experimentation to build a performance AI that manages to land properly on the moon led to the choice of 64 neurons.
- **fc2**: represents the second fully connection layer, the first parameter is the number of neurons in the fist fully connected layer, if the archtecture were build with 2 connections layers, the second parameter would be the number of discrete actions, however, in this case, the second layer want to have another fully connected layer, so the second parameter is again 64.
- **fc3**: the third and final fully connection layer, again, the first parameter is the number of neuron in the previously layer, 64, the second parameter is the number of discrete action of the space ship, determine by action_size.
