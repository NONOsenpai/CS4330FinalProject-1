# Classes

## Java 
***Defining***

Below the class 'Pet' is defined in java

```java
class Pet{
}
```

Classes can aslo be defined with access modifiers or be defined as abstract. 

```Java
public class Pet{
}

public abstract Pet{
}
```
***Creating new instances***

The following creates a new instance of a pet named "myPetName" 
```java

Pet myPetName = new Pet()
```
***Constructing/initializing ***

A class in Java can have numerous constructors. 
```java
public class Pet{

  Pet(){
  ...
  }
  Pet(string name){
  ...
  }
  Pet(string name, int age, string species)
  }
}
```

These constructors are called when the apporpiate arguments are given
```java
Pet spot = new Pet()
Pet rudy = new Pet('Rudy")
Pet Spartan = new Pet ('Spartan', 6, 'dog')
```

*** Destructing/de-initializing*** 
Objects are destroied by the garbage collector when they can no longer be reached. See memory management page for more information. 


sources https://docs.oracle.com/javase/tutorial/java/javaOO/classes.html


## PHP  
***Defining***

Below the class 'Pet' is defined in PHP

```PHP
class Pet{
}
```

***Creating new instances***

The following creates a new instance of a pet named "myPetName" 
```PHP

$myPetName = new $Pet;
```
***Constructing/initializing ***

Below is an example of a php constuctor. 
```PHP
class Pet {
   function __construct() {
       $this->name = "Pet";
   }

   function __destruct() {
       print "Destroying " . $this->name . "\n";
   }
}
```

*** Destructing/de-initializing*** 
Below is an example of a php destructor. To destruct the class the programmer must call upon the destruct function  

```PHP
class Pet {
   function __destruct() {
       print "Destroying " . $this->name . "\n";
   }
}
```

sources http://php.net/manual/en/language.oop5.decon.php


## C# 
***Defining***

Below the class 'Pet' is defined in C#

```C#
Public class Pet{
}
```

***Creating new instances***

The following creates a new instance of a pet named "myPetName" 
```C#

Pet myPetName = new Pet()
```
***Constructing/initializing ***

A class in c# can have numerous constructors. 
```C#
public class Pet{

  Pet(){
  ...
  }
  Pet(string name){
  ...
  }
  Pet(string name, int age, string species)
  }
}
```

These constructors are called when the apporpiate arguments are given
```c#
Pet spot = new Pet()
Pet rudy = new Pet('Rudy")
Pet Spartan = new Pet ('Spartan', 6, 'dog')
```

*** Destructing/de-initializing*** 
```C#
class Pet
{
    ~Pet()  // destructor
    {
        // cleanup statements...
    }
}
```

sources https://docs.microsoft.com/en-us/dotnet/articles/csharp/programming-guide/classes-and-structs/classes
https://docs.microsoft.com/en-us/dotnet/articles/csharp/programming-guide/classes-and-structs/destructors
