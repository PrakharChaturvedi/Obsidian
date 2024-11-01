## *Heuristic Search* :
- Heuristic search is an important concept in the field of artificial intelligence and computer science. It refers to a search algorithm that uses heuristics or rules of thumb to guide its search through a problem space.
- Heuristics are domain-specific techniques that provide a way to estimate the "goodness" or optimality of different paths, states, or solutions in a search problem. The goal of heuristic search is to find solutions efficiently by focusing on more promising areas of the search space.
- Youtube video link : [https://www.youtube.com/watch?v=5F9YzkpnaRw&t=386s]
- Example :
	- Initial State 
		 2 8 3 
		 1 - 4 
		 7 6 5
	- Final State
		1 2 3 
		8 - 4 
		7 6 5
	- Manhattan distance 
		- The Manhattan distance heuristic measures the sum of the distances each tile is from its desired position. 
		- Manhattan Distance = |1-1| + |2-2| + |3-3| + |8-2| + |7-3| + |6-4| + |5-5| = 14
	- Euclidian distance 
		- It is used to find the shortest distance between 2 nodes
		- Euclidian distance = Root[(x2-x1)^2 + (y2-y1)^2]

## *A* * *Algorithm* :
- Also known as informed search, it is a admissible algorithm which means optimal solution is confirmed.
- We use the equation -> f(N) = g(n)+h(n), where g(n) = Actual cost from start node to n
	   h(n) = Estimate cost from n to goal node.
- Time and space complexity  = O(b^d), where b -> branch factor and d -> depth  
- Youtube link : https://www.youtube.com/watch?v=tvAh0JZF2YE&t=16s
- Example :      ![[Pasted image 20231117005715.png]]

- Underestimate and overestimate of A* algorithm
	- <font color="#ffc000">h(n) => estimated value, h*(n) => actual value</font> 
	- <font color="#92d050">Underestimate</font> : h(n) <= h*(n)
		- When estimated cost <= actual cost, so will you move to the next node?
	- <font color="#92d050">Overestimate</font> : h(n) >= h*(n) 
		- When estimated cost >= actual cost, so will you move to the next node?
	- In case of underestimation, there is a guarantee that you are going to find optimal answer while in case of overestimation it's not a compulsion of finding an optimal answer.  

## *AO* * *Algorithm* :
- It also works on BFS just like A* algorithm, while A* always gives optimal solution if we work on underestimation while AO* has no guarantee that it will give optimal solution.  
- In this algorithm we break the problem into smaller pieces and then find the solution. Process is also called <font color="#ffc000">Problem decomposition</font>. 
- AND/OR graph is a specialized graph, which we use in AO* algorithm.
- AO* does not explore all the solutions paths once it gets a solution.
- Example :
- ![[Pasted image 20231117015831.png]]

## *Hill Climbing Algorithm*
- It is a local search algorithm which continuously moves in the direction of increasing elevation/value to find the peak of the mountain or best solution to the problem. It terminates when it reaches a peak value where no neighbor has a higher value.
- Youtube video -> [https://www.youtube.com/watch?v=3SiWtAnUROs]
- No back tracking. 
- Example : ABCD to DCBA 
- Generate and Test variant.
- Greedy approach.
- Problems with hill climbing algorithm :
	- Local maximum : 
		-  A local maximum is a peak state in the landscape which is better than each of its neighboring states, but there is another state also present which is higher than the local maximum.![[Pasted image 20231117123808.png]]
	- Plateau/Flat maximum
		- A plateau is the flat area of the search space in which all the neighbor states of the current state contains the same value, because of this algorithm does not find any best direction to move. A hill-climbing search might be lost in the plateau area.![[Pasted image 20231117123835.png]]
	- Ridge
		- A ridge is a special form of the local maximum. It has an area which is higher than its surrounding areas, but itself has a slope, and cannot be reached in a single move.![[Pasted image 20231117123858.png]]


## *Knowledge Representation in AI*
- Knowledge is knowing about the things, the facts and about commonsense reasoning. It consists of facts, concepts and rules. 
- To solve AI problems, we needs both a large amount of knowledge and some mechanisms for manipulating that knowledge to create solutions to new problems.
- *Knowledge Representation is a study of how knowledge is actually picturized and how effectively it resembles the representation of knowledge in human brain.*
- Different approaches of knowledge representation 
	- Representation adequacy
		- The ability to represent all of kinds of knowledge that are needed in that domain.
	- Inferential adequacy
		- The ability to manipulate the representational structures in such a way as to derive new structures corresponding to new knowledge inferred from old.
	- Inferential efficiency
		- The ability to incorporate into the knowledge structure additional information that can be used to focus the attention of the inference mechanisms in the most promising directions.
	- Acquisitional efficiency
		- The ability to acquire new information easily. The simplest case involves direct insertion, by a person, of new knowledge into the database.

### Semantic net :
- In Semantic networks, we can represent our knowledge in the form of graphical networks. This network consists of nodes representing objects and arcs which describe the relationship between those objects.

## *Constraint Satisfaction Problem*
- Way of representation is quite different, we represent each problem with *V,D and C*.
	- V -> Set of variables {v1, v2, v3, ......vn}
	- D -> Set of domains {D1, D2, D3, .......Dn} -> one for each variable.
	- C -> Set of constraints that specify allowable combination of values. 
		- Ci = (scope, rel), example : C1 = ((V1,V2) , (V1 != V2))
		- Here scope is set of variables that participate in a constraint and rel is relation that defines the values that variables can take.  
	- No 2 letters have same value, sum of digits must be as shown in problem, there should only be one carry forward.
	- Example : 
		- CP + IS + FUN = TRUE
		- Solution : 
			    C P | 23
			    I S | 74
			+F U N | 968
		     *T R U E* | 1065
		- T -> 1 as left most is always 1
		- Now F has to be 9 to give a carry to T for it to be 1 so, F -> 9
		- And so on.... uk prakhar how to solve it 

## <font color="#ffc000">Prolog</font>  
- Prolog is **a powerful and flexible programming language that's well-suited for developing logic-based artificial intelligence applications**.
- Unlike many other programming languages, Prolog is intended primarily as a declarative programming language. In prolog, logic is expressed as relations (called as Facts and Rules).
- Core heart of prolog lies at the **logic** being applied. Formulation or Computation is carried out by running a query over these relations.
## <font color="#ffc000">Resolution</font> 
- In the field of Resolution In Artificial Intelligence, resolution refers to **a method used to derive logical conclusions from a set of premises**. The resolution method is widely used in automated theorem proving, where it is applied to prove or disprove theorems using logical reasoning.

## <font color="#ffc000">Propositional Logic</font>
- Proposition means sentence/statement. Logic is argument
- Proposition can be either true or false, not both.
- A sentence should be both Syntactically (Atomic or Complex) and Semantically correct.
- It consist of 5 symbols :
	- -  Negation (today is not Friday) [Makes sentence false] 
	- ∨  Disjunction (you should watch tv or eat at same time) [OR] 
	- ∧  Conjunction (he wears pink and he is gay!) [AND]
	- ->  if then (if monkey pass then monkey happy) [If-then]
	- <-> iff (I will go to mall iff I have to do shopping) [if and only if]

## <font color="#ffc000">Predicate</font>
- A predicate is an expression of one or more variables determined on some specific domain. A predicate with variables can be made a proposition by either authorizing a value to the variable or by quantifying the variable.
## <font color="#ffc000">Quantifier</font> 
- In AI, a quantifier is a logical operator that expresses the quantity of something. For example, the quantifier "there exists" expresses the existence of something, while the quantifier "for all" expresses the universality of something.
- In AI, there are two main types of quantifiers: universal and existential. 
	- An *universal quantifier* is an operator that returns true if and only if all values in the specified set satisfy the given condition. 
	- An *existential quantifier* is an operator that returns true if and only if at least one value in the specified set satisfies the given condition.
## <font color="#ffc000">Partitioned Semantic Net</font>
- A semantic network is **a knowledge structure that depicts how concepts are related to one another and illustrates how they interconnect**. Semantic networks use artificial intelligence (AI) programming to mine data, connect concepts and call attention to relationships.