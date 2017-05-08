# Multithreading
Multithreading is an execution model that allows multiple threads of a program to execute simultaneously.

## Java
Java fully supports multithreaded programming. Java designates a main thread that is present in each program and allows the ability to create multiple threads to run concurrently.

### Defining a Thread
Java specifies two ways to define and execute a thread through the use of an interface, named Runnable, and a class, named Thread.

The first method of defining a thread is by providing a Runnable object, or an instance of a class that implements the Runnable interface, to the Thread class constructor.

The second method of defining a thread is by providing an object that inherits from the Thread class.

In both cases, a no-argument run method must be implemented because the Runnable interface, which contains the no-argument run method, is implemented directly in the first case, and through use of the Thread class in the second case. The run method, which contains the code to be executed by the thread, is invoked by the Thread class's start method.

According to the official Java Documentation, defining a thread by implementing the Runnable interface is the preferred method in order to allow inheritance of another class if necessary.

#### Examples
An example of defining a thread through implementation of the Runnable interface:

```java
public class MyThread implements Runnable {

	// The run method is implemented here
	public void run() {
		System.out.println("The thread is running!");
	}

	public static void main(String args[]) {

		// Create and start the thread
		Thread thread = new Thread(new MyThread());
		thread.start();
	}
}
```
An example of defining a thread through inheritance of the Thread class:

```java
public class MyThread extends Thread {

	// The run method is implemented here
	public void run() {
		System.out.println("The thread is running!");
	}

	public static void main(String args[]) {

		// Create and start the thread
		MyThread myThread = new MyThread();
		myThread.start();
	}
}
```

### Interrupting a Thread
Java's Thread class supports interruption of a thread through use of the interrupt method. Invocation of the interrupt method results in an InterruptedException.

The Thread class also has a sleep method that will temporarily pause execution for the specified amount of time.

### Stopping a Thread
Once a thread's run method has ceased executing, the thread stops. Java also allows joining another thread with use of the Thread class's join method. Invocation of the join method will cause the invoking thread to wait until the desired thread has finished executing.

## C# #
C#, like Java, fully supports multithreaded programming. C# designates the BackgroundWorker and Thread classes to control simultaneous execution of threads.

### Defining a Thread
The following example illustrates defining a thread in C# using the Thread class:

```cs
class MyThread
{
    public static void Main(string[] args)
    {
        // Create and start thread
        System.Threading.Thread myThread = new System.Threading.Thread(Method);
        myThread.Start();
    }

    public static void Method()
    {
        System.Console.WriteLine("The thread is running!");
    }
}
```
*A thread in C# that executed the method "Method"*

## PHP
Multithreading is not a supported feature of PHP; however, PHP does enable concurrent programming through use of provided process control functions.
