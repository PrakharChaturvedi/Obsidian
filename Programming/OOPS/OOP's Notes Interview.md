## Object-Oriented Programming (OOP) Fundamentals
- Object-oriented programming (OOP) is a programming paradigm that revolves around creating "objects" to represent real-world entities. These objects encapsulate data (properties) and the actions (methods) that can be performed on that data. Here’s a breakdown of the key concepts in OOP :
	- **Classes and Objects** :
		- **Class :** A class is a blueprint that defines the properties and methods that objects of a certain kind will share. It acts as a template for creating objects. 
		- **Object :** An object is an instance of a class. It’s a concrete entity that possesses the properties and methods defined in the class.
		- Imagine a class ‘Car‘ - it defines what a car is (properties like wheels, color) and what it can do (methods like accelerate, brake). Each actual car you see on the road (red Honda Civic, blue Toyota Camry) is an object, an instance of the ‘Car‘ class
	- **Encapsulation** :
		- Encapsulation is the concept of bundling data (properties) and the methods that operate on that data together within an object. It restricts direct access to the data, allowing it to be modified only through the object’s methods. This promotes data protection and prevents accidental changes from outside code.
	- **Inheritance :**
		- Inheritance allows creating new classes (subclasses) that inherit properties and methods from existing classes (super classes). This promotes code reusability and creates a hierarchical relationship between classes. 
		- For example, a ‘SportsCar‘ class might inherit from the ‘Car‘ class, gaining all its general functionalities while adding specific methods like ‘useTurboBoost‘.
	- **Polymorphism :**
		- Polymorphism allows objects of different classes to respond to the same method call in different ways. This is achieved through method overriding in subclasses. For instance, a ‘fly‘ method on a ‘Bird‘ class would have different behavior compared to a ‘fly‘ method on an ‘Airplane‘ class, even though they share the same name.
	- **Abstraction :** 
		- Abstraction focuses on providing a simplified interface to an object’s functionalities. It hides the implementation details and exposes only essential methods for users to interact with. 
		- For example, a ‘Car‘ class might have an ‘accelerate‘ method that hides the complex mechanics behind increasing speed.
	- **Modularity :**
		- Modularity refers to dividing a program into smaller, independent, and reusable units. Objects themselves promote modularity by encapsulating functionalities. This makes code easier to understand, maintain, and test.
	- **Coupling and Cohesion :**
		- Coupling refers to the interdependency between different parts of a program. Ideally, we strive for loose coupling, where objects rely on each other minimally.
		- Cohesion refers to how focused and related the functionalities within a single class or module are. Tight cohesion means a class has a clear responsibility and its methods work together towards a single goal.

## Class Design Principles (SOLID)
- In object-oriented programming, creating well-designed classes is essential for building maintainable and flexible software. The SOLID principles provide a set of guidelines to achieve this goal. SOLID is an acronym for five key design principles :
	- **Single Responsibility Principle (SRP) :**
		- A class should have one, and only one, reason to change. This means a class should focus on a single functionality or responsibility.
		- If a class has multiple unrelated functionalities, it’s better to separate them into distinct classes.
		- Following SRP promotes loose coupling and improves code maintainability.
	- **Open/Closed Principle (OCP) :**
		- Software entities (classes, modules) should be open for extension but closed for modification. This means you should be able to extend the functionality of a class without altering its existing code.
		- Techniques like inheritance and abstract classes allow adding new functionalities through subclasses without modifying the base class.
	- **Liskov Substitution Principle (LSP) :**
		- Objects of a superclass should be replaceable with objects of its subclasses without affecting the program’s correctness.
		- In simpler terms, if you have a function that expects a superclass object, it should work seamlessly with objects of its subclasses as well.
		- LSP ensures consistency and predictability in object behavior within inheritance hierarchies.
	- **Interface Segregation Principle (ISP) :**
		- Clients (other parts of the code) should not be forced to depend on methods they don’t use.
		- This principle suggests creating smaller, more specific interfaces instead of one large general-purpose interface.
		- Clients can then choose the interface that best suits their needs, promoting loose coupling and reducing unnecessary dependencies.
	- **Dependency Inversion Principle (DIP) :**
		- High-level modules should not depend on low-level modules. Both should depend on abstractions. Abstractions should not depend on details. Details should depend on abstractions. This principle emphasizes relying on abstractions (interfaces) instead of concrete implementations (classes).
		- This allows for easier switching between different implementations without modifying the high-level code that depends on the abstraction.
