
[Eng](https://github.com/JohnJim0816/reinforcement-learning-tutorials/blob/master/README_en.md)|[中文](https://github.com/JohnJim0816/reinforcement-learning-tutorials/blob/master/README.md)

## 写在前面

本项目用于学习RL基础算法，尽量做到: **注释详细**，**结构清晰**。

代码结构主要分为以下几个脚本：

* ```model.py``` 强化学习算法的基本模型，比如神经网络，actor，critic等
* ```memory.py``` 保存Replay Buffer，用于off-policy
* ```plot.py``` 利用matplotlib或seaborn绘制rewards图，包括滑动平均的reward，结果保存在result文件夹中
* ```env.py``` 用于构建强化学习环境，也可以重新自定义环境，比如给action加noise
* ```agent.py``` RL核心算法，比如dqn等，主要包含update和choose_action两个方法，
* ```main.py``` 运行主函数

其中```model.py```,```memory.py```,```plot.py``` 由于不同算法都会用到，所以放入```common```文件夹中。

## 运行环境

python 3.7、pytorch 1.6.0-1.7.1、gym 0.17.0-0.18.0

## 使用说明

运行带有```train```的py文件或ipynb文件进行训练，如果前面带有```task```如```task0_train.py```，表示对task0任务训练
类似的带有```eval```即为测试。

## 算法进度

|                 算法名称                 |                         相关论文材料                         | 环境                                      |                备注                |
| :--------------------------------------: | :----------------------------------------------------------: | ----------------------------------------- | :--------------------------------: |
| [On-Policy First-Visit MC](./MonteCarlo) |                                                              | [Racetrack](./envs/racetrack_env.md)      |                                    |
|        [Q-Learning](./QLearning)         |                                                              | [CliffWalking-v0](./envs/gym_info.md)     |                                    |
|             [Sarsa](./Sarsa)             |                                                              | [Racetrack](./envs/racetrack_env.md)      |                                    |
|               [DQN](./DQN)               | [DQN Paper](https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf),[Nature DQN Paper](https://www.nature.com/articles/nature14236) | [CartPole-v0](./envs/gym_info.md)         |                                    |
|           [DQN-cnn](./DQN_cnn)           | [DQN Paper](https://www.cs.toronto.edu/~vmnih/docs/dqn.pdf)  | [CartPole-v0](./envs/gym_info.md)         | 与DQN相比使用了CNN而不是全链接网络 |
|         [DoubleDQN](./DoubleDQN)         |                                                              | [CartPole-v0](./envs/gym_info.md)         |                                    |
|   [Hierarchical DQN](HierarchicalDQN)    |       [H-DQN Paper](https://arxiv.org/abs/1604.06057)        | [CartPole-v0](./envs/gym_info.md)         |                                    |
|    [PolicyGradient](./PolicyGradient)    |                                                              | [CartPole-v0](./envs/gym_info.md)         |                                    |
|               [A2C](./A2C)               |        [A3C Paper](https://arxiv.org/abs/1602.01783)         | [CartPole-v0](./envs/gym_info.md)         |                                    |
|               [SAC](./SAC)               |        [SAC Paper](https://arxiv.org/abs/1801.01290)         | [Pendulum-v0](./envs/gym_info.md)         |                                    |
|               [PPO](./PPO)               |        [PPO paper](https://arxiv.org/abs/1707.06347)         | [CartPole-v0](./envs/gym_info.md)         |                                    |
|              [DDPG](./DDPG)              |        [DDPG Paper](https://arxiv.org/abs/1509.02971)        | [Pendulum-v0](./envs/gym_info.md)         |                                    |
|               [TD3](./TD3)               |        [TD3 Paper](https://arxiv.org/abs/1802.09477)         | [HalfCheetah-v2]((./envs/mujoco_info.md)) |                                    |



## Refs

[RL-Adventure-2](https://github.com/higgsfield/RL-Adventure-2)

[RL-Adventure](https://github.com/higgsfield/RL-Adventure)
