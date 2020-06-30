# Temporal-Attention-Based-MARL

## Description

### Abstract

> In   multi-agent   systems,   an   agent’s   behaviour   isaffected  by  the  dynamicity  of  the  environment  and  that  of  theinteractions  among  agents.  Thus,  in  learning  to  cooperate  tosolve  complex  tasks,  such  considerations  should  be  taken  intoaccount. Reinforcement learning has gained immense interest inthis line of research as it allows agents to learn useful behaviourby  dynamically  interacting  with  the  environment  and  with  oneanother.  In  this  work,  we  propose  a  model  which  exploits  theinherent graph-like structure of multi-agent networks to facilitatethe learning of more robust behaviour strategies by capturing thespatial  dependencies  and  temporal  dynamics  of  the  underlyinggraph. In practice, partial observability, as well as restricted com-munication  can  result  in  agents  learning  sub-optimal  strategies.The proposed model addresses these issues by allowing each agentto recurrently propagate information through its neighbourhood,thus  gradually  increasing  its  receptive  field.  Empirically,  wedemonstrate the effectiveness of the proposed model on a varietyof  cooperative  control  tasks.
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

