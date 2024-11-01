## Semantics
- When we talk about the "semantics" of a language, we're talking about the meaning behind the words and how they work together. Just like in everyday language, words have meanings, and the way they're put together forms sentences with specific meanings.

- In computer programming, the words are like the building blocks of a program. These building blocks are called "tokens," and the way they're organized is called "syntax structure." However, just putting these blocks together correctly doesn't guarantee that the program makes sense.

- This is where "semantic analysis" comes in. It's like a check to see if the program not only looks right but also makes logical sense. For example, if you write something like "int a = 'value';" in a programming language, it might look fine at first glance, but it's actually a mistake. The computer understands that 'value' is text, but "int" is for numbers. So, it's like saying, "store this text as a number," which doesn't make sense.

- The set of rules that define what makes sense in a programming language is like the grammar of that language. These rules are checked during the semantic analysis phase to make sure the program is not just correctly written but also logically sound. If there's a mistake in how the words are being used, it's flagged as a "semantic error."

- Some of the semantics errors that the semantic analyzer is expected to recognize: 
	 • Type mismatch 
	 • Undeclared variable 
	 • Reserved identifier misuse. 
	 • Multiple declaration of variable in a scope. 
	 • Accessing an out of scope variable. 
	 • Actual and formal parameter mismatch.
## Syntax Directed Translation (SDT)
- When we're building a compiler, a program that translates code written by a programmer into something a computer can understand, one way to do it is by using the parser. The parser is like a language interpreter that figures out the structure of the code.

- Now, in this method, we don't just stop at figuring out the structure; we use the parser's results to guide two important tasks: semantic analysis and translation of the code. Semantic analysis is about making sure the code makes logical sense, and translation is about turning it into a form the computer can execute.

- To make this process work, we tweak the regular grammar (rules that define how sentences in a language are structured) a bit. We add extra information to it, and this new kind of grammar is called an "attribute grammar."

- There are two main ways to use this approach, and they are called <font color="#ffc000">Syntax-Directed Translation (SDT)</font> methods. In SDT, the information we added to the grammar helps control both the semantic analysis and the translation of the source code. It's like giving our parser some extra guidance on how to understand and convert the code correctly. <font color="#ffc000">The two methods under SDT are Attribute Grammars and Syntax-Directed Translation Schemes.</font> They are the tools that help us make sense of the code and turn it into something the computer can run.


## Attributes
- **Attributes:**
	- An attribute is like a property or characteristic of a grammar symbol (like a part of the code).
	- Attribute computation functions, also called semantic functions, are functions associated with the rules of a grammar. They help calculate the values of these attributes.
	- Predicate functions state some syntax and static semantic rules of a grammar.

- **Types of Attributes:**
	1. **Type:** Associates data objects with allowed sets of values.
	2. **Location:** Can be changed by the memory management routine of the operating system.
	3. **Value:** The result of an assignment operation.
	4. **Name:** Can be changed when a sub-program is called and returns.
	5. **Component:** Data objects made up of other data objects, represented by a pointer and changed accordingly.

- **Synthesized Attributes:**
	- These attributes get their values from the attribute values of their child nodes.
	- For example, if you have a production like `S → ABC`, and S is getting values from its child nodes A, B, and C, then S is said to have synthesized attributes. The values of A, B, and C are synthesized to S.
	- Synthesized attributes don't take values from their parent nodes or any sibling nodes.

- **Inherited Attributes:**
	- In contrast to synthesized attributes, inherited attributes can take values from parent and/or sibling nodes.
	- For example, in the production `S → ABC`, A can get values from S, B, and C. B can take values from S, A, and C. Similarly, C can take values from S, A, and B. So, they inherit values from their parent and sibling nodes.

## Reduction 
1. **Terminal and Non-terminal:**    
    - Terminals are the actual symbols in your code (like keywords or values).
    - Non-terminals are higher-level structures that represent groups of terminals.
2. **Syntax Trees:**
    - Imagine reading your code from top to bottom and left to right.
    - When you see a group of symbols that matches a non-terminal in the grammar rules, you replace them with that non-terminal. This is called "reduction."
3. **Semantic Rules and Actions:**
    - As you parse the syntax tree, whenever you do a reduction (replace symbols with non-terminals), you apply some special rules or actions. These are the "semantic rules" or "actions."
4. **Syntax Directed Translations:**
    - The process of going from the syntax tree to the final translated code is called "Syntax Directed Translation" (SDT).
    - This involves applying rules or actions associated with the syntax tree nodes.
