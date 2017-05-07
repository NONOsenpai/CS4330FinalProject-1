# Memory management
## Java
* **Automatic Memory Management**.
<br></br>
The Java Virtual Machine (JVM) handles all of the memory and allocates/ deallocates when necessary. The JVM and garbage collection takes this so seriously, that Java will not allow the developer to access memory.
<br></br>
* **Garbage Collection**
## PHP
* **Direct Memory Management**
<br></br>
PHP allows for direct memory management through API calls. The management is so direct, that a developer can use a delay to delay the memory communicating from say a server and a user's local machine. This could be useful to not overload a server or spread traffic.
<br></br>
![PHP Memory API](https://github.com/agom94/CS4330FinalProject/blob/master/PHPMemory.PNG)
* **Thread-Safe Resource Manager**
## C#
* **Automatic memory management.**
<br></br>
If the object hasn't been used in awhile, or the garbage collector sees that the object is no longer in use, it will be considered for destruction. Once it is considered for destruction, the object's destructor can be run at some random time the garbage collector sees fit. Once an object is destructed, it cannot be accessed at all.
<br></br>
* **The language supports manual memory management through various frameworks and API's from old WIN32 applications, however the language was not intended to do so.**
* **Garbage Collection**
