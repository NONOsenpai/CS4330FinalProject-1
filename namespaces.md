# Name Spaces
## Java

Namespaces in Java are called 'Packages'.

***How are name spaces used?***
- group related classes and define a namespace for the classes they contain
- makes types easier to find and use
- helps avoid naming conflicts
- helps control access

***How are name spaces implemented?***
Defining a Package
```Java
  package animals;
```
the above code should be at the top of a page and will define a package name 'animals' for the page it is written on

Importing a Package
```Java
  import java.io;
```
the above code will import all of the classes in the java.io package

Source https://docs.oracle.com/javase/tutorial/java/package/packages.html

## PHP
***How are name spaces used?***
- very similiar to filing system on a computer
-  a way of encapsulating items
- prevent name colisions 

***How are name spaces implemented?***

```php
namespace Foo\Bar\subnamespace;
```
the above code impletments the namespace as a qualified name meaning 'subnamespace' is found in 'bar' which is found in 'foo' which  is found in the current directory

```php
namespace \Foo\Bar\subnamespace;
```
Though adding the extra '\' in the code above the programmer is using a fully qualified name meaning that the namespace is an absolutle path and ignoring the current directory in which it is found. 

Source http://php.net/manual/en/language.namespaces.basics.php
       http://php.net/manual/en/language.namespaces.rationale.php

## C#
***How are name spaces used?***
- organize classes
- declaring your own namespaces can help you control the scope of class and method names in larger programming projects

***How are name spaces implemented?***

```C#
using System;
```
Seen above the 'using keyword' allows acess to system and all of its deravitives such as 'Console' so the programmer doesnt have to delcare System.Console every time he wishes to use a method found in System.Console. The '.' is used to delimit namespaces. 

```C#
namespace SampleNamespace
{
    class SampleClass
    {
        public void SampleMethod()
        {
            System.Console.WriteLine(
              "SampleMethod inside SampleNamespace");
        }
    }
}
```
Seen above a namespace is being used to control the scope of a class, allowing for better organization, especially in larger projects. 

Source https://docs.microsoft.com/en-us/dotnet/articles/csharp/programming-guide/namespaces/
