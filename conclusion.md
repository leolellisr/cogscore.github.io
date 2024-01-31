---
layout: default
title: Conclusion and Partial Results
subtitle: 
---

# Partial Results
## Cognitive Experiments Design
Despite the significant advancements in Cognitive Architectures and Development Robotics, there remains a noticeable void within the literature related to the evaluation of cognitive architectures and the sophisticated functionalities displayed by robots. Acknowledging this gap, our objective is to forge a connection between the insights derived from human developmental theories and their potential implications in the field of robotics. Central to our investigation is the premise that learning follows a cumulative trajectory characterized by increasing complexity. Consequently, our focus centers on the initial stages of human development, particularly within the domain encompassing children aged 0 to 2 years.

Drawing inspiration from Piaget's constructivist theory and aligning it with empirical studies in the sphere of Developmental Robotics, we introduce a framework that facilitates the categorization of these investigations. In this context, we curate a sequence of progressive experiments mirroring the motor and cognitive progression exhibited by children from birth to two years of age, to be executed with robots. Additionally, we articulate a methodology for designing these experiments, taking into account the nuances of robotics. These findings have been documented in our [published work](https://doi.org/10.1016/j.cogsys.2023.101170). This study presents a series of incremental experiments aimed at assessing cognitive robots based on Jean Piaget's constructivist studies involving children aged 0 to 2 years, alongside other relevant psychology studies.

[Our work](https://doi.org/10.1016/j.cogsys.2023.101170) contributes substantially through a comprehensive literature review delineating crucial facets within developmental robotics projects, highlighting fundamental concepts proposed by Jean Piaget's studies, and summarizing pertinent projects in the field of devRobotics that utilize Piaget's theory as a foundational framework. Moreover, we provide an introductory overview of human sensory development during the sensorimotor stage, essential for a comprehensive understanding of the incremental experiments proposed in our research. We establish a sequence of cognitive experiments to evaluate the cognitive abilities of robots in progressive stages and delineate a methodology for their implementation. Finally, we present a sample case study illustrating the application of the proposed methodology in one of the experiment sets.

## Marta Humanoid Robot
For this preliminary experiments, we choose the [Marta humanoid robot](http://sistemaolimpo.org/midias/uploads/e6d5d0a492bae57e6aed09c99f816152.pdf) in [CoppeliaSim](https://www.coppeliarobotics.com/), with an analogy of sensorimotor development of children during the 1st sensorimotor substage proposed by [Jean Piaget](https://doi.org/10.1037/11494-000). 

Marta is seated in a small delimited space and a wide view of her surroundings. An arena was delimited outside this first space, and colored blocks (blue and green) were randomly distributed. The Pioneer P3DX, which will not have cognitive algorithms implemented, was used as a mobile distractor. Marta's goal is to track the Pioneer robot as it moves through the environment.

<figure>
  <img src="{{'assets//figures/Marta/marta_comBratemberg_back.png' | relative_url }}" alt="Scene2" style="width:80%">
  <figcaption>Scene: Marta in environment with Pioneer and blocks</figcaption>
</figure>


### Environment characteristics
In the 1st and 2nd substages, Marta's action space has 10 actions, that can be performed to move its neck motors or a virtual actuator, called a fovea, which acts as the movement of the eyes. In the 3rd substage, Marta's action space has 15 actions, that can be performed to move its neck motors or a virtual actuator, called a fovea, which acts as the movement of the eyes, and use your attentional mechanism to direct your attention and make decisions. The observation space is an array of 256 elements, corresponding to the salience map acquired by the agent through the attentional system of the CONAIM model. 

<figure>
  <img src="{{'assets//figures/Marta/Plan_Marta_Chart-Quali_Ações_Marta.png' | relative_url }}" alt="Marta's action space" style="width:80%">
  <figcaption>Marta's action space. 1st and 2nd substages: AM0 - AM13; 3rd substage: AM0 - AA2.</figcaption>
</figure>


### Rewards
The following is given to the agent: 
i) +1 reward for each new data inserted in procedural memory; 
ii) +1 for holding or directing an actuator (motor or virtual) to the attention winner of the attencional cycle; 
iii) -10 if the agent falls or exceeds the limits of physical actuators, or if the agent has no saliences in its attentional cycle for several iterations. 


### Final state
 Each episode ends when one of the following conditions is reached: 
