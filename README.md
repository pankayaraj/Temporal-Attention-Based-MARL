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

#### On Linux:
* Open the terminal in the directory where you want to setup the virtual environment.
* Use the following command to create a python3 virtual environment named "env"

```python3 -m venv env```

* Use the following command to activate the virtual environment created.

```source env/bin/activate```

* Use the following command to leave the virtual environment.

```deactivate```

> Installing the list of required dependencies within the created virtual environment.

* Execute the following command to install the list of required dependencies from ```requirements.txt``` file

```pip3 install -r requirements.txt```


## Example

* Running the ```main.py``` script with the following arguments will train 3 agents in a ```simple_line``` environment and dump the results into a new directory named 0 in within marlsave directory.

```python3 main.py --env-name simple_line --num-agents 3 --save-dir 0```

* Please refer ```arguments.py``` for a complete list of arguments.
* TIP: Redirecting the both stdout and stderr into two separate files would make it easier to debug and to track outputs. In the following example, the standard output stream is redirected to log.txt file while, standard error stream is redirected to log.err.txt file. You could casually ```cat``` the log.txt to see current status.

```python3 main.py --env-name simple_line --num-agents 3 --save-dir 0 > log.txt 2> log.err.txt  ``` 

To get cleaner version of the output from the log.txt, you could use following command. This will produce the new file ```filtered.txt```

```cat log.txt | grep "Num success" > filtered.txt
