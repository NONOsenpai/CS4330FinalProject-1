## Lambda Expressions, Closures, or Functions as Types
Programming languages typically support the ability to reference and pass groupings of code that contain their own scope as well as access to an outer function's scope, commonly known as *closures*. The following comparison will offer an in-depth comparison of the implementations of this philosophy in Java, PHP, and C#.

## Java
Java does not support closures; however, Java provides an alternative to closures through the use of nested, or *inner classes*. The official Java documentation from Oracle lists two possible types of inner classes, local and anonymous.

This comparison will focus on the use of *anonymous inner classes*, which are most commonly defined using *lambda expressions* and more closely resemble closures.

The Java lambda expression syntax is made up of a parameter list, an arrow-token, and an expression or statements.

```java
// Java lambda expression syntax
(parameter-list) -> {
	// statements
}
```
*An illustration of the Java lambda expression syntax*


```java
public class Lambda {
    public static void main(String args[]) {

		// Lambda expression assigned to funtional interface here
        Greeting greeting = (name) -> {
            System.out.println("Hello, " + name + "!");
        };

		// Lambda expression invoked here
        greeting.greet("Fred");
    }

	// Functional interface declared here
	@FunctionalInterface
    interface Greeting {
        void greet(String name);
    }
}
```
*An example of a Java lambda expression assigned to the functional interface Greeting*

## PHP
PHP supports closures by creating anonymous functions that return an instance of the Closure class. The following is the Java example implemented in PHP as an anonymous function:

```php
<?php  
// Anonymous function assigned here
$greeting = function($name) {
	echo("Hello, " . $name . "!");
};

$greeting("Fred");
?>
```
*A closure assigned to a variable in PHP*

## C# #
Like Java, C# also supports the use of Lambda expressions; however, they are anonymous functions and not anonymous inner classes. Rather than assigning a lambda expression to a functional interface, lambda expressions in C# are assigned to *delegates* or *expression tree types*.

```cs
// C# lambda expression syntax
(parameter-list) => // statements
```
*An illustration of the C# lambda expression syntax*


```cs
class Lambda
{
  delegate void del(string name);
  static void Main(string[] args)
  {
      // Lambda expression assigned to delegate here
      del greetingDelegate = name => System.Console.WriteLine("Hello, " + name + "!");

      // Lambda expression invoked through delegate here
      greetingDelegate("Fred");
  }
}
```
*An example of a Java lambda expression assigned to a delegate*
