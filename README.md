# Competitive Tennis Agents Training with Deep Reinforcement Learning DDPG

![Agent Playing]
(https://github.com/kinwo/deeprl-tennis-competition/blob/master/AgentPlaying2.png)

## Introduction
This repository contains a Deep Deterministic Policy Gradients (DDPG) agent running in the Unity ML Agent Tennis (https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#tennis) environment. It can be used to train and evaluate the result of the training.

It is an extension of my previous project [Learning Continuous Control in Deep Reinforcement Learning](https://github.com/kinwo/deeprl-continuous-control/) to try out the "AlphaGo Zero" like competitive agents training in which 2 agents knows nothing about the rules at the beginning and gradually gains experience and rewards by playing with each other. 

The DDPG agent is implemented in Python 3 using PyTorch.


### Environment
The 3D environment contains 2 tennis agents who can move forward, backward or jump.

### Goal
The goal is to bounce the ball across the net to other side while not dropping it and the ball is still within the bounds.

### Environment Solved Criteria
The environment is considered solved when the average max score of either agent reach 0.5+ in the last 100 epsisodes.
 
### Rewards
* A reward of +0.1 is provided for each step that the agent bounces the ball to other side successfully.
* A reward of -0.1 is provided for each step that the agent let the ball drop or out of the bounds.

### Actions
Vector Action space: (Continuous) Size of 2, corresponding to moving forward, backward or jump.

### Spaces
The observation space is composed of 8 variables:  
position, velocity of ball and velocity

## Getting Started
1. Clone this Git repository https://github.com/kinwo/deeprl-tennis-competition

2. Install Unity ML
https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Installation.md

3. Download the Unity ML environment from one of the links below based on your OS:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

Then unzip the file and place the file in the project folder.

3. Create Conda Environment   

Install conda from https://conda.io. Create a new Conda environment with Python 3.6.

```bash
conda create --name deeprl python=3.6
source activate deeprl
```

4. Install Dependencies
```bash
cd python
pip install .
```


## How to run the agent
Start Jupyter Notebook
```bash
jupyter notebook
```

To start training, simply open *Tennis.ipynb* in Jupyter Notebook and follow the instructions there:

Trained model weights is included for quickly running the agent and seeing the result in Unity ML Agent.
Simply skip the training step and run the last step of the *Tennis.ipynb*
