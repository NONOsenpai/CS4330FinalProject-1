# Errors and Exception Handling
An *exception* is the occurence of an unanticipated event during normal program operation. *Exception handling* refers to the process of controlling what happens when an exception occurs.

Many langauges support the use of *try-catch statements* for exception handling, where code that may generate or throw an exception is placed in a try block, and code that is to be executed when the exception occurs is placed in a catch block. A third block is often included, called a finally block. A finally block is used to include code that will always be executed whether or not an exception is thrown by code placed in the try block. The finally block is optional and is often used to free system resources allocated by code in the try block.

The example below illustrates what a typical try-catch statement looks like.

```Java
try {
	// code that can throw an exception
} catch (Exception e) {
	// code that executes when an exception is thrown
} finally {
	// code that executes whether an exception is thrown or not
}
```
*A typical try-catch statement with a finally block in Java*

Java, PHP, and C# all support the use of try-catch statements and alternative methods for handling errors and exceptions. The following sections will take a more in-depth look at the error and exception handling abilities of these three languages.

## Java
As mentioned in the previous section, Java supports the use of try-catch statements. In addition to try-catch statements, Java supports a *try-with-resources* statement. A try-with-resources statement is used to open resources that must be closed after being utilized by the program. Any resources opened using a try-with-resources statement will be closed after the statement finishes execution.

```java
try (BufferedReader userInput = new BufferedReader(new InputStreamReader(System.in));) {
	// code that can throw an exception
} catch (Exception e) {
	// code that executes after an exception occurs
}
```
*A try-with-resources statement in Java*

In the example above, the BufferedReader and InputStreamReader resources will be closed after the try-with-resources statement finishes executing. A try-with-resources statement in Java also does not require use of a catch block and may be used with a finally block.

## PHP
PHP, like Java, also supports try-catch statements and additional error handling methods.

```php
<?php
try {
	// code that can throw an exception
} catch (Exception $e) {
	// code that executes when an exception is thrown
} finally {
	// code that executes whether an exception is thrown or not
}
?>
```
*A typical try-catch statement with a finally block in PHP*

Another error handling method in PHP, called the *die function*, exits the program and produces an error message to STDOUT when an error occurs. This error handling method is often used for debugging more than production, as error messages being displayed in STDOUT creates a poor user experience and poses a potential security risk.

```php
<?php
$conn = mysql_connect('localhost', 'root', 'password') or
die('There was an error connecting to the database: ' . mysql_error());

mysql_close($conn);
?>
```
*An error handling statement utilizing the die function in PHP. The program exits and writes an error to STDOUT when an error occurs connecting to the mySQL database.*

## C# #
C#, like Java, supports both try-catch statments, and an equivalent to try-with-resources statements, the *using statement*.

```cs
try
{
	// code that can throw an exception
}
catch (Exception e)
{
	// code that executes when an exception is thrown
}
finally
{
	// code that executes whether an exception is thrown or not
}
```
*A typical try-catch statement with a finally block in C#*

```cs
using (System.IO.StreamReader sr = System.IO.File.OpenText(file))
{
    // code that can throw an exception
}
```
*A using statement in C#*

Similarly to Java, resources allocated in a using statement will be closed after the using statement has finished executing.