- By following these SOLID principles, you can design classes that are : 
	- **More maintainable :** Easier to understand, modify, and extend.
	- **More reusable : ** Code can be reused in different contexts. 
	- **Less error-prone:** Promotes predictable behavior and reduces chances of unexpected issues. 
	- **More flexible:** Easier to adapt to changing requirements.

## Class Relationships: Inheritance, Composition, and Aggregation
- In object-oriented programming (OOP), classes can interact and relate to each other in various ways. Three fundamental relationships play a key role in structuring these interactions: inheritance, composition, and aggregation.
	- **Inheritance :**
		- Inheritance establishes an "is-a" relationship between classes. A subclass (child class) inherits properties and methods from its superclass (parent class).  This promotes code reusability as the subclass gains access to the functionality defined in the superclass. Inheritance allows for specialization - the subclass can add its own specific properties and methods while retaining the inherited ones.
	- **Composition :**
		- Composition represents a "has-a" relationship between classes. A class (whole) has a member variable that is an instance of another class (part). The whole object is responsible for the lifetime of the part object. This means when the whole object is destroyed, the part object is also destroyed. Composition establishes a strong dependency between the classes.
	- **Aggregation :**
		- Aggregation is also a "has-a" relationship, similar to composition. However, the difference lies in the lifetime management. In aggregation, the part object can exist independently of the whole object. Destroying the whole object does not necessarily destroy the part object. Aggregation represents a weaker dependency compared to composition.
- **Here’s a table summarizing the key differences :** 

| Feature             | Inheritance                  | Composition           | Aggrigation           |
| ------------------- | ---------------------------- | --------------------- | --------------------- |
| Relationship        | "is-a"                       | "has-a" (strong)      | "has-a" (weak)        |
| Lifetime Management | Independent                  | Owned by the whole    | Independent           |
| Example             | 'Dog' inherits from 'Animal' | 'Car' has an 'Engine' | 'Library' has 'Books' |
- **Choosing the right relationship :**
	- Use inheritance when there’s a clear "is-a" relationship between classes and you want to promote code reusability. Use composition when the whole object has a strong ownership of the part object and is responsible for its lifecycle. Use aggregation when the whole object has a "uses-a" or "associated-with" relationship with the part object, and their lifecycles are independent.


## Inheritance in Depth: Types and Mechanisms
- Inheritance, a cornerstone of object-oriented programming (OOP), allows creating new classes (subclasses) that inherit properties and behaviors from existing classes (super classes). This promotes code reuse and creates hierarchical relationships between classes. But inheritance goes beyond the basic concept of "is-a" relationships. Let’s delve deeper into its types and mechanisms.
- **Types of Inheritance:**
	- There are several ways classes can inherit from other classes, each with its own advantages and considerations :
		- **Single Inheritance:** 
			- This is the most common type, where a subclass inherits from a single superclass. 
			- It promotes clear and well-defined class hierarchies. * Example: ‘Dog‘ class inherits from ‘Animal‘ class.
		- **Multilevel Inheritance:**
			- A subclass inherits from another subclass, forming a chain of inheritance.
			- This allows for more specific specializations but can lead to complex hierarchies that might be difficult to maintain.
			- Example: ‘Labrador‘ class inherits from ‘Dog‘ class, which inherits from ‘Animal‘ class.
		- **Hierarchical Inheritance:**
			- Multiple subclasses inherit from a single superclass. This is useful for modeling classes with similar functionalities but slight variations. Example: ‘Dog‘ class, ‘Cat‘ class, and ‘Bird‘ class all inherit from ‘Animal‘ class.
		- **Multiple Inheritance (Language Dependent):**
			- A subclass inherits from multiple super classes, gaining access to properties and methods from all of them. 
			- This can be powerful but can also lead to ambiguity (the "diamond problem") if both super classes have methods with the same name. Not all OOP languages support multiple inheritance. 
			- **Diamond Problem:** Imagine a class ‘Shape‘ with a method ‘draw‘ and classes ‘Circle‘ and ‘Square‘ inherit from ‘Shape‘. Now, a class ‘Rectangle‘ inherits from both ‘Circle‘ and ‘Square‘. If ‘Rectangle‘ also tries to implement ‘draw‘, it’s unclear which parent class’s ‘draw‘ method it should inherit. This ambiguity is the diamond problem.
		- **Hybrid Inheritance (Combination):**
			- Combines different types of inheritance like single, multilevel, and hierarchical inheritance to create complex class structures. Use with caution as it can make code harder to understand and maintain.
	- **Mechanisms of Inheritance:**
		- **Public Inheritance:** Subclass inherits all public and protected members from the superclass. 
		- **Protected Inheritance:** Subclass inherits protected and public members from the superclass, but private members are not inherited. 
		- **Private Inheritance (Java/C++):** Subclass cannot inherit private members, but they can still be accessed by the superclass itself. Not all languages support private inheritance.
	- **Key Points to Remember:**
		- Inheritance promotes code reusability and reduces redundancy. 
		- Subclasses can specialize inherited behavior by overriding methods from the superclass. 
		- Overriding methods allows subclasses to define their own implementation for inherited functionalities.
		- Choose the appropriate type of inheritance based on the desired relationship between classes.
		- Overuse of inheritance can lead to complex and difficult-to-maintain code structures.


