# Report
---


## Learning algorithm

The agent uses `ddpg` function in the navigation notebook. 

I used DDPG algorithm as illustrated in [
this paper](https://arxiv.org/pdf/1509.02971.pdf) environment is considered solved when the average reward (over the last 100 episodes) is at least +0.5.



### Neural Network
The ddpg model consits of 2 neural netowrks actor and critic.<br /> 
I have chosen the actor to be 128 x 128 Fully Connected Layers with Relu activation followed by a final Fully Connected layer 
with the same number of units as the action size, also used a batch normalization layer after the first linear layer.<br /> 
The critic is 128 x 128 + action size x 256 Fully Connected Layers with Relu activation followed by a final Fully Connected layer 
with 256 x 1 as output layer, also used a batch normalization layer after the first linear layer.<br />





### Hyper Parameters  

- n_episodes : chosed it to be 5000 and the training will stop just when score reached 0.5 or higher 
- max_t : maximum number of timesteps per episode = 1000
- BUFFER_SIZE : replay buffer size = int(1e6)
- BATCH_SIZ : mini batch size = 128
- GAMMA : discount factor = 0.99
- TAU : for soft update of target parameters = 1e-3 
- LR_ACTOR : learning rate for actor optimizer = 1e-3
- LR_CRITIC : learning rate for critic optimizer = 1e-3


## Performance plot

![Reward Plot](https://github.com/helmogey/p3_collab_compet/blob/master/plot.png?raw=true)


## Future Work
Use convolutional layer. 