5. **Semantic Analysis:**
    - The semantic analyzer comes into play.
    - It gets the Abstract Syntax Tree (AST) from the previous stage (syntax analysis).
    - It adds extra information to the AST, called "attributes." These attributes are like extra details about different parts of your code.
6. **Attributed AST:**
    - The AST, with these added attributes, is now called an "Attributed AST."
    - Each attribute is a two-part thing: the name of the attribute and its value.

So, in simpler terms, think of it like reading a story (your code) top to bottom and left to right. As you read, you replace some words with more general terms (reduction). At each replacement, you also do something special (semantic action). Later, you go back and add extra details to your story (attributes) to make sure everything makes sense. The final result is a story with more information, ready to be understood by the computer.

## **S-attributed SDT (Syntax Directed Translation):**

- When an SDT uses only "synthesized attributes," it's called an S-attributed SDT.
- Synthesized attributes are values calculated from child nodes and used by parent nodes.
- In S-attributed SDTs, these attributes are evaluated during bottom-up parsing. This means you start with the child nodes and work your way up to the parent nodes because the values of parent nodes depend on the values of child nodes.
- Semantic actions (things you do with the values) are written after the production (right-hand side of the grammar rule).

## **L-attributed SDT:**

- L-attributed SDTs use both "synthesized and inherited attributes."
- Synthesized attributes are values from child nodes, and inherited attributes can get values from parent and/or sibling nodes.
- There's a restriction in L-attributed SDTs: non-terminals can't take values from their right siblings.
- In a production like `S → ABC`, S can take values from A, B, and C (synthesized), A can take values from S only, B can take values from S and A, and C can get values from S, A, and B.
- Attributes in L-attributed SDTs are evaluated by depth-first and left-to-right parsing. This means you go through the tree from top to bottom and from left to right.
- If a definition is S-attributed, it is also L-attributed because L-attributed definitions include S-attributed definitions.

## Attribute Grammar

- It's a special kind of grammar where we add extra information to non-terminals to provide context-sensitive details.
- Another way to think of it is as Syntax Directed Definitions (SDDs) without side-effects.
- It helps define both the structure and meaning of a programming language.
- Imagine it as a way to pass information among different parts (nodes) of a tree, especially when looking at it like a parse tree.

- **Example:** Consider this grammar rule: `E → E + T { E.value = E.value + T.value }`
	- This rule tells us how to interpret the grammar. It says that the value of `E` should be the sum of its current value and the value of `T`.
 
- **Another Example:** Now, let's take a grammar for signed binary numbers:
	- number → signlist
	    sign → + | − 
	    list → listbit | bit 
	    bit → 0 | 1
	- - We want to create an attribute grammar that tells us the value represented by a "number."
	- We associate attributes with grammar symbols like this: `number` has a value (`val`), `sign` can be negative (`neg`), `list` has a positive value (`pos`) and a value (`val`), and `bit` has a positive value (`pos`) and a value (`val`).

- This way, we use attributes to pass information around and understand not just the structure but also the meaning of the code. It's like adding extra notes to a story so that we can understand not only how it's written but also what it means.


## Semantic Analysis in Compiler Design

- **Semantic Analysis Overview:**
	- Semantic Analysis is the third phase of a compiler.
	- It ensures that declarations and statements in a program make sense.
	- The parser calls a collection of procedures during syntax analysis as needed by the grammar.
	- Both the syntax tree from the previous phase and the symbol table are used to check the consistency of the code.

- **Type Checking:**
	- A crucial part of semantic analysis.
	- It ensures that each operator in the code has matching operands.
	- The compiler checks that data types are used in a way consistent with their definitions.

- **Functions of Semantic Analysis:**
	1. **Type Checking:**
	    - Ensures consistent use of data types in the code.
	2. **Label Checking:**
	    - Verifies that the program contains label references.
	3. **Flow Control Check:**
	    - Ensures proper usage of control structures (e.g., no break statement outside a loop).

- **Example:**
	- float x = 10.1; 
		float y = x * 30;
	- In this example, the integer 30 will be converted to a float (30.0) before multiplication by the semantic analyzer.

- **Static and Dynamic Semantics:**
	- **Static Semantics:**
	    - Checked at compile time.
	    - Concerned with the correctness of the code structure.
	- **Dynamic Semantic Analysis:**
	    - Checked at runtime.
	    - Defines the meaning of different program units (expressions, statements) during execution.

## Symbol table 

- **Symbol Table Overview:**
	- The symbol table is like a database maintained by the compiler.
	- It consists of Name and Value pairs.
	- It keeps track of the semantics of variables, storing information about names, scopes, and binding details.
	- Built during lexical and syntax analysis phases of the compiler.
	- Information collected by analysis phases is used by synthesis phases for code generation.

