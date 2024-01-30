---
layout: default
title: Literature Review
subtitle: 
---

#  Literature Review
## Developmental Robotics

Developmental Robotics, also known as epigenetic robotics or "devRobotics," is a multidisciplinary field that combines theories from developmental psychology, neuroscience, biology, and linguistics to create adaptable robots capable of navigating complex and unpredictable environments [(Lungarella et. al., 2007)](https://doi.org/10.1080/09540090310001655110). It utilizes formalized and extended versions of these theories to develop control architectures for robots.

The emergence of Developmental Robotics stems from the demand for robots that can perform tasks requiring human-level intelligence in challenging environments by adapting and evolving their behavior. Models and experiments in this field draw inspiration from the principles and mechanisms observed in early human development, notably in Piaget's experiments, where robots exhibit cognitive abilities similar to those seen in children [(Piaget, 1952)](https://doi.org/10.1037/11494-000). Piaget's work emphasizes the incremental nature of human cognitive development [(Cangelosi & Schlesinger, 2014)](https://mitpress.mit.edu/books/developmental-robotics).


### Piaget's Theory
Developmental Robotics draws inspiration from the influential theories of Jean Piaget, a Swiss psychologist known for his theory of genetic epistemology, which explores the relationship between human biological and cognitive processes, and the development of complex behaviors [(Piaget, 1952)](https://doi.org/10.1037/11494-000). Central to Piaget's theory are schemas, which are mental structures that aid in the interpretation of concepts and understanding of the environment. As cognitive processes become more sophisticated, new schemas emerge, leading to more complex and adaptive behavior in response to the environment [(Piaget, 1952)](https://doi.org/10.1037/11494-000).

According to Piaget, **adaptation** or **learning** involves the adjustment of cognitive structures to the environment through the processes of **assimilation** and **accommodation** [(Cook & Cook, 2005)](https://psycnet.apa.org/record/2004-19883-000). **Assimilation** involves using existing mental structures to interpret experiences and make decisions, while **accommodation** adjusts existing schemas in response to new information [(Piaget, 1952)](https://doi.org/10.1037/11494-000). These processes are complementary and occur simultaneously, enabling individuals to effectively handle new situations by modifying existing structures or creating new ones [(Piaget, 1952)](https://doi.org/10.1037/11494-000).

Piaget identified circular reactions as a result of assimilation, which involve repetitive cycles of actions that have been acquired or are in the process of acquisition [(Piaget, 1952)](https://doi.org/10.1037/11494-000). Circular reactions occur when individuals rediscover or repeat actions that lead to satisfying outcomes, allowing them to reproduce desired results that were initially discovered by chance. Piaget distinguished three types of circular reactions: primary, secondary, and tertiary [(Piaget, 1952)](https://doi.org/10.1037/11494-000).

In the **primary circular reactions**, behaviors stem from reflexes and involve the coordination of sensory and motor activities, contributing to the development of new schemas [(Piaget, 1952)](https://doi.org/10.1037/11494-000). 
**Secondary circular reactions** emerge as purposeful behaviors directed towards external results rather than the baby's body [(Piaget, 1952)](https://doi.org/10.1037/11494-000). 
**Tertiary circular reactions** represent an extension of the secondary circular reactions and involve the exploration of new experiences through trial and error, as individuals attempt to absorb new information in familiar situations [(Piaget, 1952)](https://doi.org/10.1037/11494-000).

Piaget's analysis of cognitive development in children led to the identification of four distinct stages: the sensorimotor stage, preoperational stage, concrete operational stage, and formal operational stage [(Piaget, 1952)](https://doi.org/10.1037/11494-000). During these stages, Piaget observed children's abilities to manipulate objects, their curiosity, and their exploration of sensory stimuli, such as light and sound. 

The **sensorimotor stage**, lasting from birth to around two years of age, involves the coordination of sensations and motor behaviors as infants perceive and act upon the world [(Piaget, 1952)](https://doi.org/10.1037/11494-000). Mental functions during this stage are primarily based on innate reflexes and instinctual tendencies, gradually evolving to more refined skills and a developing understanding of reality [(Wood et. al., 2011)](https://resources.saylor.org/wwwresources/archived/site/wp-content/uploads/2011/07/psych406-5.3.2.pdf). Piaget described the sensorimotor stage in six substages: use of reflexes, primary circular reactions, secondary circular reactions, coordination of secondary schemas, tertiary circular reactions, and mental combinations [(Piaget, 1952)](https://doi.org/10.1037/11494-000).

In summary, Developmental Robotics integrates Piaget's theories of cognitive development and the concept of schemas to design and develop adaptable robot control architectures. These architectures aim to replicate the incremental and sequential nature of human cognitive development, allowing robots to learn and adapt to complex environments.  

By integrating Piaget's theories and concepts, Developmental Robotics aims to create intelligent robots capable of autonomous and sophisticated behavior in complex environments.

Drawing inspiration from Piaget's work in cognitive development, this project seeks to design robot control architectures that exhibit adaptive learning and the incremental nature of human cognition. This interdisciplinary approach fosters the development of robots that can learn, adapt, and thrive in real-world scenarios.

### Berto's Cognitive Experiments

In order to establish standardized approaches for investigating the evolution of learning mechanisms in robots within the field of developmental robotics, [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257) and [(Berto et. al., 2023)](https://doi.org/10.1016/j.cogsys.2023.101170) conducted studies on cognitive functions to identify the necessary components for validating cognitive architectures in this context. Drawing on Piaget's research on the sensorimotor period [(Piaget, 1952)](https://doi.org/10.1037/11494-000), the [Bayley Child Development Scale](https://doi.org/10.1007/978-0-387-79061-9_295), literature describing evaluation scenarios for infant learning development, and the parameters and levels of the [ConsScale](https://www.conscious-robots.com/consscale/index.html), [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257) and [(Berto et. al., 2023)](https://doi.org/10.1016/j.cogsys.2023.101170) proposed computational approaches to incorporate human behavior into robots and analyze artificial cognitive development. The experiments were classified based on the specific skills intended for the agent's learning.

To bridge Piaget's theory with cognitive models and structures, [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257) and [(Berto et. al., 2023)](https://doi.org/10.1016/j.cogsys.2023.101170) introduced an analogy to Piaget's schemas within the framework of sensorimotor stage development [(Piaget, 1952)](https://doi.org/10.1037/11494-000). [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257) utilized the concept of "cognit" to model memory processing elements, incorporating an evaluation level. The concept of "cognits" captures the following characteristics within Piaget's sensorimotor stage:

* **1st Substage (Use of Reflexes):** This substage involves the creation of innate cognits, encompassing actions, states, and learning mechanisms;

* **2nd Substage (Primary Circular Reactions):** During this substage, cognits are created and adapted based on functions rather than intentions;

* **3rd Substage (Secondary Circular Reactions):** Cognits are created and adapted to form plans, goals, and intentions;

* **4th Substage (Coordination of secondary schemes):** reuse and generalization of plans. Learn the concept of object permanence;

* **5th Substage (Tertiary Circular Reactions):** exploration of *Affordances*. *Affordances* are qualities of objects that allow identifying their functionality without the need for prior explanations, occurring intuitively or based on previous experiences [(Colombini, 2017)](https://dx.doi.org/10.1109/JSYST.2015.2499304). The greater the *affordance* of an object, the better the identification of its use;

* **6th Substage (Mental combinations):** realization of imagination and mental simulation.


By aligning the concept of cognits with Piaget's substage development, [(Berto, 2020)](https://repositorio.unicamp.br/acervo/detalhe/1129257) aimed to establish a closer connection between Piaget's theory and computational models, facilitating the analysis of cognitive processes and promoting artificial cognitive development. These advancements contribute to the ongoing exploration of developmental robotics and its potential for creating adaptive and intelligent robotic systems.

Berto's classification of experiments based on specific skills intended for the agent's learning served as a valuable reference for designing and evaluating our cognitive experiments with mobile humanoid robots. This allowed us to capture the incremental nature of human learning, similar to Piaget's substage development.



## Cognitive Architectures

The cognitive revolution [(Harari, 2011)](https://edisciplinas.usp.br/pluginfile.php/4899892/mod_resource/content/2/Sapiens%20Uma%20Breve%20História%20da%20Humanidade.pdf) has spurred computational investigations into various aspects of human mental processes, resulting in the development of cognitive architectures and structures. These frameworks aim to facilitate the study of the human mind, encompassing not only its behavioral aspects but also the underlying cognitive processes that shape and influence behavior [(Harris, 2006)](https://onlinelibrary.wiley.com/doi/10.1002/0470018860.s00559). Over the past few decades, several standard cognitive models have been proposed, employing different methods and approaches to achieve functionality and implementation [(Simões et. al., 2017)](https://doi.org/10.1109/JSYST.2015.2498542).


[(Kotseruba et al, 2020)](http://jtl.lassonde.yorku.ca/project/cognitive_architectures_survey/bib_html/index.html) describe cognitive architectures as systems capable of reasoning across various domains, incorporating multiple perspectives, adapting to new circumstances, and possessing introspective abilities. The authors note that the term "cognitive architecture" is not limited to specific graphical or algorithmic proposals, but rather encompasses a range of approaches that manipulate these representations. [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005) define cognitive architectures as general-purpose control systems based on scientific theories of cognition in humans and animals. These architectures comprise a combination of modules responsible for implementing various cognitive functions such as perception, attention, memory, thinking, and learning.

[(Vernon, 2016)](https://doi.org/10.1016/j.bica.2016.10.004) defines a cognitive architecture as a computational model that represents cognition by explicitly specifying the set of processes and underlying assumptions upon which the model is based. These assumptions can be derived from biological or psychological sources, philosophical arguments, or working hypotheses in various disciplines such as neurophysiology, psychology, or artificial intelligence. According to [(Laird, 2008)](https://www.researchgate.net/publication/221328941_Extending_the_Soar_Cognitive_Architecture), a cognitive architecture consists of processing units that represent, extract, select, and integrate knowledge, along with memory stores that preserve this knowledge. [(Sun, 2004)](https://doi.org/10.1080/0951508042000286721) characterizes cognitive architectures as essential structures and processes that encompass a broad scope of cognition and behavior across multiple levels and domains. [(Thomson et. al., 2014)](https://www.researchgate.net/publication/268520256_Extending_the_Influence_of_Contextual_Information_in_ACT-R_using_Buffer_Decay) describes cognitive architectures as systems composed of several modules or components working together to produce behavior. These modules encompass knowledge representations, memory systems for content storage, and processes for acquiring and utilizing knowledge.

These advancements in cognitive architectures contribute to the exploration of complex cognitive processes in robots and pave the way for the development of intelligent and adaptive robotic systems. In this project, we aim to develop a systematic framework for the evaluation of cognitive architectures, offering seamless integration with existing models like SOAR, CONAIM, and more. Our system will be designed to learn iteratively from the environment, mimicking the incremental nature of human learning. By integrating elements from the human cognitive system, our approach aimed to achieve machine consciousness and provide insights into reinforcement learning and the acquire of sensorimotor and procedural knowledge.

### CONAIM
The CONAIM model (Conscious Attention-Based Integrated Model) [(Simões et. al., 2017)](https://doi.org/10.1109/JSYST.2015.2498542) draws inspiration from the attentional architecture proposed by [(Colombini, 2017)](https://dx.doi.org/10.1109/JSYST.2015.2499304), with a specific focus on replacing the attentional controller. This model aims to endow an attention-based agent with awareness and the ability to compute over the saliency map, resulting in a significant reduction in the dimensionality of the model's input space. The CONAIM model consists of two main systems: an attentional system and a cognitive system.

The attentional system, as proposed by [(Simões et. al., 2017)](https://doi.org/10.1109/JSYST.2015.2498542), builds upon the selection for perception model introduced by [(Colombini, 2017)](https://dx.doi.org/10.1109/JSYST.2015.2499304). This architecture incorporates various elements from related works and is capable of handling multiple sensory systems, employing multiple processes for feature extraction, decision-making, and learning support [(Colombini, 2017)](https://dx.doi.org/10.1109/JSYST.2015.2499304).

The cognitive system, also presented by [(Simões et. al., 2017)](https://doi.org/10.1109/JSYST.2015.2498542), encompasses memory blocks such as semantic, episodic, procedural, and working memory, as well as performance and individuality modules, which include internal states and body schema. The working memory receives information from the attentional system, specifically the saliency map and sensory memory, and provides information for motivation, emotions, decision-making, performance, and other cognitive processes. The exchange of information between semantic, episodic, and procedural memories and working memory occurs bidirectionally, facilitating a comprehensive information flow [(Simões et. al., 2017)](https://doi.org/10.1109/JSYST.2015.2498542).

Additionally, a set of processes operate in parallel and synchronize with the modules to perform actions on the elements of the cognitive system. The CONAIM model operates under the paradigm that any function or process within the cognitive system can request information from any other module and/or modify the agent's internal states at any given time. Consequently, the flow of information through the decision-making module is not obligatory [(Simões et. al., 2017)](https://doi.org/10.1109/JSYST.2015.2498542).

In our project, we aim to employ the CONAIM model (Conscious Attention-Based Integrated Model) in our framework.  By building upon the CONAIM model and incorporating neural network-based learning, our research aimed to address challenges in reinforcement learning and the acquire of sensorimotor and procedural knowledge. Through this research, we sought to provide insights into achieving machine consciousness in complex environments while overcoming limitations in existing tools and techniques for implementing cognitive architectures.

### SOAR
The SOAR architecture is a cognitive architecture designed to simulate human intelligence and problem-solving processes [(Laird, 2008)](https://www.researchgate.net/publication/221328941_Extending_the_Soar_Cognitive_Architecture). In our project, we also aim to employ the SOAR model in our framework.  
 SOAR models and simulates human cognition, including problem-solving, decision-making, learning, and memory. It stands for "State, Operator, And Result" reflecting its fundamental components:
* **State:** SOAR maintains an internal representation of the current state of the problem or task. This state consists of a set of working memory elements that encode information about the world, goals, and current intentions;
* **Operator:** Operators are rules or procedures that represent potential actions or steps to achieve goals or modify the current state. Operators are encoded in productions, which are conditional statements specifying when to execute a particular operator;
* **Result:** The resulting phase involves the execution of selected operators to modify the state. The system evaluates and selects the most appropriate operator based on its knowledge and the current state.
    
In our project, we also aim to employ the SOAR model (State, Operator, And Result) in our framework. 

### CST
The Cognitive Systems Toolkit (CST) [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005) is a Java-based toolkit designed for constructing cognitive architectures. 
At its core, the CST comprises a collection of fundamental concepts that can be employed in a generalized manner to build any cognitive architecture [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005). Its cognitive functions are represented as classes that can be combined into a parallel set of interaction devices, enabling the creation of multi-agent systems with asynchronous and parallel execution capabilities.

The CST framework revolves around the concept of codelets, which are small pieces of code implemented as asynchronous functions. These codelets execute in parallel, performing simple and well-defined tasks [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005). They represent the major cognitive functions of the system and operate in a constant and cyclical manner, driving the system's behaviors. 
They are organized into groups, where each group corresponds to a cognitive model of a specific cognitive function [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005). The CST toolkit provides default implementations for some of these codelet groups.

Within the CST, each codelet has two inputs: Local (Li) and Global (Gi). The Local input (Li) serves as the default input for information regarding selected memory objects and is typically fixed but can be modified through learning mechanisms [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005). On the other hand, the Global input (Gi) is utilized to access information from the Global Workspace (GW) and is continuously updated through consciousness mechanisms [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005).

**Codelets** in the CST also produce two outputs: Default (O) and Activation Level (A). The Standard output (O) is responsible for modifying or creating new information within the system's memory [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005). The Activation Level output (A) indicates the relevance of the information generated in the Standard output and assists in selecting the information to be employed in the Global Workspace.

A **memory object (MO)** represents a signal or internal representation used, alongside other MOs, by codelets for storing and accessing data. The primary attribute of an MO is its information (I), which is modeled as a generic object in Java and can be represented as a single value, lists, or collections [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005). Each MO also possesses a timestamp (T) indicating its last update and a rating (E) [(Paraense et. al., 2016)](https://dx.doi.org/10.1016/j.bica.2016.07.005).

By utilizing the CST framework and its concepts, we were able to construct and implement cognitive architectures to our framework. The integration of codelets, memory objects, and the parallel execution capabilities offered by the CST allowed us to create a dynamic and flexible cognitive architectures for our project, supporting incremental learning and addressing the challenges of operating in complex environments.