i) the agent reached the maximum number of steps/actions (500); 
ii) the robot falls over or exceeds the limits of its motorized actuators;
iii) the robot has no saliences for several iterations. 

<figure>
  <img src="{{'assets//figures/Marta/Plan_Marta_Chart-Quali_Recompensas.png' | relative_url }}" alt="Marta's rewards" style="width:80%">
  <figcaption>Marta's rewards</figcaption>
</figure>



The performance of the procedural constructive learning mechanism based on deep reinforcement learning was evaluated across three substages of the sensorimotor period. Our constructive agent utilized a modified version of the DQN algorithm with radial basis functions (RBFs) as activation functions with a constructive mechanism that allows it to add neurons to its last hidden layer and to add new layers. To simplify the internal neural network architecture, we initialized it with three layers: an input layer, a hidden layer with a single neuron, and an output layer.

In order to assess the effectiveness of our constructive agent, we compared its performance with two other agents. One of them, called DQN-RBF, utilized the three layer modified version of the DQN algorithm with radial basis functions (RBFs) as activation functions, but without a constructive mechanism. The other agent, called Tabular, employed a cognitive-attentional algorithm developed in [(Rossi, 2022)](http://hdl.handle.net/11449/214316) [(Rossi et. al., 2022)](https://doi.org/10.5753/wtdr_ctdr.2022.227371), utilizing the RL Q-Learning algorithm. Due to limitations in the available computational resources, the Tabular agent required a preprocessing step to reduce the dimensionality of its states. We applied a *MaxPool* operator with a 4x4 kernel and a stride of 4 over the saliency map ($\mathcal{L}$), resulting in a 4x4 matrix. Each element of this matrix was discretized into two levels based on a threshold, resulting in a state vector of size 65,536 (2^16). 

### Results

#### 1st Substage

 In this substage, our computational implementation focuses on modeling the development of reflex reactions and the learning of cause-effect relationships in spatial and temporal contexts. The process establishes a connection between the sensory and motor systems, enabling procedural learning. Initially, the states and actions have low resolution, resembling the limited muscle control and visual acuity observed in young children. However, the resolution gradually increases through the learning algorithm. It is important to note that intentionality and motivation are not incorporated into the model.  

<figure>
  <img src="{{'assets//figures/results/1st/Number of Actions Performed.jpg' | relative_url }}" alt="Marta's actions 1st" style="width:80%">
  <figcaption>(a) 1st substage - Actions performed with each experiment;</figcaption>
</figure>

<figure>
  <img src="{{'assets//figures/results/1st/Rewards.jpg' | relative_url }}" alt="Marta's rewards 1st" style="width:80%">
  <figcaption>(b) 1st substage - Rewards adquired with each experiment.</figcaption>
</figure>

 Preliminary findings reveal that the constructive agent exhibited notable advantages over the DQN-RBF and the Tabular agent. Specifically, during training in the first substage, the constructive agent exhibited a 21% increase in the number of actions performed over the Tabular agent. The constructive agent received 39.8% more rewards than the DQN-RBF and 184% more rewards than the Tabular agent during training in the 1st substage. However, it is important to note that the constructive agent utilized approximately 39% more memory and required 12.7% more training time on average. In test scenarios, the constructive agent executed 15.32% more actions than the DQN-RBF agent and 58% more actions than the Tabular agent.

The robot possesses bottom-up features such as RGB color channel intensities and relative distance. It can execute motor actions, including maintaining focus, manipulating physical actuators, and controlling a virtual actuator. Initially, the network had only one neuron and one hidden layer. As the network develops and validates its performance, it verifies if it is necessary to insert more neurons  in its last hidden layer and to add new layers. At the end of the epochs in this substage, the network has 6 hidden layers and 510 neurons in its hidden last layer. 

Both agents were trained for 100 epochs in this substage, with a maximum of 500 steps per epoch. Additionally, we conducted 100 epoch tests for both agents. 

#### 2nd Substage 
This implementation presents a computational process aimed at modeling the development of primary circular reactions, which involves establishing connections between the sensory and motor systems in the current substage to facilitate procedural learning of spatio-temporal cause-effect relationships. As the learning process unfolds, it is anticipated that the reflex reactions initiated in the 1st substage will become more consistent in their outcomes. It is hypothesized that gradually adjusting the exploitation rate and exploration rate of the reinforcement learning algorithm could potentially enhance the expression of these behaviors.

<figure>
  <img src="{{'assets//figures/results/2nd/Number of Actions Performed.jpg' | relative_url }}" alt="Marta's actions" style="width:80%">
  <figcaption>(a) 2nd substage - Actions performed with each experiment;</figcaption>
</figure>

<figure>
  <img src="{{'assets//figures/results/2nd/Rewards.jpg' | relative_url }}" alt="Marta's rewards" style="width:80%">
  <figcaption>(b) 2nd substage - Rewards adquired with each experiment.</figcaption>
</figure>

The robot's bottom-up features encompass color channel intensities (RGB) and relative distance. It is capable of executing motor actions such as maintaining focus, manipulating physical actuators, and controlling the virtual actuator (fovea). In this substage, the robot incorporates a curiosity and motivation driver, which enables the reuse of knowledge acquired in the previous substage. This allows the agent to influence the selection and execution of certain actions based on its performance. At the beginning of training in this substage, the neural network of the constructive agent had 6 layers and 510 neurons in its last hidden layer. The agent performed layer and neuron insertions in this substage, reaching 14 hidden layers and 1050 neurons in the last hidden layer at the end of training.


Comparing the constructive agent to the DQN-RBF agent and the Tabular agent in this substage, the constructive agent achieved a 101.9% increase in rewards over the DQN-RBF agent and a 192% increase in rewards over the Tabular agent. In this substage, the constructive agent performed 8% more actions than the DQN-RBF agent and 6% over the Tabular agent. Additionally, the constructive agent utilized, on average, approximately 29% more memory. During testing, the constructive agent performed 31% more actions than the DQN-RBF agent and 62% more actions than the Tabular agent.

 Both agents were trained for 100 epochs in this substage, with a maximum of 500 steps per epoch. Additionally, we conducted 100 epoch tests for both agents. 


#### 3rd Substage
This implementation introduces a computational process aimed at modeling the development of secondary circular reactions, where the agent acquires intentionality to perform actions and deliberately selects them to achieve specific goals. A top-down attention mechanism is employed in this phase to facilitate intentional behavior. The agent's intentionality is simulated by establishing explicit objectives, which redirect the robot's focus externally and enable purposeful actions.

<figure>
  <img src="{{'assets//figures/results/3rd/Number of Actions Performed.jpg' | relative_url }}" alt="Marta's actions" style="width:80%">
  <figcaption>(a) 3rd substage - Actions performed with each experiment;</figcaption>
</figure>

<figure>
  <img src="{{'assets//figures/results/3rd/Rewards.jpg' | relative_url }}" alt="Marta's rewards" style="width:80%">
  <figcaption>(b) 3rd substage - Rewards adquired with each experiment.</figcaption>
</figure>

The robot incorporates both bottom-up features, such as color channel intensities (RGB) and relative distance, and top-down features, including desired color, desired distance, and desired region. It is capable of executing motor actions, such as maintaining focus, manipulating physical actuators, and controlling the virtual actuator. Moreover, the robot can perform attentional actions to direct its focus based on the top-down features. The implementation also incorporates a curiosity and motivation driver in this substage. In this substage, the constructive agent has its internal neural network started with 14 hidden layers and 1050 neurons in the last hidden layer. At the end of training, the constructive agent reaches 30 hidden layers and 1350 neurons in the last hidden layer.

In this substage, when compared to the Tabular agent and the DQN-RBF agent, the constructive achieved 49% more rewards than the DQN-RBF agent and 97% more rewards than the Tabular agent. The constructive agent also performed 12% more actions than the DQN-RBF agent and 22% more actions than the Tabular agent. Additionally, the constructive agent utilized, on average, approximately 29% more memory. During testing, the constructive agent performed 18% more actions than the DQN-RBF agent and 73% more actions than the Tabular agent.


Both agents were trained for 100 epochs in this substage, with a maximum of 500 steps per epoch. Additionally, we conducted 100 epoch tests for both agents. 




# Conclusion

In summation, the experiments and analysis of preliminary results affirm the viability and substantial promise of the proposed schedule outlined in the previous chapter. The results garnered from these experiments suggests that this schedule holds significant potential to advance the forefront of cognitive architectures. These preliminary findings not only validate the feasibility of the proposed approach but also underscore its capacity to stimulate further inquiry and innovation in the field. As such, this research lays a robust foundation for future investigations, aiming to propel the evolution of cognitive architectures toward new horizons of understanding and application. 


# PhD Qualification

* [PhD Qualification Presentation (PT-BR)](quali_video.md)

