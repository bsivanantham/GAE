# Reinforcement learning algorithms with Generalized Advantage Estimation
source : https://github.com/Anjum48/rl-examples/tree/56aca982fcf4426c02aa7e5fb58a4f8affab8020
Examples of published reinforcement learning algorithms in recent
literature implemented in TensorFlow.
Most of my research is in the continuous domain, and I haven't spent much
time testing these in discrete domains such as Atari etc.

![PPO LSTM solving BipedalWalker-v2](https://github.com/anonymous73/GAE/blob/master/ppo/BipedalWalker_PPO-LSTM.gif)

![PPO LSTM solving BipedalWalker-v2](https://github.com/anonymous73/GAE/blob/master/ppo/BipedalWalker_PPO-LSTM.png)

*BipedalWalker-v2 solved using PPO with a LSTM layer*

## Algorithms Implemented
Thanks to DeepMind and OpenAI for making their research openly available.
Big thanks also to the TensorFlow community.

| Algorithm | Paper                                                   | 
| --------- | ------------------------------------------------------- |
| PPO       | [Proximal Policy Optimization Algorithms](https://arxiv.org/abs/1707.06347)                 |
| GAE       | [High-Dimensional Continuous Control Using Generalized Advantage Estimation](https://arxiv.org/abs/1506.02438) |


- GAE was used in all algorithms except for DPPG
- Where possible, I've added an LSTM layer to the policy and value functions.
This usually made the more complex environments more stable (but slower)
- PPO is completely working and ready for testing different enviroonment in MuJuCo.

![PPO MuJuCo Ant-v2](https://github.com/anonymous73/GAE/blob/master/ppo/MuJuCoANT.gif)
![PPO MuJuCo Humanoid-v2](https://github.com/anonymous73/GAE/blob/master/ppo/MuJuCoHumanoid.gif)
Source : https://gym.openai.com/envs/#mujoco 

## Training
All the Python scripts are written as standalone scripts. Just run them
as you would for a single file or in your IDE. The models
and TensorBoard summaries are saved in the same directory as the script.


## Requirements
- Python 3.5+
- OpenAI Gym
- TensorFlow 1.4
- Numpy 1.13+
- MuJoCo mjpro150

PPO was tested on a 16 core machine using CPU only.
For my setup, there was usually no speed advantage training on the 
CPU vs GPU (GTX 1080), but your performance may differ.

## Testing
Python file ppo.py is a standalone file .Once MuJuCo installed and activated . 
In the python file 'ppo.py' change the checkpoint saving directory to the desired 
location or if you are using the check points available in the repository add 
the file path . 
Once these are done the python is file is good run . MuJuCo environment will pop up showing the 
visulatisation and console or in the terminal based on the method of excuting the python file , 
episode and its reward will be printed .
