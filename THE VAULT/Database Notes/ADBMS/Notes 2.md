## Transactions 
- A **transaction** is a sequence of operations that interact with the database, acting like a single unit of work. It either completes all its actions successfully or none at all.
- #### Key Operations
	- **Read (X)**: This operation gets the value of data item X from the database.
	- **Write (X)**: This operation saves the value of data item X back to the database.
- #### States of a Transaction
	- **Active**: The transaction is currently running.
	- **Partially Committed**: The last step has been completed, but not yet fully committed.
	- **Failed**: Something went wrong during execution.
	- **Aborted**: The transaction was canceled, and changes were rolled back.
	- **Committed**: The transaction completed successfully and changes are saved.
- #### Example of a Transaction
	- For instance, transferring $100 from account A to account B involves:
		1. Reading the balance of account A.
		2. Subtracting $100 from A.
		3. Writing the new balance back to A.
		4. Reading the balance of account B.
		5. Adding $100 to B.
		6. Writing the new balance back to B.
	- During this process, the database cannot be queried, as it might show incorrect data.
- #### Example of Concurrent Transactions
	- Two transactions can operate at the same time (concurrently):
		- **Transaction T** takes $100 from A to B.
		- **Transaction T'** takes 10% of A and adds it to B.
	- If executed one after the other (serial execution), they maintain the total money (A + B remains the same). However, if they run at the same time without proper control, they could create an inconsistency, like showing more money than exists.
- #### Issues with Concurrent Execution
	- In some cases, concurrent execution can lead to problems:
	- If T reads A, modifies it, and before writing, T' also reads and modifies A, the final results can end up incorrect, creating extra money that wasn't actually there.
## ACID Properties
- Transactions are designed to follow four key properties known as ACID:
	1. **Atomicity**: All parts of a transaction must complete; if one fails, none do.
	2. **Consistency**: Transactions should not violate database rules, ensuring data remains valid.
	3. **Isolation**: Transactions running at the same time should not interfere with each other. It should seem like each transaction is the only one executing.
	4. **Durability**: Once a transaction is completed, its changes are permanent, even if the system crashes.

## Fundamental Operators
- **Selection(σ):**** It is used to select required tuples of the relations.
- **Projection(π):*** It is used to project required column data from a relation.
- **Union(U):*** Union operation in relational algebra is the same as union operation in set theory.
- **Set Difference(-):*** Set Difference in relational algebra is the same set difference operation as in set theory. 
- **Set Intersection(∩):*** Set Intersection in relational algebra is the same set intersection operation in set theory. 
- **Rename(ρ):** Rename is a unary operation used for renaming attributes of a relation.
- ***Cross Product(X):*** Cross-product between two relations. Let’s say A and B, so the cross product between A X B will result in all the attributes of A followed by each attribute of B. Each record of A will pair with every record of B.
## Derived Operators
- **Natural Join(⋈):*** Natural join is a binary operator. Natural join between two or more relations will result in a set of all combinations of tuples where they have an equal common attribute.
- **Conditional Join:*** Conditional join works similarly to natural join. In natural join, by default condition is equal between common attributes while in conditional join we can specify any condition such as greater than, less than, or not equal.

## Query Processing Overview
- **Definition**: Query processing involves translating, optimizing, and evaluating queries to extract data from a database.
- **Basic Steps**:
	- Parsing and Translation : 
		- Queries are converted into an internal format (similar to compiler parsing).
		- Checks syntax, verifies relation names, and constructs a parse tree.
			`SELECT balance FROM account WHERE balance < 2500;`
		- Possible relational-algebra translations :
			- `σbalance < 2500(Πbalance(account))`
			- `Πbalance(σbalance < 2500(account))`
	- Optimization : 
		- Generates different query-evaluation plans, aiming to reduce execution cost.
	- Evaluation:
		- The query execution engine runs the chosen plan and returns results.
	- Diagram :  
	- ![[Pasted image 20241024215358.png]]

## Measures of Query Cost
- **Cost Factors**:
	- Disk accesses, CPU time, and communication costs (in distributed systems) are considered.
	- Disk access is usually the most significant cost, as it is slower compared to in-memory operations.
- **Primary Measure**: 
	- Number of block transfers from disk.
	- CPU speeds have been improving much faster than have disk speeds. Thus, it is likely that the time spent in disk activity will continue to dominate the total time to execute a query. Finally, estimating the CPU time is relatively hard, compared to estimating the disk-access cost. 
	- Therefore, most people consider the disk-access cost a reasonable measure of the cost of a query-evaluation plan. We use the number of block transfers from disk as a measure of the actual cost.

## Selection Operations
- **Basic Scan Algorithms**:
	1. **Linear Search (A1)**:
	    - Scans each block and tests records.
	    - Cost: b $r​$ (total blocks), average cost b $r$ /2 for key attributes.
	2. **Binary Search (A2)**:
	    - Used on ordered files for equality conditions.
	    - Cost: O(log⁡ b$r$)for finding the block, but may require reading multiple blocks for non-key attributes.

