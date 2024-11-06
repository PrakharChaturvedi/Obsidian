Tags : #Ai-ML-DL
Topics covered: Semantic Net, Frame, Conceptual Dependency, Standard components and Neural network, Expert systems, Script, Knowledge base, Sigmoid, ANN, Node and unit, Understand and Dendral. 

## Semantic Net
- It is a structure for representing knowledge as a pattern of interconnected nodes and arcs.
- It is also define as a graphical representation of knowledge.
- In a semantic net information is represented as a set of nodes connected to each other by a set of labeled arcs, which represent relationships among the nodes.
- Rules of about nodes and arcs, (generally applied rules):
		- Nodes in the semantic net represent either entities, attributes, states or events.
		- Arcs in the net give the relationship between the nodes and labels on the arc specify what type of relationship actually exists.
- Example :   ![[Pasted image 20231211202739.png]]
![[Pasted image 20231211202759.png]]
## Frame
- A frame is a data structure that represents a "snapshot" of the world at a particular moment in time. It contains all of the information that an AI system needs to know about the world in order to make decisions.
- Frames are used extensively in AI systems, especially in those that use artificial neural networks. This is because they provide a way to store and manipulate information in a way that is similar to how the human brain does it.
- Frames are also used in other AI paradigms, such as rule-based systems and decision trees. However, they are not as widely used in these paradigms as they are in neural networks.
- Why use frames?
	- There are many benefits to using frames in AI. Frames provide a structure for representing knowledge that can be used by AI systems to reason about the world. 
	- They can also be used to store and retrieve information from memory, and to make inferences about new situations. Frames can also be used to represent plans and goals, and to generate new actions.
- Types:
	- **Conceptual Frames:** These frames represent abstract concepts or categories. For instance, a "Vehicle" frame might have slots for "make," "model," "color," "speed," etc.
	- **Object Frames:** These frames represent specific instances of objects or entities. For example, an "Car" object frame might inherit from the "Vehicle" conceptual frame and have slots specific to a particular car instance.
	- **Script Frames:** These frames capture sequences of events or actions. A "Restaurant Visit" script frame might have slots for "arrival time," "order placed," "meal served," and "payment made."
	- **Semantic Frames:** These frames represent meanings or concepts within a particular domain. In natural language processing, semantic frames might capture the meaning of words or phrases in context.
- Action frame has the following slots:
		- Action slot: This slot holds information about who is performing the activity
		- Object slot: This slot has information about the item to be operated on.
		- Source slot: Source slot holds information from where the action has to begin.
		- Destination slot: Holds the information about the place where the action has to end.
		- This generates the necessary sub-frames required to perform the operation.  
- Example :
	- "Tweety is a yellow birds having wings to fly"
	- Tweety(
		 (Species  (Value bird))
		 (Color  (Value yellow))
		 (Activity (Value Fly))
		 (Instrument (Wings))
		)

- Example of semantic network:![[Pasted image 20231211184310.png]]
 
## Conceptual Dependency 
- Conceptual dependency is a method of representing statements in a language and word independent form. The CD provide primitive acts which represents the English (or any other language) verbs in simpler structure. 
- There are total 11 primitive acts and whenever an English verb is observed, it is converted to a form containing one or more primitive acts. The representation of a single idea is called conceptualization. 
- The conceptualization connects actors, recipients, objects and instruments by different dependencies. Those dependencies or links are specifically designed to indicate the purpose. 
- Single or double lines indicate strength of the relationship, arrows and their directions indicate dependencies while indicators over the link provides further information. ![[Pasted image 20231211202526.png]]
- Examples: 
	- I gave the man a book 
		- Agent: I
		- Action: give
		- Object: book
		- Recipient: the man
	- John ate ice cream with a spoon
		- Agent: John  
		- Action: eat 
		- Object: ice cream 
		- Recipient: spoon

## Standard components and Neural Network
- Standard Components:
	- **Definition:** Standard components often refer to traditional or classical AI techniques that rely on explicit programming and rule-based systems.
	- **Characteristics:**
	    - **Rule-Based Systems:** These systems use predefined rules and logic to make decisions or perform tasks.
	    - **Symbolic Representation:** Knowledge is represented using symbols and explicit rules.
	    - **Expert Systems:** Systems that emulate the decision-making abilities of a human expert in a particular domain.
	    - **Limited Adaptability:** These systems may lack adaptability and flexibility in handling complex, dynamic environments.
- Neural Networks:
	- **Definition:** Neural networks are a subset of machine learning and are inspired by the structure and function of the human brain. They are a type of computational model that learns patterns from data.
	- **Characteristics:**
	    - **Learning from Data:** Neural networks learn from data through a process of training and adjustment of internal parameters.
	    - **Nonlinear Function Approximation:** They are capable of approximating complex, nonlinear relationships in data.
	    - **Feature Learning:** Neural networks automatically learn relevant features from the input data, reducing the need for manual feature engineering.
	    - **Adaptability:** Neural networks can adapt and generalize well to new, unseen data, making them suitable for a wide range of tasks.
- Key differences:
	- **Programming Paradigm:**
    - Standard components rely on explicit programming, where rules and logic are explicitly defined by developers.
    - Neural networks learn from data, allowing them to generalize patterns without explicit programming.