## Access Modifiers in OOP
- Access modifiers are keywords used in object-oriented programming (OOP) to control the visibility and accessibility of class members (properties, methods, constructors) from different parts of your program. They play a vital role in achieving encapsulation, a core principle of OOP.
- Here’s a breakdown of the most common access modifiers : 
	- **Public:** Members declared as ‘public‘ are accessible from anywhere within your program, including other classes, the current class, and even outside the package (depending on the programming language).  
		- Public members are meant to be used by other parts of the program.
		- Example: 
			‘‘‘java 
			public class Car { 
			 public String color; 
			 public void startEngine() { 
			 // implementation details 
			} } ‘‘‘
		- In this example, ‘color‘ and ‘startEngine‘ are accessible from any code in the program.
		
	- **Private:** Members declared as ‘private‘ are only accessible within the class they are defined in. They are invisible to other classes and cannot be accessed directly from outside the class. Private members promote encapsulation by hiding internal implementation details and protecting them from unintended modifications.
		- Example: ‘‘‘java 
					class Engine { 
					private int horsePower; 
					private void increasePower() {
					 // implementation details 
					} } ‘‘‘
		- Here, ‘horsePower‘ and ‘increasePower‘ are private to the ‘Engine‘ class.
	- **Protected:** Members declared as ‘protected‘ are accessible from within the class they are defined in, as well as from subclasses that inherit from that class. They are invisible to completely unrelated classes. Protected members are useful for providing controlled access to certain functionalities for subclasses. while maintaining encapsulation within the inheritance hierarchy.
		- Example : 
		 ‘‘‘ java 
		 class Animal { 
		 protected String name; 
		 protected void makeSound() { 
			 System.out.println("Generic animal sound");
			  } } 
		 class Dog extends Animal {
		  public void bark() { 
			  makeSound(); // Inherited protected method 
			  System.out.println("Woof!"); 
			  } } 
			‘‘‘
		- In this example, ‘name‘ and ‘makeSound‘ are protected in ‘Animal‘. The ‘Dog‘ class, being a subclass, can access and use them.
	- **Default (Package-Private):** This modifier (sometimes called "package-private" or "internal") varies slightly depending on the programming language. Generally, members declared without any access modifier are considered package-private. This means they are accessible from within the same package (group of related classes) but are invisible outside the package. Default access provides a middle ground between public and private, allowing controlled access within a specific program module.
		- **Choosing the Right Modifier:**
			- Use ‘public‘ for members that need to be accessed from other parts of your program. 
			- Use ‘private‘ to hide internal implementation details and promote data protection. 
			- Use ‘protected‘ for members that should be accessible to subclasses but not directly from outside the inheritance hierarchy. 
			- Use ‘default‘ (package-private) for members that should be used within a specific package but not globally throughout the program.

## Constructors in OOP
- In object-oriented programming (OOP), a constructor is a special type of method that is automatically called when you create an object of a class. Its primary purpose is to initialize the object’s state by setting values for its properties (member variables). 
- There are several types of constructors that provide flexibility in object creation :
	- 