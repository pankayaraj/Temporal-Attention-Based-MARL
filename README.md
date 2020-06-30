# Temporal-Attention-Based-MARL

## Description
### About
> This repository includes the corresponding implementation for the work on "Multi-Agent Reinforcement Learning in Sparsely Connected Cooperative Environments"

### Abstract

> In recent years, the consensus among adaptive agents within multi-agent systems (MAS) has been an emerging area of research in the field of autonomous control. Reinforcement Learning (RL) has gained immense interest in this line of work as it aims to learn optimal cooperative policies through trial and error by dynamically interacting with the environment. However, in practice, connectivity within the multi-agent network may be sparse and the agents are often subjected to partial observability. This can result in the learning of sub-optimal policies. In this work, we consider the problem of learning optimal policies in cooperative multi-agent environments in the face of partial observability and sparse connectivity. The proposed model exploits the inherent graph-like structure of multi-agent systems. Graph Neural Networks (GNNs) are utilized to extract spatial dependencies and temporal dynamics of the underlying graph. Such spatio-temporal information is exploited to generate better state representations so as to facilitate the learning of more robust policies. Empirically, we demonstrate the effectiveness of the proposed model on a variety of well-known cooperative control tasks. 
## Code Structure

#### 1. arguments.py
> The input arguments define the algorithim are collected

#### 2. main.py
>The algorithm is run 

#### 3. mpnn.py
> Preporcessing of the input data (spatial, temporal modelling happens here)

#### 4. rlcore
> The base algorithm implementation. (PPO)

#### 5. learner.py, rlagent.py
> the multi agents are set up  and the preprocessed inputs are fed into the base RL algorithm. 

#### 6. mape
> consists of the RL enviornment implementation 

## Installation
> Create a virtualenv in Python3.5

> Execute ''''pip3 install -r requirements.txt''' to install the list of required dependencies from ```requirements.txt``` file


