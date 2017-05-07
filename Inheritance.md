# Inheritance / extension

## Java 
- Supports inheritance
- Does not support multiple inheritance 
- Classes that dont already inherit from another class always inherit from Object which creates an inheritance tree
- Cannot change the protection level of members of base class

```java 
public class dog() extends pet{
}
```


sources https://docs.oracle.com/javase/tutorial/java/IandI/subclasses.html

## PHP 
- Supports inheritance
- Does not support multiple inheritance 

```PHP 
class dog() extends pet{
}
```


sources http://php.net/manual/en/language.oop5.inheritance.php

## C# 
- Supports inheritance
- Does not support multiple inheritance 
- Classes do not have to inherit from another class therefore in C# there is an inheritance forest
- Can change the protection level of members of base class

```C# 
public class dog : pet{
}
```


sources https://docs.microsoft.com/en-us/dotnet/articles/csharp/programming-guide/classes-and-structs/inheritance
