## Procedural programming

* Does the language support procedural programming?

# Java
* Java does not support procedural programming, since every function must be inside of a class. It was designed to be purely object oriented. The creator of Java once said that if he could change one thing about the language, he would do away with the classes. Data is too tightly related to the functions that it's very tough to avoid changing state and write a pure function. At the same time, it is possible to bend the rules and write procedural code that will also fit Java's standards. 
```java
class Fibonacci:
   def __init__(self):
       self.cache = {}
   def fib(self, n):
       if self.cache.has_key(n):
           return self.cache[n]
       if n == 1 or n == 2:
            return 1
       else:
           a = 1
           b = 1
           for i in range(2, n):
               f = a + b;
               b = a;
               a = f;
           self.cache[n] = f;
           return f;


fibonaccyCounter = Fibonacci()
print fibonaccyCounter.fib(6)
```
# PHP
Much more flexible than Java, PHP allows for procedural programming, where functions can stand alone. A stackExchange user wrote these bullet points on the topic: 
* You can write PHP source code that does useful tasks
* You can organize useful tasks into "chunks" of code
* You can think of "chunks" of code independently of the individual files where they are saved
* Sometimes those "chunks" of code will behave differently based on parameters you pass in
* Chunks of code that accept parameters are called "Functions"
* Functions can be "chunked" together, and there are different ways of doing this:
* For example: you could have just one big PHP file with all the functions you have ever written in your entire life, listed in alphabetical order by function name
* For example: you could have multiple PHP files with functions that are chunked together by subject matter [e.g., functions for doing basic string manipulation, functions for processing arrays, functions for file input/output, etc]

# C#
* Like PHP, C# allows both procedural programming and object oriented programming styles. A quick google search of "C# procedural programming" yields an awful lot of opinions and perspectives on which of the two are better. In that case, I always assume that both are probably right in their own ways.
* The code above could be rewritten in a procedural style
```c#
program Fibonacci;

function fib(n: Integer): Integer;
var a: Integer = 1;
    b: Integer = 1;
    f: Integer;
    i: Integer;
begin
  if (n = 1) or (n = 2) then
     fib := 1
  else
    begin
      for i := 3 to n do
      begin
         f := a + b;
         b := a;
         a := f;
      end;
      fib := f;
    end;
end;

begin
  WriteLn(fib(6));
end.
```
# Summary
* To restate what is said in the Functional programming section, it really depends on what the programmer prefers to use when it comes to programming paradigms. Languages these days seem to blur the lines between object oriented, procedural, and functional. By allowing multiple style of programming, the tool becomes more useful and work in many more situations.

