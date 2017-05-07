# Instance Reference
Instance reference refers to the referencing of members from within an instantiated object.

## Java
Java designates the *this* keyword for referencing members of an instantiated object from within a constructor or an instance method.

```Java
public class Pet {
	private String name;
	private String gender;

	public Pet(String name, String gender) {
		this.name = name; // this.name references the current object instance
		this.gender = gender; // this.gender references the current object instance
	}
}
```
*An example illustrating the use of instance referencing from within a constructor in Java*

In addition to referencing class properties, the *this* keyword in Java can be used to call another constructor in the same class.

```java
public class Pet {
	private String name;
	private String gender;

	/* Creates a male pet named Pete using the Pet constructor
	from the previous example */
	public Pet() {
		this("Pete", "male");
	}

	public Pet(String name, String gender) {
		this.name = name; // this.name references the current object instance
		this.gender = gender; // this.gender references the current object instance
	}
}
```

## PHP
PHP designates use of a pseudo-variable called *$this* to reference properties and methods of an instantiated object from within.

```php
<?php
class Pet {
	private $name;
	private $gender;

	function __construct($name, $gender) {
		$this->name = $name; // $this->name references the current object instance
		$this->gender = $gender; // $this->gender references the current object instance
	}
}
?>
```
*An example illustrating use of the pseudo-variable $this in PHP.*

PHP, however, does not allow function overloading. Because of this, it is only possible to define one constructor for a class in PHP. Therefore, calling a class's constructor using $this is not allowed.

## C# #
Like Java, C# designates use of the *this* keyword to reference members of instantiated objects from within.

```cs
class Pet
{
	private string name;
	private string gender;

	public Pet(string name, string gender)
	{
		this.name = name; // this.name references the current object instance
		this.gender = gender; // this.gender references the current object instance
	}
}
```
*An example illustrating the use of instance referencing from within a constructor in C#*

C# also allows the invocation of another constructor in a class using this, however, this must be located before the constructor body as shown in the example below.

```cs
class Pet
{
	private string name;
	private string gender;

	/* Creates a male pet named Pete using the Pet constructor
	from the previous example */
	public Pet() : this("Pete", "male") {}

	public Pet(string name, string gender)
	{
		this.name = name; // this.name references the current object instance
		this.gender = gender; // this.gender references the current object instance
	}
}
```
