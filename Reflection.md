# Reflection
[From Wikipedia.org](https://en.wikipedia.org/wiki/Reflection_(computer_programming))
<br></br>
"In computer science, reflection is the ability of a computer program to examine, introspect, and modify its own structure and behavior at runtime."
## Java
* Java includes methods for any and all forms of reflection.
<br></br>
Some examples include `instanceof`,`.getDeclaredMethods()`,`.getClass()`,  and A LOT of other methods.
* Allows for  changing values of fields at runtime
* Java defined the standard for reflection in OO- programming languages, all the way back in January of 1998.
<br></br>
[1998 Documentation](http://www.oracle.com/technetwork/articles/java/javareflection-1536171.html)
* Java was very focused on providing reflection throughout the language. Since Java 7, they even included a package [java.lang.reflect](https://docs.oracle.com/javase/7/docs/api/java/lang/reflect/package-summary.html)
## PHP
* [PHP reflection](http://php.net/manual/en/book.reflection.php)
* Reflection includes the ability to look into classes, interfaces, functions, methods, and EVEN extensions

## C#
* RuntimeType(s) : `Type` and `MethodInfo`
* `System.Reflection.Emit` allows a way to reflect types at run time.
* Over time, C# has included close to all of the reflection techniques and methods 

## Summary
Over time, all of the languages support reflection that Java originally implemented. They all can introspect VERY in depth of classes and methods. They all also include ways to modify behavior at runtime. Some languages are easier to do this with, however they all support a technique to do so. 
