## Syllabus :
- Class 
- Object
- Access modifiers
- Abstraction
- Inheritance
- Encapsulation
- Polymorphism
	- Compile Time
	- Run Time

### Class : 
- User defined blueprint from which objects are created. It represents the set of properties that are common to all objects of one type.
### Objects :
- Instance of a class created with the help of new keyword in java. Through objects one can interact with methods of the class.
### Access Modifiers : 
- Public :  When an element (class, method, or variable) is declared `public`, it means that the element is accessible from any other class, regardless of the package in which the other class is located. In other words, the `public` modifier provides the least restrictive level of access.

- Private : The `private` access modifier restricts access to the element to only within the class in which it is defined. Other classes, even within the same package, cannot access `private` members. This is the most restrictive access level.

- Protected : A `protected` element is accessible within its own package and by subclasses (even if they are in different packages). It offers a middle ground between `public` and `private`, allowing access within the package and to derived classes.

- **Default (Package-Private)**: If no access modifier is specified, the element is considered to have **default** access, which is also known as package-private. This means that the element is accessible only within the same package, but not from classes in other packages.

### Abstraction : 
- Data abstraction is the property by virtue of which only the essential details are displayed to the user.
- The Trivial and non-trivial units are not displayed to the user. 
- Example : 
	- Car, accelration