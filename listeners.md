## Implementation of listeners and event handlers

# Java
* In Java there are a multitude of listeners and event handlers. An event handler can be placed onto just about any UI object to allow for mouseClick events and such. Listeners can be placed on all sorts of properties, and you can even create your own properties to be listened to. 
```java
server.addEventListener("message", clientData.class, new DataListener<clientData>() {
        @Override
        public void onData(SocketIOClient client, clientData data, AckRequest ackRequest) throws Exception {
            System.out.println("Message from client: " + data.getMessage());

        }

    });
```

# PHP
* PHP has an EventListener class that does similar things to the event listeners in Java. It allows for thread-safe execution and reusability. 
```PHP
public EventListener::__construct ( EventBase $base , callable $cb , mixed $data , int $flags , int $backlog , mixed $target )
```

# C#
* In C# and C++, you can create event handlers using the Properties window. In Visual Basic, you can use the Class Name and Method Name drop-down boxes in the Code Editor. This one seems to be very similar to the Java and PHP listeners.

```c#
private void StartProcess(object sender, System.EventArgs e) 
{
   // Add event handler code here.
}
```
