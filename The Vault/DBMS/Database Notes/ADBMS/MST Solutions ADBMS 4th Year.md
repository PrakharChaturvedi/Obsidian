
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

##### How does locking work in SQL? Describe different types of locks. 

##### Explain the steps involved in query processing from parsing to execution.

##### Why database design methodologies are needed? Write its significance.

#####  What will be the output of following statement? `SELECT * FROM employee WHERE name LIKE "A%":`

##### Explain SQL WHERE Clause with UPDATE Statement with example.

##### Create an index file for Lname attribute of the EMPLOYEE Table of a Database. 
##### What is the difference between static and dynamic hashing? 

##### What is a dense index and a sparse index?

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
- **Data integrity** refers to the accuracy, consistency, and reliability of data throughout its lifecycle. 
- It ensures that data is correct, complete, and stored in a manner that prevents unauthorized access, corruption, or loss. 
- Data integrity is maintained through validation rules, constraints, and regular data audits.

##### How do you enforce referential integrity in a database?  
- **Referential integrity** is enforced using **foreign keys**. A foreign key ensures that a value in one table matches a value in another table. It can be maintained with cascading actions like **CASCADE**, **SET NULL**, **NO ACTION**, or **RESTRICT** to ensure consistency between related tables.

##### Define Conflict serializability. 
- 

##### Write a common difference between logical and physical query optimization.

##### The duplication of Data is called........

##### Define data integrity. 

##### In PL/SQL. what is meaning of P? 

##### How BET WEEN operator work? 

##### Write syntax for IN operator.

##### Why is file organization important in database management systems? 

##### What is a record?  

##### Define overflow in hashing. 
##### What is a hash function? 

##### Differentiate b/w DBMS & OODBMS.