- **Phases and Uses of Symbol Table:**
	1. **Lexical Analysis:**
	   - Creates new entries in the table, such as entries for tokens.
	
	2. **Syntax Analysis:**
	   - Adds information like attribute type, scope, dimension, line of reference, use, etc., in the table.
	
	3. **Semantic Analysis:**
	   - Uses table information to check semantics (e.g., type checking) and updates it accordingly.
	
	4. **Intermediate Code Generation:**
	   - Refers to the symbol table for knowing runtime allocation details, aiding in adding temporary variable information.
	
	5. **Code Optimization:**
	   - Uses symbol table information for machine-dependent optimization.
	
	6. **Target Code Generation:**
	   - Generates code using address information of identifiers in the table.

- **Symbol Table Entries:**
	- Each entry in the symbol table has attributes supporting the compiler in different phases.

- **Use of Symbol Table:**
	- Symbol tables are typically used in compilers.
	- During the scan of an application program, compiler stores identifiers in the table.
	- Identifiers are stored with name, value, address, and type information.
	- This way, the compiler keeps track of all identifiers with necessary details.

- **Items Stored in Symbol Table:**
	1. Variable names and constants
	2. Procedure and function names
	3. Literal constants and strings
	4. Compiler-generated temporaries
	5. Labels in source languages

- **Information Used by Compiler from Symbol Table:**
	1. Data type and name
	2. Declaring procedures
	3. Offset in storage
	4. For structures or records, a pointer to the structure table
	5. For parameters, whether passed by value or by reference
	6. Number and type of arguments passed to a function
	7. Base Address

- **Operations on Symbol Table:**
	1. Insertion of an item in the symbol table.
	2. Deletion of any item from the symbol table.
	3. Searching for a desired item in the symbol table.

- **Applications of symbol table:**
	1. **Resolution of Variable and Function Names:**
	   - Symbol tables help identify the data types and memory locations of variables and functions.
	   - They are essential for resolving the names of variables and functions in a program.

	2. **Resolution of Scope Issues:**
	   - Symbol tables are used to resolve naming conflicts and determine the scope or range of variables and functions.
	   - They help the compiler understand where in the program a particular name is valid.
	
	3. **Optimizing Code Execution:**
	   - Symbol tables provide quick access to information like memory locations.
	   - This quick access helps optimize the execution of the code by efficiently managing data and variables.
	
	4. **Code Generation:**
	   - Symbol tables play a crucial role in code generation.
	   - They provide necessary details, such as memory locations and data types, to generate machine code from the source code.
	
	5. **Error Checking and Code Debugging:**
	   - Symbol tables supply details about the program's status during execution.
	   - They are used for error checking and debugging code by providing insights into variable values and states.
	
	6. **Code Organization and Documentation:**
	   - Symbol tables contain information about a program's structure.
	   - They are valuable for organizing code and making it easier to understand, contributing to documentation efforts.
	 
	- In essence, symbol tables serve as a central repository of information that aids the compiler in various tasks, from understanding the structure of the code to generating efficient machine code and facilitating error checking and debugging.

## Intermediate Code Generation in Compiler Design 
- ye slides se h dekh lo, nothing to simplify 

## Code Optimization in Compiler Design
- Code optimization is like refining a recipe to use fewer ingredients but still taste just as good. The compiler aims to make the program run faster and use resources more efficiently, all while ensuring that the optimizations do not change the intended meaning of the code and do not significantly slow down the compilation process.
- **Code Optimization Overview:**
	- Code optimization is a technique used in the synthesis phase of a compiler.
	- Its goal is to improve the intermediate code generated by the compiler, making it use fewer resources (like CPU and Memory) to produce faster-running machine code.
- **Objectives of Code Optimization:**
	1. **Correctness:**
	    - Optimization must be correct and should not change the meaning of the program.
	    - It ensures that the transformed code still performs the same logical operations as the original code.
	2. **Speed and Performance:**
	    - Optimization should enhance the speed and overall performance of the program.
	    - The idea is to make the program run faster and more efficiently.
	3. **Reasonable Compilation Time:**
	    - While optimizing, the compilation time (the time it takes to convert source code into machine code) should be kept reasonable.
	    - It ensures that the optimization process doesn't significantly slow down the compilation process.
	4. **Minimal Impact on Compilation Process:**
	    - The optimization process should not introduce delays to the overall compilation process.
	    - It ensures that the benefits gained from optimization are achieved without causing unnecessary delays.