- **Representation of Knowledge:**
    - Standard components use symbolic representation and rule-based systems to encode knowledge.
    - Neural networks use distributed representations and learn implicit representations of knowledge from data.
- **Adaptability:**
    - Standard components may have limited adaptability and require manual adjustments for changes in the environment.
    - Neural networks are adaptive and can generalize well to new data, making them suitable for a broader range of applications.
- **Task Complexity:**
    - Standard components may struggle with tasks that involve complex, ambiguous, or rapidly changing information.
    - Neural networks excel at handling complex tasks and are particularly effective in tasks like image recognition, natural language processing, and speech recognition.

## Expert Systems
- An expert system is a computer program that is designed to solve complex problems and to provide decision-making ability like a human expert. It performs this by extracting knowledge from its knowledge base using the reasoning and inference rules according to the user queries.
- It is called so because it contains the expert knowledge of a specific domain and can solve any complex problem of that particular domain.
- The performance of an expert system is based on the expert's knowledge stored in its knowledge base. The more knowledge stored in the KB, the more that system improves its performance. One of the common examples of an ES is a suggestion of spelling errors while typing in the Google search box.
- #### Note: It is important to remember that an expert system is not used to replace the human experts; instead, it is used to assist the human in making a complex decision. These systems do not have human capabilities of thinking and work on the basis of the knowledge base of the particular domain.
- Architecture: ![[Pasted image 20231211191619.png]]
	- **Knowledge Base –**  
	    The knowledge base represents facts and rules. It consists of knowledge in a particular domain as well as rules to solve a problem, procedures and intrinsic data relevant to the domain.
	- **Inference Engine –**  
	    The function of the inference engine is to fetch the relevant knowledge from the knowledge base, interpret it and to find a solution relevant to the user’s problem. The inference engine acquires the rules from its knowledge base and applies them to the known facts to infer new facts. Inference engines can also include an explanation and debugging abilities.
	- **Knowledge Acquisition and Learning Module –**  
	    The function of this component is to allow the expert system to acquire more and more knowledge from various sources and store it in the knowledge base.
	- **User Interface –**  
	    This module makes it possible for a non-expert user to interact with the expert system and find a solution to the problem.
	- **Explanation Module –**  
	    This module helps the expert system to give the user an explanation about how the expert system reached a particular conclusion.
- Characteristics:
	- High Performance
	- Understandable
	- Reliable
	- Highly responsive
	- Advising
	- Explanation
	- Interpreting input
	- Predicting result
	- Justifying the conclusion
	- Suggestive alternative options to problems
 - Applications:
	 - Different types of medical diagnosis like internal medicine, blood diseases and show on.
	 - Planning experiment in biology, chemistry and molecular genetics.
	 - Teaching students specialize task.
	 - Diagnosis of a software development project.
	 - Diagnosis of the complex electronic and electromechanical system.
- Examples : 
	- **MYCIN –** One of the earliest expert systems based on backward chaining. It can identify various bacteria that can cause severe infections and can also recommend drugs based on the person’s weight.
	- **DENDRAL –** It was an artificial intelligence-based expert system used for chemical analysis. It used a substance’s spectrographic data to predict its molecular structure.
	- **R1/XCON –** It could select specific software to generate a computer system wished by the user.
	- **PXDES –** It could easily determine the type and the degree of lung cancer in a patient based on the data.
	- **CaDet –** It is a clinical support system that could identify cancer in its early stages in patients.
	- **DXplain –** It was also a clinical support system that could suggest a variety of diseases based on the findings of the doctor.

## Script : 
- A script is a structured representation describing a stereotyped sequence of events in a particular context.
- Scripts are used in natural language understanding systems to organize a knowledge base in terms of the situations that the system should understand. Scripts use a frame-like structure to represent the commonly occurring experience like going to the movies eating in a restaurant, shopping in a supermarket, or visiting an ophthalmologist.
- Components of a script
	- **Entry condition:** These are basic condition which must be fulfilled before events in the script can occur.
	- **Results:** Condition that will be true after events in script occurred.
	- **Props:** Slots representing objects involved in events
	- **Roles:** These are the actions that the individual participants perform.
	- **Track:** Variations on the script. Different tracks may share components of the same scripts.
	- **Scenes:** The sequence of events that occur.
## 1 Markers 
- **Knowledge Base**: A knowledge base refers to a centralized storage of information that an AI system can access and utilize to reason, make decisions, or respond to queries.
- **Sigmoid**: The sigmoid function is a mathematical function that compresses any range of values into a value between 0 and 1.
- **ANN**: ANN stands for Artificial Neural Network. It's a computational model inspired by the human brain's neural structure and designed to simulate how biological neurons work.
- **Node and Unit**: 
	- Node: A node is a fundamental component of a neural network. It's an abstraction representing a computational unit. 
	- Unit: In the context of neural networks, a unit refers to the same concept as a node or neuron. It represents an individual computational element within a neural network.
- **Understand and dendral**: 
	- UNDERSTAND: It was a natural language understanding system developed in the 1970s
	- DENDRAL: It was designed to infer the structure of organic molecules from mass spectrometry data, using a knowledge base of chemical rules and heuristics.
