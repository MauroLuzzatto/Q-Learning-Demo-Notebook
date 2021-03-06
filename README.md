# Q-Learning - Jupyter Notebook
This repositoy contains a Jupyter Notebook with an implemenation of a Q-Learning Agent, which learns to solve the n-Chain OpenAI Gym environment 

This notebook is inspired by the following notebook: [Deep Reinforcement Learning Course Notebook](https://github.com/simoninithomas/Deep_reinforcement_learning_Course/blob/master/Q%20learning/Taxi-v2/Q%20Learning%20with%20OpenAI%20Taxi-v2%20video%20version.ipynb)

## Getting Started
Download the repository:

`git clone git@github.com:MauroLuzzatto/Q-Learning-Demo-Notebook.git`

Run the Jupyter Notebook:

`q_learning_notebook.ipynb`

## Description of the Q-Learning Algorithm

The notebook contains a Q-Learning algorithm implementation and a training loop to solve the n-Chain OpenAI Gym environment. The below imgage describes the Q-Learning Algorithm (an oﬀ-policy Temporal-Difference control algorithm):

<img src="/images/Sutton_Barto.png" alt="TicTacToe Environment" width="600"/>

Q-Learning Algorithm - [Image](http://incompleteideas.net/book/the-book-2nd.html) taken from **Richard S. Sutton and Andrew G. Barto, Reinforcement Learning: An Introduction, Second edition, 2014/2015, page 158**

Legend:

- Q: action-value function
- s: state
- s': next state
- a: action
- r: reward
- alpha: learning rate
- gamma: discount factor

## The n-Chain Environment

The n-Chain environment is taken from the OpenAI Gym module: 

[n-Chain](https://gym.openai.com/envs/NChain-v0/): Official Documentation

The image below shows an example of a 5-Chain (n = 5) environment with 5 states. "a" stands for action and "r" for the reward ([Image Source](https://adventuresinmachinelearning.com/reinforcement-learning-tutorial-python-keras/)).
<!-- ![NChain](images/NChain-illustration.png)
 -->
<img src="/images/NChain-illustration.png" alt="NChain" width="600"/>


#### Environment States

This environment contains of a chain with n positions, every chain position corresponds to a possible state the agent can be in:
- state n: position n on the cahin


#### Environment Actions and Rewards

The agent can move along the chain using two actions (for which the agent will get a different reward):
- action 0: move forward along the chain - get no reward
- action 1: jump back to state 0 -  get a small reward of 2

The end of the chain, presents a large reward of 10, and standing at the end of the chain and still moving forward (action 0) the large reward can be gained repeatedly.


## Further Information about Reinforcement Learning
- [OpenAI Gym](https://gym.openai.com/): Gym is a toolkit for developing and comparing reinforcement learning algorithms from OpenAI
- [OpenAI Baselines](https://github.com/openai/baselines): OpenAI Baselines is a set of high-quality implementations of reinforcement learning algorithms
- [Spining Up AI](https://spinningup.openai.com): This is an educational resource produced by OpenAI that makes it easier to learn about deep reinforcement learning
- [A Long Peek into Reinforcement Learning](https://lilianweng.github.io/lil-log/2018/02/19/a-long-peek-into-reinforcement-learning.html): Great blog post from Lilian Weng, where she is briefly going over the field of Reinforcement Learning (RL), from fundamental concepts to classic algorithms
- [Policy Gradient Algorithms](https://lilianweng.github.io/lil-log/2018/04/08/policy-gradient-algorithms.html): Another great blog post from Lilian Weng, where she writes about policy gradient algorithms


