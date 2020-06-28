# Dueling Deep Q Network with Prioritized Experience Replay

## Overview
In this project, we build a Dueling Deep Q Network with Experience Replay as an reinforcement learning agent to solve the discrete Lunar Lander environment in OpenAI Gym. The goal of this environment is to land the Lunar Lander on the Landing pad with zero speed. This task is considered solved when the average reward is +200 points. 

By splitting the q-values of q network into two streams called state-value and action-advantages, Dueling Deep q Network is able to predict more acurratly on q-values. The prioritized experience replay allows the network to select and train experiences which have high td errors, making the training focus on significant experiences. The implemtation also uses fix q-target and soft-update network to further stabilize the training process. 

(This project is implemented in python and tensorflow 2 and is only for self-practice purpose.)

<p align="center">
  <img src="https://github.com/ChienTeLee/dueling_dqn_lunar_lander/raw/master/doc/figure8.png" width="45%" height="45%"> 
</p>

## Dependencies
1. python 3.6.9
2. tensorflow 2.2.0
3. OpenAI Gym 0.17.2 
4. box2d-py

## How to run
1. Run Dueling_DQN_with_Prioritized_Experience_Replay.ipynb
2. After running, the video of trained result will show up in "after_train" folder

## Paper
The implementation is based on the following papers:

1. [Playing Atari with Deep Reinforcement Learning](https://arxiv.org/abs/1312.5602)

2. [Human-level control through deep reinforcement learning](https://www.nature.com/articles/nature14236)

3. [Deep Reinforcement Learning with Double Q-learning](https://arxiv.org/abs/1509.06461)

4. [Prioritized Experience Replay](https://arxiv.org/abs/1511.05952)

5. [Dueling Network Architectures for Deep Reinforcement Learning](https://arxiv.org/abs/1511.06581)

## Implementation
1. The Dueling Deep Q Network with Prioritized Experience Replay is implemented using the following network architecture:
<p align="center">
  <img src="https://github.com/ChienTeLee/dueling_dqn_lunar_lander/raw/master/doc/figure0.png" width="70%" height="70%"> 
</p>

2. The network training algorithm is based on the pseudocode:
<p align="center">
  <img src="https://github.com/ChienTeLee/dueling_dqn_lunar_lander/raw/master/doc/figure2.png" width="70%" height="70%"> 
</p>

3. The data flow is shown in the following diagram:
 <p align="center">
  <img src="https://github.com/ChienTeLee/dueling_dqn_lunar_lander/raw/master/doc/figure1.png" width="70%" height="70%"> 
</p>

## Result
1. The dueling dqn agent after training:
<p align="center">
  <img src="https://github.com/ChienTeLee/dueling_dqn_lunar_lander/raw/master/doc/after_train.gif" width="60%" height="60%"> 
</p>

2. Training reward per iteration:
<p align="center">
  <img src="https://github.com/ChienTeLee/dueling_dqn_lunar_lander/raw/master/doc/figure6.png" width="60%" height="55%"> 
</p>

3. Average for last 50 rewards:
<p align="center">
  <img src="https://github.com/ChienTeLee/dueling_dqn_lunar_lander/raw/master/doc/figure7.png" width="60%" height="55%"> 
</p>

## Reference
This project is inspired by the following blogs:

1. [Deep Q-Learning with Keras and Gym](https://keon.github.io/deep-q-learning/)

2. [Q-learning](https://artint.info/html/ArtInt_265.html)

3. [Understanding Prioritized Experience Replay](https://danieltakeshi.github.io/2019/07/14/per/)

4. [Dueling DQN](https://morvanzhou.github.io/tutorials/machine-learning/reinforcement-learning/4-7-dueling-DQN/)

5. [Prioritised Experience Replay in Deep Q Learning](https://adventuresinmachinelearning.com/prioritised-experience-replay/)

