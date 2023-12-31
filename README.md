# RL-Task01笔记
绪论，马尔可夫过程，动态规划

**课程资料来源**：https://github.com/datawhalechina/joyrl-book

# 对强化学习的认识
* 1.**分类**：强化学习包括试错学习，观察学习（对应模仿学习、离线强化学习等技术）等。试错学习是强化学习中最鲜明的要素之一，但并不是强化学习的全部。
* 2.**解决问题**：对于任意问题，只要能够建模成序列决策(Sequential decision making)问题或者带有鲜明的试错学习特征，都可以使用强化学习来解决。强化学习主要的方向有多智能体强化学习和从数据中学习。
* 3.**算法**：尽管强化学习算法很多，但基本上就分为两类，即基于价值的和基于策略梯度的算法，这两种算法各有优势。基于价值的方法通常更稳定，因为它们估计了每个状态（或状态动作对）的价值，从而提供了对环境的全局了解；基于策略梯度方法通常更适用于高维度和连续动作空间，因为它们直接学习策略而不需要对值函数进行明确的估计，但其收敛性较难保证。
# 马尔可夫决策过程(Markov decision process,MDP)
* 1.**原理**：马尔可夫决策过程描述的是智能体在与环境交互过程中(通常为离散时步(time step))学到一个目标的过程，而这个目标通常是以最大化累积的奖励来呈现的。
* 2.**性质**：在给定历史状态的情况下，某个状态的未来只与当前状态有关而与历史状态无关。
  (强化学习所解决的问题不一定要严格满足马尔可夫性质，能满足尽量满足；当要解决的问题不能严格满足马尔可夫性质的条件时，可以结合其他的方法来辅助强化学习进行决策。)
* 3.**构成要素**：由状态，动作，奖励，状态转移矩阵及折扣因子五部分组成。可以用一个五元组<S,A,R,P,ɣ> 来表示。其中 S表示状态空间，即所有状态的集合，A表示动作空间，R表示奖励函数，P表示状态转移矩阵，ɣ表示折扣因子。
# 动态规划(Dynamic Programming,DP)
* 1.**用途**：求解值函数和最优策略。
* 2.**求解步骤**：确定状态，写出状态转移方程和寻找边界条件。
* 3.**主要性质**：最优化原理、无后效性和有重叠子问题。
* 4.**常见算法**：价值迭代（Value Iteration）、策略迭代（Policy Iteration）和 Q-learning 算法等。策略迭代比价值迭代能够更快地接近最优解。
  
