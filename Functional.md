# Functional programming 
* Does it support functional programming? 
## Java 
* No, Java does not support functional programming. All functions or code must be inside of a class. The term for this is a closure; a record storing function together with an environment. The language also lacks other features like range type, first class lambda expressions and currying.
## PHP 
* Yes, PHP supports functional programming. There are numerous examples in their documentation which show how to do things both in an object oriented or a functional style. "Users migrating from the old mysql extension may prefer the procedural interface. The procedural interface is similar to that of the old mysql extension. In many cases, the function names differ only by prefix. Some mysqli functions take a connection handle as their first argument, whereas matching functions in the old mysql interface take it as an optional last argument." Here is an example of switching paradigms on the fly, which is regarded as bad style.
```php
<?php
$mysqli = new mysqli("example.com", "user", "password", "database");
if ($mysqli->connect_errno) {
    echo "Failed to connect to MySQL: " . $mysqli->connect_error;
}

$res = mysqli_query($mysqli, "SELECT 'Possible but bad style.' AS _msg FROM DUAL");
if (!$res) {
    echo "Failed to run query: (" . $mysqli->errno . ") " . $mysqli->error;
}

if ($row = $res->fetch_assoc()) {
    echo $row['_msg'];
}
?>
```
## C# 
* Like PHP, C# does support functional programming in the essence that functions can stand alone outside of a class.
* C# 2.0 brought us parametric polymorphism (or "generics"). I've heard that Dom Syme, one of the creators of F#, was largely responsible for implementing generics in the .NET BCL.
* C# 2.0 also allows programmers to pass and returns functions as values for higher-order functions, and has limited support for anonymous delegates.
* C# 3.0 and 3.5 improved support anonymous functions for true closures.
* LINQ can be considered C#'s own flavor of list comprehensions.
* Anonymous types look like an approximation of ML records
* Type-inference is a given.



## Summary 
From much of my research, I found a lot of mixed opinions on whether some of these languages are functional, procedural, object oriented, etc. What I make of this is that possibly there is no right answer. Some languages, like Java, don't necessarily support functional programming, but there are ways to use a functional style. PHP as well as C# aren't purely functional, the programmer chooses which style to use when they write. According to the programming paradigms wikipedia page it says "Programming paradigms are a way to classify programming languages based on the features of various programming languages." I feel though, that the paradigm is based more off of the combination of the programming language and the programmer using it. For example, if you have a lighter but use it as a [bottle opener (video)](https://www.youtube.com/watch?v=Ly24ycL1lRI), would you consider it a lighter or a bottle opener? I think that depends on what you want to use it for.
