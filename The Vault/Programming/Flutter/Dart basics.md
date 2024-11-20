#Programming #flutter 
## Objects and classes 
- Before objects and classes in dart, just few basic codes : 
	- For input we use : `var name = stdin. ReadLineSync();`
	- For output we use :
		- `print('Welcome : $name')` or
		- `stdout.write('Welcome : $name')`
- Example of classes and object : 
``` 
// Define the class
class SumCalculator {
  // Method to calculate the sum of two numbers
  int calculateSum(int num1, int num2) {
    return num1 + num2;
  }
}
void main() {
  	// Create an object (instance) of the SumCalculator class
  SumCalculator calculator = new SumCalculator(); 
  	// new keyword is optional in new dart 	versions
  int result = calculator.calculateSum(10, 20);
  print("The sum is: $result");
}
```

## Variables and data types in dart  
- Dart is a statically typed language, meaning the type of a variable is determined at compile-time. However, Dart also has type inference, so you can often leave out explicit type declarations, and Dart will infer the type based on the value assigned to the variable.
- **Variables :** 
	- A variable in Dart is a storage location that can hold a value. You declare a variable using the `var`, `final`, or `const` keywords.
		- `var` : Used to declare a variable where the type is inferred from the assigned value. The type can be changed later.
		- `final` : Used for variables that can only be assigned once. The type is inferred when the value is assigned. `final age = 25;`, here age is inferred when the value is assigned. 
		- `const` : Used for compile-time constants. The value of the variable is fixed and cannot be changed. Can only hold values that are known at compile-time.
		- `Explicit type` : - Dart allows explicit type declaration if you want to be specific about the type of a variable. `String name = 'Prakhar' or int age = 25`!
- **Data Types :** 
	- `int, double, String, Boolean, List, Set, Map, Runnes, Null`
	- Code examples : 
```
		
```