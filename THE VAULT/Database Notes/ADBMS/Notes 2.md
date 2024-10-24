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
