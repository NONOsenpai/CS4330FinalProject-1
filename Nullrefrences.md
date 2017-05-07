# Null/nil reference

* Which does the language use? (null/nil/etc)
* Does the language have features for handling null/nil references?

## C#
* "The null keyword is a literal that represents a null reference, one that does not refer to any object. null is the default value of reference-type variables. Ordinary value types cannot be null. However, C# 2.0 introduced nullable value types. See Nullable Types." -.NET Documentation

* Nullable Types are instances of System.Nullable and add the feature of being able to be set to null in addition to the usual type, hence the name Nullable. This helps with working with data that may not be there, i.e. databases where some values are not set.

## PHP
* PHP uses null to represent a variable with no value. Variables equal null if it has been set to the constant NULL, hasn't yet been set to a value, or has been set to unset().

* There are a multitude of functions that will check if a variable is empty() or is_null().

## Java
* According to the Java Language Specification: "There is also a special null type, the type of the expression null, which has no name. Because the null type has no name, it is impossible to declare a variable of the null type or to cast to the null type. The null reference is the only possible value of an expression of null type. The null reference can always be assigned or cast to any reference type"

* A major feature to handle null is the NullPointerException, which will be thrown on any method invocation on a null reference. In my opinion, it seems to be a very passive way of dealing with null values compared to the other two languages, which can limit which variables can be null.


