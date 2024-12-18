
## 7 Marks
##### There are two transactions T and T'. T takes $100 rom account A to account B while T takes 10% of account A to account B. Property of T and T does not change when we do A+B. Create two serial executions for T and T'.

##### How does query processing work? Explain necessary steps in query processing with suitable diagram.

##### Explain Two-phase locking method with suitable example.

##### Create an ER Model for Employee Management Sy stem.

##### Define functional dependency. Explain different functional dependencies with suitable rm example.

##### Why normal form is needed in database tables? Explain 1st 2nd 3rd and BCNF normal form with suitable example. 

##### What is an Index? Explain primary indexing and secondary indexing with examples.

##### Explain B+-tree index with suitable example.

##### Discuss the various file organization methods (Heap, Sequential, Indexed, and Hashed) in detail.

## 3 Marks

##### Write the significance of ACID properties in a database. 
- The ACID properties (Atomicity, Consistency, Isolation, Durability) are crucial for ensuring reliable transaction processing in a database:
	- **Atomicity**: 
		- Ensures that all operations within a transaction are completed successfully. If one part fails, the entire transaction is rolled back, leaving the database in a consistent state.
	- **Consistency**: 
		- Guarantees that a transaction will bring the database from one valid state to another, preserving data integrity. Any changes made during the transaction are compliant with the defined rules, constraints, and data integrity.
	- **Isolation**: 
		- Ensures that concurrently executed transactions do not affect each other. The operations of one transaction are isolated from others, even if they occur simultaneously, ensuring that intermediate states are not visible to other transactions.
	- **Durability**: 
		- Once a transaction is committed, it is permanently stored in the database, even in the event of a system crash. The changes made are not lost.
- These properties help in maintaining the integrity, reliability, and correctness of data in a multi-user, distributed database system.

##### How does locking work in SQL? Describe different types of locks. 
- Locking in SQL is a mechanism used to prevent conflicts and ensure data consistency when multiple transactions try to access the same data concurrently. It prevents other transactions from modifying or reading data that is currently being modified by another transaction. There are several types of locks in SQL:
	- **Shared Lock (S-lock)**: 
		- Allows a transaction to read data, but prevents other transactions from modifying it. Multiple transactions can hold shared locks on the same data item concurrently.
	- **Exclusive Lock (X-lock)**: 
		- Prevents both read and write access to the data by other transactions. Only one transaction can hold an exclusive lock on a data item at a time.
	- **Intent Lock**: 
		- A higher-level lock used to indicate that a transaction intends to acquire a specific type of lock (e.g., shared or exclusive) on a data item within a page or table. It helps in preventing conflicts when multiple transactions are working with different parts of the same resource.
	- **Update Lock (U-lock)**: 
		- A lock that prevents other transactions from acquiring an exclusive lock on the data, but still allows shared locks. It’s typically used in situations where a transaction is intending to update data, but not yet doing so.
	- **Table-Level Lock**: 
		- A lock applied to the entire table, which prevents any other transaction from accessing any rows of the table until the lock is released.
- Locking ensures data integrity and consistency, particularly in concurrent transactions. However, improper use of locks can lead to issues like deadlocks, where two or more transactions are waiting for each other to release locks, causing them to hang.

##### Explain the steps involved in query processing from parsing to execution.
- Query processing in a database involves multiple steps to efficiently execute a query. The process can be broken down into the following stages:
	- **Parsing**: The SQL query is first parsed to check for syntax errors. The query is transformed into a parse tree, which represents the structure of the query and checks for any logical or syntactic errors.
	- **Translation**: The parse tree is then translated into a relational algebra expression or a query tree. This step converts the SQL query into a more usable form for the optimizer to process.
	- **Optimization**: The query optimizer evaluates different query execution plans. The optimizer looks at the possible ways to access the data, choose the most efficient plan, and reduce the execution time, considering factors such as available indexes and statistics.
	- **Execution Plan Generation**: Once the best execution plan is selected, an execution plan is generated, which outlines how the query will be executed (e.g., the use of indexes, joins, scans, etc.).
	- **Execution**: The final step involves executing the query using the chosen plan. The database engine fetches the data, performs the necessary operations (such as joins, aggregations, etc.), and returns the result to the user.
- These steps ensure that queries are executed in an efficient, optimized manner, providing accurate and timely results to users.