## Selections Using Indices
- **Index Types**:
	 - **A3 (Primary Index, Equality on Key)**: 
		 - Sigle fetch, heigh of B-tree+ I/O operation
		 - For equality comparisons on a key attribute with a primary index, a single record can be retrieved using the index. 
		 - The cost is equal to the height of the B+-tree plus one I/O operation to fetch the record.
	- **A4 (Primary Index, Equality on Non-key)**:
		- Multiple fetch, heigh of B-tree + no. block (b $r$) containing non-key attribute.
		- When performing equality comparisons on a non-key attribute, multiple records can be retrieved. 
		- The cost is still proportional to the height of the tree, plus the number of blocks containing records that match the non-key attribute.
	- **A5 (Secondary Index, Equality)**: 
		- Single fetch, heigh of B-tree+ I/O operation
		- For equality conditions using a secondary index, a single record can be fetched if the condition is on a key, with costs equal to the height of the tree plus one I/O. 
		- If the condition is on a non-key attribute, multiple records may be spread across different blocks, potentially leading to higher costs—up to one I/O operation per retrieved record, which can be worse than linear search for a large number of records.

## Selections Involving Comparisons
- **Primary Index (A6)**:
	- **Usage**: This method is used for comparison conditions, such as A > $v$ or A <u>></u> $v$.
	- **Process**:
	    1. **Index Lookup**: First, the system looks up the value $v$ in the primary index (like a B+-tree) to find the first record that matches or exceeds $v$.
	    2. **File Scan**: Once the starting point is located, the system performs a file scan from that point to the end of the file to retrieve all records that satisfy the condition.
- **Secondary Index (A7)**:
	- **Usage**: This method can be used for all types of comparison conditions, including <, ≤, >, and ≥.
	- **Process**:
	    1. **Index Scan**: The system scans the index blocks in the direction specified by the comparison. For instance:
	        - For A< $v$ A < $v$ A< $v$, it scans from the beginning of the index up to $v$.
	        - For A>$v$A > $v$A>$v$, it scans from $v$ to the end of the index.
	    2. **Record Retrieval**: This method allows the retrieval of records that meet the comparison condition, using the index to guide the search efficiently.

## JOIN NAHI AAYA

## Evaluation of Expressions in Relational Operations
- #### Overview
	- Evaluating expressions with multiple relational operations can be done through two main methods: materialization and pipelining.
- #### Materialization
	- **Definition**: Evaluates one operation at a time and stores the result in temporary relations.
	- **Process**:
	    - Start from the lowest-level operations in an operator tree.
	    - Execute operations using algorithms and store results as temporary relations.
	    - Use these temporary relations for the next level of operations until reaching the root.
	    - The final result is obtained from the root operation (e.g., projection).
	- **Advantages**:
	    - Intuitive understanding via operator trees.
	- **Disadvantages**:
	    - Inefficient due to the creation and storage of potentially large temporary relations, which require disk I/O.
- #### Pipelining
	- **Definition**: Evaluates multiple operations simultaneously, passing results directly to subsequent operations without temporary relations.
	- **Process**:
	    - Operations are combined into a pipeline.
	    - Results are generated and passed immediately (e.g., a join operation immediately passing tuples to a projection).
	- **Advantages**:
	    - Reduces the need for intermediate storage.
	    - Enhances query evaluation efficiency by minimizing disk I/O.
- #### Implementation of Pipelining
	- **Structure**: Construct a single complex operation that integrates multiple operations.
	- **Memory Efficiency**: Low memory requirements since results are not stored long-term.
	- **Execution Methods**:
	    1. **Demand-Driven**:
	        - System requests tuples from the top of the pipeline.
	        - Each operation computes and returns the next tuple upon request.
	        - If inputs are pipelined, it also requests tuples from lower operations.
	    2. **Producer-Driven**:
	        - Operations generate tuples eagerly.
	        - Bottom-level operations continuously produce output until the buffer is full.
	        - Higher-level operations produce output as they receive input until their buffer is full.

## Query Optimization in Database Management Systems
- #### Overview
	- Query optimization is the process of selecting the most efficient execution plan for a query, particularly when dealing with complex queries. This involves several key operations to transform and streamline the evaluation of expressions.
- #### 1. Optimizer Operations
	- **Evaluation of Expressions**: Simplifies expressions and conditions containing constants.
	- **Statement Transformation**: Converts complex statements (like correlated subqueries or views) into equivalent, simpler forms (e.g., join statements).
	- **Choice of Optimizer Goals**: Establishes the objectives of optimization.
	- **Choice of Access Paths**: Selects the best access methods for retrieving data from tables.
	- **Choice of Join Orders**: Determines the optimal order in which tables are joined.
- #### 2. Cost-Based Optimization
	- **Definition**: Generates various query-evaluation plans and selects the one with the lowest estimated cost.
	- **Join Orderings**: For multiple tables, the number of possible join orders grows exponentially. For n tables, there are 2(n−1)!/(n−1)! different join orders.
	- **Dynamic Programming Approach**:
	    - Stores results of previously computed plans in an associative array (`bestplan`).
	    - Recursively divides sets of relations to find the cheapest plan by evaluating all possible divisions.
	    - Time complexity is O(3n), where n is the number of relations.
- #### 3. Heuristic Optimization
	- **Definition**: Uses heuristic rules to reduce the complexity of optimization without calculating costs for every option.
	- **Common Heuristic Rules**:
	    - **Perform Selection Early**: Reduces the size of intermediate results by filtering tuples before other operations.
	    - **Perform Projections Early**: Eliminates unnecessary attributes to reduce data size in subsequent operations.
	- **Steps in Heuristic Optimization** : 
		1. **Deconstruct Selections**: Break down conjunctive selections into single operations for more effective execution.
		2. **Optimize Execution Order**: Determine the best order of operations to produce smaller intermediate relations based on selectivity.
		3. **Replace Cartesian Products**: Transform Cartesian products followed by selection conditions into join operations.
		4. **Identify Pipelining Opportunities**: Recognize and execute subtrees that can be pipelined for efficiency.