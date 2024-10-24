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


## Query Processing Overview
- **Definition**: Query processing involves translating, optimizing, and evaluating queries to extract data from a database.
- **Basic Steps**:
	- Parsing and Translation : 
		- Queries are converted into an internal format (similar to compiler parsing).
		- Checks syntax, verifies relation names, and constructs a parse tree.
			`SELECT balance FROM account WHERE balance < 2500;`
		- Possible relational-algebra translations:
			- Possible relational-algebra translations:
				- `σbalance<2500(Πbalance(account))`
				- `Πbalance(σbalance<2500(account))`
	- Optimization : 
		- Generates different query-evaluation plans, aiming to reduce execution cost.
	- Evaluation:
		- The query execution engine runs the chosen plan and returns results.

## Measures of Query Cost
- **Cost Factors**:
	- Disk accesses, CPU time, and communication costs (in distributed systems) are considered.
	- Disk access is usually the most significant cost, as it is slower compared to in-memory operations.
- **Primary Measure**: 
	- Number of block transfers from disk.
	- CPU speeds have been improving much faster than have disk speeds. Thus, it is likely that the time spent in disk activity will continue to dominate the total time to execute a query. Finally, estimating the CPU time is relatively hard, compared to estimating the disk-access cost. Therefore, most people consider the disk-access cost a reasonable measure of the cost of a query-evaluation plan. We use the number of block transfers from disk as a measure of the actual cost.

## Selection Operations
- **Basic Scan Algorithms**:
	1. **Linear Search (A 1)**:
	    - Scans each block and tests records.
	    - Cost: b $r​$ (total blocks), average cost b $r$ /2 for key attributes.
	2. **Binary Search (A2)**:
	    - Used on ordered files for equality conditions.
	    - Cost: O(log⁡b $r$)for finding the block, but may require reading multiple blocks for non-key attributes.

## Selections Using Indices
- **Index Types**:
	1. **Primary Index (A3)**:
	    - For key attributes with equality condition.
	    - Cost: Height of B+-tree + 1 I/O for the record.
	2. **Primary Index for non-key (A4)**:
	    - Retrieves multiple records; cost includes the tree height + additional I/O's for blocks containing records.
	3. **Secondary Index (A5)**:
	    - Similar to primary but may involve multiple I/O's for non-key attributes.

## Selections Involving Comparisons
- **Primary Index (A6)**:
	- **Usage**: This method is used for comparison conditions, such as A > $v$ or A <u>></u> $v$.
	- **Process**:
	    1. **Index Lookup**: First, the system looks up the value vvv in the primary index (like a B+-tree) to find the first record that matches or exceeds vvv.
	    2. **File Scan**: Once the starting point is located, the system performs a file scan from that point to the end of the file to retrieve all records that satisfy the condition.
- **Secondary Index (A7)**:
	- **Usage**: This method can be used for all types of comparison conditions, including <,≤,>,<, \leq, >,<,≤,>, and ≥.
	- **Process**:
	    1. **Index Scan**: The system scans the index blocks in the direction specified by the comparison. For instance:
	        - For A<vA < vA<v, it scans from the beginning of the index up to vvv.
	        - For A>vA > vA>v, it scans from vvv to the end of the index.
	    2. **Record Retrieval**: This method allows the retrieval of records that meet the comparison condition, using the index to guide the search efficiently.

## Join Operation
- Equi-join attributes from two relations, $r$ and $s$.
- Used to combine records based on equality between specified attributes.
## Nested-Loop Join
- **Algorithm**: Two nested loops:
    1. Outer loop iterates over each tuple tr in relation r.
    2. Inner loop iterates over each tuple ts in relation s.
    3. Checks if tuples satisfy the join condition θ\thetaθ; if yes, concatenates and adds to result.
- **Cost**:
    - Total number of tuple pairs examined: nr×ns \times (where nrn_rnr​ and nsn_sns​ are the number of tuples in r and s, respectively).
    - **Block Accesses**:
        - Worst case: nr×bs+brn_r \times b_s + b_rnr​×bs​+br​ (where brb_rbr​ and bsb_sbs​ are the number of blocks for rrr and sss).
        - Best case: br+bsb_r + b_sbr​+bs​ if both relations fit in memory.

## Block Nested-Loop Join
- Variation where blocks of the inner relation are paired with blocks of the outer relation.
- Within each block pair, all tuples are joined.
- **Optimization Techniques**:
    - If join attributes form a key on the inner relation, exit inner loop upon the first match.
    - Use as many blocks of the outer relation as fit in memory, reserving space for inner relation and output.
    - Alternate scanning of the inner relation forward and backward to reuse buffer space.
    - Use indices on the join attribute for more efficient lookups.
## Indexed Nested-Loop Join
- Utilizes an index on the join attribute in the inner relation.
- For each tuple in the outer relation $r$:
    - Look up relevant tuples in $s$ that satisfy the join condition using the index.
- **Cost Calculation**:
    - Total cost: b$r$+n$r$×c (where $c$ is the cost of a single selection on $s$).

## Merge Join
- **Overview**:
    - Also known as the sort-merge join algorithm.
    - Suitable for natural joins and equi-joins.
- **Process**:
    - Requires both relations r(R)r(R)r(R) and s(S)s(S)s(S) to be sorted based on the join attributes R∩SR \cap SR∩S.
    - Two pointers are initialized, each pointing to the first tuple of the respective relations.
    - The algorithm reads groups of tuples with the same value on the join attributes.
    - Concatenates tuples that match and projects out any repeated attributes.
- **Key Points**:
    - Efficient when both relations are already sorted.
    - Requires sorting if the relations are not pre-sorted, which adds to the cost.

## 4.3.4 Hash Join
- **Overview**:
    - Suitable for implementing natural joins and equi-joins.
    - Utilizes a hash function to partition tuples from both relations.
- **Process**:
    - A hash function h maps the join attribute values to a set of partitions.
    - Tuples from relation r are placed into partitions Hr0,Hr1,…,HrnhHr_0, Hr_1, \ldots, Hr_{nh}Hr0​,Hr1​,…,Hrnh​ based on their hash values.
    - Similarly, tuples from relation sss are placed into partitions Hs0,Hs1,…,HsnhHs_0, Hs_1, \ldots, Hs_{nh}Hs0​,Hs1​,…,Hsnh​.
    - Only tuples from matching partitions Hri and HsiHsiHsi are compared, reducing the number of comparisons needed.
- **Key Points**:
    
    - Efficient for large datasets when the join attributes have a good hash distribution.
    - Does not require sorting but needs sufficient memory for partitions.

### Summary of Costs

- **Merge Join**:
    
    - Cost involves sorting the relations if not pre-sorted, followed by a linear scan to perform the join.
- **Hash Join**:
    
    - Cost depends on the efficiency of the hash function and memory availability for partitioning; typically more efficient than merge joins for large datasets without pre-sorting.