##### Why database design methodologies are needed? Write its significance.
- Database design methodologies are essential for creating efficient, scalable, and reliable databases. These methodologies provide systematic approaches to designing databases that meet both functional and performance requirements.
- **Significance of Database Design Methodologies:**
	- **Data Integrity**: Well-designed databases ensure that the data is accurate, consistent, and valid by enforcing rules like primary keys, foreign keys, and unique constraints.
	- **Efficiency**: Proper design minimizes data redundancy and ensures efficient data retrieval. It helps in creating optimal relationships between tables, reducing storage space, and improving query performance.
	- **Scalability**: Good design practices help in scaling the database to handle increasing volumes of data, ensuring it can support future growth.
	- **Data Redundancy Reduction**: Effective design minimizes duplicate data, which not only saves storage space but also ensures that changes made in one place do not cause inconsistencies.
	- **Maintainability**: With structured database design, the system becomes easier to maintain, troubleshoot, and extend without introducing problems or breaking functionality.
	- **Security**: Proper design ensures that data is accessible only to authorized users, preventing unauthorized access and ensuring confidentiality.
- Database design methodologies like ER modeling (Entity-Relationship) or normalization help in structuring the database logically, ensuring it supports business needs while being efficient and easy to manage.

#####  What will be the output of following statement? `SELECT * FROM employee WHERE name LIKE "A%":`
- The SQL query will retrieve all rows from the `employee` table where the `name` column starts with the letter **"A"**.
- The **`LIKE`** operator is used for pattern matching. The **`"A%"`** pattern means:
	- `"A"`: The name must start with the letter "A".
	- `"%"`: The `%` is a wildcard that matches any sequence of characters (including no characters at all).
- Thus, the output will be all the rows from the `employee` table where the `name` starts with "A", such as "Alice", "Alex", "Adam", etc.

##### Explain SQL WHERE Clause with UPDATE Statement with example.
- The **`WHERE`** clause is used in SQL to specify which rows of a table should be updated. When used with the **`UPDATE`** statement, it restricts the update operation to only those rows that meet the condition defined in the `WHERE` clause. Without the `WHERE` clause, all rows in the table will be updated.
-  ``` UPDATE EMPLOYEE SET salary = salary * 1.10 WHERE name = 'Bob'; ```
	
##### Create an index file for Lname attribute of the EMPLOYEE Table of a Database. 
- An index in SQL is a database object used to improve the speed of data retrieval operations. To create an index on the `Lname` attribute of the `EMPLOYEE` table, you can use the `CREATE INDEX` statement.
- **SQL Syntax:** `CREATE INDEX index_name ON EMPLOYEE(Lname);`
- Example :  `CREATE INDEX idx_lname ON EMPLOYEE(Lname);`
- 
##### What is the difference between static and dynamic hashing? 
- Both **static** and **dynamic hashing** are techniques used in database systems to manage hash tables. The main difference lies in how the size of the hash table is handled during insertion and deletion operations.
- **Static Hashing**:
    - In static hashing, the size of the hash table is fixed and does not change.
    - It uses a fixed number of buckets (or slots) to store data.
    - If the table becomes full or experiences a high number of collisions, performance degrades because the fixed number of buckets cannot accommodate more entries without a performance hit.
    - There is no automatic resizing of the hash table, making static hashing less flexible.
- **Dynamic Hashing**:
    - In dynamic hashing, the size of the hash table can grow or shrink dynamically as more data is added or removed.
    - When the number of records exceeds the current capacity of the hash table, the table can be expanded, and new buckets are created to accommodate the increased data.
    - Dynamic hashing helps maintain good performance even with a large amount of data.
    - It can handle growing datasets efficiently without significant degradation in query performance.
- **Key Difference**: Static hashing has a fixed size, while dynamic hashing allows the hash table to adjust its size during runtime, ensuring better handling of large and growing datasets.

##### What is a dense index and a sparse index?
- Both **dense** and **sparse** indexes are techniques used to speed up data retrieval in database systems. They differ primarily in the number of entries they contain and how they relate to the data table.
- **Dense Index :**
	- A **dense index** is an index in which **every record** (or row) in the data table has a corresponding entry in the index.
	- **Structure**: In a dense index, for each record in the table, there is an index entry. This means that the index contains a key for every row in the table.
	- **Space Usage**: Since it indexes every record, it uses more storage space. The index is larger as it has one entry for each row in the data table.
	- **Lookup Performance**: Dense indexes allow **faster lookups** because each row in the data table can be directly mapped to an index entry.
	- **Example**: If a table has 100 rows, a dense index will have 100 index entries, each corresponding to a row in the table.
	- **Example Scenario**:  
		- Consider an employee table where each employee has a unique employee ID. A dense index would contain an entry for every employee (every employee ID) and point to the actual record in the table.
