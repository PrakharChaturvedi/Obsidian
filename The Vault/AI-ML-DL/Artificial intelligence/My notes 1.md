Tags : #Ai-ML-DL
## *What is AI?*
- **Artificial intelligence** leverages computers and machines to mimic the problem-solving and decision-making capabilities of the human mind.
- Artificial intelligence is **the science of making machines that can think like humans**. It can do things that are considered "smart". AI technology can process large amounts of data in ways, unlike humans. The goal for AI is to be able to do things such as recognize patterns, make decisions, and judge like humans.
## *Turning Machine* :
- The Turing Test is a method of inquiry in artificial intelligence (AI) for determining whether or not a computer is capable of thinking like a human being. The test is named after Alan Turing, the founder of the Turing Test and an English computer scientist, cryptanalyst, mathematician and theoretical biologist.
  
- Turing proposed that a computer can be said to possess artificial intelligence if it can mimic human responses under specific conditions. The original Turing Test requires three terminals, each of which is physically separated from the other two. One terminal is operated by a computer, while the other two are operated by humans.

- During the test, one of the humans functions as the questioner, while the second human and the computer function as respondents. The questioner interrogates the respondents within a specific subject area, using a specified format and context. After a preset length of time or number of questions, the questioner is then asked to decide which respondent was human and which was a computer.

- The test is repeated many times. If the questioner makes the correct determination in half of the test runs or less, the computer is considered to have artificial intelligence because the questioner regards it as "just as human" as the human respondent. 
## *Types of AI* :
- Narrow/Weak AI 
	- Refers to artificial intelligence systems that are designed and trained for a specific task or a limited set of tasks.
	- Example : Alexa, Google Assistance, NLP, etc.
- General/Strong AI 
	- Form of artificial intelligence that possesses human-like cognitive abilities. Unlike Narrow AI, which is specialized in performing specific tasks, General AI would have the capacity to understand, learn, and apply knowledge across a broad spectrum of tasks and domains in a manner similar to human intelligence.
- Super AI
	- It's possible that you are referring to "Superintelligence," which is a concept that has been discussed in the context of advanced AI systems.
	- Superintelligence refers to an AI system that surpasses human intelligence in a broad and general sense. It would have the ability to perform intellectual tasks at a level that is not only equivalent to but significantly superior to the cognitive abilities of the most intelligent humans.
## *Agents* :
- In the context of artificial intelligence (AI), an "agent" is a fundamental concept used to describe a system or entity that can perceive its environment, make decisions, and take actions to achieve specific goals. Agents are a key part of many AI systems and can be designed to operate in a wide range of applications and environments.
- Types of agents :
	-  **Simple Reactive Agents:** These agents make decisions based solely on the current state of the environment and do not consider past or future states. They are typically used for straightforward tasks.
	- **Model-Based Agents:** These agents maintain an internal model of the environment and use it to plan and make decisions. They can consider future consequences of their actions.
	- **Goal-Based Agents:** These agents have explicit goals and objectives, and they make decisions that are aimed at achieving those goals.    
	- **Learning Agents:** These agents use machine learning techniques to improve their performance over time through experience and data.
## *State based search* :
- State-based search is a fundamental concept in artificial intelligence and computer science, particularly in the field of search algorithms. It refers to the process of searching through a space of states to find a solution to a problem. State-based search is commonly used in various AI applications, including problem-solving, planning, robotics, and games.
- The goal of state-based search is to find a sequence of actions or operators that, when applied to the initial state, lead to a goal state. The search algorithms explore the state space systematically or heuristically, and they aim to find a solution while minimizing the computational resources (time and memory) required.
## *Blind Search*
- Blind search, also known as an uniformed search, is a searching algorithm used to traverse or explore a graph or a tree without any knowledge about the problem other than its structure. One common type of blind search algorithm are BFS, DFS, etc.
## *BFS* :
- It is an algorithm used for traversing or searching tree and graph data structures. It explores all the neighbor nodes at the present depth prior to moving on to nodes at the next depth level. In other words, it visits all nodes at a particular depth level before proceeding to the next level.
- The basic steps of BFS are as follows:
	1. Start with the initial or source node.
	2. Add this node to the queue and mark it as visited.
	3. While the queue is not empty, do the following: 
		 a. Remove the node at the front of the queue (the current node). 
		 b. Visit and process the current node. 
		 c. Add all unvisited neighbors of the current node to the queue and mark them as visited. 

BFS continues this process until the queue is empty, meaning all reachable nodes have been visited and processed. The order in which nodes are visited reflects a breadth-first exploration of the graph or tree.
## *DFS* :
- Depth-First Search (DFS) is an algorithm used for traversing or searching tree and graph data structures. Unlike Breadth-First Search (BFS), which explores all neighbor nodes at the current depth before moving to the next level, DFS explores as far down a branch as possible before backtracking.
- The basic steps of DFS are as follows:
	1. Start with the initial or source node.
	2. Visit and process the current node.
	3. Explore one of the unvisited neighbors of the current node.
	4. Repeat steps 2 and 3 for the newly selected node.
	5. When there are no unvisited neighbors, backtrack to the previous node and repeat steps 2 and 3 until all nodes are visited.
- DFS can be implemented using either a recursive approach or an iterative approach with a stack. In the recursive approach, the algorithm's call stack implicitly acts as the "stack" to keep track of nodes to visit.