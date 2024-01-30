---
layout: default
title: Project Details and Methodology
subtitle: 
---
# Project Details 

The present study introduces a framework designed for the evaluation of cognitive architectures within various cognitive contexts. We aim to provide an open-source framework that can be utilized for the evaluation of different cognitive architectures, such as SOAR and CONAIM, through cognitive experiments and the utilization of mobile robots. This framework is intended to be an integral part of the Cognitive System Toolkit (CST), facilitating collaborative development and its application in diverse scenarios, with different functionalities and cognitive architectures.

Within the scope of this research, we will implement a learning strategy featuring a constructive mechanism rooted in neural networks for procedural learning. This mechanism, capable of incremental learning akin to human sensorimotor development, will be integrated into the cognitive framework employing CST's cognitive tools. This learning mechanism empowers the model to dynamically adapt the structure of its internal neural network, allowing for the creation or modification of elements within its procedural memory to enable the reuse of previously acquired functions or procedures. Moreover, in more intricate scenarios, this mechanism permits the model to combine previously learned elements to form new ones, thus facilitating its ability to adapt to novel situations and augment the complexity of its internal network.

To implement the architectures with a view to executing and evaluating the set of cognitive experiments (proposed by [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257)), we will use mobile humanoid robots. The implementations and ways of analyzing the results are based on the experiments proposed by [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257) for the acquisition of intelligent behaviors in artificial agents, the related literature [(Piaget, 1952)](https://doi.org/10.1037/11494-000) [Lungarella et al. (2007)](https://www.researchgate.net/publication/220233671_Developmental_robotics_A_survey), and adaptations derived from other projects of the work group [(Rossi, 2022)](http://hdl.handle.net/11449/214316) [(Rossi et. al., 2022)](https://doi.org/10.5753/wtdr_ctdr.2022.227371)[(Berto et. al., 2023)](https://doi.org/10.1016/j.cogsys.2023.101170). Humanoid robots will be used to perform the cognitive experiments and validate the architectures.

<figure>
  <img src="{{'assets/figures/Plan_Marta_Chart-quali_stages.png' | relative_url }}" style="width:100%">

</figure>


## Materials

### Robotic Agents

We propose to implement and validate the proposed system with humanoid robots. 

The Marta humanoid robot [(Chenatti et. al., 2018)](http://sistemaolimpo.org/midias/uploads/e6d5d0a492bae57e6aed09c99f816152.pdf), a 1.1 m tall female robot, was physically designed and built by our workgroup. Marta has 25 degrees of freedom, and her head can perform *pitch* and *yaw* movements. Marta is equipped with an RGB-D camera on her head, to inspect the world in three distinct channels of color (R, G and B) and distance information (D).

Other robots, such as the Pioneer P3DX, which will not have cognitive algorithms implemented, can be used as mobile distractors.  

 The Marta robot is equipped with an RGB-D camera and has a virtual actuator, named as "fovea". The environment is distributed with colored blocks and a Pioneer P3DX robot acts as a distractor. 

<figure>
  <img src="{{'assets/figures/Marta/Marta.png' | relative_url }}" alt="(a)" style="width:50%">
  <figcaption>(a) Scene 1: Marta in Table with objects</figcaption>
</figure>

<figure>
  <img src="{{'assets/figures/Marta/marta_comBratemberg_back.png' | relative_url }}" alt="(b)" style="width:50%">
  <figcaption>(b) Scene 2: Marta in environment with Pioneer and blocks</figcaption>
</figure>

<figure>
  <img src="{{'assets/figures/Marta/marta_view.jpg' | relative_url }}" alt="(c)" style="width:50%">
  <figcaption>(c) Marta </figcaption>
</figure>

### Simulation Environment

We aim to perform the experiments on physical platforms to study learning development in robots supported with continual and incremental learning through sensorimotor experimentation. However, to avoid damage to physical models during preliminary experimentation, the cognitive system will first be tested in simulated environments.
The environment for simulating robotic agents chosen to carry out the experiments with humanoid Marta is [CoppeliaSim](https://www.coppeliarobotics.com/), an update of the V-REP simulator. 


### Deeplearning4j - DL4J

The  mechanism for procedural learning based on neural networks implementation will be performed with [Eclipse Deeplearning4j toolkit](https://deeplearning4j.konduit.ai). DL4J is a framework to perform deep learning in the JVM, that allows training java models while interacting with the python ecosystem through a mixture of python execution through cpython bindings, model import support, and interoperability with other runtimes such as *tensorflow-java* and *onnxruntime*. The libraries are fully open source, *Apache 2.0 under open governance on the Eclipse foundation*.

# Methodology

## CONAIM Implementation Scheme

To implement the CONAIM architecture, CONAIM classes will be adapted to perform *bottom-up* and *top-down* attention with the  mechanism for procedural learning, using CST and DL4J tools. The agent's attentional system receives stimuli related to the objectives of each experiment. These stimuli are submitted to the attentional system of CONAIM composed of *bottom-up* and *top-down* mechanisms. The classes that collect sensory data and the mechanisms that make up the attentional system of CONAIM will be implemented for the agent with cognitive tools of CST in language *Java*. 

<figure>
  <img src="{{'assets/figures/Schemes/plan_quali_phd.png' | relative_url }}" alt="CONAIM Implementation Scheme" style="width:100%">
  <figcaption>CONAIM Implementation Scheme</figcaption>
</figure>

## SOAR Implementation Scheme

To implement the SOAR architecture, SOAR classes will be adapted to perform with [CST Bindings](https://github.com/CST-Group/cst-bindings). CST Bindings allows to use SOAR rules with Java classes. The classes that collect sensory data will be implemented for the agent with cognitive tools of CST in language *Java*. 

<figure>
  <img src="{{'assets/figures/Schemes/marta_soar.png' | relative_url }}" alt="SOAR Implementation Scheme" style="width:100%">
  <figcaption>SOAR Implementation Scheme</figcaption>
</figure>

## Analysis Of Results

The primary objective of this study is to establish a framework to evaluate cognitive architectures within the context of developmental robotics. This proposed framework aims to evaluate cognitive agents to determine their capacity for continuous learning while avoiding catastrophic forgetting. Additionally, it seeks to evaluate their adeptness in conducting increasingly complex cognitive experiments and optimizing both memory utilization during processing and the time expended at each stage of training. In pursuit of this objective, the subsequent analysis of results is proposed:

- **Cognitive Analysis**: the architectures' modules that are activated and used during agents' learning and during their validation will be analyzed according to the proposes of  [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257) and compared with propositions from cognitive psychology for human development, in particular, the studies of [(Piaget, 1952)](https://doi.org/10.1037/11494-000);

- **Continuous Learning**: it will be verified whether the proposed methodology provides the agents the ability to learn new procedures, at different times, without forgetting previously learned procedures. Specifically, the agents' procedural memory, which stores all learned procedures, will be continuously checked;

- **Cognitive Experiments**: the agents' performance will be verified when executing the proposed cognitive experiments, with the evaluation criteria proposed by [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257). In addition, comparisons will be made with other agents that do not have cognitive architectures implemented, through the analysis of the obtained rewards and the maximum number of actions performed by the agents during the execution of the cognitive experiments;

- **Memory And Training Step Time Optimization**: the memory used and the time elapsed at each step during agents learning and during their validation will be continuously checked. Comparisons will be made with other agents that do not have cognitive architectures implemented.

## Project Schedule

This section presents the schedule for the implementation of this research project. We propose the following activities:

**(*Done*) A1. Literature Review:** Continuous process of literature verification, base bibliographies and new related works. Works from the implementation areas (devRobotics, Deep Learning, Cognitive Architectures) and works from human psychology will be analyzed, in order to adapt new cognitive abilities in the used robots.

**(*Done*) A2. Constructive Learning Mechanism Modeling:** We developed a constructive learning mechanism. This mechanism will be extended to agregate new adaptive methods. The constructive learning mechanism will be modeled to fulfill all the needs of humanoid agents.

**(*In progress*) A3. System Implementation:** The cognitive systems will be implemented with cognitive modules of CST.

**(*In progress*) Design The Experiments:** The cognitive experiments will be modeled according to the parameters and validation methods proposed by [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257), the related literature [(Piaget, 1952)](https://doi.org/10.1037/11494-000)[Lungarella et al. (2007)](https://www.researchgate.net/publication/220233671_Developmental_robotics_A_survey) and adaptations derived from other projects in our work group [(Rossi, 2022)](http://hdl.handle.net/11449/214316) [(Rossi et. al., 2022)](https://doi.org/10.5753/wtdr_ctdr.2022.227371).

**(*To do*) A5. Architectural Refinements:** Continuous process of improvement in the architectures according to obtained results.

**(*To do*) A6. Implement The Experiments:** Implementation of cognitive experiments with mobile robots to verify the proposed architectures' performance.

**(*To do*) A7. Perform The Tests And Evaluate Results:** Perform tests to analyze what was proposed in each cognitive experiment and evaluate the results according to the defined criteria.

**(*To do*) A8. Implement The Cognitive Architectures Evaluation Framework:** With the implementations of the chosen architectures, the framework will be implemented to access the architectures and validate their performance with cognitive experiments.

**(*To do*) A9. Implement RESTful API For The Cognitive Architectures Evaluation Framework:** With the implementation of the framework for validating chosen architectures, the RESTful API will be implemented to access the tool.

**(*To do*) A10. Implement Online Access To The Cognitive Architectures Assessment Framework:** With the implementation of the framework for validating chosen architectures, online access to the tool will be implemented.

# PhD Qualification

* [PhD Qualification Presentation (PT-BR)](https://drive.google.com/file/d/10oMXmbGDphLCk4LO8JjkqT2qnDOpHyaU/view?usp=sharing)


