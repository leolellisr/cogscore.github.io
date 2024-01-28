---
layout: default
title: Related Work
subtitle: 
---
# Related Work
## Online Playgrounds

In order to further advance the reinforcement learning area, the scholarly community necessitates robust benchmarks for the comparative analysis of algorithms. Various benchmarks have been introduced, such as the [Arcade Learning Environment (ALE)](https://github.com/Farama-Foundation/Arcade-Learning-Environment), which presented a suite of Atari 2600 games as problems in reinforcement learning. Additionally, the [RLLab benchmark for continuous control](https://arxiv.org/abs/1604.06778) has been introduced, providing an overview of other benchmarks in the field. [OpenAI Gym](https://github.com/openai/gym) aims to amalgamate the most advantageous features from prior benchmark collections into a software package that maximizes convenience and accessibility.

[OpenAI Gym](https://github.com/openai/gym) encompasses a collection of Environments (Partially Observable Markov Decision Processes - POMDPs) that will expand over time.  [OpenAI Gym](https://github.com/openai/gym) specifically concentrates on the episodic framework within reinforcement learning, wherein the agent's experiences are segmented into a sequence of episodes. In each episode, the initial state of the agent is randomly drawn from a distribution, and interaction proceeds until the environment reaches a terminal state. The primary objective in episodic reinforcement learning involves maximizing the expected total reward per episode while striving for optimal performance within a minimal number of episodes.

## Cognitive Evaluation

[ConsScale](https://www.conscious-robots.com/consscale/index.html) leverages the analogy between cognitive architectures and biological entities to evaluate the implementations of machine consciousness. This tool employs both architectural and behavioral criteria, operating at various functional abstraction levels, to discern cognitive functionalities associated with consciousness in artificial agents. The ConsScale evaluation necessitates manual input from the user, utilizing a quantitative scoring system termed the "ConsScale Quantitative Score" (CQS). 
Its primary objective is to offer a numerical metric signifying the cognitive capacity of a given implementation.

## Developmental Robotics And Cognitive Architectures

Cognitive architectures are particularly relevant for highly complex tasks, such as those encountered in the field of developmental robotics. [Lungarella et al. (2007)](https://www.researchgate.net/publication/220233671_Developmental_robotics_A_survey) present a collection of projects in this area, inspired by developmental psychology and aimed at modeling cognitive development in order to investigate the influence of agent-environment interactions. The authors investigated implementations inspired by developmental psychology that aimed to model cognitive development to verify the influence of the interaction experienced by the agent and that provided evidence for experiments in robots.

The CLARION architecture was used by [Licato (2015)](https://ceur-ws.org/Vol-1510/paper3.pdf)  in a virtual agent to perform Piaget's floating task. The agent is asked to respond if an object will sink or float in this task. The [CLARION](http://www.clarioncognitivearchitecture.com/) architecture is a cognitive architecture designed to model various aspects of human cognition, including learning, decision-making, and memory. It combines connectionist (neural network) and symbolic processing approaches. CLARION's hybrid architecture, combining neural networks and symbolic processing, allows it to simulate the gradual development of cognitive abilities observed in Piaget's experiments. It can start with basic sensory-motor interactions and progressively build more advanced cognitive functions, mirroring the stages of cognitive development proposed by Piaget. 

A cognitive model for navigation, based on the LIDA architecture, was implemented by [Madl (2016)](https://doi.org/10.1371/journal.pone.0157343) in a humanoid robot. The [LIDA (Learning Intelligent Distribution Agent)](http://ccrg.cs.memphis.edu/framework.html) architecture is a cognitive architecture designed to model and simulate various aspects of human cognition and intelligence. It represents a framework for understanding how the mind processes information, makes decisions, and learns. In the context of Madl's work, LIDA has been applied to simulate human-like cognitive processes, including perception, attention, memory, learning, and decision-making. LIDA's key components include a global workspace for integrating information, a perceptual module for processing sensory input, a working memory system for representing and manipulating information, and a set of processes for attention, learning, and decision-making. 

The SOAR architecture was used by [Laird (2014)](https://www.sciencedirect.com/science/article/abs/pii/S2212683X14000164) with physical robots coupled with camera and laser, used for the symbolic classification of objects. 

## Developmental Robotics And Reinforcement Learning

An iCub humanoid robot, described by [Metta et al. (2008)](http://portal.acm.org/citation.cfm?doid=1774674.1774683) and [Metta et al. (2010)](http://linkinghub.elsevier.com/retrieve/pii/S0893608010001619), was specifically designed to investigate the embodied cognition hypothesis. This theory posits that human-like manipulation is crucial for developing human cognitive abilities. The iCub robot possesses perceptual and motor systems akin to a young child's, enabling it to interact with its surroundings in a manner similar to a child's interaction.
    
The research conducted by [Fachantidis et al. (2013)](http://ieeexplore.ieee.org/document/6609170/) utilized the iCub simulator with Reinforcement Learning (RL) to explore the autonomous development of robot controllers capable of performing intricate tasks in complex scenarios through the learning process. The iCub robot was subjected to challenging tasks, including hitting a ball and throwing a cube at a target, guided by internal perception-based reward signals as well as external ones. The study's outcomes showcased the RL algorithm's capacity to operate and learn in highly unpredictable environments, effectively controlling a substantial number of Degrees of Freedom (DoF) without prior knowledge. The authors concluded that reward signals based on embodiment features tend to outperform external reward signals.


## Reinforcement Learning And Radial Basis Functions
A Square Multi-Layer Perceptron was implemented by [Shannon (2018)](https://arxiv.org/pdf/1806.07692.pdf) with DQN and radial basis functions (RBFs) on two classic control problems (Mountain Car and Acrobot) and a spiral-shaped maze for a Gridworld problem.

[Lin et al. (2018)](https://ieeexplore.ieee.org/abstract/document/8320372) adopted ideas from constructive neural networks in approximation theory, local average in statistics, Voronoi partition in numerical analysis, and Landweber-type iteration for saturation problem in inverse problems to propose a constructive learning scheme for feed-forward neural networks in classification tasks with large datasets.

Reinforcement learning (RL) was implemented by [Asadi (2021)](https://doi.org/10.1609/aaai.v35i8.16828) with radial basis functions (RBFs) in an extension of the standard DQN algorithm for continuous control with various OpenAI Gym environments (Pendulum, LunarLander, BipedalWalker, Hopper, HalfCheetah and Ant).


