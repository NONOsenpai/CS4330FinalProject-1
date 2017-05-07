## Singleton

* How is a singleton implemented?
* Can it be made thread-safe?
* Can the singleton instance be lazily instantiated?

# Java
* According to the link given to us on singletons in early April: ""University of Maryland Computer Science researcher Bill Pugh has written about the code issues underlying the Singleton pattern when implemented in Java. Pugh's efforts on the "Double-checked locking" idiom led to changes in the Java memory model in Java 5 and to what is generally regarded as the standard method to implement Singletons in Java. The technique is known as the initialization on demand holder idiom, is as lazy as possible, and works in all known versions of Java. It takes advantage of language guarantees about class initialization, and will therefore work correctly in all Java-compliant compilers and virtual machines.

* The inner class is referenced no earlier (and therefore loaded no earlier by the class loader) than the moment that getInstance() is called. Thus, this solution is thread-safe without requiring special language constructs (i.e. volatile or synchronized)."

# C#
```C#
using System;

public class Singleton
{
   private static Singleton instance;

   private Singleton() {}

   public static Singleton Instance
   {
      get 
      {
         if (instance == null)
         {
            instance = new Singleton();
         }
         return instance;
      }
   }
}
 ```
* This implementation has two main advantages:Because the instance is created inside the Instance property method, the class can exercise additional functionality (for example, instantiating a subclass), even though it may introduce unwelcome dependencies.
* The instantiation is not performed until an object asks for an instance; this approach is referred to as lazy instantiation. Lazy instantiation avoids instantiating unnecessary singletons when the application starts.
* The main disadvantage of this implementation, however, is that it is not safe for multithreaded environments. If separate threads of execution enter the Instance property method at the same time, more that one instance of the Singleton object may be created. Each thread could execute the following statement and decide that a new instance has to be created:

```if (instance == null)```
* Various approaches solve this problem. One approach is to use an idiom referred to as Double-Check Locking [Lea99]. However, C# in combination with the common language runtime provides a static initialization approach, which circumvents these issues without requiring the developer to explicitly code for thread safety.


# PHP
```PHP
class Singleton
{
    protected static $instance = null;

    protected function __construct()
    {
        //Thou shalt not construct that which is unconstructable!
    }

    protected function __clone()
    {
        //Me not like clones! Me smash clones!
    }

    public static function getInstance()
    {
        if (!isset(static::$instance)) {
            static::$instance = new static;
        }
        return static::$instance;
    }
}
```

* PHP singletons, if written properly, can be thread safe and also have lazy initialization
