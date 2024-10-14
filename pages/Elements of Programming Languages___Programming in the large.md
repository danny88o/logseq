- Slides:
	- ![lec9.pdf](../assets/lec9_1699269743753_0.pdf) CPL: 9
	- ![lec10.pdf](../assets/lec10_1699269754365_0.pdf) CPL: 10
	- ![lec11.pdf](../assets/lec11_1699269760398_0.pdf) [Reading](https://cacm.acm.org/magazines/2014/4/173220-unifying-functional-and-object-oriented-programming-with-scala/fulltext)
- # Programs, Modules, Interfaces
-
- # Objects and Classes
-
- # Object Oriented Functional Programming
	- ## Advances Classes
		- ### Inner Class
			- ((6548d855-cbc8-44af-aca3-a57563fb5481))
			- ListIterator has access to the private head and tail by being a nested class
		- ### Local Class
			- A class inside a method
			- ((6548d902-24d6-46d4-b514-044f337716d4))
		- ### Anonymous Classes
			- Usually implement an interface without explicitly making a new class
			- ```javascript
			  interface Greeting {
			      void greet();
			  }
			  
			  public class Main {
			      public static void main(String[] args) {
			          Greeting greeting = new Greeting() {
			              @Override
			              public void greet() {
			                  System.out.println("Hello, World!");
			              }
			          };
			  
			          greeting.greet();
			      }
			  }
			  ```
	- ## Advanced Types
		- ### Parameterized Types
			- In Scala there is 3 ways:
				- ```javascript
				  type Pair[A,B] = (A,B)
				  ```
				- ```javascript
				  abstract class List[A] 
				  case class Cons[A](head: A, tail: List[A]) 
				  	extends List[A]
				  ```
				- ```javascript
				  trait Stack[A] { ...
				  }
				  ```
			- Type paramaters are implicitly available to all components
			  ((6548de76-beff-41f3-966a-2ed9f98ff0e6))
		- ### Type Bounds
			-