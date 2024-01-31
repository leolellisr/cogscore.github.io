---
layout: default
title: Introduction
subtitle: 
---
# Introduction

The remarkable progress in the fields of artificial intelligence and deep learning has propelled the need for artificial agents to function effectively in increasingly intricate environments [(LeCun et al., 2015)](https://doi.org/10.1038/nature14539). As the complexity of tasks escalates, the development of cognitive architectures has emerged as a significant avenue of exploration. These architectures propose that attaining machine consciousness demands a harmonized amalgamation of diverse elements mirroring the human cognitive system, encompassing faculties like memory, reasoning, planning, decision-making, learning, motivation, and attention.

<figure>
  <img src="{{'assets/figures/intro1.jpg' | relative_url }}" alt="Human Evolution" style="width:70%">
</figure>

The multi-disciplinary field of developmental robotics draws inspiration from developmental psychology, cognitive science and neuroscience, among other fields to create robots that can learn and develop in similar ways to humans and animals [(Sun, 2004)](https://doi.org/10.1080/0951508042000286721). This cognitive models and architectures require the coordination of a set of mechanisms that depend on each other and aim to reproduce complex behaviors of the human mind in artificial entities [(Thomson et. al., 2014)](https://www.researchgate.net/publication/268520256_Extending_the_Influence_of_Contextual_Information_in_ACT-R_using_Buffer_Decay). 

<figure>
  <img src="{{'assets/img/intro1.png' | relative_url }}" style="width:70%">
</figure>

<figure>
  <img src="{{'assets/img/intro2.png' | relative_url }}" style="width:70%">
</figure>


However, the practical realization of such cognitive architectures has encountered formidable challenges, necessitating specialized computational tools with limited applicability. Moreover, these tools confront constraints related to continuous learning and knowledge capacity. The developmental process within these architectures further imposes substantial data processing requirements, entailing the allocation of substantial memory resources. Addressing these complexities, our previous research during my master's degree featured the integration of attentional, cognitive, and reinforcement learning (RL) modules into a cognitive architecture employing artificial cognitive tools.

<figure>
  <img src="{{'assets/img/intro3.png' | relative_url }}" style="width:80%">
</figure>


In this context, we introduce an innovative system to evaluate cognitive architectures. Our system integrates established models, including SOAR, CONAIM, and more, within a versatile "plug-and-play" framework. This approach unveils a dynamic cognitive architecture playground, enabling online testing and interaction through a RESTful API. Our proposition sets forth a systematic framework for the assessment of cognitive architectures, fostering a harmonious coexistence with existing models. This "plug-and-play" paradigm establishes a cognitive architecture playground, thus expanding the horizons of online testing and interaction. Our trailblazing approach is poised to effectively address the longstanding limitations and challenges inherent in the implementation and evaluation of cognitive architectures, thereby propelling the field of artificial intelligence to new heights.

<figure>
  <img src="{{'assets/img/intro4.png' | relative_url }}" style="width:70%">
</figure>


## Motivation

During my masters [(Rossi, 2022)](http://hdl.handle.net/11449/214316) [(Rossi et. al., 2022)](https://doi.org/10.5753/wtdr_ctdr.2022.227371), a cognitive robot model was designed to investigate which cognitive modules should be present in an agent that can learn incrementally to perform experiments with increasing levels of difficulty. This robot had as a cognitive-attentional algorithm the architecture of CONAIM (*Conscious Attention-Based Integrated Model*) [(Simões et. al., 2017)](https://doi.org/10.1109/JSYST.2015.2498542) implemented with CST (*Cognitive Systems Toolkit*) tools [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005). The agent's procedural learning was performed using a tabular reinforcement learning algorithm, the Q-Learning [(Sutton & Barto, 1998)](https://www.andrew.cmu.edu/course/10-703/textbook/BartoSutton.pdf). The experiments demonstrated the viability of using a cognitive-attentional architecture modeled with cognitive robotics tools, proposed for conscious agents computing on the attentional paradigm. 

<figure>
  <img src="{{'assets/img/intro5.png' | relative_url }}" style="width:70%">
</figure>


However, during the execution of the experiments, we found that the amount of memory used by the tabular learning algorithm exceeded the limits of the machine we used, requiring preprocessing of the data used as states. In addition, the execution time of each training step was too long, resulting in hours of training. The design of the experiments was particularly challenging, and we realized how useful it would be if a predesigned set of canonical experiments was available, each of them focusing on a specific cognitive capability, ordered according to different levels of difficulty. Also, we realized that making changes in the architecture to address shortcomings in a specific capability might break its performance in previous capabilities, which it was proficient in before the modifications. So, after making changes in the architecture, the whole set of experiments might be re-executed in order to validate new improvements.  

In our current work, we introduce a system to evaluate cognitive architectures. Our system integrates established models, including SOAR, CONAIM, and more, within a versatile "plug-and-play" framework. This approach unveils a dynamic cognitive architecture playground, enabling online testing and interaction through a RESTful API. Our proposition establishes a systematic framework for the assessment of cognitive architectures, fostering a harmonious coexistence with existing models. This "plug-and-play" paradigm expands the horizons of online testing and interaction. Our approach is poised to effectively address the longstanding limitations and challenges inherent in the implementation and evaluation of cognitive architectures. 



Within this context, we advocate for the implementation of our system using emerging frameworks specifically designed for the creation of cognitive architectures [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005) and deep learning systems [(DL4J, 2022)](https://deeplearning4j.konduit.ai). This strategic choice is motivated by our aspiration to disseminate our innovative approach to a broader spectrum of knowledge domains, transcending the boundaries of artificial intelligence. This approach encapsulates the essence of our innovative paradigm, with the aim of addressing the limitations and challenges associated with the implementation and evaluation of cognitive architectures while advancing the broader field of artificial intelligence.

<figure>
  <img src="{{'assets/img/intro7.png' | relative_url }}" style="width:70%">
</figure>


In addition to our technical innovations, we extend the exploration initiated during my master's degree [(Rossi, 2022)](http://hdl.handle.net/11449/214316) [(Rossi et. al., 2022)](https://doi.org/10.5753/wtdr_ctdr.2022.227371).  We transition from the conventional tabular learning algorithm of the cognitive architecture to a procedural learning mechanism based on constructive neural networks [(Huang et. al., 2008)](https://doi.org/10.1109/TNN.2008.2004370). This shift is driven by our objective to empower artificial agents to engage in continual learning. By doing so, we enhance their ability to acquire new actions and increase the complexity of their learning processes. This transition is a pivotal aspect of our approach, as it optimizes memory utilization and streamlines the training process, aligning with the core innovation of our work.

Another aspect of our proposal is the incorporation of radial basis functions (RBFs) [(Dash et. al., 2016)](https://doi.org/10.1515/comp-2016-0005) as activation functions within the procedural learning mechanism. This critical choice instills a culture of ongoing learning and effectively mitigates the risk of catastrophic forgetting. Through the adoption of RBFs, we ensure that our system can adapt and expand its knowledge base without erasing previously acquired knowledge [(Parisi et. al., 2019)](https://www.sciencedirect.com/science/article/pii/S0893608019300231). This addresses a fundamental challenge within the field of cognitive architectures.

<figure>
  <img src="{{'assets/img/intro6.png' | relative_url }}" style="width:70%">
</figure>


Moreover, our research extends its scope to encompass the integration of other constructive mechanisms, allowing the utilization of neural networks in various stages of the cognitive cycle. This includes tasks such as the classification of sensory stimuli to determine attentional focus, enriching the overall integration of cognitive architectures.

## Objectives

This work aims to implement a general framework for the automated evaluation of different levels of diverse cognitive capabilities of cognitive architectures. The architectures will be implemented with CST [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005), the Cognitive Systems Toolkit. The strategy is to set an incremental repertoire of experiments (inspired by research in human development) for a simulated robot in the context of *devRobotics*. For these experiments, Piaget's theory of cognitive development and related literature, in particular the experiments proposed by [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257), will be considered as guides to carry out experiments with developed agents and validate implemented modules.

<figure>
  <img src="{{'assets/img/intro8.png' | relative_url }}" style="width:70%">
</figure>


As a bonus, we intend to make available an easy integration tool for composing new configurations of cognitive architecture, using available pieces of software made available in the field of cognitive architectures, including SOAR, CONAIM, and more, providing a versatile "plug-and-play" framework for the composition of new and improved cognitive architectures. This approach unveils a dynamic cognitive architecture playground, enabling online testing and interaction through a RESTful API. Our proposition sets forth a systematic framework for the evaluation of cognitive architectures, fostering a harmonious coexistence with existing models. Our approach is prepared to address the longstanding limitations and challenges inherent in the implementation and evaluation of cognitive architectures.

More specifically, to achieve this goal, we aimed:
* To use the cognitive experiments outlined in Berto (2020) [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257) as a guideline for a canonical set of experiments with increasing cognitive complexities and develop computational implementations of them that might be easily plugged-in to different cognitive architectures, which are meant to be tested;

* Model and implement a framework for evaluate sensorimotor and procedural learning, using cognitive computing tools provided by CST (*Cognitive System Toolkit*) [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005) and deep learning computing tools provided by DL4J (*Deep Learning for Java*) [(DL4J, 2022)](https://deeplearning4j.konduit.ai);

* To integrate established cognitive architectures, including SOAR, CONAIM, and more, within a versatile "plug-and-play" framework, enabling online testing and interaction through a RESTful API; 

* To model and implement a framework for evaluating sensory-motor and procedural learning, using cognitive computing tools provided by CST (*Cognitive System Toolkit*) [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005) and deep learning computing tools provided by DL4J (*Deep Learning for Java*) [(DL4J, 2022)](https://deeplearning4j.konduit.ai);
    
* Execute the proposed experiments with a view to promoting the investigation of the processes involved in cognitive development focused on the field of developmental robotics (devRobotics).

<figure>
  <img src="{{'assets/img/intro9.png' | relative_url }}" style="width:70%">
</figure>


## Justifications

In view of our objectives, and our studies in philosophy [(Castro & Landeira, 2011)](https://www.scielo.br/pdf/prc/v24n4/a21v24n4.pdf), psychology [(Piaget, 1952)](https://doi.org/10.1037/11494-000), neuroscience [(Koch & Greenfield, 2007](https://www.researchgate.net/publication/5917959_How_Does_Consciousness_Happen) and computer science and engineering [(Reggia, 2013)](https://www.sciencedirect.com/science/article/abs/pii/S0893608013000968), we formulated the following hypotheses to justify this work:
* A framework for evaluate cognitive architectures sensorimotor and procedural learning can be implemented using cognitive computing tools provided by CST (*Cognitive System Toolkit*) [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005) and deep learning computing tools provided by DL4J (*Deep Learning for Java*) [(DL4J, 2022)](https://deeplearning4j.konduit.ai);
* A constructive procedural learning mechanism can be implemented with neural networks and radial basis activation functions, in order to promote continual learning, optimize the use of memory and training step time, and avoid catastrophic forgetting;
* An attentional-cognitive artificial system can be implemented with the mentioned mechanism, artificial cognitive tools and deep learning methods to demonstrate procedural learning according to development human cognition theories;
* A cognitive architecture implemented with the proposed mechanism can be trained through reinforcement learning to perform cognitive experiments of increasing difficulty.

## Expected Contributions
As the main contributions of this work, we expect:
* The development and implementation of a general framework for the evaluation of cognitive architectures performance, based on a set of canonical cognitive experiments of increasing difficulty, to demonstrate incremental and continual development;
* Modeling and implementation of a framework to evaluate procedural learning and sensorimotor learning with different cognitive architectures;
* Modeling and implementation of a constructive mechanism for procedural learning, based on neural networks, for incremental and continual learning
* Modeling and implementation of a cognitive-attentional system capable of incremental and continual learning;
* Modeling and implementation of attentional, cognitive and deep learning functions that can be reused in robotic systems;
* Validation of the proposed system modules with a cognitive-attentional agent in cognitive experiments of increasing difficulty, to demonstrate incremental and continual development.

# PhD Qualification

* [PhD Qualification Presentation (PT-BR)](https://drive.google.com/file/d/10oMXmbGDphLCk4LO8JjkqT2qnDOpHyaU/view?usp=sharing)