- **Sparse Index :**
	- A **sparse index**, on the other hand, **does not** contain an index entry for every record. Instead, it contains an entry for only **some of the rows**, often one per data block or page in the table.
	- **Structure**: A sparse index typically contains entries only for the first record in each data block or page. It might not have an index entry for every row in the table, but it will have enough entries to allow for efficient searching.
	- **Space Usage**: Sparse indexes are **more space-efficient** because they don’t store an entry for every row. They require less storage compared to dense indexes.
	- **Lookup Performance**: Sparse indexes can be slower to look up compared to dense indexes because the system may need to read more data or check multiple blocks to find the required entry.
	- **Example**: If a table has 100 rows and data is stored in blocks of 10 rows, a sparse index would contain only 10 entries, one for each block (or page).
	- **Example Scenario**:  
		- Consider a table with employee data, where employee names are indexed. Instead of indexing every employee name, the sparse index might index only the first name in each block of 10 records.
## 1 Marks 
##### What is the difference between DELETE, TRUNCATE, and DROP?
- **DELETE**:
    - Removes rows from a table based on a condition (with a WHERE clause).
    - It can be rolled back (if using transactions).
    - It does not affect the table structure or schema.
- **TRUNCATE**:
    - Removes all rows from a table without any condition.
    - It is faster than DELETE because it does not log individual row deletions.
    - Cannot be rolled back in some DBMS (depending on transaction settings).
    - Does not affect the table structure or schema.
- **DROP**:
    - Removes the entire table, including its data, structure, and schema.
    - Cannot be rolled back.
    - The table and its data are permanently deleted.

##### Define data integrity.
- **Data integrity** refers to the accuracy, consistency, and reliability of data throughout its lifecycle. It ensures that data is correct, complete, and stored in a manner that prevents unauthorized access, corruption, or loss. Data integrity is maintained through validation rules, constraints, and regular data audits.

##### How do you enforce referential integrity in a database?  
- **Referential integrity** is enforced using **foreign keys**. A foreign key ensures that a value in one table matches a value in another table. It can be maintained with cascading actions like **CASCADE**, **SET NULL**, **NO ACTION**, or **RESTRICT** to ensure consistency between related tables.

##### Define Conflict serializability. 
- **Conflict serializability** refers to the ability to rearrange the operations (reads and writes) of transactions in a way that results in the same final database state as a serial execution, without violating any data consistency. It ensures that transactions can be reordered without conflicts, preserving the correctness of the database.

##### Write a common difference between logical and physical query optimization.
- A common difference between **logical** and **physical query optimization** is:
	- **Logical query optimization** focuses on choosing the most efficient **logical** execution plan for a query (e.g., reordering joins, pushing selections), independent of how the data is stored.
	- **Physical query optimization** focuses on selecting the most efficient **physical** plan (e.g., choosing indexes, join methods) based on the actual data storage and access methods.

##### The duplication of Data is called........
- Data redundancy

##### In PL/SQL. what is meaning of P? 
- Parameter

##### How BETWEEN operator work? 
- The **BETWEEN** operator in SQL is used to filter the result set within a specified range. It can be used for **numeric**, **date**, or **text** values. It includes the **boundary values** in the range. 
- Example : 
	- `SELECT * FROM tableName WHERE column BETWEEN value1 AND value2;`

##### Write syntax for IN operator.
- ```SELECT * FROM employees
  WHERE department IN ('Sales', 'Marketing', 'HR');```

##### Why is file organization important in database management systems? 
- **File organization** in DBMS is important because it affects data access speed, storage efficiency, data integrity, and system performance. Proper organization ensures fast retrieval, optimal space usage, and effective management of large datasets.

##### What is a record?  
- A **record** is a collection of related data items (fields or attributes) stored as a single unit in a database, typically representing a single entity or object. Each field in a record contains a specific piece of information about that entity.

##### Define overflow in hashing. 
-  **Overflow in hashing** occurs when more data is inserted into a hash table than it can accommodate, causing multiple elements to hash to the same index. This results in a need for handling collisions, often using techniques like **chaining** or **open addressing**.

##### What is a hash function? 
- A **hash function** is a function that takes an input (or key) and returns a fixed-size string of bytes, typically a hash code, which is used to index data in a hash table. It helps in quickly locating a data record based on its key.

##### Differentiate b/w DBMS & OODBMS.
- **DBMS (Database Management System)**:
	- Stores data in tables (relational model).
	- Uses SQL for querying.
	- Data is organized in rows and columns.
- **OODBMS (Object-Oriented Database Management System)**:
	- Stores data as objects (object-oriented model).
	- Supports concepts like inheritance, polymorphism, and encapsulation.
	- Data is organized as objects, similar to how data is represented in programming languages.

